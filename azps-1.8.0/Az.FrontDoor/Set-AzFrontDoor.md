---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916687"
---
# <span data-ttu-id="c5d11-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c5d11-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="c5d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d11-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d11-103">Ön kapı yük dengeleyicisi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c5d11-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="c5d11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5d11-104">SYNTAX</span></span>

### <span data-ttu-id="c5d11-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5d11-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5d11-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5d11-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5d11-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c5d11-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5d11-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5d11-108">DESCRIPTION</span></span>
<span data-ttu-id="c5d11-109">**Set-Azfrontkapı** cmdlet 'i, bir ön kapı yük dengeleyicisine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="c5d11-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="c5d11-110">Giriş parametreleri sağlanmadıysa, var olan ön kapıdan gelen eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c5d11-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="c5d11-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5d11-111">EXAMPLES</span></span>

### <span data-ttu-id="c5d11-112">Örnek 1: FrontDoorName ve ResourceGroupName ile mevcut bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d11-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="c5d11-113">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d11-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="c5d11-114">Örnek 2: Psfrontkapısı nesnesiyle varolan bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d11-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="c5d11-115">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d11-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="c5d11-116">Örnek 3: RESOURCEID ile mevcut bir ön kapıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c5d11-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
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

<span data-ttu-id="c5d11-117">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d11-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="c5d11-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5d11-118">PARAMETERS</span></span>

### <span data-ttu-id="c5d11-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="c5d11-119">-BackendPool</span></span>
<span data-ttu-id="c5d11-120">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="c5d11-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="c5d11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d11-121">-DefaultProfile</span></span>
<span data-ttu-id="c5d11-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5d11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d11-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c5d11-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="c5d11-124">HTTPS isteklerinin tüm arka uç havuzlarına yönelik sertifika adı denetimini devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="c5d11-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="c5d11-125">HTTPS olmayan isteklerde hiçbir etkiye gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="c5d11-125">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d11-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c5d11-126">-EnabledState</span></span>
<span data-ttu-id="c5d11-127">Ön kapı yük dengeleyicinin işletim durumu.</span><span class="sxs-lookup"><span data-stu-id="c5d11-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="c5d11-128">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="c5d11-128">-FrontendEndpoint</span></span>
<span data-ttu-id="c5d11-129">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="c5d11-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="c5d11-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c5d11-130">-HealthProbeSetting</span></span>
<span data-ttu-id="c5d11-131">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="c5d11-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c5d11-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5d11-132">-InputObject</span></span>
<span data-ttu-id="c5d11-133">Güncelleştirilecek ön kapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c5d11-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d11-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="c5d11-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="c5d11-135">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="c5d11-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c5d11-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5d11-136">-Name</span></span>
<span data-ttu-id="c5d11-137">Güncelleştirilecek ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="c5d11-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d11-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d11-138">-ResourceGroupName</span></span>
<span data-ttu-id="c5d11-139">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c5d11-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d11-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5d11-140">-ResourceId</span></span>
<span data-ttu-id="c5d11-141">Güncelleştirilecek ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c5d11-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d11-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="c5d11-142">-RoutingRule</span></span>
<span data-ttu-id="c5d11-143">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="c5d11-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="c5d11-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c5d11-144">-Tag</span></span>
<span data-ttu-id="c5d11-145">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="c5d11-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="c5d11-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5d11-146">-Confirm</span></span>
<span data-ttu-id="c5d11-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5d11-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5d11-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5d11-148">-WhatIf</span></span>
<span data-ttu-id="c5d11-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5d11-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5d11-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5d11-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5d11-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d11-151">CommonParameters</span></span>
<span data-ttu-id="c5d11-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5d11-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d11-153">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5d11-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d11-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5d11-154">INPUTS</span></span>

### <span data-ttu-id="c5d11-155">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="c5d11-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="c5d11-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d11-156">System.String</span></span>

## <span data-ttu-id="c5d11-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5d11-157">OUTPUTS</span></span>

### <span data-ttu-id="c5d11-158">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="c5d11-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="c5d11-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5d11-159">NOTES</span></span>

## <span data-ttu-id="c5d11-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5d11-160">RELATED LINKS</span></span>

<span data-ttu-id="c5d11-161">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Get-Azfrontkapısı](./Get-AzFrontDoor.md) 
 [Remove-Azfrontkapısı](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="c5d11-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
