---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106870"
---
# <span data-ttu-id="dd3e2-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="dd3e2-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="dd3e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd3e2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3e2-103">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-103">Create or update a quota.</span></span>

## <span data-ttu-id="dd3e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd3e2-104">SYNTAX</span></span>

### <span data-ttu-id="dd3e2-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd3e2-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd3e2-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="dd3e2-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd3e2-107">Createviaıdentity</span><span class="sxs-lookup"><span data-stu-id="dd3e2-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dd3e2-108">Createviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="dd3e2-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd3e2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd3e2-109">DESCRIPTION</span></span>
<span data-ttu-id="dd3e2-110">Kota oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-110">Create or update a quota.</span></span>

## <span data-ttu-id="dd3e2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd3e2-111">EXAMPLES</span></span>

### <span data-ttu-id="dd3e2-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd3e2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="dd3e2-113">Tüm varsayılan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="dd3e2-114">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd3e2-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="dd3e2-115">Kota için varsayılan olmayan değerlerle yeni bir ağ kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="dd3e2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd3e2-116">PARAMETERS</span></span>

### <span data-ttu-id="dd3e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3e2-117">-DefaultProfile</span></span>
<span data-ttu-id="dd3e2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd3e2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd3e2-119">-InputObject</span></span>
<span data-ttu-id="dd3e2-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="dd3e2-121">-Location</span></span>
<span data-ttu-id="dd3e2-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="dd3e2-124">Kiracı aboneliğinin hazırlayabileceğiniz maksimum yük dengeleyicili sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="dd3e2-126">Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-127">-Maxpublicıpspersubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="dd3e2-128">Kiracı aboneliğinin hazırlayabileceğiniz en fazla genel IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="dd3e2-130">Kiracı aboneliğinin yapabileceği en fazla güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="dd3e2-132">Kiracı aboneliğinin yapabileceği en fazla sanal ağ ağ geçidi bağlantısı sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="dd3e2-134">Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ geçidi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="dd3e2-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="dd3e2-136">Kiracı aboneliğinin hazırlayabileceğiniz sanal ağ sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd3e2-137">-Name</span></span>
<span data-ttu-id="dd3e2-138">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-139">-Kota</span><span class="sxs-lookup"><span data-stu-id="dd3e2-139">-Quota</span></span>
<span data-ttu-id="dd3e2-140">Ağ kotası kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-140">Network quota resource.</span></span>
<span data-ttu-id="dd3e2-141">Oluşturmak için, kota özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-142">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dd3e2-142">-SubscriptionId</span></span>
<span data-ttu-id="dd3e2-143">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd3e2-144">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dd3e2-145">-Tag</span></span>
<span data-ttu-id="dd3e2-146">Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd3e2-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd3e2-147">-Confirm</span></span>
<span data-ttu-id="dd3e2-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd3e2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3e2-149">-WhatIf</span></span>
<span data-ttu-id="dd3e2-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd3e2-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd3e2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3e2-152">CommonParameters</span></span>
<span data-ttu-id="dd3e2-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3e2-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3e2-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd3e2-155">INPUTS</span></span>

### <span data-ttu-id="dd3e2-156">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota</span><span class="sxs-lookup"><span data-stu-id="dd3e2-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="dd3e2-157">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. ınetworkadminıdentity</span><span class="sxs-lookup"><span data-stu-id="dd3e2-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="dd3e2-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd3e2-158">OUTPUTS</span></span>

### <span data-ttu-id="dd3e2-159">Microsoft. Azure. PowerShell. cmdlet. NetworkAdmin. model. Api20150615. ıquota</span><span class="sxs-lookup"><span data-stu-id="dd3e2-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="dd3e2-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd3e2-160">NOTES</span></span>

<span data-ttu-id="dd3e2-161">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd3e2-162">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dd3e2-163">INPUTOBJECT <INetworkAdminIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="dd3e2-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd3e2-164">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="dd3e2-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd3e2-165">`[Location <String>]`: Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dd3e2-166">`[ResourceName <String>]`: Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="dd3e2-167">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd3e2-168">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="dd3e2-169">Kota <IQuota> : ağ kotası kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="dd3e2-170">`[Tag <IResourceTags>]`: Anahtar değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="dd3e2-171">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dd3e2-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla yük dengeleyicileri sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-173">`[MaxNicsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla NIC sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla genel IP adresi sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için en fazla güvenlik grubu sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Kiracı aboneliğinin sağlaması için sanal ağ geçidi bağlantılarının en fazla sayısı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ ağ geçidi sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="dd3e2-178">`[MaxVnetsPerSubscription <Int64?>]`: Kiracı aboneliğinin yapabileceği sanal ağ sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="dd3e2-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd3e2-179">RELATED LINKS</span></span>

