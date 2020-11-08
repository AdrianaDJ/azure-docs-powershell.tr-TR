---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105515"
---
# New-AzureStorSimpleNetworkConfig

## SYNOPSIS
Ağ yapılandırma nesnesini hazırlar.

## INDEKI

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleNetworkConfig** cmdlet 'i, bir ağ yapılandırma nesnesini **set-AzureStorSimpleDevice** cmdlet 'ine geçirmek üzere hazırlar.
*Controller0IPAddress* parametresini ve *Controller1IPAddress* parametresini yalnızca data0 arabiriminde ayarlayın.
Data0 yalnızca üç ayarı destekler: *Controller0IPAddress* , *Controller1IPAdress* ve *enableiscsı*.

## ÖRNEKLERDEN

### Örnek 1: data0 arabirimini yapılandırma
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

Bu komut data0 arabirimi için ağ yapılandırması oluşturur.
Bu komut *Controller0IPv4Address* , *Controller1IPv4Address* ve *enableiscsı* parametrelerini belirtir.
Bu cmdlet yalnızca bu üç parametre için data0 'i yapılandırabilir.

### Örnek 2: data0
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

Bu komut, Veri1 arabirimini yapılandırır.

### Örnek 3: aygıtın yapılandırmasını değiştirme
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

İlk komut data0 arabirimi için bir ağ yapılandırması oluşturur.
Bu komut *Controller0IPv4Address* , *Controller1IPv4Address* ve *enableiscsı* parametrelerini belirtir.
Komut sonucu $NetworkConfigData 0 değişkenine depolar.

İkinci komut, çevrimiçi StorSimple aygıtı almak için **Get-AzureStorSimpleDevice** cmdlet 'Ini ve **WHERE-Object** Core cmdlet 'ini kullanır ve sonra da bunu $OnlineDevice değişkeninde depolar.

Son komutu, **set-AzureStorSimpleDevice** cmdlet 'ini kullanarak BELIRTILEN cihaz kimliğine sahip aygıtın yapılandırmasını değiştirir.
Komut, geçerli cmdlet 'in ilk komutta oluşturduğu yapılandırma nesnesini kullanır.

## PARAMETRELERINE

### -Controller0IPv4Address
Denetleyicinin IPv4 adresini belirtir.
Bu parametreyi yalnızca data0 arabirimi için belirtin.

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

### -Controller1IPv4Address
Denetleyici 1 için IPv4 adresini belirtir.
Bu parametreyi yalnızca data0 arabirimi için belirtin.

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

### -EnableCloud
Arabirimin bulut tarafından etkinleştirilip etkinleştirilmeyeceğini gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enableiscsı
Arabirim için Internet SCSI (ISCSı) etkinleştirilip etkinleştirilmeyeceğini gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Interfacealias
Bu cmdlet 'in ayarları sağladığı arabirimin arabirim diğer adını belirtir.
Geçerli değerler data0 ile Data5 arasında.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
Arabirimin IPv4 adresini belirtir.

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

### -IPv4Gateway
Ağ geçidinin IPv4 adresini belirtir.

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

### -IPv4Netmask
Arabirim için IPv4 ağ maskesi belirtir.

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

### -IPv6Gateway
Arabirim için IPv6 ağ geçidini belirtir.

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

### -IPv6Prefix
Arabirimin IPv6 önekini belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### NetworkConfig
Bu cmdlet, aşağıdaki özellikleri içeren bir NetworkConfig nesnesi döndürür: 

- **Isiscsienabled** ( **Boole değeri** ) 
- **Isalarbu** ( **Boole** )
- **Controller0IPv4Address** ( **IPAddress** ) 
- **Controller1IPv4Address** ( **IPAddress** ) 
- **IPv6Gateway** ( **IPAddress** ) 
- **IPv4Gateway** ( **IPAddress** ) 
- **IPv4Address** ( **IPAddress** ) 
- **IPv6Prefix** ( **dize** )
- **IPv4Netmask** ( **IPAddress** ) 
- **Interfacediğerad** ( **netınterfaceıd** )

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


