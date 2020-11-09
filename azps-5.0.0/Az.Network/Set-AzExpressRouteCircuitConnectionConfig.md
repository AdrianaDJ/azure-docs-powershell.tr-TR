---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324571"
---
# <span data-ttu-id="b5e4a-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5e4a-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="b5e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e4a-103">Bir hızlı rota devresi için özel Peeringte oluşturulmuş bir devre bağlantı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="b5e4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5e4a-104">SYNTAX</span></span>

### <span data-ttu-id="b5e4a-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5e4a-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e4a-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b5e4a-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5e4a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5e4a-107">DESCRIPTION</span></span>
<span data-ttu-id="b5e4a-108">**Set-Azexpressroutedevresi Connectionconfig** cmdlet 'ı ExpressRoute devresi için özel eşte oluşturulmuş bir devre bağlantı yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="b5e4a-109">Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="b5e4a-110">**Set-Azexpressroute, connectionconfig** çalıştırmadan önce, **Add-azexpressroutedevdevconfig** öğesini kullanarak devre bağlantısını eklemeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="b5e4a-111">Ayrıca, **set-Azexpressroute, Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzExpressRouteCircuit cmdlet 'ini çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="b5e4a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5e4a-112">EXAMPLES</span></span>

### <span data-ttu-id="b5e4a-113">Örnek 1: bir devre mevcut ExpressRoute devresini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b5e4a-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="b5e4a-114">Örnek 2: yöneltme kullanarak mevcut ExpressRoute devresini kullanarak bir devre bağlantı yapılandırması ayarlama</span><span class="sxs-lookup"><span data-stu-id="b5e4a-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="b5e4a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5e4a-115">PARAMETERS</span></span>

### <span data-ttu-id="b5e4a-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b5e4a-116">-AddressPrefix</span></span>
<span data-ttu-id="b5e4a-117">IPv4 tünelleri için hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="b5e4a-118">IPv6 tünellerinin hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/125 müşteri adresi alanı.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="b5e4a-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="b5e4a-119">-AddressPrefixType</span></span>
<span data-ttu-id="b5e4a-120">Adres önekinin ait olduğu adres ailesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="b5e4a-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="b5e4a-121">-AuthorizationKey</span></span>
<span data-ttu-id="b5e4a-122">Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="b5e4a-123">Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="b5e4a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e4a-124">-DefaultProfile</span></span>
<span data-ttu-id="b5e4a-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e4a-126">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b5e4a-127">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="b5e4a-128">**Get-Azexpressroute, Get-Azexpressroutedevdevile** döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="b5e4a-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5e4a-129">-Name</span></span>
<span data-ttu-id="b5e4a-130">Eklenecek devre bağlantısı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="b5e4a-131">-Peerexpressroutedevresi eşlemesi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="b5e4a-132">Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="b5e4a-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5e4a-133">-Confirm</span></span>
<span data-ttu-id="b5e4a-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5e4a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e4a-135">-WhatIf</span></span>
<span data-ttu-id="b5e4a-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5e4a-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5e4a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e4a-138">CommonParameters</span></span>
<span data-ttu-id="b5e4a-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5e4a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e4a-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e4a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e4a-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5e4a-141">INPUTS</span></span>

### <span data-ttu-id="b5e4a-142">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="b5e4a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b5e4a-143">System.String</span></span>

## <span data-ttu-id="b5e4a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5e4a-144">OUTPUTS</span></span>

### <span data-ttu-id="b5e4a-145">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b5e4a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5e4a-146">NOTES</span></span>

## <span data-ttu-id="b5e4a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5e4a-147">RELATED LINKS</span></span>

[<span data-ttu-id="b5e4a-148">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="b5e4a-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5e4a-149">Remove-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="b5e4a-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5e4a-150">Add-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="b5e4a-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b5e4a-151">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="b5e4a-152">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b5e4a-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
