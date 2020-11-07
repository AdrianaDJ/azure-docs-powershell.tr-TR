---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: d16e0579224907885a2239aa0669ae865ed19dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760012"
---
# <span data-ttu-id="02c43-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="02c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c43-102">SYNOPSIS</span></span>
<span data-ttu-id="02c43-103">Bir yük dengeleyicisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02c43-103">Updates a load balancer.</span></span>

## <span data-ttu-id="02c43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02c43-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02c43-105">DESCRIPTION</span></span>
<span data-ttu-id="02c43-106">**Set-AzLoadBalancer** cmdlet 'i bir yük dengeleyiciyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="02c43-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="02c43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02c43-107">EXAMPLES</span></span>

### <span data-ttu-id="02c43-108">Örnek 1: yük dengeleyiciyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="02c43-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="02c43-109">İlk komut NRPLB adlı yük dengeleyicın alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="02c43-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="02c43-110">İkinci $slb komut, (NewRule adlı bir gelen NAT kuralı ekleyen-AzLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="02c43-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="02c43-111">Üçüncü komut yük dengeleyicın **Ayarla-AzLoadBalancer** 'yi, yük dengeleyici yapılandırmasını güncelleştirir ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="02c43-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="02c43-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02c43-112">PARAMETERS</span></span>

### <span data-ttu-id="02c43-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="02c43-113">-AsJob</span></span>
<span data-ttu-id="02c43-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02c43-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c43-115">-DefaultProfile</span></span>
<span data-ttu-id="02c43-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02c43-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c43-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-117">-LoadBalancer</span></span>
<span data-ttu-id="02c43-118">Yük dengeleyicinin ayarlanması gereken durumu temsil eden bir yük dengeleyici nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="02c43-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02c43-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="02c43-119">-Confirm</span></span>
<span data-ttu-id="02c43-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02c43-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c43-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c43-121">-WhatIf</span></span>
<span data-ttu-id="02c43-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02c43-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02c43-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02c43-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c43-124">CommonParameters</span></span>
<span data-ttu-id="02c43-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02c43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c43-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c43-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c43-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02c43-127">INPUTS</span></span>

### <span data-ttu-id="02c43-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="02c43-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02c43-129">OUTPUTS</span></span>

### <span data-ttu-id="02c43-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="02c43-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02c43-131">NOTES</span></span>

## <span data-ttu-id="02c43-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02c43-132">RELATED LINKS</span></span>

[<span data-ttu-id="02c43-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="02c43-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="02c43-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02c43-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

