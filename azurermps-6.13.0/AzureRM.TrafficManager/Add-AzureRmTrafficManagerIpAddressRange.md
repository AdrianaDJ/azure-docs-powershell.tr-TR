---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587118"
---
# Add-AzureRmTrafficManagerIpAddressRange

## SYNOPSIS
Yerel bir Traffic Manager uç noktası nesnesine adres aralığı veya alt ağ ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-AzureRmTrafficManagerIpAddressRange** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesine IP adresi aralığı ekler.
New-AzureRmTrafficManagerEndpoint veya Get-AzureRmTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.

Bu cmdlet yerel son nokta nesnesinde çalışır.
Set-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.

## ÖRNEKLERDEN

### Örnek 1: uç noktaya IP adresi aralıkları ekleme
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

İlk komut, **New-AzureRmTrafficManagerEndpoint** cmdlet 'ini kullanarak bir Azure Traffic Manager uç noktası oluşturur.
Komut, $TrafficManagerEndpoint değişkeninde Yerel uç noktayı depolar.
İkinci komut $TrafficManagerEndpoint depolanan bitiş noktasına 5.6.7.8 'e 1.2.3.4 IP adresi aralığını ekler.
Üçüncü komut, $TrafficManagerEndpoint depolanan bitiş noktasına 9.10.11.255 için 9.10.11.0 IP adresi aralığını ekler.
Dördüncü komut, kapsamın aralığın boyutuyla eşleştiğini doğrular, ardından $TrafficManagerEndpoint depolanan bitiş noktasına 12.13.14.31 için 12.13.14.0 IP adresi aralığını ekler.
Beşinci komut, $TrafficManagerEndpoint depolanan bitiş noktasına 15.16.17.18 için 15.16.17.18 IP adresi aralığını ekler.
Son komutu, Traffic Manager 'daki yerel değeri $TrafficManagerEndpoint eşleşecek şekilde güncelleştirir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Son
Eklenecek aralıktaki son IP adresini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kapsam
Eklenecek IP adresi aralığının kapsamını belirtir.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Yerel bir **TrafficManagerEndpoint** nesnesi belirtir.
Bu cmdlet bu yerel nesneyi değiştirir.
**TrafficManagerEndpoint** nesnesi almak için Get-AzureRmTrafficManagerEndpoint veya New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Önce
Eklenecek aralıktaki ilk IP adresini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Bu cmdlet, bu cmdlet 'e bir **TrafficManagerEndpoint** nesnesi kabul eder.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Bu cmdlet değiştirilmiş bir **TrafficManagerEndpoint** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRmTrafficManagerIpAddressRange](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
