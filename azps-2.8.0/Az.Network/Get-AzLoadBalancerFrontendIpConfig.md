---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a15e72778b1d113722ba5ea414cce08c727953ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932010"
---
# <span data-ttu-id="83b75-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="83b75-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="83b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b75-102">SYNOPSIS</span></span>
<span data-ttu-id="83b75-103">Bir yük dengeleyicide ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="83b75-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="83b75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83b75-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83b75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83b75-105">DESCRIPTION</span></span>
<span data-ttu-id="83b75-106">**Get-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir yük dengeleyicide ön uç IP yapılandırmalarını veya ön uç IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="83b75-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="83b75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83b75-107">EXAMPLES</span></span>

### <span data-ttu-id="83b75-108">Örnek 1: yük dengeleyicide ön uç IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="83b75-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="83b75-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="83b75-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="83b75-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="83b75-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="83b75-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83b75-111">PARAMETERS</span></span>

### <span data-ttu-id="83b75-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b75-112">-DefaultProfile</span></span>
<span data-ttu-id="83b75-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83b75-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83b75-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b75-114">-LoadBalancer</span></span>
<span data-ttu-id="83b75-115">Alınacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="83b75-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="83b75-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="83b75-116">-Name</span></span>
<span data-ttu-id="83b75-117">Alınacak ön uç IP yapılandırmasını içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83b75-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="83b75-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b75-118">CommonParameters</span></span>
<span data-ttu-id="83b75-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83b75-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b75-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83b75-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b75-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83b75-121">INPUTS</span></span>

### <span data-ttu-id="83b75-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b75-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="83b75-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83b75-123">OUTPUTS</span></span>

### <span data-ttu-id="83b75-124">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="83b75-124">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="83b75-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83b75-125">NOTES</span></span>

## <span data-ttu-id="83b75-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83b75-126">RELATED LINKS</span></span>

[<span data-ttu-id="83b75-127">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="83b75-127">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83b75-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83b75-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="83b75-129">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="83b75-129">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83b75-130">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="83b75-130">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="83b75-131">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="83b75-131">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


