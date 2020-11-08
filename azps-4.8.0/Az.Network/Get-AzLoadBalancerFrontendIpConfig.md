---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 776ff53573fa68d1757ea7c0422579e253661968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266058"
---
# <span data-ttu-id="d7c88-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d7c88-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d7c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c88-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c88-103">Bir yük dengeleyicide ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d7c88-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="d7c88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7c88-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c88-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7c88-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c88-106">**Get-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir yük dengeleyicide ön uç IP yapılandırmalarını veya ön uç IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d7c88-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="d7c88-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7c88-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c88-108">Örnek 1: yük dengeleyicide ön uç IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="d7c88-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="d7c88-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d7c88-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d7c88-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d7c88-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="d7c88-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7c88-111">PARAMETERS</span></span>

### <span data-ttu-id="d7c88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c88-112">-DefaultProfile</span></span>
<span data-ttu-id="d7c88-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7c88-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c88-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7c88-114">-LoadBalancer</span></span>
<span data-ttu-id="d7c88-115">Alınacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7c88-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="d7c88-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7c88-116">-Name</span></span>
<span data-ttu-id="d7c88-117">Alınacak ön uç IP yapılandırmasını içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7c88-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="d7c88-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c88-118">CommonParameters</span></span>
<span data-ttu-id="d7c88-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7c88-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c88-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7c88-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c88-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7c88-121">INPUTS</span></span>

### <span data-ttu-id="d7c88-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7c88-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d7c88-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7c88-123">OUTPUTS</span></span>

### <span data-ttu-id="d7c88-124">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7c88-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d7c88-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7c88-125">NOTES</span></span>

## <span data-ttu-id="d7c88-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7c88-126">RELATED LINKS</span></span>

[<span data-ttu-id="d7c88-127">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d7c88-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d7c88-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7c88-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d7c88-129">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d7c88-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d7c88-130">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d7c88-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d7c88-131">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d7c88-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


