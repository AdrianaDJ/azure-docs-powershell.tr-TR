---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265962"
---
# <span data-ttu-id="c14da-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c14da-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="c14da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14da-102">SYNOPSIS</span></span>
<span data-ttu-id="c14da-103">Bir yük dengeleyiciden bir arka uç havuzunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="c14da-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="c14da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c14da-104">SYNTAX</span></span>

### <span data-ttu-id="c14da-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14da-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14da-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14da-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c14da-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c14da-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c14da-108">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c14da-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c14da-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c14da-109">DESCRIPTION</span></span>
<span data-ttu-id="c14da-110">Bir yük dengeleyiciden bir arka uç havuzunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="c14da-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="c14da-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c14da-111">EXAMPLES</span></span>

### <span data-ttu-id="c14da-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c14da-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="c14da-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c14da-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="c14da-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c14da-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="c14da-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c14da-115">PARAMETERS</span></span>

### <span data-ttu-id="c14da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14da-116">-DefaultProfile</span></span>
<span data-ttu-id="c14da-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c14da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c14da-118">-InputObject</span></span>
<span data-ttu-id="c14da-119">Kaldırılacak arka uç adres havuzu</span><span class="sxs-lookup"><span data-stu-id="c14da-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c14da-120">-LoadBalancer</span></span>
<span data-ttu-id="c14da-121">Yük dengeleyici kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c14da-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="c14da-122">-LoadBalancerName</span></span>
<span data-ttu-id="c14da-123">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="c14da-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="c14da-124">-Name</span></span>
<span data-ttu-id="c14da-125">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="c14da-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c14da-126">-PassThru</span></span>
<span data-ttu-id="c14da-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c14da-127">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14da-128">-ResourceGroupName</span></span>
<span data-ttu-id="c14da-129">Yük dengeleyicinin kaynak grup adı.</span><span class="sxs-lookup"><span data-stu-id="c14da-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c14da-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c14da-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c14da-131">-Confirm</span></span>
<span data-ttu-id="c14da-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c14da-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14da-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14da-133">-WhatIf</span></span>
<span data-ttu-id="c14da-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c14da-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14da-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c14da-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14da-136">CommonParameters</span></span>
<span data-ttu-id="c14da-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c14da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14da-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c14da-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14da-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c14da-139">INPUTS</span></span>

### <span data-ttu-id="c14da-140">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c14da-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c14da-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c14da-141">System.String</span></span>

## <span data-ttu-id="c14da-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c14da-142">OUTPUTS</span></span>

### <span data-ttu-id="c14da-143">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c14da-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c14da-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c14da-144">NOTES</span></span>

## <span data-ttu-id="c14da-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c14da-145">RELATED LINKS</span></span>
