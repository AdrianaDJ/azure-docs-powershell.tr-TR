---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 58ea4a4dc15a74f3f3e1f7360ec2be370b440a40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763832"
---
# <span data-ttu-id="deca6-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="deca6-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="deca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deca6-102">SYNOPSIS</span></span>
<span data-ttu-id="deca6-103">Uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="deca6-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deca6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deca6-104">SYNTAX</span></span>

### <span data-ttu-id="deca6-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="deca6-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deca6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="deca6-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deca6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="deca6-107">DESCRIPTION</span></span>
<span data-ttu-id="deca6-108">**Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i bir uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="deca6-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="deca6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deca6-109">EXAMPLES</span></span>

### <span data-ttu-id="deca6-110">Örnek 1: uygulama ağ geçidine istek yönlendirme kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="deca6-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="deca6-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="deca6-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="deca6-112">İkinci komut, uygulama ağ geçidine istek yönlendirme kuralını ekler.</span><span class="sxs-lookup"><span data-stu-id="deca6-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="deca6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deca6-113">PARAMETERS</span></span>

### <span data-ttu-id="deca6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deca6-114">-ApplicationGateway</span></span>
<span data-ttu-id="deca6-115">Bu cmdlet 'in istek yönlendirme kuralı eklediği bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="deca6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="deca6-116">-BackendAddressPool</span></span>
<span data-ttu-id="deca6-117">Uygulama ağ geçidi arka uç adres havuzu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="deca6-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="deca6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="deca6-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="deca6-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="deca6-120">-BackendHttpSettings</span></span>
<span data-ttu-id="deca6-121">Uygulama ağ geçidi için bir arka uç HTTP Ayarları nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="deca6-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="deca6-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="deca6-123">Uygulama ağ geçidi için arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="deca6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deca6-124">-DefaultProfile</span></span>
<span data-ttu-id="deca6-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="deca6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deca6-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="deca6-126">-HttpListener</span></span>
<span data-ttu-id="deca6-127">Uygulama ağ geçidi HTTP dinleyicisi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="deca6-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="deca6-128">-HttpListenerId</span></span>
<span data-ttu-id="deca6-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="deca6-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="deca6-130">-Name</span></span>
<span data-ttu-id="deca6-131">Bu cmdlet 'in eklediği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="deca6-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="deca6-132">-RedirectConfiguration</span></span>
<span data-ttu-id="deca6-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="deca6-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="deca6-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="deca6-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="deca6-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="deca6-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="deca6-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="deca6-136">-RuleType</span></span>
<span data-ttu-id="deca6-137">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="deca6-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="deca6-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="deca6-139">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="deca6-139">-UrlPathMapId</span></span>
<span data-ttu-id="deca6-140">Yönlendirme kuralı için URL yolu harita KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="deca6-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="deca6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deca6-141">CommonParameters</span></span>
<span data-ttu-id="deca6-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deca6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deca6-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deca6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deca6-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deca6-144">INPUTS</span></span>

### <span data-ttu-id="deca6-145">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deca6-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="deca6-146">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="deca6-146">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="deca6-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deca6-147">OUTPUTS</span></span>

### <span data-ttu-id="deca6-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="deca6-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="deca6-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deca6-149">NOTES</span></span>

## <span data-ttu-id="deca6-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deca6-150">RELATED LINKS</span></span>

[<span data-ttu-id="deca6-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="deca6-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="deca6-152">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="deca6-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="deca6-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="deca6-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="deca6-154">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="deca6-154">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


