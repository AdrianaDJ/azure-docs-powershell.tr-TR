---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932013"
---
# Get-AzExpressRouteServiceProvider

## SYNOPSIS
List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.

## INDEKI

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzExpressRouteServiceProvider** cmdlet 'i, bir List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır. Öznitelik, konum ve bant genişliği seçeneklerini içerir.

## ÖRNEKLERDEN

### Örnek 1: "Silicon Valley" içindeki konumlara sahip hizmet sağlayıcısının listesini alma
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSExpressRouteServiceProvider

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azexpressroute, Arptable](Get-AzExpressRouteCircuitARPTable.md)

[Get-Azexpressroute, RouteTable](Get-AzExpressRouteCircuitRouteTable.md)

[Get-Azexpressroute, Routetablesummary](Get-AzExpressRouteCircuitRouteTableSummary.md)

[Get-Azexpressroutedevresi Istatistiği](Get-AzExpressRouteCircuitStats.md)
