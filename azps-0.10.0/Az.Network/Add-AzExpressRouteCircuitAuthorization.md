---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935643"
---
# Add-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute devresi yetkilendirmesi ekler.

## INDEKI

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azexpressroutetorvazuthor,** bir ExpressRoute devresini yetkilendirme ekler. ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur. **Add-Azexpressroutetorti uthorter** bir devreye yeni bir yetkilendirme ekler ve aynı zamanda ilgili yetkilendirme anahtarını oluşturur. Bu tuşlar, Get-AzExpressRouteCircuitAuthorization cmdlet 'i çalıştırarak ve gerektiğinde uygun ağ sahibine kopyalanabilir ve iletilebileceği zaman görüntülenebilir.

**Add-Azexpressroutetortoruthorçalıştırılmı** çalıştırdıktan sonra, anahtarı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın. **Set-Azexpressroutedevresi** çağrımıyorsanız, yetkilendirme devreye eklenir ancak kullanım için etkinleştirilmeyecektir.

## ÖRNEKLERDEN

### Örnek 1: belirtilen ExpressRoute devresi için yetkilendirme ekleme
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Bu örnekteki komutlar var olan ExpressRoute devresine yeni bir yetkilendirme ekler. İlk komut, Contosodevresi adlı bir devrenin nesne başvurusunu oluşturmak için **Get-Azexpressroutedevkomutunu** kullanır. Bu nesne başvurusu $Circuit adlı bir değişkende depolanır.

İkinci komutta, New Authorization (Contosotoruthorbir kez) ExpressRoute devresi eklemek için **Add-Azexpressroutetorvazuthorme** cmdlet 'i kullanılır. Bu komut yetkilendirmeyi ekler ancak bu yetkilendirmeyi etkilemez. Yetkilendirmeyi etkinleştirmek, örnekteki son komutta gösterilen **set-Azexpressroutebir devresini** gerektirir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Psexpressroutedevresi
**Add-Azexpressroutetorsunuthor,** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.

## ÇıKıŞLAR

### Psexpressroutedevresi
**Add-Azexpressroutetorstanuthor,** **Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi** nesnesinin örneklerini değiştirir.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azexpressroutedevresi](./Get-AzExpressRouteCircuit.md)

[Get-Azexpressroutetorvazgetir](./Get-AzExpressRouteCircuitAuthorization.md)

[Yeni-Azexpressroutetorter](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-Azexpressroutetori Uthorremove](./Remove-AzExpressRouteCircuitAuthorization.md)

[Set-Azexpressroutedevresi](./Set-AzExpressRouteCircuit.md)
