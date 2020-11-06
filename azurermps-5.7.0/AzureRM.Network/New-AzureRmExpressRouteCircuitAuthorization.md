---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 68599a48c4b0e608f629a628968c1918e62ec226
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595211"
---
# New-AzureRmExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute devresi yetkilendirmesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azurermexpressroutetor,** bir ExpressRoute devresine eklenebilen bir devre yetkilendirmesi oluşturur. ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir ağı devreye bağlamak için sanal ağ sahibi tarafından kullanılabilen bir yetkilendirme anahtarı oluşturur. Sanal ağ başına yalnızca bir yetkilendirme olabilir.

ExpressRoute devresini oluşturduktan sonra, bu devreye yetki eklemek için **Add-Azurermexpressroutetorisuthorter** 'ı kullanabilirsiniz.
Alternatif olarak, devrede aynı anda yeni bir devreye eklenebilen bir yetkilendirme oluşturmak için **Yeni-Azurermexpressroutetorleruthor'i** kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: yeni bir devre yetkilendirmesi oluşturma
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Bu komut, Contosotoruthoruthori adında yeni bir devre yetkilendirmesi oluşturur ve bu nesneyi $Authorization adlı bir değişkende depolar. Nesneyi bir değişkene kaydetmek önemlidir: **Yeni-Azurermexpressroutetorruuthorter** , bir devre için bu yetkilendirmeyi bir devre yoluna ekleyemiyor. Bunun yerine, yeni bir $Authorization ExpressRoute devresi oluştururken New-AzureRmExpressRouteCircuit kullanılır.

Daha fazla bilgi için New-AzureRmExpressRouteCircuit cmdlet belgelerine bakın.

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

### -Ad
Yeni ExpressRoute devresi yetkilendirmesi için benzersiz bir ad belirtir.

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

### Yabilirsiniz
Bu cmdlet, ardışık düzen girişini kabul etmez.

## ÇıKıŞLAR

### Psexpressroutetorte
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutetorsunuthorter** nesnesi örneklerini oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermexpressroutetorisuthorter](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-Azurermexpressrouteter](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-Azurermexpressrouteter](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

