---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934727"
---
# <span data-ttu-id="0d31d-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0d31d-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="0d31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d31d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d31d-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0d31d-103">Create or update a quota.</span></span>

## <span data-ttu-id="0d31d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d31d-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d31d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d31d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d31d-106">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0d31d-106">Create or update a quota.</span></span>

## <span data-ttu-id="0d31d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d31d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d31d-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="0d31d-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="0d31d-109">Tüm varsayılan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d31d-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="0d31d-110">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="0d31d-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="0d31d-111">Kota için varsayılan olmayan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d31d-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="0d31d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d31d-112">PARAMETERS</span></span>

### <span data-ttu-id="0d31d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d31d-113">-Name</span></span>
<span data-ttu-id="0d31d-114">Ağ kotası kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0d31d-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="0d31d-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="0d31d-116">Abonelik başına izin verilen en fazla NIC.</span><span class="sxs-lookup"><span data-stu-id="0d31d-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-117">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="0d31d-118">Abonelik başına izin verilen en yüksek genel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0d31d-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="0d31d-120">Abonelik başına izin verilen en yüksek sanal ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="0d31d-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="0d31d-122">Abonelik başına izin verilen en yüksek sanal ağ sayısı.</span><span class="sxs-lookup"><span data-stu-id="0d31d-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="0d31d-124">Abonelik başına izin verilen en fazla sanal ağ ağ geçidi sayısı.</span><span class="sxs-lookup"><span data-stu-id="0d31d-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="0d31d-126">Abonelik başına izin verilen en yüksek güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="0d31d-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0d31d-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="0d31d-128">Abonelik başına izin verilen maksimum yük dengeleyicileri.</span><span class="sxs-lookup"><span data-stu-id="0d31d-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="0d31d-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="0d31d-129">-Location</span></span>
<span data-ttu-id="0d31d-130">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="0d31d-130">Location of the resource.</span></span>

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

### <span data-ttu-id="0d31d-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="0d31d-131">-MigrationPhase</span></span>
<span data-ttu-id="0d31d-132">Yok, hazırla, Commit ve Abort gibi geçişin durumu.</span><span class="sxs-lookup"><span data-stu-id="0d31d-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="0d31d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d31d-133">-WhatIf</span></span>
<span data-ttu-id="0d31d-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d31d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d31d-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d31d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d31d-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d31d-136">-Confirm</span></span>
<span data-ttu-id="0d31d-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d31d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d31d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d31d-138">CommonParameters</span></span>
<span data-ttu-id="0d31d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d31d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d31d-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d31d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d31d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d31d-141">INPUTS</span></span>

## <span data-ttu-id="0d31d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d31d-142">OUTPUTS</span></span>

### <span data-ttu-id="0d31d-143">Microsoft. AzureStack. Management. Network. admin. modeller. Quota</span><span class="sxs-lookup"><span data-stu-id="0d31d-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="0d31d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d31d-144">NOTES</span></span>

## <span data-ttu-id="0d31d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d31d-145">RELATED LINKS</span></span>
