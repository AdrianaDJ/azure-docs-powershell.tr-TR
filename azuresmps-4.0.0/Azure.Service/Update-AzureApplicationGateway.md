---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105844"
---
# Update-AzureApplicationGateway

## SYNOPSIS
Uygulama ağ geçidini güncelleştirir.

## INDEKI

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Update-AzureApplicationGateway** cmdlet 'i var olan bir uygulama ağ geçidini güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: adını kullanarak uygulama ağ geçidini değiştirme
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

İlk komut ApplicationGateway06 adlı uygulama ağ geçidini durdurur.
Sanal ağı veya alt ağları değiştirebilmeniz için bir uygulama ağ geçidi durdurulmalıdır.

İkinci komut ApplicationGateway06 adlı uygulama ağ geçidinin sanal alt ağını ve alt ağlarını değiştirir.

### Örnek 2: uygulama ağ geçidinin ek özelliklerini değiştirme
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

Bu komut, ApplicationGateway06 adlı uygulama ağ geçidinin örnek sayısını, ağ geçidi boyutunu ve açıklamasını değiştirir.
Bu komut, uygulama ağ geçidi için sanal ağı veya alt ağları değiştirmiyor.
Bu nedenle, bu komutu çalıştırmadan önce uygulama ağ geçidini durdurmanız gerekmez.

### Örnek 3: ardışık düzeni kullanarak uygulama ağ geçidini değiştirme
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

İlk komut **Get-AzureApplicationGateway** cmdlet 'Ini kullanarak ApplicationGateway06 adındaki uygulama ağ geçidini alır.
Komut, $ApplicationGateway değişkeninde depolar.

İkinci komut, ikinci değer olan **Gatewaysize** özelliğini atar.

Son komutu, güncelleştirilmiş $ApplicationGateway geçerli cmdlet 'e geçirir.

## PARAMETRELERINE

### -Açıklama
Bu cmdlet 'in uygulama ağ geçidine atadığı açıklamayı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ağboyutu
Bu cmdlet 'in uygulama ağ geçidine atadığı boyutu belirtir.
Geçerli değerler:

- Küçük
- Düzey
- 13

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceCount
Bu cmdlet 'in uygulama ağ geçidine atadığı örnek sayısını belirtir.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in güncelleştirdiği uygulama ağ geçidinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -Alt ağlar
Bu cmdlet 'in uygulama ağ geçidini dağıttığı alt ağ dizisini belirtir.

Uygulama ağ geçidi çalışırken alt ağları güncelleştiremezsiniz.
Uygulama ağ geçidini durdurmak için Stop-AzureApplicationGateway cmdlet 'ini kullanın.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vağ adı
Bu cmdlet 'in uygulama ağ geçidini dağıtan sanal ağı belirtir.

Uygulama ağ geçidi çalışırken sanal bir ağı güncelleştiremezsiniz.
Uygulama ağ geçidini durdurmak için **stop-AzureApplicationGateway** kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Windowsazme. Management. ApplicationGateway. model. ApplicationGatewayOperationResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[New-AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
