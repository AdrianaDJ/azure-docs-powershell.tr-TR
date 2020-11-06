---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593986"
---
# Add-AzureRmExpressRouteCircuitConnectionConfig

## SYNOPSIS
Bir hızlı rota devresi özel Eş'ya bir devre bağlantı yapılandırması ekler. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetByResource (varsayılan)
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Setbyresourceıd
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-Azurermexpressroutedevresi** , ExpressRoute devresi için özel eş'ya bir devre bağlantısı yapılandırması ekler. Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar. **Add-Azurermexpressroutedevresi Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzureRmExpressRouteCircuit cmdlet 'ini çağırmanız gerekir.

## ÖRNEKLERDEN

### Örnek 1: var olan ExpressRoute devresine bir devre bağlantı kaynağı ekleme
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### Örnek 2: mevcut ExpressRoute devresine boruları kullanarak bir devre bağlantı yapılandırması ekleme
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## PARAMETRELERINE

### -AddressPrefix
Hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthorizationKey
Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı. Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.

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
Değiştirilecek ExpressRoute devresi. Bu, **Get-Azurermexpressroutedevresi** cmdlet 'i tarafından döndürülen Azure nesnesidir.

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
Eklenecek devre bağlantısı kaynağının adı.

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

### -Peerexpressroutedevresi eşlemesi
Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermexpressroutedevresi](Get-AzureRmExpressRouteCircuit.md)

[Get-Azurermexpressroutedevresi Connectionconfig](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[Remove-Azurermexpressroutedevresi Connectionconfig](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-Azurermexpressroutedevresi Connectionconfig](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[New-Azurermexpressroutedevresi Connectionconfig](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[Set-Azurermexpressroutedevresi](Set-AzureRmExpressRouteCircuit.md)

[Get-Azurermexpressroutedevresi](Get-AzureRmExpressRouteCircuit.md)
