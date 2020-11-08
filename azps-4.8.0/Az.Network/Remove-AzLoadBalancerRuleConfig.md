---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265950"
---
# <span data-ttu-id="0ff29-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff29-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0ff29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ff29-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff29-103">Bir yük dengeleyicinin kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0ff29-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0ff29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ff29-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ff29-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff29-106">**Remove-AzLoadBalancerRuleConfig** cmdlet 'i, bir Azure Yük dengeleyicinin bir kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0ff29-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0ff29-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ff29-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff29-108">Örnek 1: yük dengeleyiciden bir kural yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0ff29-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0ff29-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0ff29-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="0ff29-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden MyLBruleName adlı kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0ff29-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0ff29-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ff29-111">PARAMETERS</span></span>

### <span data-ttu-id="0ff29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff29-112">-DefaultProfile</span></span>
<span data-ttu-id="0ff29-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ff29-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff29-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff29-114">-LoadBalancer</span></span>
<span data-ttu-id="0ff29-115">Bu cmdlet 'in kaldırıldığı kural yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff29-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ff29-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ff29-116">-Name</span></span>
<span data-ttu-id="0ff29-117">Bu cmdlet 'in kaldırıldığı yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ff29-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0ff29-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ff29-118">-Confirm</span></span>
<span data-ttu-id="0ff29-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ff29-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff29-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff29-120">-WhatIf</span></span>
<span data-ttu-id="0ff29-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ff29-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff29-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ff29-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff29-123">CommonParameters</span></span>
<span data-ttu-id="0ff29-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ff29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff29-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff29-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff29-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ff29-126">INPUTS</span></span>

### <span data-ttu-id="0ff29-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff29-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0ff29-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ff29-128">OUTPUTS</span></span>

### <span data-ttu-id="0ff29-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff29-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0ff29-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ff29-130">NOTES</span></span>

## <span data-ttu-id="0ff29-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ff29-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ff29-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff29-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ff29-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0ff29-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0ff29-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff29-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ff29-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff29-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ff29-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ff29-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


