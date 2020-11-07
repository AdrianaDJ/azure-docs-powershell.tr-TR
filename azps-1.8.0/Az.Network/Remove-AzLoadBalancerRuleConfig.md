---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760150"
---
# <span data-ttu-id="7335f-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7335f-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7335f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7335f-102">SYNOPSIS</span></span>
<span data-ttu-id="7335f-103">Bir yük dengeleyicinin kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7335f-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7335f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7335f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7335f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7335f-105">DESCRIPTION</span></span>
<span data-ttu-id="7335f-106">**Remove-AzLoadBalancerRuleConfig** cmdlet 'i, bir Azure Yük dengeleyicinin bir kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7335f-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7335f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7335f-107">EXAMPLES</span></span>

### <span data-ttu-id="7335f-108">Örnek 1: yük dengeleyiciden bir kural yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7335f-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7335f-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7335f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="7335f-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden MyLBruleName adlı kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7335f-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7335f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7335f-111">PARAMETERS</span></span>

### <span data-ttu-id="7335f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7335f-112">-DefaultProfile</span></span>
<span data-ttu-id="7335f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7335f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7335f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7335f-114">-LoadBalancer</span></span>
<span data-ttu-id="7335f-115">Bu cmdlet 'in kaldırıldığı kural yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7335f-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7335f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="7335f-116">-Name</span></span>
<span data-ttu-id="7335f-117">Bu cmdlet 'in kaldırıldığı yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7335f-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7335f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="7335f-118">-Confirm</span></span>
<span data-ttu-id="7335f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7335f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7335f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7335f-120">-WhatIf</span></span>
<span data-ttu-id="7335f-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7335f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7335f-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7335f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7335f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7335f-123">CommonParameters</span></span>
<span data-ttu-id="7335f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7335f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7335f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7335f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7335f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7335f-126">INPUTS</span></span>

### <span data-ttu-id="7335f-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7335f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7335f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7335f-128">OUTPUTS</span></span>

### <span data-ttu-id="7335f-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7335f-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7335f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7335f-130">NOTES</span></span>

## <span data-ttu-id="7335f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7335f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7335f-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7335f-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7335f-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7335f-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7335f-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7335f-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7335f-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7335f-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7335f-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7335f-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


