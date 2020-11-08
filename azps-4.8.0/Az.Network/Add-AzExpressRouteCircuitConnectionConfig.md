---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274902"
---
# <span data-ttu-id="3684c-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3684c-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="3684c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3684c-102">SYNOPSIS</span></span>
<span data-ttu-id="3684c-103">Bir hızlı rota devresi özel Eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3684c-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="3684c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3684c-104">SYNTAX</span></span>

### <span data-ttu-id="3684c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3684c-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3684c-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3684c-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3684c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3684c-107">DESCRIPTION</span></span>
<span data-ttu-id="3684c-108">**Add-Azexpressroute, Connectionconfig** cmdlet 'ı ExpressRoute devresi için özel eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3684c-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="3684c-109">Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar. **Add-Azexpressroute, Connectionconfig** öğesini çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3684c-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3684c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3684c-110">EXAMPLES</span></span>

### <span data-ttu-id="3684c-111">Örnek 1: var olan ExpressRoute devresine bir devre bağlantı kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="3684c-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="3684c-112">Örnek 2: mevcut ExpressRoute devresine boruları kullanarak bir devre bağlantı yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="3684c-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="3684c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3684c-113">PARAMETERS</span></span>

### <span data-ttu-id="3684c-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3684c-114">-AddressPrefix</span></span>
<span data-ttu-id="3684c-115">IPv4 tünelleri için hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="3684c-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="3684c-116">IPv6 tünellerinin hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/125 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="3684c-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="3684c-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="3684c-117">-AddressPrefixType</span></span>
<span data-ttu-id="3684c-118">Bu, adres önekinin ait olduğu adres ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3684c-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="3684c-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="3684c-119">-AuthorizationKey</span></span>
<span data-ttu-id="3684c-120">Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="3684c-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="3684c-121">Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="3684c-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="3684c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3684c-122">-DefaultProfile</span></span>
<span data-ttu-id="3684c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3684c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3684c-124">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3684c-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3684c-125">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="3684c-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3684c-126">**Get-Azexpressroute, Get-Azexpressroutedevdevile** döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="3684c-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="3684c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3684c-127">-Name</span></span>
<span data-ttu-id="3684c-128">Eklenecek devre bağlantısı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="3684c-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="3684c-129">-Peerexpressroutedevresi eşlemesi</span><span class="sxs-lookup"><span data-stu-id="3684c-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="3684c-130">Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3684c-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="3684c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="3684c-131">-Confirm</span></span>
<span data-ttu-id="3684c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3684c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3684c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3684c-133">-WhatIf</span></span>
<span data-ttu-id="3684c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3684c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3684c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3684c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3684c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3684c-136">CommonParameters</span></span>
<span data-ttu-id="3684c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3684c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3684c-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3684c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3684c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3684c-139">INPUTS</span></span>

### <span data-ttu-id="3684c-140">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3684c-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3684c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3684c-141">System.String</span></span>

## <span data-ttu-id="3684c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3684c-142">OUTPUTS</span></span>

### <span data-ttu-id="3684c-143">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3684c-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3684c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3684c-144">NOTES</span></span>

## <span data-ttu-id="3684c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3684c-145">RELATED LINKS</span></span>

[<span data-ttu-id="3684c-146">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="3684c-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3684c-147">Remove-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="3684c-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3684c-148">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="3684c-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="3684c-149">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3684c-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="3684c-150">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="3684c-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)