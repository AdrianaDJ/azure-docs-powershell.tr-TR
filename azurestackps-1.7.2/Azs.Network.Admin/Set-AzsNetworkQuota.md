---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934488"
---
# <span data-ttu-id="baaa2-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="baaa2-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="baaa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baaa2-102">SYNOPSIS</span></span>
<span data-ttu-id="baaa2-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="baaa2-103">Create or update a quota.</span></span>

## <span data-ttu-id="baaa2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baaa2-104">SYNTAX</span></span>

### <span data-ttu-id="baaa2-105">Kotalar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="baaa2-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baaa2-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="baaa2-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baaa2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="baaa2-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baaa2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="baaa2-108">DESCRIPTION</span></span>
<span data-ttu-id="baaa2-109">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="baaa2-109">Create or update a quota.</span></span>

## <span data-ttu-id="baaa2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baaa2-110">EXAMPLES</span></span>

### <span data-ttu-id="baaa2-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="baaa2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="baaa2-112">Ağ kotasını ada göre güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="baaa2-112">Update a network quota by name.</span></span>

### <span data-ttu-id="baaa2-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="baaa2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="baaa2-114">Ağ kotasını ada göre güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="baaa2-114">Update a network quota by name.</span></span>

## <span data-ttu-id="baaa2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baaa2-115">PARAMETERS</span></span>

### <span data-ttu-id="baaa2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baaa2-116">-InputObject</span></span>
<span data-ttu-id="baaa2-117">Get-AzsNetworkQuota tarafından döndürülen ağ kotasını da döndürdü</span><span class="sxs-lookup"><span data-stu-id="baaa2-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="baaa2-118">-Location</span></span>
<span data-ttu-id="baaa2-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="baaa2-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="baaa2-121">Abonelik başına izin verilen maksimum yük dengeleyicileri.</span><span class="sxs-lookup"><span data-stu-id="baaa2-121">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="baaa2-123">Abonelik başına izin verilen en fazla NIC.</span><span class="sxs-lookup"><span data-stu-id="baaa2-123">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-124">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="baaa2-125">Abonelik başına izin verilen en yüksek genel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="baaa2-125">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="baaa2-127">Abonelik başına izin verilen en yüksek güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="baaa2-127">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="baaa2-129">Abonelik başına izin verilen en yüksek sanal ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="baaa2-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="baaa2-131">Abonelik başına izin verilen en fazla sanal ağ ağ geçidi sayısı.</span><span class="sxs-lookup"><span data-stu-id="baaa2-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="baaa2-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="baaa2-133">Abonelik başına izin verilen en yüksek sanal ağ sayısı.</span><span class="sxs-lookup"><span data-stu-id="baaa2-133">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="baaa2-134">-Name</span></span>
<span data-ttu-id="baaa2-135">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="baaa2-135">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="baaa2-136">-ResourceId</span></span>
<span data-ttu-id="baaa2-137">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="baaa2-137">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaa2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="baaa2-138">-Confirm</span></span>
<span data-ttu-id="baaa2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="baaa2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baaa2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baaa2-140">-WhatIf</span></span>
<span data-ttu-id="baaa2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="baaa2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baaa2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="baaa2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baaa2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaa2-143">CommonParameters</span></span>
<span data-ttu-id="baaa2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baaa2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaa2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaa2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaa2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baaa2-146">INPUTS</span></span>

## <span data-ttu-id="baaa2-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baaa2-147">OUTPUTS</span></span>

### <span data-ttu-id="baaa2-148">Microsoft. AzureStack. Management. Network. admin. modeller. Quota</span><span class="sxs-lookup"><span data-stu-id="baaa2-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="baaa2-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baaa2-149">NOTES</span></span>

## <span data-ttu-id="baaa2-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baaa2-150">RELATED LINKS</span></span>

