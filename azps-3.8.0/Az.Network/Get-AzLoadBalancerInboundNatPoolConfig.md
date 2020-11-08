---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098814"
---
# <span data-ttu-id="22319-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22319-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="22319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22319-102">SYNOPSIS</span></span>
<span data-ttu-id="22319-103">Bir yük dengeleyiciden bir veya birden çok gelen NAT havuz yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22319-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="22319-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22319-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22319-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22319-105">DESCRIPTION</span></span>
<span data-ttu-id="22319-106">**Get-Azloadbalancerınboundnatpoolconfig** cmdlet 'i, bir yük dengeleyiciden bir veya birden çok gelen NAT havuz yapılandırması alır.</span><span class="sxs-lookup"><span data-stu-id="22319-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="22319-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22319-107">EXAMPLES</span></span>

### <span data-ttu-id="22319-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="22319-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="22319-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22319-109">PARAMETERS</span></span>

### <span data-ttu-id="22319-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22319-110">-DefaultProfile</span></span>
<span data-ttu-id="22319-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22319-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22319-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22319-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="22319-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="22319-113">-Name</span></span>
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

### <span data-ttu-id="22319-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22319-114">CommonParameters</span></span>
<span data-ttu-id="22319-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22319-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22319-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22319-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22319-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22319-117">INPUTS</span></span>

### <span data-ttu-id="22319-118">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22319-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="22319-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22319-119">OUTPUTS</span></span>

### <span data-ttu-id="22319-120">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="22319-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="22319-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22319-121">NOTES</span></span>

## <span data-ttu-id="22319-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22319-122">RELATED LINKS</span></span>

[<span data-ttu-id="22319-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22319-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="22319-124">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="22319-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="22319-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22319-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="22319-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22319-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
