---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 4a15bf67906606735b47e48b62d3e35cbcc91914
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586900"
---
# Get-AzureRmApplicationGatewayUrlPathMapConfig

## SYNOPSIS
Arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna YÖNELIK bir URL yol eşlemeleri dizisini alır.

## ÖRNEKLERDEN

### Örnek 1: URL yol haritası yapılandırmasını alma
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

Bu komut, ağ geçidi adlı uygulama ağ geçidinde bulunan arka uç sunucusundan URL yol haritası yapılandırmalarını alır.

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in URL yol haritası yapılandırmasını aldığı uygulama ağ geçidini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in yol haritası yapılandırmasını aldığı URL yol haritası adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### PSApplicationGateway
Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[New-AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Remove-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Set-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


