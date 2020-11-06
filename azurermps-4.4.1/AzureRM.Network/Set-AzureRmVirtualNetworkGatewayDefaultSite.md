---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 4ab32ab5830356740cdb1709799b7dcb8f811c90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589214"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## SYNOPSIS
Sanal ağ geçidi için varsayılan siteyi ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'i sanal ağ geçidine Zorlanmış tünel varsayılan sitesi atar.
Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.
Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.
**Set-AzureRmVirtualNetworkGatewayDefaultSite** ağ geçidine atanmış olan varsayılan siteyi değiştirmek için bir yol sağlar.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ ağ geçidine varsayılan site atama
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Bu örnek, ContosoVirtualGateway adlı sanal ağ geçidine varsayılan bir site atar.

İlk komut, ContosoLocalGateway adlı yerel bir ağ geçidine nesne başvurusu oluşturur.
$LocalGateway adlı değişkende depolanan bu nesne başvurusu, varsayılan site olarak yapılandırılacak ağ geçidini temsil eder

.
İkinci komut, sanal ağ geçidi için bir nesne başvurusu oluşturur ve sonucu $VirtualGateway adlı değişkende depolar.

Üçüncü komut, varsayılan siteyi ContosoVirtualGateway 'e atamak için **set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -GatewayDefaultSite
Belirtilen sanal ağın varsayılan sitesi olarak atanacak yerel ağ ağ geçidinin nesne başvurusunu belirtir.
Yerel ağ geçidine nesne başvurusu oluşturmak için Get-AzureRmLocalNetworkGateway cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Varsayılan sitenin atanacağı sanal ağ ağ geçidi 'ne yönelik bir nesne başvurusu belirtir.
**Get-AzureRmVirtualNetworkGateway** 'i kullanarak ve ağ geçidinin adını belirterek sanal ağ geçidi 'ne nesne başvurusu oluşturabilirsiniz.

Değişken $VirtualGateway, *Virtualnetworkgateway* parametresinin parametre değeri olarak kullanılabilir:

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
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

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.

## ÇıKıŞLAR

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


