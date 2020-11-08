---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278108"
---
# <span data-ttu-id="00983-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00983-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="00983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00983-102">SYNOPSIS</span></span>
<span data-ttu-id="00983-103">Bir yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00983-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="00983-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00983-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00983-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00983-105">DESCRIPTION</span></span>
<span data-ttu-id="00983-106">**Remove-AzLoadBalancerProbeConfig** cmdlet 'i yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00983-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="00983-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00983-107">EXAMPLES</span></span>

### <span data-ttu-id="00983-108">Örnek 1: yük dengeleyiciden yoklama yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="00983-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="00983-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00983-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="00983-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden Myyoklama adlı yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="00983-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="00983-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00983-111">PARAMETERS</span></span>

### <span data-ttu-id="00983-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00983-112">-DefaultProfile</span></span>
<span data-ttu-id="00983-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00983-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00983-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00983-114">-LoadBalancer</span></span>
<span data-ttu-id="00983-115">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="00983-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00983-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="00983-116">-Name</span></span>
<span data-ttu-id="00983-117">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00983-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00983-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="00983-118">-Confirm</span></span>
<span data-ttu-id="00983-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00983-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00983-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00983-120">-WhatIf</span></span>
<span data-ttu-id="00983-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00983-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00983-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00983-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00983-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00983-123">CommonParameters</span></span>
<span data-ttu-id="00983-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00983-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00983-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00983-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00983-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00983-126">INPUTS</span></span>

### <span data-ttu-id="00983-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00983-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00983-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00983-128">OUTPUTS</span></span>

### <span data-ttu-id="00983-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00983-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="00983-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00983-130">NOTES</span></span>

## <span data-ttu-id="00983-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00983-131">RELATED LINKS</span></span>

[<span data-ttu-id="00983-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00983-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="00983-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="00983-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="00983-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00983-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="00983-135">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00983-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="00983-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00983-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


