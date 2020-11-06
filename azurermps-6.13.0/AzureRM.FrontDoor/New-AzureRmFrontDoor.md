---
<span data-ttu-id="47bb5-101">Harici yardım dosyası: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml modül adı: AzureRM. Frontkapısı çevrimiçi sürüm: ilgili URL 'nin aşağıdaki olması gerekir: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor şema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="47bb5-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="47bb5-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="47bb5-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="47bb5-103">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47bb5-103">SYNOPSIS</span></span>
<span data-ttu-id="47bb5-104">Yeni bir Azure ön kapı yük dengeleyici oluşturma</span><span class="sxs-lookup"><span data-stu-id="47bb5-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="47bb5-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47bb5-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="47bb5-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="47bb5-106">DESCRIPTION</span></span>
<span data-ttu-id="47bb5-107">**Yeni-Azurermfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki belirtilen kaynak grubunda bir Azure ön kapı yük dengeleyici oluşturur</span><span class="sxs-lookup"><span data-stu-id="47bb5-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="47bb5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47bb5-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="47bb5-109">Örnek 1: verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47bb5-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="47bb5-110">Verilen parametrelere dayalı olarak ön kapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47bb5-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="47bb5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47bb5-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="47bb5-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="47bb5-112">-BackendPool</span></span>
<span data-ttu-id="47bb5-113">Yönlendirme kuralı için sağlanan backendpools.</span><span class="sxs-lookup"><span data-stu-id="47bb5-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="47bb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bb5-114">-DefaultProfile</span></span>
<span data-ttu-id="47bb5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47bb5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="47bb5-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="47bb5-116">-EnabledState</span></span>
<span data-ttu-id="47bb5-117">Ön kapı yük dengeleyicinin EnabledState.</span><span class="sxs-lookup"><span data-stu-id="47bb5-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="47bb5-118">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="47bb5-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="47bb5-119">-Frontendenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="47bb5-119">-FrontendEndpoint</span></span>
<span data-ttu-id="47bb5-120">Yönlendirme kuralı için kullanılabilir ön uç uç noktaları.</span><span class="sxs-lookup"><span data-stu-id="47bb5-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="47bb5-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="47bb5-121">-HealthProbeSetting</span></span>
<span data-ttu-id="47bb5-122">Bu ön kapı örneğiyle ilişkili sistem durumu araştırma ayarları.</span><span class="sxs-lookup"><span data-stu-id="47bb5-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="47bb5-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="47bb5-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="47bb5-124">Bu ön kapı örneğiyle ilişkili yük dengeleme ayarları.</span><span class="sxs-lookup"><span data-stu-id="47bb5-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="47bb5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="47bb5-125">-Name</span></span>
<span data-ttu-id="47bb5-126">Ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="47bb5-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="47bb5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47bb5-127">-ResourceGroupName</span></span>
<span data-ttu-id="47bb5-128">Ön kapıda oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="47bb5-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="47bb5-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="47bb5-129">-RoutingRule</span></span>
<span data-ttu-id="47bb5-130">Bu ön kapağın ilişkili olduğu yönlendirme kuralları</span><span class="sxs-lookup"><span data-stu-id="47bb5-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="47bb5-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="47bb5-131">-Tag</span></span>
<span data-ttu-id="47bb5-132">Etiketler ön kapıyı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="47bb5-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="47bb5-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="47bb5-133">-Confirm</span></span>
<span data-ttu-id="47bb5-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47bb5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="47bb5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47bb5-135">-WhatIf</span></span>
<span data-ttu-id="47bb5-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47bb5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47bb5-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47bb5-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="47bb5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bb5-138">CommonParameters</span></span>
<span data-ttu-id="47bb5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47bb5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bb5-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47bb5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="47bb5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47bb5-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="47bb5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="47bb5-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="47bb5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47bb5-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="47bb5-144">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="47bb5-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="47bb5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47bb5-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="47bb5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47bb5-146">RELATED LINKS</span></span>

<span data-ttu-id="47bb5-147">[Get-Azurermfrontkapısı](./Get-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md) 
 [Remove-Azurermfrontkapısı](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="47bb5-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
