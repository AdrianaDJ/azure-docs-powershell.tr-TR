---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108840"
---
# <span data-ttu-id="02068-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="02068-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="02068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02068-102">SYNOPSIS</span></span>
<span data-ttu-id="02068-103">Bir loadbalancer</span><span class="sxs-lookup"><span data-stu-id="02068-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="02068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02068-104">SYNTAX</span></span>

### <span data-ttu-id="02068-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02068-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02068-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02068-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02068-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02068-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02068-108">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="02068-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02068-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02068-109">DESCRIPTION</span></span>
<span data-ttu-id="02068-110">Bir loadbalancer</span><span class="sxs-lookup"><span data-stu-id="02068-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="02068-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02068-111">EXAMPLES</span></span>

### <span data-ttu-id="02068-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02068-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="02068-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02068-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="02068-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="02068-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="02068-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02068-115">PARAMETERS</span></span>

### <span data-ttu-id="02068-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02068-116">-DefaultProfile</span></span>
<span data-ttu-id="02068-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02068-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02068-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02068-118">-Force</span></span>
<span data-ttu-id="02068-119">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="02068-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02068-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02068-120">-InputObject</span></span>
<span data-ttu-id="02068-121">Ayarlanacak arka uç adres havuzu</span><span class="sxs-lookup"><span data-stu-id="02068-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02068-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02068-122">-LoadBalancer</span></span>
<span data-ttu-id="02068-123">Yük dengeleyici kaynağı.</span><span class="sxs-lookup"><span data-stu-id="02068-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02068-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="02068-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="02068-125">Arka uç adresleri.</span><span class="sxs-lookup"><span data-stu-id="02068-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02068-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="02068-126">-LoadBalancerName</span></span>
<span data-ttu-id="02068-127">Yük dengeleyicinin adı.</span><span class="sxs-lookup"><span data-stu-id="02068-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02068-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="02068-128">-Name</span></span>
<span data-ttu-id="02068-129">Arka uç havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="02068-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02068-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02068-130">-PassThru</span></span>
<span data-ttu-id="02068-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="02068-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="02068-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02068-132">-ResourceGroupName</span></span>
<span data-ttu-id="02068-133">Yük dengeleyicinin kaynak grup adı.</span><span class="sxs-lookup"><span data-stu-id="02068-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02068-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02068-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02068-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="02068-135">-Confirm</span></span>
<span data-ttu-id="02068-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02068-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02068-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02068-137">-WhatIf</span></span>
<span data-ttu-id="02068-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02068-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02068-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02068-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02068-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02068-140">CommonParameters</span></span>
<span data-ttu-id="02068-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02068-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02068-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02068-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02068-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02068-143">INPUTS</span></span>

### <span data-ttu-id="02068-144">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="02068-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="02068-145">System. String</span><span class="sxs-lookup"><span data-stu-id="02068-145">System.String</span></span>

## <span data-ttu-id="02068-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02068-146">OUTPUTS</span></span>

### <span data-ttu-id="02068-147">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="02068-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="02068-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02068-148">NOTES</span></span>

## <span data-ttu-id="02068-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02068-149">RELATED LINKS</span></span>
