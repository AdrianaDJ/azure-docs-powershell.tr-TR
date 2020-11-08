---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106869"
---
# <span data-ttu-id="0ef36-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0ef36-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="0ef36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef36-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef36-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0ef36-103">Create or update a quota.</span></span>

## <span data-ttu-id="0ef36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ef36-104">SYNTAX</span></span>

### <span data-ttu-id="0ef36-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ef36-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ef36-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="0ef36-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ef36-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ef36-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef36-108">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0ef36-108">Create or update a quota.</span></span>

## <span data-ttu-id="0ef36-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ef36-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef36-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ef36-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="0ef36-111">Ağ kotasını ada göre güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0ef36-111">Update a network quota by name.</span></span>

### <span data-ttu-id="0ef36-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ef36-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="0ef36-113">Ağ kotasını ada göre güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0ef36-113">Update a network quota by name.</span></span>

## <span data-ttu-id="0ef36-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ef36-114">PARAMETERS</span></span>

### <span data-ttu-id="0ef36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef36-115">-DefaultProfile</span></span>
<span data-ttu-id="0ef36-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ef36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0ef36-117">-Location</span></span>
<span data-ttu-id="0ef36-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="0ef36-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="0ef36-120">Kiracı aboneliğinin hazırlayabileceğiniz maksimum yük dengeleyicili sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="0ef36-122">Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-123">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="0ef36-124">Kiracı aboneliğinin hazırlayabileceğiniz en fazla genel IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="0ef36-126">Kiracı aboneliğinin yapabileceği en fazla güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="0ef36-128">Kiracı aboneliğinin yapabileceği en fazla sanal ağ ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="0ef36-130">Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ geçidi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0ef36-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="0ef36-132">Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ef36-133">-Name</span></span>
<span data-ttu-id="0ef36-134">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-135">-Kota</span><span class="sxs-lookup"><span data-stu-id="0ef36-135">-Quota</span></span>
<span data-ttu-id="0ef36-136">Ağ kotası kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-136">Network quota resource.</span></span>
<span data-ttu-id="0ef36-137">Oluşturmak için, kota özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ef36-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0ef36-138">-SubscriptionId</span></span>
<span data-ttu-id="0ef36-139">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="0ef36-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ef36-140">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0ef36-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0ef36-141">-Tag</span></span>
<span data-ttu-id="0ef36-142">Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="0ef36-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ef36-143">-Confirm</span></span>
<span data-ttu-id="0ef36-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ef36-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef36-145">-WhatIf</span></span>
<span data-ttu-id="0ef36-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ef36-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef36-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0ef36-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0ef36-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef36-148">CommonParameters</span></span>
<span data-ttu-id="0ef36-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ef36-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef36-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0ef36-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef36-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ef36-151">INPUTS</span></span>

### <span data-ttu-id="0ef36-152">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota</span><span class="sxs-lookup"><span data-stu-id="0ef36-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="0ef36-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ef36-153">OUTPUTS</span></span>

### <span data-ttu-id="0ef36-154">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota</span><span class="sxs-lookup"><span data-stu-id="0ef36-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="0ef36-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ef36-155">NOTES</span></span>

<span data-ttu-id="0ef36-156">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ef36-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ef36-157">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ef36-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0ef36-158">Kota <IQuota> : ağ kotası kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="0ef36-159">`[Tag <IResourceTags>]`: Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="0ef36-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="0ef36-160">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ef36-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0ef36-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla yük dengeleyicileri sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-162">`[MaxNicsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla genel IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için sanal ağ geçidi bağlantılarının en fazla sayısı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ ağ geçidi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0ef36-167">`[MaxVnetsPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="0ef36-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="0ef36-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ef36-168">RELATED LINKS</span></span>

