---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760720"
---
# <span data-ttu-id="db97b-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="db97b-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="db97b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db97b-102">SYNOPSIS</span></span>
<span data-ttu-id="db97b-103">Bir hızlı rota devresi özel Eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="db97b-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="db97b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db97b-104">SYNTAX</span></span>

### <span data-ttu-id="db97b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db97b-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db97b-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="db97b-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db97b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="db97b-107">DESCRIPTION</span></span>
<span data-ttu-id="db97b-108">**Add-Azexpressroute, Connectionconfig** cmdlet 'ı ExpressRoute devresi için özel eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="db97b-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="db97b-109">Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar. **Add-Azexpressroute, Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="db97b-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="db97b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db97b-110">EXAMPLES</span></span>

### <span data-ttu-id="db97b-111">Örnek 1: var olan ExpressRoute devresine bir devre bağlantı kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="db97b-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="db97b-112">Örnek 2: mevcut ExpressRoute devresine boruları kullanarak bir devre bağlantı yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="db97b-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="db97b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db97b-113">PARAMETERS</span></span>

### <span data-ttu-id="db97b-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="db97b-114">-AddressPrefix</span></span>
<span data-ttu-id="db97b-115">Hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı</span><span class="sxs-lookup"><span data-stu-id="db97b-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="db97b-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="db97b-116">-AuthorizationKey</span></span>
<span data-ttu-id="db97b-117">Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="db97b-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="db97b-118">Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="db97b-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="db97b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db97b-119">-DefaultProfile</span></span>
<span data-ttu-id="db97b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db97b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db97b-121">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="db97b-122">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="db97b-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="db97b-123">**Get-Azexpressroute, Get-Azexpressroutedevdevile** döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="db97b-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="db97b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="db97b-124">-Name</span></span>
<span data-ttu-id="db97b-125">Eklenecek devre bağlantısı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="db97b-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="db97b-126">-Peerexpressroutedevresi eşlemesi</span><span class="sxs-lookup"><span data-stu-id="db97b-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="db97b-127">Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="db97b-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="db97b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="db97b-128">-Confirm</span></span>
<span data-ttu-id="db97b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db97b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db97b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db97b-130">-WhatIf</span></span>
<span data-ttu-id="db97b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db97b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db97b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db97b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db97b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db97b-133">CommonParameters</span></span>
<span data-ttu-id="db97b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db97b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db97b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db97b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db97b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db97b-136">INPUTS</span></span>

### <span data-ttu-id="db97b-137">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="db97b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="db97b-138">System.String</span></span>

## <span data-ttu-id="db97b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db97b-139">OUTPUTS</span></span>

### <span data-ttu-id="db97b-140">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="db97b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db97b-141">NOTES</span></span>

## <span data-ttu-id="db97b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db97b-142">RELATED LINKS</span></span>

[<span data-ttu-id="db97b-143">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="db97b-144">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="db97b-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="db97b-145">Remove-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="db97b-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="db97b-146">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="db97b-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="db97b-147">Yeni-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="db97b-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="db97b-148">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="db97b-149">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="db97b-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)