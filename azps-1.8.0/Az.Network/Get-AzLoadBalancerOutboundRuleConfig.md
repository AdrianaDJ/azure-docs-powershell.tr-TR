---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760550"
---
# <span data-ttu-id="0e36f-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e36f-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="0e36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e36f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e36f-103">Bir yük dengeleyicide giden kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="0e36f-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="0e36f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e36f-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e36f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e36f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e36f-106">Get-Azloadbalanceroutboundbir yük dengeleyicide giden kural yapılandırmalarının bir listesini veya **Get-Azloadbalanceroutboundoutboundruleconfig** cmdlet 'i alır.</span><span class="sxs-lookup"><span data-stu-id="0e36f-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="0e36f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e36f-107">EXAMPLES</span></span>

### <span data-ttu-id="0e36f-108">Örnek 1: yük dengeleyicide giden kural yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="0e36f-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="0e36f-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0e36f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0e36f-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş MyRule adlı giden kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="0e36f-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="0e36f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e36f-111">PARAMETERS</span></span>

### <span data-ttu-id="0e36f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e36f-112">-DefaultProfile</span></span>
<span data-ttu-id="0e36f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e36f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e36f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e36f-114">-LoadBalancer</span></span>
<span data-ttu-id="0e36f-115">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="0e36f-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="0e36f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e36f-116">-Name</span></span>
<span data-ttu-id="0e36f-117">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="0e36f-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="0e36f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e36f-118">CommonParameters</span></span>
<span data-ttu-id="0e36f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e36f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e36f-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e36f-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e36f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e36f-121">INPUTS</span></span>

### <span data-ttu-id="0e36f-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e36f-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0e36f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e36f-123">OUTPUTS</span></span>

### <span data-ttu-id="0e36f-124">Microsoft. Azure. Commands. Network. model. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="0e36f-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="0e36f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e36f-125">NOTES</span></span>

## <span data-ttu-id="0e36f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e36f-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e36f-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e36f-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0e36f-128">Yeni-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e36f-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0e36f-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e36f-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0e36f-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e36f-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
