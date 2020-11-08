---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105753"
---
# Set-AzureStorSimpleDevice

## SYNOPSIS
Aygıtın aygıt yapılandırmasını değiştirir.

## INDEKI

### Identifybyname (varsayılan)
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Identifybyıd
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureStorSimpleDevice** cmdlet 'i bir cihazın cihaz yapılandırmasını değiştirir.
Bir cihazı ilk kez ayarlıyorsanız, *TimeZone* , *Secondarydnsserver* ve *storsimplenetworkconfig* parametrelerini belirtmeniz gerekir.
Controller0 ve Controller1 ve IP adresleriyle data0 için ağ yapılandırması eklemeniz gerekir.
Cihazı ilk kez yapılandırmak için en az bir Internet SCSI (ISCSı) etkinleştirilmiş ağ arabirimi olmalıdır.

## ÖRNEKLERDEN

### Örnek 1: aygıtın yapılandırmasını değiştirme
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

İlk komut data0 arabirimi için bir ağ yapılandırması oluşturur.
Bu komut *Controller0IPv4Address* , *Controller1IPv4Address* ve *enableiscsı* parametrelerini belirtir.
Komut sonucu $NetworkConfigData 0 değişkenine depolar.

İkinci komut, Pasifik standart saat dilimini almak için **System. TimeZoneInfo** .NET sınıfını ve standart söz dizimini kullanır ve bu nesneyi $TimeZoneInfo değişkeninde depolar.

Üçüncü komut, çevrimiçi StorSimple aygıtı almak için **Get-AzureStorSimpleDevice** cmdlet 'Ini ve **WHERE-Object** Core cmdlet 'ini kullanır ve sonra da bunu $OnlineDevice değişkeninde depolar.

Son komutu, belirtilen cihaz KIMLIĞINE sahip aygıtın yapılandırmasını değiştirir.
Komut, geçerli cmdlet 'in ilk komutta oluşturduğu yapılandırma nesnesini kullanır.
Komut, $TimeZoneInfo depolanan saat dilimini kullanır.

### Örnek 2: cihazı değiştirmek için yapılandırma nesnesini boru yapma
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Bu örnekte, ilk örnekle aynı yapılandırma güncelleştirmesi yapılır, ancak son komut, ardışık düzen işlecini kullanarak ağ yapılandırma nesnesini geçerli cmdlet 'e geçirir.

### Örnek 3: bir cihazı değiştirmek için saat dilimi nesnesini boru yapma
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Bu örnekte, ilk örnekle aynı yapılandırma güncelleştirmesi yapılır, ancak son komut zaman dilimi işlecini kullanarak saat dilimi nesnesini geçerli cmdlet 'e geçirir.

## PARAMETRELERINE

### -DeviceID
Yapılandırılacak StorSimple aygıtının örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aygıtadı
Yapılandırılacak StorSimple aygıtının kolay adını belirtir.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
StorSimple aygıtının yeni kolay adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bir Azure profili belirtir.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryDnsServer
StorSimple cihazı için ikincil bir DNS sunucusu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorSimpleNetworkConfig
Cihazdaki arabirimler için ağ yapılandırması objectss dizisini belirtir.
**Networkconfig** nesnesi edinmek için New-AzureStorSimpleNetworkConfig cmdlet 'ini kullanın.

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeZone
Cihaz için bir saat dilimi belirtir.
**Getsystemtimezone ()** yöntemini kullanarak bir **TimeZoneInfo** nesnesi oluşturabilirsiniz.
Örneğin bu komut, Pasifik standart saati için saat dilimi bilgileri nesnesi oluşturur: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### NetworkConfig, TimeZoneInfo
Bir **Networkconfig** nesnesini veya **TimeZoneInfo 'yu** bu cmdlet 'e yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### DeviceDetails
Bu cmdlet sanal cihazın güncelleştirilmiş cihaz ayrıntılarını döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleNetworkConfig](./New-AzureStorSimpleNetworkConfig.md)

[Set-AzureStorSimpleVirtualDevice](./Set-AzureStorSimpleVirtualDevice.md)


