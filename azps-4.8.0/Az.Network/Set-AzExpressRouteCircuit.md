---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274789"
---
# Set-AzExpressRouteCircuit

## SYNOPSIS
ExpressRoute devresini değiştirir.

## INDEKI

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azexpressroutedevresi** cmdlet 'ı değiştirilmiş ExpressRoute devresini Azure 'a kaydeder.

## ÖRNEKLERDEN

### Örnek 1: ExpressRoute devresi ServiceKey 'i değiştirme
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
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
Bu cmdlet 'in değiştirdiği **Expressroutedevresi** nesnesini belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azexpressroutedevresi](./Get-AzExpressRouteCircuit.md)

[Taşıma-Azexpressroutedevresi](./Move-AzExpressRouteCircuit.md)

[Yeni-Azexpressroutedevresi](./New-AzExpressRouteCircuit.md)

[Remove-Azexpressroutedevresi](./Remove-AzExpressRouteCircuit.md)
