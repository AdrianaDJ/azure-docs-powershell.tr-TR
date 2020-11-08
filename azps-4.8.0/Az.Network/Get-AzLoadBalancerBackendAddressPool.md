---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274135"
---
# <span data-ttu-id="e7374-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7374-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="e7374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7374-102">SYNOPSIS</span></span>
<span data-ttu-id="e7374-103">Get-AzLoadBalancerBackendAddressPool bir yük dengeleyiciyle ilişkili bir veya daha fazla arka uç adres havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="e7374-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="e7374-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7374-104">SYNTAX</span></span>

### <span data-ttu-id="e7374-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7374-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7374-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7374-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7374-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e7374-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7374-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7374-108">DESCRIPTION</span></span>
<span data-ttu-id="e7374-109">Get-AzLoadBalancerBackendAddressPool bir yük dengeleyiciyle ilişkili bir veya daha fazla arka uç adres havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="e7374-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="e7374-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7374-110">EXAMPLES</span></span>

### <span data-ttu-id="e7374-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7374-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="e7374-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7374-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="e7374-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e7374-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="e7374-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7374-114">PARAMETERS</span></span>

### <span data-ttu-id="e7374-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7374-115">-DefaultProfile</span></span>
<span data-ttu-id="e7374-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7374-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7374-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7374-117">-LoadBalancer</span></span>
<span data-ttu-id="e7374-118">{{Fill LoadBalancer açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="e7374-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7374-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="e7374-119">-LoadBalancerName</span></span>
<span data-ttu-id="e7374-120">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="e7374-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7374-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7374-121">-Name</span></span>
<span data-ttu-id="e7374-122">Arka uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e7374-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7374-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7374-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7374-124">Yük dengeleyicinin kaynak grup adı.</span><span class="sxs-lookup"><span data-stu-id="e7374-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7374-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7374-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7374-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7374-126">CommonParameters</span></span>
<span data-ttu-id="e7374-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7374-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7374-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7374-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7374-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7374-129">INPUTS</span></span>

### <span data-ttu-id="e7374-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7374-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e7374-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e7374-131">System.String</span></span>

## <span data-ttu-id="e7374-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7374-132">OUTPUTS</span></span>

### <span data-ttu-id="e7374-133">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7374-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e7374-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7374-134">NOTES</span></span>

## <span data-ttu-id="e7374-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7374-135">RELATED LINKS</span></span>
