---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ec85b643294f65aceefae2d4a52e9a5d48f15191
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935424"
---
# <span data-ttu-id="c24fb-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c24fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c24fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c24fb-103">Uygulama ağ geçidi için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c24fb-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="c24fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c24fb-104">SYNTAX</span></span>

### <span data-ttu-id="c24fb-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c24fb-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c24fb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c24fb-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c24fb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c24fb-107">DESCRIPTION</span></span>
<span data-ttu-id="c24fb-108">**Add-AzApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure Application Gateway için bir istek yönlendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c24fb-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="c24fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c24fb-109">EXAMPLES</span></span>

### <span data-ttu-id="c24fb-110">Örnek 1: uygulama ağ geçidi için istek yönlendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c24fb-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c24fb-111">Bu komut, Rule01 adında bir temel istek yönlendirme kuralı oluşturur ve sonucu $Rule adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c24fb-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="c24fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c24fb-112">PARAMETERS</span></span>

### <span data-ttu-id="c24fb-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c24fb-113">-BackendAddressPool</span></span>
<span data-ttu-id="c24fb-114">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-115">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="c24fb-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="c24fb-116">Oluşturulacak istek yönlendirme kuralının arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c24fb-117">-BackendHttpSettings</span></span>
<span data-ttu-id="c24fb-118">Oluşturulacak istek yönlendirme kuralı için bir nesne olarak arka uç HTTP ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c24fb-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c24fb-120">Oluşturulacak istek yönlendirme kuralının arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24fb-121">-DefaultProfile</span></span>
<span data-ttu-id="c24fb-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c24fb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24fb-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c24fb-123">-HttpListener</span></span>
<span data-ttu-id="c24fb-124">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-125">-Httplistenerıd</span><span class="sxs-lookup"><span data-stu-id="c24fb-125">-HttpListenerId</span></span>
<span data-ttu-id="c24fb-126">Oluşturulacak istek yönlendirme kuralı için arka uç HTTP dinleyicisi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="c24fb-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c24fb-127">-Name</span></span>
<span data-ttu-id="c24fb-128">Bu cmdlet 'in oluşturduğu istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c24fb-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24fb-129">-RedirectConfiguration</span></span>
<span data-ttu-id="c24fb-130">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="c24fb-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c24fb-131">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="c24fb-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="c24fb-132">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c24fb-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c24fb-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c24fb-133">-RuleType</span></span>
<span data-ttu-id="c24fb-134">İstek yönlendirme kuralının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c24fb-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="c24fb-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c24fb-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="c24fb-136">-Urlyolmapıd</span><span class="sxs-lookup"><span data-stu-id="c24fb-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="c24fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24fb-137">CommonParameters</span></span>
<span data-ttu-id="c24fb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c24fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24fb-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24fb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24fb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c24fb-140">INPUTS</span></span>

### <span data-ttu-id="c24fb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c24fb-141">System.String</span></span>

## <span data-ttu-id="c24fb-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c24fb-142">OUTPUTS</span></span>

### <span data-ttu-id="c24fb-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c24fb-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c24fb-144">NOTES</span></span>

## <span data-ttu-id="c24fb-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c24fb-145">RELATED LINKS</span></span>

[<span data-ttu-id="c24fb-146">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-146">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c24fb-147">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-147">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c24fb-148">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-148">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c24fb-149">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c24fb-149">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

