---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104035"
---
# <span data-ttu-id="c3357-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3357-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c3357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3357-102">SYNOPSIS</span></span>
<span data-ttu-id="c3357-103">Bir yük dengeleyiciden gelen NAT havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3357-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="c3357-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3357-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3357-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3357-105">DESCRIPTION</span></span>
<span data-ttu-id="c3357-106">**Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet 'i, bir yük DENGELEYICIDEN gelen NAT havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3357-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="c3357-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3357-107">EXAMPLES</span></span>

### <span data-ttu-id="c3357-108">1: kaldırma</span><span class="sxs-lookup"><span data-stu-id="c3357-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="c3357-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3357-109">PARAMETERS</span></span>

### <span data-ttu-id="c3357-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3357-110">-DefaultProfile</span></span>
<span data-ttu-id="c3357-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3357-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3357-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3357-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="c3357-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3357-113">-Name</span></span>
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

### <span data-ttu-id="c3357-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3357-114">-Confirm</span></span>
<span data-ttu-id="c3357-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3357-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3357-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3357-116">-WhatIf</span></span>
<span data-ttu-id="c3357-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3357-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3357-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3357-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3357-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3357-119">CommonParameters</span></span>
<span data-ttu-id="c3357-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3357-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3357-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3357-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3357-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3357-122">INPUTS</span></span>

### <span data-ttu-id="c3357-123">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3357-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3357-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3357-124">OUTPUTS</span></span>

### <span data-ttu-id="c3357-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3357-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3357-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3357-126">NOTES</span></span>

## <span data-ttu-id="c3357-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3357-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3357-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3357-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c3357-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3357-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c3357-130">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="c3357-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c3357-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3357-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
