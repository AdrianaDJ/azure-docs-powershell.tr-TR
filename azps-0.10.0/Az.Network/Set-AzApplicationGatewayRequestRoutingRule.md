---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c2c212d3cf80044ce7c81d9d4ebd318f6a1e93ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936561"
---
# <span data-ttu-id="c937e-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c937e-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c937e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c937e-102">SYNOPSIS</span></span>
<span data-ttu-id="c937e-103">Uygulama ağ geçidi için bir istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c937e-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="c937e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c937e-104">SYNTAX</span></span>

### <span data-ttu-id="c937e-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c937e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c937e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c937e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c937e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c937e-107">DESCRIPTION</span></span>
<span data-ttu-id="c937e-108">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet 'i istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c937e-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="c937e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c937e-109">EXAMPLES</span></span>

### <span data-ttu-id="c937e-110">Örnek 1: istek yönlendirme kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c937e-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c937e-111">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c937e-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="c937e-112">İkinci komut, uygulama ağ geçidi için $Setting değişkeninde belirtilen arka uç HTTP ayarlarını, $Listener değişkeninde belirtilen bir HTTP dinleyicisini ve $Pool değişkeninde belirtilen bir arka uç adres havuzunu kullanacak şekilde istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c937e-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="c937e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c937e-113">PARAMETERS</span></span>

### <span data-ttu-id="c937e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c937e-114">-ApplicationGateway</span></span>
<span data-ttu-id="c937e-115">Bu cmdlet 'in istek yönlendirme kuralını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="c937e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c937e-116">-BackendAddressPool</span></span>
<span data-ttu-id="c937e-117">Uygulama ağ geçidi arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="c937e-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="c937e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c937e-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="c937e-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c937e-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c937e-121">Uygulama ağ geçidi arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="c937e-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c937e-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c937e-123">Uygulama ağ geçidi arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="c937e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c937e-124">-DefaultProfile</span></span>
<span data-ttu-id="c937e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c937e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c937e-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c937e-126">-HttpListener</span></span>
<span data-ttu-id="c937e-127">Uygulama ağ geçidi HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="c937e-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="c937e-128">-HttpListenerId</span></span>
<span data-ttu-id="c937e-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="c937e-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="c937e-130">-Name</span></span>
<span data-ttu-id="c937e-131">Bu cmdlet 'in değiştirdiği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c937e-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c937e-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c937e-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="c937e-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c937e-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="c937e-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c937e-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c937e-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c937e-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c937e-136">-RuleType</span></span>
<span data-ttu-id="c937e-137">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c937e-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="c937e-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c937e-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="c937e-139">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="c937e-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="c937e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c937e-140">CommonParameters</span></span>
<span data-ttu-id="c937e-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c937e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c937e-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c937e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c937e-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c937e-143">INPUTS</span></span>

### <span data-ttu-id="c937e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c937e-144">System.String</span></span>

## <span data-ttu-id="c937e-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c937e-145">OUTPUTS</span></span>

### <span data-ttu-id="c937e-146">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c937e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c937e-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c937e-147">NOTES</span></span>

## <span data-ttu-id="c937e-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c937e-148">RELATED LINKS</span></span>

[<span data-ttu-id="c937e-149">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c937e-149">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c937e-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c937e-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c937e-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c937e-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c937e-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c937e-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

