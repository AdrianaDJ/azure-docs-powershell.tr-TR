---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279867"
---
# Get-AzExpressRouteCircuitAuthorization

## SYNOPSIS
ExpressRoute devresi yetkilendirmeleri hakkında bilgi alır.

## INDEKI

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azexpressroutetorkuruthorter** cmdlet 'ı ExpressRoute devresine atanmış yetkilendirmeler hakkında bilgi alır. ExpressRoute devreler şirket içi ağınızı, ortak Internet yerine bir bağlantı sağlayıcısı kullanarak Microsoft bulut 'a bağlayın. ExpressRoute devresi sahibi her bir devrein en fazla 10 yetkilendirmesi oluşturabilir; Bu yetkilendirmeler, bir sanal ağ sahibi tarafından ağı devreye (sanal ağ başına bir yetkilendirme) bağlamak için kullanılabilecek bir yetkilendirme anahtarı oluşturur. Yetkilendirme anahtarlarının yanı sıra yetkilendirme ile ilgili diğer bilgiler de, **Get-Azexpressroutetordi** 'i çalıştırarak herhangi bir zamanda görüntülenebilir.

## ÖRNEKLERDEN

### Örnek 1: tüm ExpressRoute yetkilendirmelerini alma
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

Bu komutlar ExpressRoute devresi ile ilişkilendirilmiş tüm ExpressRoute yetkilendirmeleri hakkındaki bilgileri döndürür. İlk komut, Contosodevresi adlı bir devrenin nesne başvurusu oluşturmak için **Get-Azexpressroutedevresi** öğesini kullanır; Bu nesne başvurusu $Circuit değişkeninde depolanır. İkinci komut daha sonra, bu nesne başvurusunu ve **Get-Azexpressroutetorınuthorwıth**

### Örnek 2: Where-Object cmdlet 'ini kullanarak tüm ExpressRoute yetkilendirmelerini alma
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Bu komutlar, örnek 1 ' de kullanılan komutlarda çeşitlemesini temsil eder. Bu durumda, bilgiler yalnızca kullanılabilir (yani sanal bir ağa atanmamış yetkilendirmeler için) için kullanılabilir olan yetkilendirmeler için döndürülür. Bunu yapmak için, devre yetkilendirme bilgileri komut 2 ' de döndürülür ve **WHERE-Object** cmdlet 'ine gönderilir.
**Burada-Object** , yalnızca *authorizationusestatus* özelliğinin kullanılabilir olduğu yetkilendirmeler seçer. Yalnızca kullanılamayan yetkilendirmeleri listelemek için, WHERE yan tümcesi için şu söz dizimini kullanın: `{$_.AuthorizationUseStatus -ne "Available"}`

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expressroutedevresi
ExpressRoute devresi yetkilendirmesini belirtir.

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
Bu cmdlet 'in aldığı ExpressRoute devresi yetkilendirmesinin adını belirtir.
-Name "Contosotorun"

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psexpressroutetorduthorter

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azexpressroutetori Uthorter](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-Azexpressroutedevresi](./Get-AzExpressRouteCircuit.md)

[Yeni-Azexpressroutetorter](./New-AzExpressRouteCircuitAuthorization.md)

[Remove-Azexpressroutetori Uthorremove](./Remove-AzExpressRouteCircuitAuthorization.md)
