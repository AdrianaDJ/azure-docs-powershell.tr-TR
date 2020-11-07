---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1e9a97d01fd42bae636d93311b41bc6150394d9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760372"
---
# <span data-ttu-id="874c9-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="874c9-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="874c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="874c9-102">SYNOPSIS</span></span>
<span data-ttu-id="874c9-103">Arka uç sunucu havuzuna yönelik bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="874c9-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="874c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="874c9-104">SYNTAX</span></span>

### <span data-ttu-id="874c9-105">BackendSetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="874c9-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="874c9-106">Backendsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="874c9-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="874c9-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="874c9-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="874c9-108">Redirectsetbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="874c9-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="874c9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="874c9-109">DESCRIPTION</span></span>
<span data-ttu-id="874c9-110">**Yeni-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="874c9-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="874c9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="874c9-111">EXAMPLES</span></span>

### <span data-ttu-id="874c9-112">Örnek 1: arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="874c9-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="874c9-113">Bu komut, arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="874c9-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="874c9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="874c9-114">PARAMETERS</span></span>

### <span data-ttu-id="874c9-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="874c9-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="874c9-116">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="874c9-117">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="874c9-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="874c9-118">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="874c9-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="874c9-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="874c9-120">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="874c9-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="874c9-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="874c9-122">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="874c9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874c9-123">-DefaultProfile</span></span>
<span data-ttu-id="874c9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="874c9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="874c9-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="874c9-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="874c9-126">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="874c9-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="874c9-127">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="874c9-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="874c9-128">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="874c9-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="874c9-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="874c9-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="874c9-130">Uygulama ağ geçidi varsayılan yeniden yazma kuralı kümesi</span><span class="sxs-lookup"><span data-stu-id="874c9-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="874c9-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="874c9-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="874c9-132">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="874c9-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="874c9-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="874c9-133">-Name</span></span>
<span data-ttu-id="874c9-134">Bu cmdlet 'in oluşturduğu URL yol eşleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="874c9-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="874c9-135">-PathRules</span></span>
<span data-ttu-id="874c9-136">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="874c9-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="874c9-137">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="874c9-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="874c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874c9-138">CommonParameters</span></span>
<span data-ttu-id="874c9-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="874c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874c9-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874c9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874c9-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="874c9-141">INPUTS</span></span>

### <span data-ttu-id="874c9-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="874c9-142">None</span></span>

## <span data-ttu-id="874c9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="874c9-143">OUTPUTS</span></span>

### <span data-ttu-id="874c9-144">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="874c9-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="874c9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="874c9-145">NOTES</span></span>

## <span data-ttu-id="874c9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="874c9-146">RELATED LINKS</span></span>

[<span data-ttu-id="874c9-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="874c9-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="874c9-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="874c9-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="874c9-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="874c9-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="874c9-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="874c9-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


