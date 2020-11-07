---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 82f14ce9418566793572e2b5722d09460ab1e827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931925"
---
# <span data-ttu-id="c1f29-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c1f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f29-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f29-103">Uygulama ağ geçidi için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1f29-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="c1f29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1f29-104">SYNTAX</span></span>

### <span data-ttu-id="c1f29-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c1f29-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1f29-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1f29-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1f29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1f29-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f29-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure Application Gateway için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c1f29-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="c1f29-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1f29-109">EXAMPLES</span></span>

### <span data-ttu-id="c1f29-110">Örnek 1: uygulama ağ geçidi için istek yönlendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1f29-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c1f29-111">Bu komut, Rule01 adında bir temel istek yönlendirme kuralı oluşturur ve sonucu $Rule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c1f29-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="c1f29-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1f29-112">PARAMETERS</span></span>

### <span data-ttu-id="c1f29-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1f29-113">-BackendAddressPool</span></span>
<span data-ttu-id="c1f29-114">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-115">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="c1f29-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="c1f29-116">Oluşturulacak istek yönlendirme kuralının arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1f29-117">-BackendHttpSettings</span></span>
<span data-ttu-id="c1f29-118">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c1f29-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c1f29-120">Oluşturulacak istek yönlendirme kuralının arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f29-121">-DefaultProfile</span></span>
<span data-ttu-id="c1f29-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1f29-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1f29-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c1f29-123">-HttpListener</span></span>
<span data-ttu-id="c1f29-124">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-125">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="c1f29-125">-HttpListenerId</span></span>
<span data-ttu-id="c1f29-126">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c1f29-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1f29-127">-Name</span></span>
<span data-ttu-id="c1f29-128">Bu cmdlet 'in oluşturduğu istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c1f29-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1f29-129">-RedirectConfiguration</span></span>
<span data-ttu-id="c1f29-130">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="c1f29-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1f29-131">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="c1f29-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="c1f29-132">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c1f29-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1f29-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1f29-133">-RewriteRuleSet</span></span>
<span data-ttu-id="c1f29-134">Uygulama ağ geçidi Rewriterset</span><span class="sxs-lookup"><span data-stu-id="c1f29-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1f29-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c1f29-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="c1f29-136">Uygulama ağ geçidi Rewriterset 'in KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c1f29-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1f29-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c1f29-137">-RuleType</span></span>
<span data-ttu-id="c1f29-138">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f29-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="c1f29-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c1f29-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="c1f29-140">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="c1f29-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="c1f29-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f29-141">CommonParameters</span></span>
<span data-ttu-id="c1f29-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1f29-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f29-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f29-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f29-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1f29-144">INPUTS</span></span>

### <span data-ttu-id="c1f29-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1f29-145">None</span></span>

## <span data-ttu-id="c1f29-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1f29-146">OUTPUTS</span></span>

### <span data-ttu-id="c1f29-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c1f29-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1f29-148">NOTES</span></span>

## <span data-ttu-id="c1f29-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1f29-149">RELATED LINKS</span></span>

[<span data-ttu-id="c1f29-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1f29-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1f29-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c1f29-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c1f29-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

