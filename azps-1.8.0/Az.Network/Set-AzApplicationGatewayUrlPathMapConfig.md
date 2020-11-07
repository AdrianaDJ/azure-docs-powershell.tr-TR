---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d384d1b0db463253052ab7efa53233bdd302f496
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760031"
---
# <span data-ttu-id="2847f-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2847f-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2847f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2847f-102">SYNOPSIS</span></span>
<span data-ttu-id="2847f-103">Arka uç sunucu havuzuna ait bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2847f-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2847f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2847f-104">SYNTAX</span></span>

### <span data-ttu-id="2847f-105">BackendSetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2847f-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2847f-106">Backendsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2847f-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2847f-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="2847f-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2847f-108">Redirectsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2847f-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2847f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2847f-109">DESCRIPTION</span></span>
<span data-ttu-id="2847f-110">**Set-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna AIT bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2847f-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2847f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2847f-111">EXAMPLES</span></span>

### <span data-ttu-id="2847f-112">Örnek 1: URL yol eşlemesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2847f-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2847f-113">İlk komut appGwName adlı uygulama ağ geçidini alır ve sonucu $appgw değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="2847f-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="2847f-114">İkinci komut, uygulama ağ geçidinde map01 adındaki URL yol eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2847f-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="2847f-115">Üçüncü komut, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2847f-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="2847f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2847f-116">PARAMETERS</span></span>

### <span data-ttu-id="2847f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2847f-117">-ApplicationGateway</span></span>
<span data-ttu-id="2847f-118">Bu cmdlet 'in URL yol haritası yapılandırmasını ayarladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="2847f-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2847f-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="2847f-120">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-121">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2847f-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="2847f-122">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-122">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2847f-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="2847f-124">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2847f-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="2847f-126">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-126">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2847f-127">-DefaultProfile</span></span>
<span data-ttu-id="2847f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2847f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2847f-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2847f-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="2847f-130">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="2847f-130">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-131">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="2847f-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="2847f-132">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2847f-132">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2847f-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="2847f-134">Uygulama ağ geçidi varsayılan yeniden yazma kuralı kümesi</span><span class="sxs-lookup"><span data-stu-id="2847f-134">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2847f-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="2847f-136">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="2847f-136">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="2847f-137">-Name</span></span>
<span data-ttu-id="2847f-138">Bu cmdlet 'in yapılandırmasını ayarladığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="2847f-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="2847f-139">-PathRules</span></span>
<span data-ttu-id="2847f-140">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2847f-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="2847f-141">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2847f-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2847f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2847f-142">CommonParameters</span></span>
<span data-ttu-id="2847f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2847f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2847f-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2847f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2847f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2847f-145">INPUTS</span></span>

### <span data-ttu-id="2847f-146">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2847f-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2847f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2847f-147">OUTPUTS</span></span>

### <span data-ttu-id="2847f-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2847f-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2847f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2847f-149">NOTES</span></span>

## <span data-ttu-id="2847f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2847f-150">RELATED LINKS</span></span>

[<span data-ttu-id="2847f-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2847f-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2847f-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2847f-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2847f-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2847f-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2847f-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2847f-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


