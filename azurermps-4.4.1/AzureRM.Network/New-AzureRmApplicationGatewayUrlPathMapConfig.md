---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5c3a59b497208c761ffcf7a24bc12b5ab2c50f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589968"
---
# <span data-ttu-id="2bad6-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2bad6-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2bad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bad6-102">SYNOPSIS</span></span>
<span data-ttu-id="2bad6-103">Arka uç sunucu havuzuna yönelik bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bad6-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bad6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bad6-104">SYNTAX</span></span>

### <span data-ttu-id="2bad6-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2bad6-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bad6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2bad6-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bad6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bad6-107">DESCRIPTION</span></span>
<span data-ttu-id="2bad6-108">**New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bad6-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2bad6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bad6-109">EXAMPLES</span></span>

### <span data-ttu-id="2bad6-110">Örnek 1: arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="2bad6-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="2bad6-111">Bu komut, arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bad6-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2bad6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bad6-112">PARAMETERS</span></span>

### <span data-ttu-id="2bad6-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2bad6-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="2bad6-114">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="2bad6-115">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2bad6-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="2bad6-116">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="2bad6-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bad6-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="2bad6-118">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="2bad6-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2bad6-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="2bad6-120">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="2bad6-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bad6-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="2bad6-122">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="2bad6-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="2bad6-123">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="2bad6-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="2bad6-124">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2bad6-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="2bad6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bad6-125">-Name</span></span>
<span data-ttu-id="2bad6-126">Bu cmdlet 'in oluşturduğu URL yol eşleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-126">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2bad6-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="2bad6-127">-PathRules</span></span>
<span data-ttu-id="2bad6-128">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bad6-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="2bad6-129">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2bad6-129">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="2bad6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bad6-130">-DefaultProfile</span></span>
<span data-ttu-id="2bad6-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bad6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bad6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bad6-132">CommonParameters</span></span>
<span data-ttu-id="2bad6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bad6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bad6-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bad6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bad6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bad6-135">INPUTS</span></span>

## <span data-ttu-id="2bad6-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bad6-136">OUTPUTS</span></span>

### <span data-ttu-id="2bad6-137">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2bad6-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="2bad6-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bad6-138">NOTES</span></span>

## <span data-ttu-id="2bad6-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bad6-139">RELATED LINKS</span></span>

[<span data-ttu-id="2bad6-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2bad6-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2bad6-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2bad6-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2bad6-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2bad6-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2bad6-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2bad6-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


