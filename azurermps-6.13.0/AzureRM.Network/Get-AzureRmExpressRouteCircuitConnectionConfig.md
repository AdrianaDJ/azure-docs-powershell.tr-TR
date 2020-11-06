---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 4d9442ba87ba46704aaa93b31f41f111519c980b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594383"
---
# Get-AzureRmExpressRouteCircuitConnectionConfig

## SYNOPSIS
Expressroutedevresi özel eşiyle ilişkili bir ExpressRoute devre bağlantısı yapılandırmasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermexpressroutedevresi Connectionconfig** cmdlet 'ı ExpressRoute devresi Için özel eşiyle ilişkili bir devre bağlantısının yapılandırmasını alır.

## ÖRNEKLERDEN

### Örnek 1: ExpressRoute devresi için devre bağlantısı yapılandırmasını görüntüleme
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### Örnek 2: boru kullanarak ExpressRoute devresi ile ilişkili devre
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

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
Devre bağlantı yapılandırmasını içeren ExpressRoute devresi nesnesi.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Alınacak devre bağlantısı yapılandırmasının adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi bağlantısı

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermexpressroutedevresi](Get-AzureRmExpressRouteCircuit.md)

[Add-Azurermexpressroutedevresi Connectionconfig](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[Remove-Azurermexpressroutedevresi Connectionconfig](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-Azurermexpressroutedevresi Connectionconfig](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[New-Azurermexpressroutedevresi Connectionconfig](New-AzureRmExpressRouteCircuitConnectionConfig.md)
