---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279493"
---
# <span data-ttu-id="93bde-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93bde-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="93bde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bde-102">SYNOPSIS</span></span>
<span data-ttu-id="93bde-103">Get-AzLoadBalancerBackendAddressPool bir yük dengeleyiciyle ilişkili bir veya daha fazla arka uç adres havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="93bde-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="93bde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93bde-104">SYNTAX</span></span>

### <span data-ttu-id="93bde-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bde-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bde-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bde-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bde-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="93bde-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93bde-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="93bde-108">DESCRIPTION</span></span>
<span data-ttu-id="93bde-109">Get-AzLoadBalancerBackendAddressPool bir yük dengeleyiciyle ilişkili bir veya daha fazla arka uç adres havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="93bde-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="93bde-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93bde-110">EXAMPLES</span></span>

### <span data-ttu-id="93bde-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="93bde-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="93bde-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="93bde-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="93bde-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="93bde-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="93bde-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93bde-114">PARAMETERS</span></span>

### <span data-ttu-id="93bde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bde-115">-DefaultProfile</span></span>
<span data-ttu-id="93bde-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93bde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93bde-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93bde-117">-LoadBalancer</span></span>
<span data-ttu-id="93bde-118">{{Fill LoadBalancer açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="93bde-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="93bde-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="93bde-119">-LoadBalancerName</span></span>
<span data-ttu-id="93bde-120">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="93bde-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="93bde-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="93bde-121">-Name</span></span>
<span data-ttu-id="93bde-122">Arka uç adres havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="93bde-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="93bde-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bde-123">-ResourceGroupName</span></span>
<span data-ttu-id="93bde-124">Yük dengeleyicinin kaynak grup adı.</span><span class="sxs-lookup"><span data-stu-id="93bde-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="93bde-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="93bde-125">-ResourceId</span></span>

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

### <span data-ttu-id="93bde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bde-126">CommonParameters</span></span>
<span data-ttu-id="93bde-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93bde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bde-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="93bde-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bde-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93bde-129">INPUTS</span></span>

### <span data-ttu-id="93bde-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="93bde-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="93bde-131">System. String</span><span class="sxs-lookup"><span data-stu-id="93bde-131">System.String</span></span>

## <span data-ttu-id="93bde-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93bde-132">OUTPUTS</span></span>

### <span data-ttu-id="93bde-133">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93bde-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="93bde-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93bde-134">NOTES</span></span>

## <span data-ttu-id="93bde-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93bde-135">RELATED LINKS</span></span>
