---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: a37502abcee157e9666a49ea5db5d2afe206aa8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939889"
---
# Set-AzureRmExpressRouteCircuit

## SYNOPSIS
ExpressRoute devresini değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azurermexpressroutedevresi** cmdlet 'ı değiştirilmiş ExpressRoute devresini Azure 'a kaydeder.

## ÖRNEKLERDEN

### Örnek 1: ExpressRoute devresi ServiceKey 'i değiştirme
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: SwitchParameter
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
Bu cmdlet 'in değiştirdiği **Expressroutedevresi** nesnesini belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Psexpressroutedevresi
' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermexpressroutedevresi](./Get-AzureRmExpressRouteCircuit.md)

[Taşı-Azurermexpressroutedevresi](./Move-AzureRmExpressRouteCircuit.md)

[New-Azurermexpressroutedevresi](./New-AzureRmExpressRouteCircuit.md)

[Remove-Azurermexpressroutedevresi](./Remove-AzureRmExpressRouteCircuit.md)
