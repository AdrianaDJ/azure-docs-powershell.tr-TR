---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935409"
---
# <span data-ttu-id="3c4bf-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c4bf-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="3c4bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4bf-103">Arka uç sunucu havuzuna yönelik bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3c4bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c4bf-104">SYNTAX</span></span>

### <span data-ttu-id="3c4bf-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3c4bf-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c4bf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3c4bf-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c4bf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c4bf-107">DESCRIPTION</span></span>
<span data-ttu-id="3c4bf-108">**Yeni-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3c4bf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c4bf-109">EXAMPLES</span></span>

### <span data-ttu-id="3c4bf-110">Örnek 1: arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="3c4bf-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="3c4bf-111">Bu komut, arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3c4bf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c4bf-112">PARAMETERS</span></span>

### <span data-ttu-id="3c4bf-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3c4bf-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="3c4bf-114">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="3c4bf-115">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="3c4bf-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="3c4bf-116">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="3c4bf-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3c4bf-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="3c4bf-118">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="3c4bf-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="3c4bf-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="3c4bf-120">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="3c4bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4bf-121">-DefaultProfile</span></span>
<span data-ttu-id="3c4bf-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c4bf-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c4bf-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="3c4bf-124">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="3c4bf-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="3c4bf-125">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="3c4bf-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="3c4bf-126">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3c4bf-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="3c4bf-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c4bf-127">-Name</span></span>
<span data-ttu-id="3c4bf-128">Bu cmdlet 'in oluşturduğu URL yol eşleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3c4bf-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="3c4bf-129">-PathRules</span></span>
<span data-ttu-id="3c4bf-130">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="3c4bf-131">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="3c4bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4bf-132">CommonParameters</span></span>
<span data-ttu-id="3c4bf-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c4bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4bf-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4bf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4bf-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c4bf-135">INPUTS</span></span>

## <span data-ttu-id="3c4bf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c4bf-136">OUTPUTS</span></span>

### <span data-ttu-id="3c4bf-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3c4bf-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="3c4bf-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c4bf-138">NOTES</span></span>

## <span data-ttu-id="3c4bf-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c4bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="3c4bf-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c4bf-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3c4bf-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c4bf-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3c4bf-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c4bf-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3c4bf-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c4bf-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


