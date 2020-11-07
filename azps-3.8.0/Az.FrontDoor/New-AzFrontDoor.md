---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937484"
---
# <span data-ttu-id="5008e-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="5008e-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="5008e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5008e-102">SYNOPSIS</span></span>
<span data-ttu-id="5008e-103">Yeni bir Azure ön kapı yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="5008e-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="5008e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5008e-104">SYNTAX</span></span>

### <span data-ttu-id="5008e-105">Byalanlarıbackendpoolssettingparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5008e-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5008e-106">Byalanalan</span><span class="sxs-lookup"><span data-stu-id="5008e-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5008e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5008e-107">DESCRIPTION</span></span>
<span data-ttu-id="5008e-108">**New-Azfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki belirtilen kaynak grubunda yeni bir Azure ön kapı yük dengeleyicisi oluşturur</span><span class="sxs-lookup"><span data-stu-id="5008e-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="5008e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5008e-109">EXAMPLES</span></span>

### <span data-ttu-id="5008e-110">Örnek 1: verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5008e-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="5008e-111">Verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5008e-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="5008e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5008e-112">PARAMETERS</span></span>

### <span data-ttu-id="5008e-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="5008e-113">-BackendPool</span></span>
<span data-ttu-id="5008e-114">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="5008e-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="5008e-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="5008e-116">Tüm backendPools için ayarlar</span><span class="sxs-lookup"><span data-stu-id="5008e-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5008e-117">-DefaultProfile</span></span>
<span data-ttu-id="5008e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5008e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5008e-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="5008e-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="5008e-120">HTTPS isteklerinin tüm arka uç havuzlarına yönelik sertifika adı denetimini devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="5008e-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="5008e-121">HTTPS olmayan isteklerde hiçbir etkiye gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="5008e-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5008e-122">-EnabledState</span></span>
<span data-ttu-id="5008e-123">Ön kapı yük dengeleyicinin EnabledState.</span><span class="sxs-lookup"><span data-stu-id="5008e-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="5008e-124">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="5008e-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="5008e-125">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="5008e-125">-FrontendEndpoint</span></span>
<span data-ttu-id="5008e-126">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="5008e-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="5008e-127">-HealthProbeSetting</span></span>
<span data-ttu-id="5008e-128">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="5008e-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="5008e-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="5008e-130">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="5008e-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="5008e-131">-Name</span></span>
<span data-ttu-id="5008e-132">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="5008e-132">Front Door name.</span></span>

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

### <span data-ttu-id="5008e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5008e-133">-ResourceGroupName</span></span>
<span data-ttu-id="5008e-134">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5008e-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="5008e-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="5008e-135">-RoutingRule</span></span>
<span data-ttu-id="5008e-136">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="5008e-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5008e-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5008e-137">-Tag</span></span>
<span data-ttu-id="5008e-138">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="5008e-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="5008e-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="5008e-139">-Confirm</span></span>
<span data-ttu-id="5008e-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5008e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5008e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5008e-141">-WhatIf</span></span>
<span data-ttu-id="5008e-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5008e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5008e-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5008e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5008e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5008e-144">CommonParameters</span></span>
<span data-ttu-id="5008e-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5008e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5008e-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5008e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5008e-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5008e-147">INPUTS</span></span>

### <span data-ttu-id="5008e-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5008e-148">None</span></span>
## <span data-ttu-id="5008e-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5008e-149">OUTPUTS</span></span>

### <span data-ttu-id="5008e-150">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="5008e-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="5008e-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5008e-151">NOTES</span></span>

## <span data-ttu-id="5008e-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5008e-152">RELATED LINKS</span></span>

<span data-ttu-id="5008e-153">[Get-Azfrontkapısı](./Get-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md) 
 [Remove-Azfrontkapısı](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="5008e-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>