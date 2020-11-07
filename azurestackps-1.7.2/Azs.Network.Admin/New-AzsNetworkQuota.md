---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751116"
---
# <span data-ttu-id="47247-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="47247-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="47247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47247-102">SYNOPSIS</span></span>
<span data-ttu-id="47247-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="47247-103">Create or update a quota.</span></span>

## <span data-ttu-id="47247-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47247-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47247-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47247-105">DESCRIPTION</span></span>
<span data-ttu-id="47247-106">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="47247-106">Create or update a quota.</span></span>

## <span data-ttu-id="47247-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47247-107">EXAMPLES</span></span>

### <span data-ttu-id="47247-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="47247-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="47247-109">Tüm varsayılan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47247-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="47247-110">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="47247-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="47247-111">Kota için varsayılan olmayan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47247-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="47247-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47247-112">PARAMETERS</span></span>

### <span data-ttu-id="47247-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="47247-113">-Location</span></span>
<span data-ttu-id="47247-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="47247-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="47247-116">Abonelik başına izin verilen maksimum yük dengeleyicileri.</span><span class="sxs-lookup"><span data-stu-id="47247-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="47247-118">Abonelik başına izin verilen en fazla NIC.</span><span class="sxs-lookup"><span data-stu-id="47247-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-119">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="47247-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="47247-120">Abonelik başına izin verilen en yüksek genel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="47247-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="47247-122">Abonelik başına izin verilen en yüksek güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="47247-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="47247-124">Abonelik başına izin verilen en yüksek sanal ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="47247-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="47247-126">Abonelik başına izin verilen en fazla sanal ağ ağ geçidi sayısı.</span><span class="sxs-lookup"><span data-stu-id="47247-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="47247-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="47247-128">Abonelik başına izin verilen en yüksek sanal ağ sayısı.</span><span class="sxs-lookup"><span data-stu-id="47247-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="47247-129">-MigrationPhase</span></span>
<span data-ttu-id="47247-130">Bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="47247-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="47247-131">-Name</span></span>
<span data-ttu-id="47247-132">Ağ kotası kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="47247-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47247-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="47247-133">-Confirm</span></span>
<span data-ttu-id="47247-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47247-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47247-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47247-135">-WhatIf</span></span>
<span data-ttu-id="47247-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47247-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47247-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47247-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47247-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47247-138">CommonParameters</span></span>
<span data-ttu-id="47247-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47247-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47247-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47247-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47247-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47247-141">INPUTS</span></span>

## <span data-ttu-id="47247-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47247-142">OUTPUTS</span></span>

### <span data-ttu-id="47247-143">Microsoft. AzureStack. Management. Network. admin. modeller. Quota</span><span class="sxs-lookup"><span data-stu-id="47247-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="47247-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47247-144">NOTES</span></span>

## <span data-ttu-id="47247-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47247-145">RELATED LINKS</span></span>
