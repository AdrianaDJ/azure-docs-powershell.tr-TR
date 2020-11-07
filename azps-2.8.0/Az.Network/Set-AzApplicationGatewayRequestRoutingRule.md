---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd6888402a2e3a88b9d3d19da752b0ac18d20f32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932217"
---
# <span data-ttu-id="d9a1d-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d9a1d-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d9a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a1d-103">Uygulama ağ geçidi için bir istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="d9a1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9a1d-104">SYNTAX</span></span>

### <span data-ttu-id="d9a1d-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d9a1d-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9a1d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9a1d-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9a1d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9a1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d9a1d-108">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet 'i istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="d9a1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9a1d-109">EXAMPLES</span></span>

### <span data-ttu-id="d9a1d-110">Örnek 1: istek yönlendirme kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d9a1d-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="d9a1d-111">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d9a1d-112">İkinci komut, uygulama ağ geçidi için $Setting değişkeninde belirtilen arka uç HTTP ayarlarını, $Listener değişkeninde belirtilen bir HTTP dinleyicisini ve $Pool değişkeninde belirtilen bir arka uç adres havuzunu kullanacak şekilde istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="d9a1d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9a1d-113">PARAMETERS</span></span>

### <span data-ttu-id="d9a1d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9a1d-114">-ApplicationGateway</span></span>
<span data-ttu-id="d9a1d-115">Bu cmdlet 'in istek yönlendirme kuralını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="d9a1d-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d9a1d-116">-BackendAddressPool</span></span>
<span data-ttu-id="d9a1d-117">Uygulama ağ geçidi arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="d9a1d-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="d9a1d-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d9a1d-120">-BackendHttpSettings</span></span>
<span data-ttu-id="d9a1d-121">Uygulama ağ geçidi arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d9a1d-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d9a1d-123">Uygulama ağ geçidi arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a1d-124">-DefaultProfile</span></span>
<span data-ttu-id="d9a1d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9a1d-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d9a1d-126">-HttpListener</span></span>
<span data-ttu-id="d9a1d-127">Uygulama ağ geçidi HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="d9a1d-128">-HttpListenerId</span></span>
<span data-ttu-id="d9a1d-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9a1d-130">-Name</span></span>
<span data-ttu-id="d9a1d-131">Bu cmdlet 'in değiştirdiği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d9a1d-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9a1d-132">-RedirectConfiguration</span></span>
<span data-ttu-id="d9a1d-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="d9a1d-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="d9a1d-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="d9a1d-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="d9a1d-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d9a1d-136">-RewriteRuleSet</span></span>
<span data-ttu-id="d9a1d-137">Uygulama ağ geçidi Rewriterset</span><span class="sxs-lookup"><span data-stu-id="d9a1d-137">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d9a1d-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="d9a1d-139">Uygulama ağ geçidi Rewriterset 'in KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="d9a1d-139">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d9a1d-140">-RuleType</span></span>
<span data-ttu-id="d9a1d-141">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-141">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d9a1d-142">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-143">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="d9a1d-143">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a1d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a1d-144">CommonParameters</span></span>
<span data-ttu-id="d9a1d-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9a1d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a1d-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a1d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a1d-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9a1d-147">INPUTS</span></span>

### <span data-ttu-id="d9a1d-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9a1d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9a1d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9a1d-149">OUTPUTS</span></span>

### <span data-ttu-id="d9a1d-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9a1d-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9a1d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9a1d-151">NOTES</span></span>

## <span data-ttu-id="d9a1d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9a1d-152">RELATED LINKS</span></span>

[<span data-ttu-id="d9a1d-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d9a1d-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d9a1d-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d9a1d-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d9a1d-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d9a1d-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d9a1d-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d9a1d-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


