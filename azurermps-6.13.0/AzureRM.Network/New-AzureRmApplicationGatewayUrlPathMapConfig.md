---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 6752526e5c6f035d6446c4e6e3ed31724bdbd337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764933"
---
# <span data-ttu-id="c2267-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2267-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="c2267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2267-102">SYNOPSIS</span></span>
<span data-ttu-id="c2267-103">Arka uç sunucu havuzuna yönelik bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2267-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2267-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2267-104">SYNTAX</span></span>

### <span data-ttu-id="c2267-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2267-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2267-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2267-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2267-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2267-107">DESCRIPTION</span></span>
<span data-ttu-id="c2267-108">**New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2267-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c2267-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2267-109">EXAMPLES</span></span>

### <span data-ttu-id="c2267-110">Örnek 1: arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2267-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="c2267-111">Bu komut, arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2267-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c2267-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2267-112">PARAMETERS</span></span>

### <span data-ttu-id="c2267-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c2267-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="c2267-114">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="c2267-115">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="c2267-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="c2267-116">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="c2267-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2267-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="c2267-118">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="c2267-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c2267-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="c2267-120">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="c2267-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2267-121">-DefaultProfile</span></span>
<span data-ttu-id="c2267-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2267-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2267-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2267-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="c2267-124">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="c2267-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="c2267-125">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="c2267-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="c2267-126">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="c2267-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="c2267-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2267-127">-Name</span></span>
<span data-ttu-id="c2267-128">Bu cmdlet 'in oluşturduğu URL yol eşleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2267-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="c2267-129">-PathRules</span></span>
<span data-ttu-id="c2267-130">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2267-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="c2267-131">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c2267-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2267-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2267-132">CommonParameters</span></span>
<span data-ttu-id="c2267-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2267-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2267-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2267-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2267-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2267-135">INPUTS</span></span>

### <span data-ttu-id="c2267-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c2267-136">None</span></span>

## <span data-ttu-id="c2267-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2267-137">OUTPUTS</span></span>

### <span data-ttu-id="c2267-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c2267-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="c2267-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2267-139">NOTES</span></span>

## <span data-ttu-id="c2267-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2267-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2267-141">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2267-141">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2267-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2267-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2267-143">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2267-143">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c2267-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c2267-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


