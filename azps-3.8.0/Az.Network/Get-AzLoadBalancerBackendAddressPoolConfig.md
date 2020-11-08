---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098818"
---
# <span data-ttu-id="79339-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79339-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="79339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79339-102">SYNOPSIS</span></span>
<span data-ttu-id="79339-103">Bir yük dengeleyicinin arka uç adres havuzu yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="79339-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="79339-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79339-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79339-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79339-105">DESCRIPTION</span></span>
<span data-ttu-id="79339-106">**Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'i, tek bir arka uç adres havuzunu veya bir yük dengeleyicide arka uç adresi havuzlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="79339-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="79339-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79339-107">EXAMPLES</span></span>

### <span data-ttu-id="79339-108">Örnek 1: arka uç adres havuzunu alma</span><span class="sxs-lookup"><span data-stu-id="79339-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="79339-109">İlk komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı mevcut bir yük dengeleyicisi alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79339-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="79339-110">İkinci komut $loadbalancer 'teki yük dengeleyicinin BackendAddressPool02 adlı ilişkili arka uç adres havuzu yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="79339-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="79339-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79339-111">PARAMETERS</span></span>

### <span data-ttu-id="79339-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79339-112">-DefaultProfile</span></span>
<span data-ttu-id="79339-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79339-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79339-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79339-114">-LoadBalancer</span></span>
<span data-ttu-id="79339-115">Alınacak arka uç adres havuzuyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="79339-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="79339-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="79339-116">-Name</span></span>
<span data-ttu-id="79339-117">Alınacak arka uç adres havuzunu içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79339-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="79339-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79339-118">CommonParameters</span></span>
<span data-ttu-id="79339-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79339-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79339-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79339-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79339-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79339-121">INPUTS</span></span>

### <span data-ttu-id="79339-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79339-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79339-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79339-123">OUTPUTS</span></span>

### <span data-ttu-id="79339-124">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79339-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="79339-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79339-125">NOTES</span></span>

## <span data-ttu-id="79339-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79339-126">RELATED LINKS</span></span>

[<span data-ttu-id="79339-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79339-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="79339-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79339-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="79339-129">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79339-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="79339-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="79339-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

