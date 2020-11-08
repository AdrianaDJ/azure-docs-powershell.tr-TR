---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278259"
---
# <span data-ttu-id="3d6e7-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3d6e7-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="3d6e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6e7-103">Bir loadbalancer 'da arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="3d6e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d6e7-104">SYNTAX</span></span>

### <span data-ttu-id="3d6e7-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6e7-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6e7-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d6e7-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6e7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d6e7-107">DESCRIPTION</span></span>
<span data-ttu-id="3d6e7-108">Bir loadbalancer 'da arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="3d6e7-109">PSLoadBalancerBackendAddress dizisini belirtilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="3d6e7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d6e7-110">EXAMPLES</span></span>

### <span data-ttu-id="3d6e7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d6e7-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="3d6e7-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d6e7-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="3d6e7-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3d6e7-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="3d6e7-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3d6e7-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="3d6e7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d6e7-115">PARAMETERS</span></span>

### <span data-ttu-id="3d6e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6e7-116">-DefaultProfile</span></span>
<span data-ttu-id="3d6e7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d6e7-118">-LoadBalancer</span></span>
<span data-ttu-id="3d6e7-119">Yük dengeleyici kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="3d6e7-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="3d6e7-121">Arka uç adresleri.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3d6e7-122">-LoadBalancerName</span></span>
<span data-ttu-id="3d6e7-123">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d6e7-124">-Name</span></span>
<span data-ttu-id="3d6e7-125">Arka uç havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-125">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d6e7-127">Yük dengeleyicinin kaynak grup adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d6e7-128">-Confirm</span></span>
<span data-ttu-id="3d6e7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6e7-130">-WhatIf</span></span>
<span data-ttu-id="3d6e7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6e7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6e7-133">CommonParameters</span></span>
<span data-ttu-id="3d6e7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6e7-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d6e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6e7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d6e7-136">INPUTS</span></span>

### <span data-ttu-id="3d6e7-137">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3d6e7-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3d6e7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d6e7-138">OUTPUTS</span></span>

### <span data-ttu-id="3d6e7-139">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3d6e7-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3d6e7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d6e7-140">NOTES</span></span>

## <span data-ttu-id="3d6e7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d6e7-141">RELATED LINKS</span></span>
