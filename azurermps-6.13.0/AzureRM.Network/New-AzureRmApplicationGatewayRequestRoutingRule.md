---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: e812d0cbe6bd587e02a88cf59f8d8df5bccd1766
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592299"
---
# <span data-ttu-id="e7ca5-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e7ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ca5-103">Uygulama ağ geçidi için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7ca5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7ca5-104">SYNTAX</span></span>

### <span data-ttu-id="e7ca5-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ca5-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ca5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e7ca5-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7ca5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="e7ca5-108">**Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure Application Gateway için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e7ca5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="e7ca5-110">Örnek 1: uygulama ağ geçidi için istek yönlendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e7ca5-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e7ca5-111">Bu komut, Rule01 adında bir temel istek yönlendirme kuralı oluşturur ve sonucu $Rule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="e7ca5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7ca5-112">PARAMETERS</span></span>

### <span data-ttu-id="e7ca5-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e7ca5-113">-BackendAddressPool</span></span>
<span data-ttu-id="e7ca5-114">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-115">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="e7ca5-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="e7ca5-116">Oluşturulacak istek yönlendirme kuralının arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e7ca5-117">-BackendHttpSettings</span></span>
<span data-ttu-id="e7ca5-118">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e7ca5-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e7ca5-120">Oluşturulacak istek yönlendirme kuralının arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ca5-121">-DefaultProfile</span></span>
<span data-ttu-id="e7ca5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7ca5-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e7ca5-123">-HttpListener</span></span>
<span data-ttu-id="e7ca5-124">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-125">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="e7ca5-125">-HttpListenerId</span></span>
<span data-ttu-id="e7ca5-126">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="e7ca5-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7ca5-127">-Name</span></span>
<span data-ttu-id="e7ca5-128">Bu cmdlet 'in oluşturduğu istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7ca5-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7ca5-129">-RedirectConfiguration</span></span>
<span data-ttu-id="e7ca5-130">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="e7ca5-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e7ca5-131">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="e7ca5-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="e7ca5-132">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="e7ca5-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e7ca5-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e7ca5-133">-RuleType</span></span>
<span data-ttu-id="e7ca5-134">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="e7ca5-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e7ca5-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="e7ca5-136">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="e7ca5-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e7ca5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ca5-137">CommonParameters</span></span>
<span data-ttu-id="e7ca5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7ca5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ca5-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ca5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ca5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7ca5-140">INPUTS</span></span>

### <span data-ttu-id="e7ca5-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e7ca5-141">None</span></span>

## <span data-ttu-id="e7ca5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7ca5-142">OUTPUTS</span></span>

### <span data-ttu-id="e7ca5-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e7ca5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7ca5-144">NOTES</span></span>

## <span data-ttu-id="e7ca5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7ca5-145">RELATED LINKS</span></span>

[<span data-ttu-id="e7ca5-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e7ca5-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e7ca5-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e7ca5-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e7ca5-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)

