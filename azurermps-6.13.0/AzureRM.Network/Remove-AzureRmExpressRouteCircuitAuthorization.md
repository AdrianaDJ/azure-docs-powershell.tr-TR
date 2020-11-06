---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 6a8c81f8c130f322e868c91e18c7fff7b1175d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593968"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## SYNOPSIS
Var olan ExpressRoute yapılandırma yetkilendirmesini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermexpressroutetormauthorter** cmdlet 'ı ExpressRoute devresine atanan bir yetkilendirmeyi kaldırır. ExpressRoute devreleri ortak Internet yerine bir bağlantı sağlayıcısı kullanarak şirket içi ağınızı Azure 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler sanal ağ sahibi tarafından, ağı devreye bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur. Sanal ağ başına yalnızca bir yetkilendirme olabilir. Ancak, herhangi bir zamanda, devre sahibi sanal ağa atanmış olan yetkilendirmeyi kaldırmak için **Remove-Azurermexpressroutedöngüye** at 'ı kullanabilir. Bu durumda, ilgili sanal ağ artık Azure 'a bağlanmak için ExpressRoute devresini kullanamaz.

## ÖRNEKLERDEN

### Örnek 1: ExpressRoute devresi 'den devre yetkilendirmeyi kaldırma
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Bu örnekte, ExpressRoute devresi bir devre yetkilendirmesi kaldırılır. İlk komut **Get-Azurermexpressroutedevresi** öğesini kullanarak, contosodevresi adlı bir ExpressRoute devresine nesne başvurusu oluşturabilir ve sonucu $Circuit adlı değişkende depolar.
İkinci komut devre yetkisini kaldırmak için devre
Üçüncü komut, $Circuit değişkeninde depolanan ExpressRoute devresini kaldırmayı onaylamak için Set-AzureRmExpressRouteCircuit cmdlet 'ini kullanır.

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

### -Expressroutedevresi
Bu cmdlet 'in kaldırdığı Expressroutedevresi nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in kaldırdığı devre yetkilendirmesinin adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi
Parametreler: Expressroutedevresi (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermexpressroutetorisuthorter](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-Azurermexpressroutedevresi](./Get-AzureRmExpressRouteCircuit.md)

[Get-Azurermexpressrouteter](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Yeni-azurermexpressroutepatlar](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-Azurermexpressroutedevresi](./Set-AzureRmExpressRouteCircuit.md)
