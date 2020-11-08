---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108922"
---
# <span data-ttu-id="6498a-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6498a-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="6498a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6498a-102">SYNOPSIS</span></span>
<span data-ttu-id="6498a-103">Bir yük dengeleyicinin kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="6498a-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="6498a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6498a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6498a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6498a-105">DESCRIPTION</span></span>
<span data-ttu-id="6498a-106">**Get-AzLoadBalancerRuleConfig** cmdlet 'i, bir yük dengeleyicinin bir veya daha fazla kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="6498a-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="6498a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6498a-107">EXAMPLES</span></span>

### <span data-ttu-id="6498a-108">Örnek 1: yük dengeleyicinin kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="6498a-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="6498a-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="6498a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6498a-110">İkinci komut, $slb 'teki yük dengeleyiciden MyLBrulename adlı ilişkili kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="6498a-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="6498a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6498a-111">PARAMETERS</span></span>

### <span data-ttu-id="6498a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6498a-112">-DefaultProfile</span></span>
<span data-ttu-id="6498a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6498a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6498a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6498a-114">-LoadBalancer</span></span>
<span data-ttu-id="6498a-115">Alınacak kural yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498a-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6498a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="6498a-116">-Name</span></span>
<span data-ttu-id="6498a-117">Alınacak kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6498a-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="6498a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6498a-118">CommonParameters</span></span>
<span data-ttu-id="6498a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6498a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6498a-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6498a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6498a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6498a-121">INPUTS</span></span>

### <span data-ttu-id="6498a-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6498a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6498a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6498a-123">OUTPUTS</span></span>

### <span data-ttu-id="6498a-124">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="6498a-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="6498a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6498a-125">NOTES</span></span>

## <span data-ttu-id="6498a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6498a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6498a-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6498a-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6498a-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6498a-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6498a-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6498a-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="6498a-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6498a-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


