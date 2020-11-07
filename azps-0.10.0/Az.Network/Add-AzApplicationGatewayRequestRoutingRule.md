---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 32695204a153d04643063f4d991b577e619edcea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935649"
---
# <span data-ttu-id="732e2-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="732e2-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="732e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="732e2-102">SYNOPSIS</span></span>
<span data-ttu-id="732e2-103">Uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="732e2-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="732e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="732e2-104">SYNTAX</span></span>

### <span data-ttu-id="732e2-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="732e2-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732e2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="732e2-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="732e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="732e2-107">DESCRIPTION</span></span>
<span data-ttu-id="732e2-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet 'i bir uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="732e2-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="732e2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="732e2-109">EXAMPLES</span></span>

### <span data-ttu-id="732e2-110">Örnek 1: uygulama ağ geçidine istek yönlendirme kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="732e2-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="732e2-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="732e2-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="732e2-112">İkinci komut, uygulama ağ geçidine istek yönlendirme kuralını ekler.</span><span class="sxs-lookup"><span data-stu-id="732e2-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="732e2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="732e2-113">PARAMETERS</span></span>

### <span data-ttu-id="732e2-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="732e2-114">-ApplicationGateway</span></span>
<span data-ttu-id="732e2-115">Bu cmdlet 'in istek yönlendirme kuralı eklediği bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="732e2-116">-BackendAddressPool</span></span>
<span data-ttu-id="732e2-117">Uygulama ağ geçidi arka uç adres havuzu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="732e2-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="732e2-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="732e2-120">-BackendHttpSettings</span></span>
<span data-ttu-id="732e2-121">Uygulama ağ geçidi için bir arka uç HTTP Ayarları nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="732e2-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="732e2-123">Uygulama ağ geçidi için arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732e2-124">-DefaultProfile</span></span>
<span data-ttu-id="732e2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="732e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="732e2-126">-HttpListener</span></span>
<span data-ttu-id="732e2-127">Uygulama ağ geçidi HTTP dinleyicisi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="732e2-128">-HttpListenerId</span></span>
<span data-ttu-id="732e2-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="732e2-130">-Name</span></span>
<span data-ttu-id="732e2-131">Bu cmdlet 'in eklediği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="732e2-132">-RedirectConfiguration</span></span>
<span data-ttu-id="732e2-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="732e2-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="732e2-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="732e2-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="732e2-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="732e2-136">-RuleType</span></span>
<span data-ttu-id="732e2-137">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="732e2-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-139">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="732e2-139">-UrlPathMapId</span></span>
<span data-ttu-id="732e2-140">Yönlendirme kuralı için URL yolu harita KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="732e2-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="732e2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732e2-141">CommonParameters</span></span>
<span data-ttu-id="732e2-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="732e2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732e2-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732e2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732e2-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="732e2-144">INPUTS</span></span>

### <span data-ttu-id="732e2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="732e2-145">System.String</span></span>

## <span data-ttu-id="732e2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="732e2-146">OUTPUTS</span></span>

### <span data-ttu-id="732e2-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="732e2-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="732e2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="732e2-148">NOTES</span></span>

## <span data-ttu-id="732e2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="732e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="732e2-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="732e2-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="732e2-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="732e2-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="732e2-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="732e2-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="732e2-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="732e2-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


