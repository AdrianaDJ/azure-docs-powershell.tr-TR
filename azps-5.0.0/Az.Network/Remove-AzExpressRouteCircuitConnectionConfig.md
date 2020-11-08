---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279642"
---
# <span data-ttu-id="a318f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a318f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="a318f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a318f-102">SYNOPSIS</span></span>
<span data-ttu-id="a318f-103">ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a318f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="a318f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a318f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a318f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a318f-105">DESCRIPTION</span></span>
<span data-ttu-id="a318f-106">**Remove-Azexpressroute, Connectionconfig** cmdlet 'i, belirli bir hızlı rota devresi ile Ilişkilendirilmiş bir ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a318f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="a318f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a318f-107">EXAMPLES</span></span>

### <span data-ttu-id="a318f-108">Örnek 1: ExpressRoute devresi 'den devre bağlantısı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a318f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="a318f-109">Örnek 2: ExpressRoute devresi boruları kullanarak devre bağlantı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a318f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="a318f-110">Örnek 3: belirli bir adres ailesi için ExpressRoute devresi 'den bir devre bağlantı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a318f-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="a318f-111">Örnek 4: belirli bir adres ailesi için ExpressRoute devresi kullanarak bir devre bağlantı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a318f-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="a318f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a318f-112">PARAMETERS</span></span>

### <span data-ttu-id="a318f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a318f-113">-DefaultProfile</span></span>
<span data-ttu-id="a318f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a318f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a318f-115">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a318f-116">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="a318f-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a318f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a318f-117">-Name</span></span>
<span data-ttu-id="a318f-118">Kaldırılacak devre bağlantısı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="a318f-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="a318f-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="a318f-119">-AddressPrefixType</span></span>
<span data-ttu-id="a318f-120">Yapılandırmadan kaldırılması gereken adres ailesini belirtir</span><span class="sxs-lookup"><span data-stu-id="a318f-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a318f-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a318f-121">-Confirm</span></span>
<span data-ttu-id="a318f-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a318f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a318f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a318f-123">-WhatIf</span></span>
<span data-ttu-id="a318f-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a318f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a318f-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a318f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a318f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a318f-126">CommonParameters</span></span>
<span data-ttu-id="a318f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a318f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a318f-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a318f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a318f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a318f-129">INPUTS</span></span>

### <span data-ttu-id="a318f-130">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a318f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a318f-131">OUTPUTS</span></span>

### <span data-ttu-id="a318f-132">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a318f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a318f-133">NOTES</span></span>

## <span data-ttu-id="a318f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a318f-134">RELATED LINKS</span></span>

[<span data-ttu-id="a318f-135">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a318f-136">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="a318f-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a318f-137">Add-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="a318f-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a318f-138">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="a318f-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a318f-139">Yeni-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="a318f-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="a318f-140">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="a318f-141">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a318f-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)