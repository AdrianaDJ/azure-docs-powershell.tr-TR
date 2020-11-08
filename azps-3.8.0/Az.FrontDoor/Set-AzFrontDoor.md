---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 93409d4da37498cf47a95d25bb485c6a9be152cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096642"
---
# <span data-ttu-id="958a0-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="958a0-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="958a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="958a0-102">SYNOPSIS</span></span>
<span data-ttu-id="958a0-103">Ön kapı yük dengeleyicisi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="958a0-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="958a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="958a0-104">SYNTAX</span></span>

### <span data-ttu-id="958a0-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="958a0-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958a0-106">Byalanalan</span><span class="sxs-lookup"><span data-stu-id="958a0-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958a0-107">Byalanlarıbackendpoolssettingparameterset</span><span class="sxs-lookup"><span data-stu-id="958a0-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958a0-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="958a0-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958a0-109">ByObjectWithCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="958a0-109">ByObjectWithCertificateNameCheck</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="958a0-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="958a0-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="958a0-111">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="958a0-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="958a0-112">Byresourceıdwithcertificatenamecheckparameterset</span><span class="sxs-lookup"><span data-stu-id="958a0-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="958a0-113">ByResourceIdWithBackendPoolSettingsParameterSet</span><span class="sxs-lookup"><span data-stu-id="958a0-113">ByResourceIdWithBackendPoolSettingsParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="958a0-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="958a0-114">DESCRIPTION</span></span>
<span data-ttu-id="958a0-115">**Set-Azfrontkapı** cmdlet 'i, bir ön kapı yük dengeleyicisine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="958a0-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="958a0-116">Giriş parametreleri sağlanmadıysa, var olan ön kapıdan gelen eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="958a0-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="958a0-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="958a0-117">EXAMPLES</span></span>

### <span data-ttu-id="958a0-118">Örnek 1: FrontDoorName ve ResourceGroupName ile mevcut bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="958a0-119">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="958a0-120">Örnek 2: Psfrontkapısı nesnesiyle varolan bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="958a0-121">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="958a0-122">Örnek 3: RESOURCEID ile mevcut bir ön kapıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="958a0-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="958a0-123">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="958a0-124">Örnek 4: güncelleştirme BackendPoolSetting özelliği, var olan bir ön kapıdan</span><span class="sxs-lookup"><span data-stu-id="958a0-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="958a0-125">Güncellenecek ön kapı, en sona ve tam ad ile ResourceGroupName, Psfrontkapı nesnesi veya RESOURCEID kullanılarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="958a0-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="958a0-126">(Örneğin, 3 örneğe bakın) Aşağıdaki örnek Psfrontkapı nesnesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="958a0-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="958a0-127">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="958a0-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="958a0-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="958a0-128">PARAMETERS</span></span>

### <span data-ttu-id="958a0-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="958a0-129">-BackendPool</span></span>
<span data-ttu-id="958a0-130">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="958a0-130">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="958a0-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="958a0-132">Tüm backendPools için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="958a0-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolSettingsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958a0-133">-DefaultProfile</span></span>
<span data-ttu-id="958a0-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="958a0-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="958a0-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="958a0-136">HTTPS isteklerinin tüm arka uç havuzlarına yönelik sertifika adı denetimini devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="958a0-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="958a0-137">HTTPS olmayan isteklerde hiçbir etkiye gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="958a0-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheck, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="958a0-138">-EnabledState</span></span>
<span data-ttu-id="958a0-139">Ön kapı yük dengeleyicinin işletim durumu.</span><span class="sxs-lookup"><span data-stu-id="958a0-139">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-140">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="958a0-140">-FrontendEndpoint</span></span>
<span data-ttu-id="958a0-141">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="958a0-141">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="958a0-142">-HealthProbeSetting</span></span>
<span data-ttu-id="958a0-143">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="958a0-143">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="958a0-144">-InputObject</span></span>
<span data-ttu-id="958a0-145">Güncelleştirilecek ön kapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="958a0-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheck, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="958a0-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="958a0-147">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="958a0-147">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="958a0-148">-Name</span></span>
<span data-ttu-id="958a0-149">Güncelleştirilecek ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="958a0-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958a0-150">-ResourceGroupName</span></span>
<span data-ttu-id="958a0-151">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="958a0-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="958a0-152">-ResourceId</span></span>
<span data-ttu-id="958a0-153">Güncelleştirilecek ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="958a0-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolSettingsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="958a0-154">-RoutingRule</span></span>
<span data-ttu-id="958a0-155">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="958a0-155">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="958a0-156">-Tag</span></span>
<span data-ttu-id="958a0-157">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="958a0-157">The tags associate with the FrontDoor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958a0-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="958a0-158">-Confirm</span></span>
<span data-ttu-id="958a0-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="958a0-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="958a0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="958a0-160">-WhatIf</span></span>
<span data-ttu-id="958a0-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="958a0-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="958a0-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="958a0-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="958a0-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958a0-163">CommonParameters</span></span>
<span data-ttu-id="958a0-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="958a0-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958a0-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="958a0-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958a0-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="958a0-166">INPUTS</span></span>

### <span data-ttu-id="958a0-167">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="958a0-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="958a0-168">System. String</span><span class="sxs-lookup"><span data-stu-id="958a0-168">System.String</span></span>
## <span data-ttu-id="958a0-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="958a0-169">OUTPUTS</span></span>

### <span data-ttu-id="958a0-170">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="958a0-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="958a0-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="958a0-171">NOTES</span></span>

## <span data-ttu-id="958a0-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="958a0-172">RELATED LINKS</span></span>

<span data-ttu-id="958a0-173">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Get-Azfrontkapısı](./Get-AzFrontDoor.md) 
 [Remove-Azfrontkapısı](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="958a0-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>