---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591949"
---
# <span data-ttu-id="7ce60-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="7ce60-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="7ce60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce60-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce60-103">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ce60-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ce60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ce60-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ce60-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ce60-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce60-106">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ce60-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="7ce60-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ce60-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce60-108">Örnek 1: ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ce60-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="7ce60-109">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ce60-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="7ce60-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ce60-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce60-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="7ce60-111">-AcceptedProtocol</span></span>
<span data-ttu-id="7ce60-112">Bu kuralla eşleşecek iletişim kuralı düzenleri.</span><span class="sxs-lookup"><span data-stu-id="7ce60-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="7ce60-113">Varsayılan değer: {https, http}</span><span class="sxs-lookup"><span data-stu-id="7ce60-113">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="7ce60-114">-BackendPoolName</span></span>
<span data-ttu-id="7ce60-115">Bu kuralın yönlendirme yolu</span><span class="sxs-lookup"><span data-stu-id="7ce60-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="7ce60-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="7ce60-116">-CustomForwardingPath</span></span>
<span data-ttu-id="7ce60-117">Bu kuralla eşleşen kaynak yollarını yeniden yazmak için kullanılan özel yol.</span><span class="sxs-lookup"><span data-stu-id="7ce60-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="7ce60-118">Gelen yolu kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7ce60-118">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce60-119">-DefaultProfile</span></span>
<span data-ttu-id="7ce60-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ce60-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce60-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="7ce60-121">-DynamicCompression</span></span>
<span data-ttu-id="7ce60-122">Önbelleğe alma etkinleştirildiğinde önbelleğe alınan içerikte dinamik sıkıştırmanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="7ce60-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="7ce60-123">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="7ce60-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="7ce60-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="7ce60-124">-EnableCaching</span></span>
<span data-ttu-id="7ce60-125">Bu yol için önbelleğe almanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="7ce60-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="7ce60-126">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="7ce60-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7ce60-127">-EnabledState</span></span>
<span data-ttu-id="7ce60-128">Bu kuralın kullanımını etkinleştirip etkinleştirmeyeceğinizi.</span><span class="sxs-lookup"><span data-stu-id="7ce60-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="7ce60-129">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="7ce60-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="7ce60-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="7ce60-130">-ForwardingProtocol</span></span>
<span data-ttu-id="7ce60-131">Trafiği backends varsayılan değerine iletirken kullanılacak protokol</span><span class="sxs-lookup"><span data-stu-id="7ce60-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="7ce60-132">-FrontDoorName</span></span>
<span data-ttu-id="7ce60-133">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="7ce60-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="7ce60-134">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="7ce60-134">-FrontendEndpointName</span></span>
<span data-ttu-id="7ce60-135">Bu kuralla ilişkili ön uç uç noktalarının adları</span><span class="sxs-lookup"><span data-stu-id="7ce60-135">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ce60-136">-Name</span></span>
<span data-ttu-id="7ce60-137">Yönlendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="7ce60-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="7ce60-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="7ce60-138">-PatternToMatch</span></span>
<span data-ttu-id="7ce60-139">Kuralın yol desenleri, yolun son/son ucunda olanlar dışında \* içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="7ce60-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="7ce60-140">Varsayılan değer/\*</span><span class="sxs-lookup"><span data-stu-id="7ce60-140">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="7ce60-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="7ce60-142">Önbellek anahtarı oluşturulurken URL sorgu koşullarının kullanımı.</span><span class="sxs-lookup"><span data-stu-id="7ce60-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="7ce60-143">Varsayılan değer StripAll</span><span class="sxs-lookup"><span data-stu-id="7ce60-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce60-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce60-144">-ResourceGroupName</span></span>
<span data-ttu-id="7ce60-145">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7ce60-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="7ce60-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce60-146">CommonParameters</span></span>
<span data-ttu-id="7ce60-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ce60-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce60-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce60-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce60-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ce60-149">INPUTS</span></span>

### <span data-ttu-id="7ce60-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7ce60-150">None</span></span>

## <span data-ttu-id="7ce60-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ce60-151">OUTPUTS</span></span>

### <span data-ttu-id="7ce60-152">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7ce60-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="7ce60-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ce60-153">NOTES</span></span>

## <span data-ttu-id="7ce60-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ce60-154">RELATED LINKS</span></span>

<span data-ttu-id="7ce60-155">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Set-Azurermfrontkapısı](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="7ce60-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
