---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95e46bfc1f90f4e9760077b11f52d8020cb7f409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593932"
---
# <span data-ttu-id="5b6ea-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b6ea-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5b6ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6ea-103">Uygulama ağ geçidi için bir istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b6ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b6ea-104">SYNTAX</span></span>

### <span data-ttu-id="5b6ea-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5b6ea-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b6ea-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5b6ea-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b6ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b6ea-107">DESCRIPTION</span></span>
<span data-ttu-id="5b6ea-108">**Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="5b6ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b6ea-109">EXAMPLES</span></span>

### <span data-ttu-id="5b6ea-110">Örnek 1: istek yönlendirme kuralını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5b6ea-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="5b6ea-111">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5b6ea-112">İkinci komut, uygulama ağ geçidi için $Setting değişkeninde belirtilen arka uç HTTP ayarlarını, $Listener değişkeninde belirtilen bir HTTP dinleyicisini ve $Pool değişkeninde belirtilen bir arka uç adres havuzunu kullanacak şekilde istek yönlendirme kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="5b6ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b6ea-113">PARAMETERS</span></span>

### <span data-ttu-id="5b6ea-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b6ea-114">-ApplicationGateway</span></span>
<span data-ttu-id="5b6ea-115">Bu cmdlet 'in istek yönlendirme kuralını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="5b6ea-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5b6ea-116">-BackendAddressPool</span></span>
<span data-ttu-id="5b6ea-117">Uygulama ağ geçidi arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="5b6ea-118">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="5b6ea-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="5b6ea-119">Uygulama ağ geçidi arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="5b6ea-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b6ea-120">-BackendHttpSettings</span></span>
<span data-ttu-id="5b6ea-121">Uygulama ağ geçidi arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="5b6ea-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5b6ea-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="5b6ea-123">Uygulama ağ geçidi arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="5b6ea-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6ea-124">-DefaultProfile</span></span>
<span data-ttu-id="5b6ea-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b6ea-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="5b6ea-126">-HttpListener</span></span>
<span data-ttu-id="5b6ea-127">Uygulama ağ geçidi HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="5b6ea-128">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="5b6ea-128">-HttpListenerId</span></span>
<span data-ttu-id="5b6ea-129">Uygulama ağ geçidi HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="5b6ea-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b6ea-130">-Name</span></span>
<span data-ttu-id="5b6ea-131">Bu cmdlet 'in değiştirdiği istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5b6ea-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b6ea-132">-RedirectConfiguration</span></span>
<span data-ttu-id="5b6ea-133">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="5b6ea-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="5b6ea-134">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="5b6ea-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="5b6ea-135">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="5b6ea-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="5b6ea-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="5b6ea-136">-RuleType</span></span>
<span data-ttu-id="5b6ea-137">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="5b6ea-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="5b6ea-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="5b6ea-139">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="5b6ea-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="5b6ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6ea-140">CommonParameters</span></span>
<span data-ttu-id="5b6ea-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6ea-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6ea-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6ea-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b6ea-143">INPUTS</span></span>

### <span data-ttu-id="5b6ea-144">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b6ea-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5b6ea-145">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b6ea-145">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5b6ea-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b6ea-146">OUTPUTS</span></span>

### <span data-ttu-id="5b6ea-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5b6ea-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5b6ea-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b6ea-148">NOTES</span></span>

## <span data-ttu-id="5b6ea-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b6ea-149">RELATED LINKS</span></span>

[<span data-ttu-id="5b6ea-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b6ea-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b6ea-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b6ea-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b6ea-152">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b6ea-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5b6ea-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5b6ea-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


