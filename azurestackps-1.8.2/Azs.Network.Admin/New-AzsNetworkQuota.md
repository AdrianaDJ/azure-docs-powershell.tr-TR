---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106815"
---
# <span data-ttu-id="0c0a7-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0c0a7-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="0c0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0a7-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-103">Create or update a quota.</span></span>

## <span data-ttu-id="0c0a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c0a7-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c0a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0a7-106">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-106">Create or update a quota.</span></span>

## <span data-ttu-id="0c0a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0a7-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="0c0a7-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="0c0a7-109">Tüm varsayılan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="0c0a7-110">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="0c0a7-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="0c0a7-111">Kota için varsayılan olmayan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="0c0a7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c0a7-112">PARAMETERS</span></span>

### <span data-ttu-id="0c0a7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c0a7-113">-Name</span></span>
<span data-ttu-id="0c0a7-114">Ağ kotası kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="0c0a7-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="0c0a7-116">Abonelik başına izin verilen en fazla NIC.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-117">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="0c0a7-118">Abonelik başına izin verilen en yüksek genel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="0c0a7-120">Abonelik başına izin verilen en yüksek sanal ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="0c0a7-122">Abonelik başına izin verilen en yüksek sanal ağ sayısı.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="0c0a7-124">Abonelik başına izin verilen en fazla sanal ağ ağ geçidi sayısı.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="0c0a7-126">Abonelik başına izin verilen en yüksek güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0c0a7-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="0c0a7-128">Abonelik başına izin verilen maksimum yük dengeleyicileri.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="0c0a7-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="0c0a7-129">-Location</span></span>
<span data-ttu-id="0c0a7-130">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-130">Location of the resource.</span></span>

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

### <span data-ttu-id="0c0a7-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="0c0a7-131">-MigrationPhase</span></span>
<span data-ttu-id="0c0a7-132">Yok, hazırla, Commit ve Abort gibi geçişin durumu.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="0c0a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0a7-133">-WhatIf</span></span>
<span data-ttu-id="0c0a7-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c0a7-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c0a7-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c0a7-136">-Confirm</span></span>
<span data-ttu-id="0c0a7-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c0a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0a7-138">CommonParameters</span></span>
<span data-ttu-id="0c0a7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c0a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0a7-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0a7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0a7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c0a7-141">INPUTS</span></span>

## <span data-ttu-id="0c0a7-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c0a7-142">OUTPUTS</span></span>

### <span data-ttu-id="0c0a7-143">Microsoft. AzureStack. Management. Network. admin. modeller. Quota</span><span class="sxs-lookup"><span data-stu-id="0c0a7-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="0c0a7-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c0a7-144">NOTES</span></span>

## <span data-ttu-id="0c0a7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c0a7-145">RELATED LINKS</span></span>
