---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265956"
---
# <span data-ttu-id="6e559-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e559-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="6e559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e559-102">SYNOPSIS</span></span>
<span data-ttu-id="6e559-103">Bir yük dengeleyiciden giden kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e559-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="6e559-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e559-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e559-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e559-105">DESCRIPTION</span></span>
<span data-ttu-id="6e559-106">**Remove-Azloadbalanceroutboundmaruleconfig** cmdlet 'i, bir Azure yük dengeleyiciden giden kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e559-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="6e559-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e559-107">EXAMPLES</span></span>

### <span data-ttu-id="6e559-108">Örnek 1: Azure yük dengeleyiciden giden kuralı silme</span><span class="sxs-lookup"><span data-stu-id="6e559-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="6e559-109">İlk komut, kaldırmak istediğiniz giden kuralı yapılandırmasıyla ilişkili yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6e559-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="6e559-110">İkinci komut, yük dengeleyiciden ilişkili giden kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e559-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="6e559-111">Üçüncü komut yük dengeleyiciden günceller.</span><span class="sxs-lookup"><span data-stu-id="6e559-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="6e559-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e559-112">PARAMETERS</span></span>

### <span data-ttu-id="6e559-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e559-113">-DefaultProfile</span></span>
<span data-ttu-id="6e559-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e559-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e559-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6e559-115">-LoadBalancer</span></span>
<span data-ttu-id="6e559-116">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="6e559-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="6e559-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e559-117">-Name</span></span>
<span data-ttu-id="6e559-118">Giden kuralının adı</span><span class="sxs-lookup"><span data-stu-id="6e559-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e559-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e559-119">-Confirm</span></span>
<span data-ttu-id="6e559-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e559-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e559-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e559-121">-WhatIf</span></span>
<span data-ttu-id="6e559-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e559-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e559-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e559-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e559-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e559-124">CommonParameters</span></span>
<span data-ttu-id="6e559-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e559-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e559-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e559-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e559-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e559-127">INPUTS</span></span>

### <span data-ttu-id="6e559-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6e559-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6e559-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e559-129">OUTPUTS</span></span>

### <span data-ttu-id="6e559-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6e559-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6e559-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e559-131">NOTES</span></span>

## <span data-ttu-id="6e559-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e559-132">RELATED LINKS</span></span>

[<span data-ttu-id="6e559-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e559-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6e559-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e559-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6e559-135">Yeni-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e559-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6e559-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6e559-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
