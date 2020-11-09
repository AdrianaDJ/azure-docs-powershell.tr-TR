---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323866"
---
# <span data-ttu-id="cbb92-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cbb92-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="cbb92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb92-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb92-103">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="cbb92-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="cbb92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbb92-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb92-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbb92-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb92-106">**Get-Azloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure Yük dengeleyicide bir veya birden çok gelen ağ adresi ÇEVIRISI (NAT) kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="cbb92-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="cbb92-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbb92-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb92-108">Örnek 1: gelen NAT kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="cbb92-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="cbb92-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="cbb92-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="cbb92-110">İkinci komut, $slb MyInboundNatRule1 adındaki ilişkili NAT kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="cbb92-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="cbb92-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbb92-111">PARAMETERS</span></span>

### <span data-ttu-id="cbb92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb92-112">-DefaultProfile</span></span>
<span data-ttu-id="cbb92-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbb92-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbb92-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbb92-114">-LoadBalancer</span></span>
<span data-ttu-id="cbb92-115">Alınacak gelen NAT kuralı yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbb92-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="cbb92-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="cbb92-116">-Name</span></span>
<span data-ttu-id="cbb92-117">Alınacak gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cbb92-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="cbb92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb92-118">CommonParameters</span></span>
<span data-ttu-id="cbb92-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbb92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb92-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cbb92-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb92-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbb92-121">INPUTS</span></span>

### <span data-ttu-id="cbb92-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbb92-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cbb92-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbb92-123">OUTPUTS</span></span>

### <span data-ttu-id="cbb92-124">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="cbb92-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="cbb92-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbb92-125">NOTES</span></span>

## <span data-ttu-id="cbb92-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbb92-126">RELATED LINKS</span></span>

[<span data-ttu-id="cbb92-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cbb92-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cbb92-128">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="cbb92-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cbb92-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cbb92-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cbb92-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cbb92-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


