---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 46a6a9663e7e22fd1182656bab9cab8a263f6c44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763036"
---
# <span data-ttu-id="704b5-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="704b5-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="704b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="704b5-102">SYNOPSIS</span></span>
<span data-ttu-id="704b5-103">Uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="704b5-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="704b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="704b5-104">SYNTAX</span></span>

### <span data-ttu-id="704b5-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="704b5-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="704b5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="704b5-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="704b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="704b5-107">DESCRIPTION</span></span>
<span data-ttu-id="704b5-108">**Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i bir uygulama ağ geçidine istek yönlendirme kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="704b5-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="704b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="704b5-109">EXAMPLES</span></span>

### <span data-ttu-id="704b5-110">Örnek 1: uygulama ağ geçidine istek yönlendirme kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="704b5-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="704b5-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="704b5-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="704b5-112">İkinci komut, uygulama ağ geçidine istek yönlendirme kuralını ekler.</span><span class="sxs-lookup"><span data-stu-id="704b5-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="704b5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="704b5-113">PARAMETERS</span></span>

### <span data-ttu-id="704b5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="704b5-114">-ApplicationGateway</span></span>
<span data-ttu-id="704b5-115">Bu cmdlet 'in istek yönlendirme kuralı eklediği bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="704b5-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="704b5-116">-BackendAddressPool</span></span>
<span data-ttu-id="704b5-117">Uygulama ağ geçidi arka uç adres havuzu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="704b5-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="704b5-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="704b5-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="704b5-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="704b5-120">-BackendHttpSettings</span></span>
<span data-ttu-id="704b5-121">Uygulama ağ geçidi için bir arka uç HTTP Ayarları nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="704b5-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="704b5-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="704b5-123">Uygulama ağ geçidi için arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="704b5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704b5-124">-DefaultProfile</span></span>
<span data-ttu-id="704b5-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="704b5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="704b5-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="704b5-126">-HttpListener</span></span>
<span data-ttu-id="704b5-127">Uygulama ağ geçidi HTTP dinleyicisi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="704b5-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="704b5-128">-HttpListenerId</span></span>
<span data-ttu-id="704b5-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="704b5-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="704b5-130">-Name</span></span>
<span data-ttu-id="704b5-131">Bu cmdlet 'in eklediği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="704b5-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="704b5-132">-RedirectConfiguration</span></span>
<span data-ttu-id="704b5-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="704b5-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="704b5-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="704b5-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="704b5-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="704b5-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="704b5-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="704b5-136">-RuleType</span></span>
<span data-ttu-id="704b5-137">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="704b5-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="704b5-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="704b5-139">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="704b5-139">-UrlPathMapId</span></span>
<span data-ttu-id="704b5-140">Yönlendirme kuralı için URL yolu harita KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="704b5-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="704b5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704b5-141">CommonParameters</span></span>
<span data-ttu-id="704b5-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="704b5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704b5-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704b5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704b5-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="704b5-144">INPUTS</span></span>

### <span data-ttu-id="704b5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="704b5-145">System.String</span></span>

## <span data-ttu-id="704b5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="704b5-146">OUTPUTS</span></span>

### <span data-ttu-id="704b5-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="704b5-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="704b5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="704b5-148">NOTES</span></span>

## <span data-ttu-id="704b5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="704b5-149">RELATED LINKS</span></span>

[<span data-ttu-id="704b5-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="704b5-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="704b5-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="704b5-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="704b5-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="704b5-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="704b5-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="704b5-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


