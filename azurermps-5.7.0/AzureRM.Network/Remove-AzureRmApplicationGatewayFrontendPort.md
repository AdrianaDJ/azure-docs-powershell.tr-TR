---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 93c4c86fec18ac13622078cbc17f7a0d895fd50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764979"
---
# Remove-AzureRmApplicationGatewayFrontendPort

## SYNOPSIS
Uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmApplicationGatewayFrontendPort** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç bağlantı noktasını kaldırır.

## ÖRNEKLERDEN

### Örnek: uygulama ağ geçidinden ön uç bağlantı noktasını kaldırma
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

İlk komut, ResourceGroup01 adındaki kaynak grubuna ait olan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ağ geçidini $AppGw değişkeninde depolar.

İkinci komut FrontEndPort02 adındaki bağlantı noktasını uygulama ağ geçidinden kaldırır.

## PARAMETRELERINE

### -ApplicationGateway
Ön uç bağlantı noktasının kaldırılacağı uygulama ağ geçidini belirtir.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kaldırılacak ön uç bağlantı noktasının adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmApplicationGatewayFrontendPort](./Add-AzureRmApplicationGatewayFrontendPort.md)

[Get-AzureRmApplicationGatewayFrontendPort](./Get-AzureRmApplicationGatewayFrontendPort.md)

[New-AzureRmApplicationGatewayFrontendPort](./New-AzureRmApplicationGatewayFrontendPort.md)

[Set-AzureRmApplicationGatewayFrontendPort](./Set-AzureRmApplicationGatewayFrontendPort.md)


