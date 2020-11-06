---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589445"
---
# <span data-ttu-id="65551-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="65551-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="65551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65551-102">SYNOPSIS</span></span>
<span data-ttu-id="65551-103">ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65551-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65551-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65551-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65551-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65551-105">DESCRIPTION</span></span>
<span data-ttu-id="65551-106">**Remove-Azurermexpressroutedevresi Connectionconfig** cmdlet 'i, belirli bir hızlı rota devresi ile Ilişkilendirilmiş bir ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="65551-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="65551-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65551-107">EXAMPLES</span></span>

### <span data-ttu-id="65551-108">Örnek 1: ExpressRoute devresi 'den devre bağlantısı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="65551-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="65551-109">Örnek 2: ExpressRoute devresi boruları kullanarak devre bağlantı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="65551-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="65551-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65551-110">PARAMETERS</span></span>

### <span data-ttu-id="65551-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65551-111">-DefaultProfile</span></span>
<span data-ttu-id="65551-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65551-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65551-113">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="65551-114">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="65551-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="65551-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="65551-115">-Name</span></span>
<span data-ttu-id="65551-116">Kaldırılacak devre bağlantısı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="65551-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="65551-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="65551-117">-Confirm</span></span>
<span data-ttu-id="65551-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65551-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65551-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65551-119">-WhatIf</span></span>
<span data-ttu-id="65551-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65551-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65551-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65551-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65551-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65551-122">CommonParameters</span></span>
<span data-ttu-id="65551-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65551-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65551-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65551-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65551-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65551-125">INPUTS</span></span>

### <span data-ttu-id="65551-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="65551-127">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65551-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="65551-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65551-128">OUTPUTS</span></span>

### <span data-ttu-id="65551-129">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="65551-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65551-130">NOTES</span></span>

## <span data-ttu-id="65551-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65551-131">RELATED LINKS</span></span>

[<span data-ttu-id="65551-132">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="65551-133">Get-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="65551-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="65551-134">Add-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="65551-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="65551-135">Set-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="65551-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="65551-136">New-Azurermexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="65551-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="65551-137">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="65551-138">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="65551-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
