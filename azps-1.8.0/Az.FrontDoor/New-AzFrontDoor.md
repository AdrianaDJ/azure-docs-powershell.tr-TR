---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916759"
---
# <span data-ttu-id="eba96-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="eba96-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="eba96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eba96-102">SYNOPSIS</span></span>
<span data-ttu-id="eba96-103">Yeni bir Azure ön kapı yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="eba96-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="eba96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eba96-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eba96-105">DESCRIPTION</span></span>
<span data-ttu-id="eba96-106">**New-Azfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki belirtilen kaynak grubunda yeni bir Azure ön kapı yük dengeleyicisi oluşturur</span><span class="sxs-lookup"><span data-stu-id="eba96-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="eba96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eba96-107">EXAMPLES</span></span>

### <span data-ttu-id="eba96-108">Örnek 1: verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eba96-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="eba96-109">Verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eba96-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="eba96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eba96-110">PARAMETERS</span></span>

### <span data-ttu-id="eba96-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="eba96-111">-BackendPool</span></span>
<span data-ttu-id="eba96-112">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="eba96-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="eba96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba96-113">-DefaultProfile</span></span>
<span data-ttu-id="eba96-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eba96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba96-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="eba96-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="eba96-116">HTTPS isteklerinin tüm arka uç havuzlarına yönelik sertifika adı denetimini devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="eba96-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="eba96-117">HTTPS olmayan isteklerde hiçbir etkiye gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="eba96-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="eba96-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="eba96-118">-EnabledState</span></span>
<span data-ttu-id="eba96-119">Ön kapı yük dengeleyicinin EnabledState.</span><span class="sxs-lookup"><span data-stu-id="eba96-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="eba96-120">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="eba96-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="eba96-121">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="eba96-121">-FrontendEndpoint</span></span>
<span data-ttu-id="eba96-122">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="eba96-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="eba96-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="eba96-123">-HealthProbeSetting</span></span>
<span data-ttu-id="eba96-124">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="eba96-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="eba96-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="eba96-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="eba96-126">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="eba96-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="eba96-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="eba96-127">-Name</span></span>
<span data-ttu-id="eba96-128">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="eba96-128">Front Door name.</span></span>

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

### <span data-ttu-id="eba96-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba96-129">-ResourceGroupName</span></span>
<span data-ttu-id="eba96-130">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="eba96-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="eba96-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="eba96-131">-RoutingRule</span></span>
<span data-ttu-id="eba96-132">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="eba96-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="eba96-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="eba96-133">-Tag</span></span>
<span data-ttu-id="eba96-134">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="eba96-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="eba96-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="eba96-135">-Confirm</span></span>
<span data-ttu-id="eba96-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eba96-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba96-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba96-137">-WhatIf</span></span>
<span data-ttu-id="eba96-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eba96-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba96-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eba96-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba96-140">CommonParameters</span></span>
<span data-ttu-id="eba96-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eba96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba96-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eba96-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba96-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eba96-143">INPUTS</span></span>

### <span data-ttu-id="eba96-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eba96-144">None</span></span>

## <span data-ttu-id="eba96-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eba96-145">OUTPUTS</span></span>

### <span data-ttu-id="eba96-146">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="eba96-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="eba96-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eba96-147">NOTES</span></span>

## <span data-ttu-id="eba96-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eba96-148">RELATED LINKS</span></span>

<span data-ttu-id="eba96-149">[Get-Azfrontkapısı](./Get-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md) 
 [Remove-Azfrontkapısı](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="eba96-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>