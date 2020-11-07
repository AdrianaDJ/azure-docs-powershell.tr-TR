---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918095"
---
# <span data-ttu-id="d048f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d048f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="d048f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d048f-102">SYNOPSIS</span></span>
<span data-ttu-id="d048f-103">ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d048f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="d048f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d048f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d048f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d048f-105">DESCRIPTION</span></span>
<span data-ttu-id="d048f-106">**Remove-Azexpressroute, Connectionconfig** cmdlet 'i, belirli bir hızlı rota devresi ile Ilişkilendirilmiş bir ExpressRoute devresi bağlantı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d048f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="d048f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d048f-107">EXAMPLES</span></span>

### <span data-ttu-id="d048f-108">Örnek 1: ExpressRoute devresi 'den devre bağlantısı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d048f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="d048f-109">Örnek 2: ExpressRoute devresi boruları kullanarak devre bağlantı yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d048f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="d048f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d048f-110">PARAMETERS</span></span>

### <span data-ttu-id="d048f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d048f-111">-DefaultProfile</span></span>
<span data-ttu-id="d048f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d048f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d048f-113">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d048f-114">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="d048f-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d048f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d048f-115">-Name</span></span>
<span data-ttu-id="d048f-116">Kaldırılacak devre bağlantısı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="d048f-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="d048f-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d048f-117">-Confirm</span></span>
<span data-ttu-id="d048f-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d048f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d048f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d048f-119">-WhatIf</span></span>
<span data-ttu-id="d048f-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d048f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d048f-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d048f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d048f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d048f-122">CommonParameters</span></span>
<span data-ttu-id="d048f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d048f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d048f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d048f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d048f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d048f-125">INPUTS</span></span>

### <span data-ttu-id="d048f-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d048f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d048f-127">OUTPUTS</span></span>

### <span data-ttu-id="d048f-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d048f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d048f-129">NOTES</span></span>

## <span data-ttu-id="d048f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d048f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d048f-131">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d048f-132">Get-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="d048f-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d048f-133">Add-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="d048f-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d048f-134">Set-Azexpressroutedevresi Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="d048f-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d048f-135">Yeni-Azexpressroute, Connectionconfig</span><span class="sxs-lookup"><span data-stu-id="d048f-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d048f-136">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="d048f-137">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="d048f-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)