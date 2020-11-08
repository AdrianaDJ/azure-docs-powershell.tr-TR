---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 2e323170bac22950b9a6ca479e8470630741c2bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104825"
---
# <span data-ttu-id="57931-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57931-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="57931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57931-102">SYNOPSIS</span></span>
<span data-ttu-id="57931-103">Uygulama ağ geçidi için bir istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="57931-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="57931-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57931-104">SYNTAX</span></span>

### <span data-ttu-id="57931-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="57931-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57931-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="57931-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57931-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57931-107">DESCRIPTION</span></span>
<span data-ttu-id="57931-108">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet 'i istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="57931-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="57931-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57931-109">EXAMPLES</span></span>

### <span data-ttu-id="57931-110">Örnek 1: istek yönlendirme kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="57931-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="57931-111">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="57931-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="57931-112">İkinci komut, uygulama ağ geçidi için $Setting değişkeninde belirtilen arka uç HTTP ayarlarını, $Listener değişkeninde belirtilen bir HTTP dinleyicisini ve $Pool değişkeninde belirtilen bir arka uç adres havuzunu kullanacak şekilde istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="57931-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="57931-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57931-113">PARAMETERS</span></span>

### <span data-ttu-id="57931-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57931-114">-ApplicationGateway</span></span>
<span data-ttu-id="57931-115">Bu cmdlet 'in istek yönlendirme kuralını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="57931-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="57931-116">-BackendAddressPool</span></span>
<span data-ttu-id="57931-117">Uygulama ağ geçidi arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="57931-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="57931-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="57931-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="57931-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="57931-120">-BackendHttpSettings</span></span>
<span data-ttu-id="57931-121">Uygulama ağ geçidi arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="57931-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="57931-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="57931-123">Uygulama ağ geçidi arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="57931-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57931-124">-DefaultProfile</span></span>
<span data-ttu-id="57931-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57931-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57931-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="57931-126">-HttpListener</span></span>
<span data-ttu-id="57931-127">Uygulama ağ geçidi HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="57931-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="57931-128">-HttpListenerId</span></span>
<span data-ttu-id="57931-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="57931-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="57931-130">-Name</span></span>
<span data-ttu-id="57931-131">Bu cmdlet 'in değiştirdiği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="57931-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="57931-132">-RedirectConfiguration</span></span>
<span data-ttu-id="57931-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="57931-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="57931-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="57931-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="57931-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="57931-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="57931-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57931-136">-RewriteRuleSet</span></span>
<span data-ttu-id="57931-137">Uygulama ağ geçidi Rewriterset</span><span class="sxs-lookup"><span data-stu-id="57931-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="57931-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="57931-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="57931-139">Uygulama ağ geçidi Rewriterset 'in KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="57931-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="57931-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="57931-140">-RuleType</span></span>
<span data-ttu-id="57931-141">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="57931-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="57931-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="57931-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="57931-143">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="57931-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="57931-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57931-144">CommonParameters</span></span>
<span data-ttu-id="57931-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57931-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57931-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57931-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57931-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57931-147">INPUTS</span></span>

### <span data-ttu-id="57931-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57931-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57931-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57931-149">OUTPUTS</span></span>

### <span data-ttu-id="57931-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57931-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57931-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57931-151">NOTES</span></span>

## <span data-ttu-id="57931-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57931-152">RELATED LINKS</span></span>

[<span data-ttu-id="57931-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57931-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="57931-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57931-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="57931-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57931-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="57931-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="57931-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


