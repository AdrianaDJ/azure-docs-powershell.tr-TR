---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097104"
---
# <span data-ttu-id="35a8f-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="35a8f-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="35a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="35a8f-103">Bir hızlı rota devresi özel Eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="35a8f-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="35a8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35a8f-104">SYNTAX</span></span>

### <span data-ttu-id="35a8f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35a8f-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35a8f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="35a8f-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a8f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35a8f-107">DESCRIPTION</span></span>
<span data-ttu-id="35a8f-108">**Add-Azexpressroute, Connectionconfig** cmdlet 'ı ExpressRoute devresi için özel eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="35a8f-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="35a8f-109">Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar. **Add-Azexpressroute, Connectionconfig** öğesini çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="35a8f-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="35a8f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35a8f-110">EXAMPLES</span></span>

### <span data-ttu-id="35a8f-111">Örnek 1: var olan ExpressRoute devresine bir devre bağlantı kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="35a8f-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="35a8f-112">Örnek 2: mevcut ExpressRoute devresine boruları kullanarak bir devre bağlantı yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="35a8f-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="35a8f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35a8f-113">PARAMETERS</span></span>

### <span data-ttu-id="35a8f-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="35a8f-114">-AddressPrefix</span></span>
<span data-ttu-id="35a8f-115">IPv4 tünelleri için hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="35a8f-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="35a8f-116">IPv6 tünellerinin hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/125 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="35a8f-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="35a8f-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="35a8f-117">-AddressPrefixType</span></span>
<span data-ttu-id="35a8f-118">Bu, adres önekinin ait olduğu adres ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="35a8f-118">This specifies the Address Family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a8f-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="35a8f-119">-AuthorizationKey</span></span>
<span data-ttu-id="35a8f-120">Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="35a8f-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="35a8f-121">Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="35a8f-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="35a8f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a8f-122">-DefaultProfile</span></span>
<span data-ttu-id="35a8f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35a8f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35a8f-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="35a8f-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="35a8f-125">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="35a8f-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="35a8f-126">**Get-Azexpressroute, Get-Azexpressroutedevdevile** döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="35a8f-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="35a8f-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="35a8f-127">-Name</span></span>
<span data-ttu-id="35a8f-128">Eklenecek devre bağlantısı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="35a8f-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="35a8f-129">-Peerexpressroutedevresi eşlemesi</span><span class="sxs-lookup"><span data-stu-id="35a8f-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="35a8f-130">Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="35a8f-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="35a8f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="35a8f-131">-Confirm</span></span>
<span data-ttu-id="35a8f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35a8f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a8f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a8f-133">-WhatIf</span></span>
<span data-ttu-id="35a8f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35a8f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35a8f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35a8f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a8f-136">CommonParameters</span></span>
<span data-ttu-id="35a8f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35a8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a8f-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a8f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a8f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35a8f-139">INPUTS</span></span>

### <span data-ttu-id="35a8f-140">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="35a8f-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="35a8f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35a8f-141">System.String</span></span>

## <span data-ttu-id="35a8f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35a8f-142">OUTPUTS</span></span>

### <span data-ttu-id="35a8f-143">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="35a8f-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="35a8f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35a8f-144">NOTES</span></span>

## <span data-ttu-id="35a8f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35a8f-145">RELATED LINKS</span></span>

[<span data-ttu-id="35a8f-146">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="35a8f-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="35a8f-147">Remove-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="35a8f-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="35a8f-148">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="35a8f-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="35a8f-149">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="35a8f-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="35a8f-150">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="35a8f-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)