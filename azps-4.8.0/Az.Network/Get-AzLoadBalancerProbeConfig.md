---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108923"
---
# <span data-ttu-id="a88f2-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a88f2-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a88f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a88f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a88f2-103">Bir yük dengeleyicinin yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a88f2-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="a88f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a88f2-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a88f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a88f2-105">DESCRIPTION</span></span>
<span data-ttu-id="a88f2-106">**Get-AzLoadBalancerProbeConfig** cmdlet 'i bir yük dengeleyicinin bir veya daha fazla yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a88f2-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="a88f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a88f2-107">EXAMPLES</span></span>

### <span data-ttu-id="a88f2-108">Örnek 1: yük dengeleyicinin yoklama yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="a88f2-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="a88f2-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a88f2-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a88f2-110">İkinci komut, $slb 'daki yük dengeleyiciden Myyoklama adlı ilişkili yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="a88f2-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="a88f2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a88f2-111">PARAMETERS</span></span>

### <span data-ttu-id="a88f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88f2-112">-DefaultProfile</span></span>
<span data-ttu-id="a88f2-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a88f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a88f2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a88f2-114">-LoadBalancer</span></span>
<span data-ttu-id="a88f2-115">Alınacak yoklama yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88f2-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="a88f2-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a88f2-116">-Name</span></span>
<span data-ttu-id="a88f2-117">Alınacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88f2-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="a88f2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88f2-118">CommonParameters</span></span>
<span data-ttu-id="a88f2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a88f2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88f2-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a88f2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88f2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a88f2-121">INPUTS</span></span>

### <span data-ttu-id="a88f2-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a88f2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a88f2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a88f2-123">OUTPUTS</span></span>

### <span data-ttu-id="a88f2-124">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="a88f2-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a88f2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a88f2-125">NOTES</span></span>

## <span data-ttu-id="a88f2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a88f2-126">RELATED LINKS</span></span>

[<span data-ttu-id="a88f2-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a88f2-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a88f2-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a88f2-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a88f2-129">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a88f2-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a88f2-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a88f2-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a88f2-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a88f2-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


