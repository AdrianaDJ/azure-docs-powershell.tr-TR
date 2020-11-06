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
# <span data-ttu-id="672b5-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="672b5-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="672b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672b5-102">SYNOPSIS</span></span>
<span data-ttu-id="672b5-103">Bir hızlı rota devresi özel Eş'ya bir devre bağlantı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="672b5-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="672b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="672b5-104">SYNTAX</span></span>

### <span data-ttu-id="672b5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="672b5-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="672b5-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="672b5-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="672b5-107">DESCRIPTION</span></span>
<span data-ttu-id="672b5-108">**Add-Azurermexpressroutedevresi** , ExpressRoute devresi için özel eş'ya bir devre bağlantısı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="672b5-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="672b5-109">Bu, bölgeler veya abonelikler arasında iki hızlı rota Devreeşlemesini sağlar. **Add-Azurermexpressroutedevresi Peeringconfig** 'i çalıştırdıktan sonra, yapılandırmayı etkinleştirmek için Set-AzureRmExpressRouteCircuit cmdlet 'ini çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="672b5-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="672b5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="672b5-110">EXAMPLES</span></span>

### <span data-ttu-id="672b5-111">Örnek 1: var olan ExpressRoute devresine bir devre bağlantı kaynağı ekleme</span><span class="sxs-lookup"><span data-stu-id="672b5-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="672b5-112">Örnek 2: mevcut ExpressRoute devresine boruları kullanarak bir devre bağlantı yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="672b5-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="672b5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="672b5-113">PARAMETERS</span></span>

### <span data-ttu-id="672b5-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="672b5-114">-AddressPrefix</span></span>
<span data-ttu-id="672b5-115">Hızlı rota devreleri arasında VxLan tünelleri oluşturmak için en az/29 müşteri adresi alanı</span><span class="sxs-lookup"><span data-stu-id="672b5-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="672b5-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="672b5-116">-AuthorizationKey</span></span>
<span data-ttu-id="672b5-117">Başka bir abonelikteki eşler arası hızlı rota devresi yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="672b5-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="672b5-118">Eşdüzey devrede yetkilendirme, var olan komutlar kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="672b5-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="672b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672b5-119">-DefaultProfile</span></span>
<span data-ttu-id="672b5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="672b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="672b5-121">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="672b5-122">Değiştirilecek ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="672b5-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="672b5-123">Bu, **Get-Azurermexpressroutedevresi** cmdlet 'i tarafından döndürülen Azure nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="672b5-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="672b5-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="672b5-124">-Name</span></span>
<span data-ttu-id="672b5-125">Eklenecek devre bağlantısı kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="672b5-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="672b5-126">-Peerexpressroutedevresi eşlemesi</span><span class="sxs-lookup"><span data-stu-id="672b5-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="672b5-127">Geçerli devre ile birlikte bırakılacak uzak devrenin özel eşlemesi için kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="672b5-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="672b5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="672b5-128">-Confirm</span></span>
<span data-ttu-id="672b5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="672b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672b5-130">-WhatIf</span></span>
<span data-ttu-id="672b5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="672b5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="672b5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="672b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672b5-133">CommonParameters</span></span>
<span data-ttu-id="672b5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="672b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672b5-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672b5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="672b5-136">INPUTS</span></span>

### <span data-ttu-id="672b5-137">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="672b5-138">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="672b5-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="672b5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="672b5-139">System.String</span></span>

## <span data-ttu-id="672b5-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="672b5-140">OUTPUTS</span></span>

### <span data-ttu-id="672b5-141">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="672b5-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="672b5-142">NOTES</span></span>

## <span data-ttu-id="672b5-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="672b5-143">RELATED LINKS</span></span>

[<span data-ttu-id="672b5-144">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="672b5-145">Get-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="672b5-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="672b5-146">Remove-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="672b5-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="672b5-147">Set-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="672b5-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="672b5-148">New-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="672b5-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="672b5-149">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="672b5-150">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="672b5-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
