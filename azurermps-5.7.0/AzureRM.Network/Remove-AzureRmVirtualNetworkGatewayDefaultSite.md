---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593729"
---
# Remove-AzureRmVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Sanal ağ ağ geçidinden varsayılan siteyi kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'i, Zorlamalı tünel varsayılan sitesini sanal ağ ağ geçidinden kaldırır.
Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.
Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.

**Remove-Azurermvirtualnetworkgatewaydefaultsıte** ağ geçidine atanmış varsayılan siteyi kaldırır.
Bunu yaparsanız, Zorlamalı tünel için kullanmadan önce yeni bir varsayılan site atamak için Set-AzureRmVirtualNetworkGatewayDefaultSite kullanmanız gerekir.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidine atanmış olan varsayılan siteyi kaldırma
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

Bu örnekte, şu anda ContosoVirtualGateway adındaki sanal ağ ağ geçidine atanmış olan varsayılan site kaldırılır.

İlk komut ağ geçidine nesne başvurusu oluşturmak için **Get-AzureRmVirtualNetworkGateway** kullanır; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.

İkinci komut, bu ağ geçidine atanmış olan varsayılan siteyi kaldırmak için **Remove-AzureRmVirtualNetworkGatewayDefaultSite** kullanır.

## PARAMETRELERINE

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

### -VirtualNetworkGateway
Kaldırılacak varsayılan siteyi içeren sanal ağ ağ geçidinin nesne başvurusunu belirtir.
Sanal ağ geçidi için Get-AzureRmVirtualNetworkGateway kullanarak ve ağ geçidinin adını belirterek bir nesne başvurusu oluşturabilirsiniz.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.

## ÇıKıŞLAR

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayDefaultSite](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


