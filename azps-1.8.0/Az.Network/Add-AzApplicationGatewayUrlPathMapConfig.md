---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 970ae86a9664dad32e7c91c35abb17cd086a0130
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760725"
---
# <span data-ttu-id="4e643-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e643-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4e643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e643-102">SYNOPSIS</span></span>
<span data-ttu-id="4e643-103">Arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="4e643-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4e643-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e643-104">SYNTAX</span></span>

### <span data-ttu-id="4e643-105">BackendSetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4e643-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e643-106">Backendsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4e643-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e643-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="4e643-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e643-108">Redirectsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4e643-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e643-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e643-109">DESCRIPTION</span></span>
<span data-ttu-id="4e643-110">**Add-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="4e643-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="4e643-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e643-111">EXAMPLES</span></span>

### <span data-ttu-id="4e643-112">Örnek 1: uygulama ağ geçidine URL yolu eşlemesi ekleme.</span><span class="sxs-lookup"><span data-stu-id="4e643-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4e643-113">İlk komut appGwName adlı bir uygulama ağ geçidini alır ve bunu $appgw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4e643-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="4e643-114">İkinci komut arka uç adres havuzunu alır ve $pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4e643-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="4e643-115">Üçüncü komut, arka uç http ayarlarını alır ve $poolSettings değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4e643-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="4e643-116">Dördüncü komut rule01 adlı yeni yol kuralı yapılandırması oluşturur ve $pathRule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4e643-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="4e643-117">Beşinci komut url01 adlı URL yol eşleştirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="4e643-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="4e643-118">Altıncı komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4e643-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="4e643-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e643-119">PARAMETERS</span></span>

### <span data-ttu-id="4e643-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e643-120">-ApplicationGateway</span></span>
<span data-ttu-id="4e643-121">Bu cmdlet 'in URL yol haritası yapılandırmasını eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e643-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4e643-123">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-124">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="4e643-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4e643-125">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e643-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4e643-127">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4e643-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4e643-129">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e643-130">-DefaultProfile</span></span>
<span data-ttu-id="4e643-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e643-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e643-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e643-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4e643-133">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="4e643-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-134">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="4e643-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4e643-135">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="4e643-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e643-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="4e643-137">Uygulama ağ geçidi varsayılan yeniden yazma kuralı kümesi</span><span class="sxs-lookup"><span data-stu-id="4e643-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="4e643-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="4e643-139">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="4e643-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e643-140">-Name</span></span>
<span data-ttu-id="4e643-141">Bu cmdlet 'in arka uç sunucu havuzuna eklediği URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="4e643-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4e643-142">-PathRules</span></span>
<span data-ttu-id="4e643-143">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e643-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="4e643-144">Yol kuralları sıralı duyarlı, belirtildikleri sırayla uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4e643-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e643-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e643-145">CommonParameters</span></span>
<span data-ttu-id="4e643-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e643-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e643-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e643-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e643-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e643-148">INPUTS</span></span>

### <span data-ttu-id="4e643-149">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e643-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e643-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e643-150">OUTPUTS</span></span>

### <span data-ttu-id="4e643-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e643-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e643-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e643-152">NOTES</span></span>

## <span data-ttu-id="4e643-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e643-153">RELATED LINKS</span></span>

[<span data-ttu-id="4e643-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e643-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e643-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e643-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e643-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e643-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e643-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e643-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

