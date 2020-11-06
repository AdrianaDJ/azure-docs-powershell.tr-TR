---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572746"
---
# <span data-ttu-id="f74a2-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="f74a2-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="f74a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f74a2-103">Ön kapı yük dengeleyicisi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f74a2-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f74a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f74a2-104">SYNTAX</span></span>

### <span data-ttu-id="f74a2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f74a2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f74a2-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74a2-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f74a2-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74a2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f74a2-108">DESCRIPTION</span></span>
<span data-ttu-id="f74a2-109">**Set-Azurermfrontkapısı** cmdlet 'i, bir ön kapı yük dengeleyicmayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f74a2-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="f74a2-110">Giriş parametreleri sağlanmadıysa, var olan ön kapıdan gelen eski parametreler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f74a2-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="f74a2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f74a2-111">EXAMPLES</span></span>

### <span data-ttu-id="f74a2-112">Örnek 1: FrontDoorName ve ResourceGroupName ile mevcut bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f74a2-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f74a2-113">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f74a2-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="f74a2-114">Örnek 2: Psfrontkapısı nesnesiyle varolan bir ön kapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f74a2-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f74a2-115">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f74a2-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="f74a2-116">Örnek 3: RESOURCEID ile mevcut bir ön kapıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f74a2-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="f74a2-117">var olan bir ön kapı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f74a2-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="f74a2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f74a2-118">PARAMETERS</span></span>

### <span data-ttu-id="f74a2-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="f74a2-119">-BackendPool</span></span>
<span data-ttu-id="f74a2-120">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="f74a2-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="f74a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74a2-121">-DefaultProfile</span></span>
<span data-ttu-id="f74a2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f74a2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74a2-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f74a2-123">-EnabledState</span></span>
<span data-ttu-id="f74a2-124">Ön kapı yük dengeleyicinin işletim durumu.</span><span class="sxs-lookup"><span data-stu-id="f74a2-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="f74a2-125">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="f74a2-125">-FrontendEndpoint</span></span>
<span data-ttu-id="f74a2-126">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="f74a2-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="f74a2-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="f74a2-127">-HealthProbeSetting</span></span>
<span data-ttu-id="f74a2-128">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="f74a2-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f74a2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f74a2-129">-InputObject</span></span>
<span data-ttu-id="f74a2-130">Güncelleştirilecek ön kapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f74a2-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="f74a2-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="f74a2-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="f74a2-132">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="f74a2-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="f74a2-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="f74a2-133">-Name</span></span>
<span data-ttu-id="f74a2-134">Güncelleştirilecek ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="f74a2-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="f74a2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74a2-135">-ResourceGroupName</span></span>
<span data-ttu-id="f74a2-136">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f74a2-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="f74a2-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f74a2-137">-ResourceId</span></span>
<span data-ttu-id="f74a2-138">Güncelleştirilecek ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f74a2-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74a2-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f74a2-139">-RoutingRule</span></span>
<span data-ttu-id="f74a2-140">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="f74a2-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="f74a2-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f74a2-141">-Tag</span></span>
<span data-ttu-id="f74a2-142">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f74a2-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="f74a2-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="f74a2-143">-Confirm</span></span>
<span data-ttu-id="f74a2-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f74a2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74a2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74a2-145">-WhatIf</span></span>
<span data-ttu-id="f74a2-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f74a2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74a2-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f74a2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74a2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74a2-148">CommonParameters</span></span>
<span data-ttu-id="f74a2-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f74a2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74a2-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74a2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74a2-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f74a2-151">INPUTS</span></span>

### <span data-ttu-id="f74a2-152">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="f74a2-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="f74a2-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f74a2-153">System.String</span></span>

## <span data-ttu-id="f74a2-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f74a2-154">OUTPUTS</span></span>

### <span data-ttu-id="f74a2-155">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="f74a2-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="f74a2-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f74a2-156">NOTES</span></span>

## <span data-ttu-id="f74a2-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f74a2-157">RELATED LINKS</span></span>

<span data-ttu-id="f74a2-158">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Get-Azurermfrontkapısı](./Get-AzureRmFrontDoor.md) 
 [Remove-Azurermfrontkapısı](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="f74a2-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
