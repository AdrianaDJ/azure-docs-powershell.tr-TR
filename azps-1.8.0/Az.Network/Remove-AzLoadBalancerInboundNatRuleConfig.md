---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760159"
---
# <span data-ttu-id="34b96-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34b96-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="34b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b96-102">SYNOPSIS</span></span>
<span data-ttu-id="34b96-103">Bir yük dengeleyiciden gelen NAT kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34b96-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="34b96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34b96-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34b96-105">DESCRIPTION</span></span>
<span data-ttu-id="34b96-106">**Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet 'i, bir Azure yük dengeleyiciden gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34b96-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="34b96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34b96-107">EXAMPLES</span></span>

### <span data-ttu-id="34b96-108">1: Azure yük dengeleyiciden gelen NAT kuralını silme</span><span class="sxs-lookup"><span data-stu-id="34b96-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="34b96-109">İlk komut, önceden "mylb" adlı bir yük dengeleyicisi yükler ve bunu değişken $load dengeleyicide depolar.</span><span class="sxs-lookup"><span data-stu-id="34b96-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="34b96-110">İkinci komut bu yük dengeleyiciyle ilişkili gelen NAT kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34b96-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="34b96-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34b96-111">PARAMETERS</span></span>

### <span data-ttu-id="34b96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b96-112">-DefaultProfile</span></span>
<span data-ttu-id="34b96-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34b96-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b96-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34b96-114">-LoadBalancer</span></span>
<span data-ttu-id="34b96-115">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34b96-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34b96-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="34b96-116">-Name</span></span>
<span data-ttu-id="34b96-117">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34b96-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34b96-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="34b96-118">-Confirm</span></span>
<span data-ttu-id="34b96-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34b96-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b96-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b96-120">-WhatIf</span></span>
<span data-ttu-id="34b96-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34b96-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34b96-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34b96-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b96-123">CommonParameters</span></span>
<span data-ttu-id="34b96-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34b96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b96-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b96-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34b96-126">INPUTS</span></span>

### <span data-ttu-id="34b96-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34b96-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="34b96-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34b96-128">OUTPUTS</span></span>

### <span data-ttu-id="34b96-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34b96-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="34b96-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34b96-130">NOTES</span></span>

## <span data-ttu-id="34b96-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34b96-131">RELATED LINKS</span></span>

[<span data-ttu-id="34b96-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34b96-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34b96-133">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="34b96-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34b96-134">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="34b96-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34b96-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34b96-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


