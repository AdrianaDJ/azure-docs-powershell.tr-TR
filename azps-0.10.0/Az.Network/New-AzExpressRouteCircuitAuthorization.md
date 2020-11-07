---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 0f17d30b6f47effab5b0039bd56172cbe580392c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935405"
---
# New-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute devresi yetkilendirmesi oluşturur.

## INDEKI

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**New-Azexpressroutetorvazuthor,** bir ExpressRoute devresine eklenebilen bir devre yetkilendirmesi oluşturur. ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir ağı devreye bağlamak için sanal ağ sahibi tarafından kullanılabilen bir yetkilendirme anahtarı oluşturur. Sanal ağ başına yalnızca bir yetkilendirme olabilir.

ExpressRoute devresini oluşturduktan sonra, **Add-Azexpressroutetori**
Alternatif olarak, devrede aynı anda yeni bir devreye eklenebilen bir yetkilendirme oluşturmak için **Yeni-Azexpressroutetorda** 'i kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: yeni bir devre yetkilendirmesi oluşturma
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Bu komut, Contosotoruthoruthori adında yeni bir devre yetkilendirmesi oluşturur ve bu nesneyi $Authorization adlı bir değişkende depolar. Nesneyi bir değişkene kaydetmek önemlidir: **New-Azexpressroutetorvazmauthorter** , bu yetkilendirmeyi bir devre Bunun yerine, yeni bir $Authorization ExpressRoute devresi oluştururken New-AzExpressRouteCircuit kullanılır.

Daha fazla bilgi için New-AzExpressRouteCircuit cmdlet belgelerine bakın.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet, ardışık düzen girişini kabul etmez.

## ÇıKıŞLAR

### Psexpressroutetorte
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. Psexpressroutetorsunuthorter** nesnesi örneklerini oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azexpressroutetori Uthorter](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-Azexpressroutetorvazgetir](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-Azexpressroutetori Uthorremove](./Remove-AzExpressRouteCircuitAuthorization.md)

