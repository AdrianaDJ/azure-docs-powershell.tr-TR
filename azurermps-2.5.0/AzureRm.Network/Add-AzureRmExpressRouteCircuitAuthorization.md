---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939352"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute devresi yetkilendirmesi ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azurermexpressroutetor,** bir ExpressRoute devresini yetkilendirme ekler. ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur. **Add-Azurermexpressroutetorisuthorter** bir devreye yeni bir yetkilendirme ekler ve aynı zamanda ilgili yetkilendirme anahtarını oluşturur. Bu tuşlar, Get-AzureRmExpressRouteCircuitAuthorization cmdlet 'i çalıştırarak ve gerektiğinde uygun ağ sahibine kopyalanabilir ve iletilebileceği zaman görüntülenebilir.

**Add-Azurermexpressrouteter** 'i çalıştırdıktan sonra, anahtarı etkinleştirmek için Set-AzureRmExpressRouteCircuit cmdlet 'ini çağırmanız gerekir. **Set-Azurermexpressroutedevresi** çağrımıyorsanız, yetkilendirme devreye eklenir ancak kullanım için etkinleştirilmeyecektir.

## ÖRNEKLERDEN

### Örnek 1: belirtilen ExpressRoute devresi için yetkilendirme ekleme
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Bu örnekteki komutlar var olan ExpressRoute devresine yeni bir yetkilendirme ekler. İlk komut, Contosodevresi adlı bir devrenin nesne başvurusunu oluşturmak için **Get-Azurermexpressroutedevresi** kullanır. Bu nesne başvurusu $Circuit adlı bir değişkende depolanır.

İkinci komutta, New Authorization (Contosoınuthorbir) ExpressRoute devresine eklemek için **Add-Azurermexpressroutetorisuthorter** cmdlet 'i kullanılır. Bu komut yetkilendirmeyi ekler ancak bu yetkilendirmeyi etkilemez. Yetkilendirmeyi etkinleştirmek, örnekteki son komutta gösterilen **set-Azurermexpressroutedevresi** gerektirir.

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

### -Expressroutedevresi
Bu cmdlet 'in yetkilendirmeyi eklediği ExpressRoute devresini belirtir.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Eklenecek devre yetkilendirmesi adını belirtir.

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

### Psexpressroutedevresi
**Add-Azurermexpressroutetorisuthorter** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık olarak kullanılan örneklerini kabul eder.

## ÇıKıŞLAR

### Psexpressroutedevresi
**Add-Azurermexpressroutepatlarmicrosoft** **. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin örneklerini değiştirir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermexpressroutedevresi](./Get-AzureRmExpressRouteCircuit.md)

[Get-Azurermexpressrouteter](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[Yeni-azurermexpressroutepatlar](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-Azurermexpressrouteter](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Set-Azurermexpressroutedevresi](./Set-AzureRmExpressRouteCircuit.md)
