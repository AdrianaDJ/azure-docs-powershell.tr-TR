---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591937"
---
# <span data-ttu-id="da198-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="da198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da198-102">SYNOPSIS</span></span>
<span data-ttu-id="da198-103">Bir yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="da198-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da198-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da198-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da198-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da198-105">DESCRIPTION</span></span>
<span data-ttu-id="da198-106">**Set-AzureRmLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="da198-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="da198-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da198-107">EXAMPLES</span></span>

### <span data-ttu-id="da198-108">Örnek 1: yük dengeleyiciyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="da198-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="da198-109">İlk komut NRPLB adlı yük dengeleyicın alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="da198-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="da198-110">İkinci $slb komut, (NewRule adlı bir gelen NAT kuralı ekleyen-AzureRmLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="da198-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="da198-111">Üçüncü komut yük dengeleyiciyi, yük dengeleyici yapılandırmasını güncelleştiren ve kaydeden **-AzureRmLoadBalancer** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="da198-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="da198-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da198-112">PARAMETERS</span></span>

### <span data-ttu-id="da198-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="da198-113">-AsJob</span></span>
<span data-ttu-id="da198-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="da198-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da198-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da198-115">-DefaultProfile</span></span>
<span data-ttu-id="da198-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da198-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da198-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-117">-LoadBalancer</span></span>
<span data-ttu-id="da198-118">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="da198-118">Specifies a load balancer.</span></span>
<span data-ttu-id="da198-119">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="da198-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="da198-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="da198-120">-Confirm</span></span>
<span data-ttu-id="da198-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da198-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da198-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da198-122">-WhatIf</span></span>
<span data-ttu-id="da198-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da198-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da198-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da198-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da198-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da198-125">CommonParameters</span></span>
<span data-ttu-id="da198-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da198-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da198-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da198-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da198-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da198-128">INPUTS</span></span>

### <span data-ttu-id="da198-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="da198-130">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da198-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="da198-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da198-131">OUTPUTS</span></span>

### <span data-ttu-id="da198-132">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="da198-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da198-133">NOTES</span></span>

## <span data-ttu-id="da198-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da198-134">RELATED LINKS</span></span>

[<span data-ttu-id="da198-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="da198-136">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="da198-137">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da198-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


