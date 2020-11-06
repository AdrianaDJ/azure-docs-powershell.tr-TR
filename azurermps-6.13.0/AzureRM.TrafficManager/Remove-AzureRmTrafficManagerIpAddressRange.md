---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587101"
---
# Remove-AzureRmTrafficManagerIpAddressRange

## SYNOPSIS
Yerel trafik Yöneticisi uç noktası nesnesinden bir adres aralığını veya alt ağı kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmTrafficManagerIpAddressRange** cmdlet 'i yerel bir Azure Traffic Manager uç nokta nesnesinden IP adresi aralığını kaldırır.
New-AzureRmTrafficManagerEndpoint veya Get-AzureRmTrafficManagerEndpoint cmdlet 'lerini kullanarak uç nokta alabilirsiniz.

Bu cmdlet yerel son nokta nesnesinde çalışır.
Set-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak, akış Yöneticisi uç noktasına değişikliklerinizi kaydedin.

## ÖRNEKLERDEN

### Örnek 1: uç noktadan IP adresi aralıklarını kaldırma
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

İlk komut ResourceGroup11 adındaki kaynak grubundaki ContosoProfile adlı profilden contoso adlı Azure uç noktasını alır ve bu nesneyi $TrafficManagerEndpoint değişkeninde depolar.
İkinci komut, $TrafficManagerEndpoint depolanan uç noktasından IP adresi aralığını kaldırır.
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
Kaldırılacak aralıktaki ilk IP adresini belirtir.

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
Bu cmdlet değiştirilmiş bir TrafficManagerEndpoint nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmTrafficManagerIpAddressRange](./Add-AzureRmTrafficManagerIpAddressRange.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)
