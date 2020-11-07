---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d0944ad15beeab3de380801480560bc216a7df16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761962"
---
# <span data-ttu-id="a8540-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8540-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a8540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8540-102">SYNOPSIS</span></span>
<span data-ttu-id="a8540-103">Arka uç sunucu havuzuna ait bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a8540-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8540-104">SYNTAX</span></span>

### <span data-ttu-id="a8540-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="a8540-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8540-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a8540-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8540-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8540-107">DESCRIPTION</span></span>
<span data-ttu-id="a8540-108">**Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna AIT bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a8540-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a8540-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8540-109">EXAMPLES</span></span>

## <span data-ttu-id="a8540-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8540-110">PARAMETERS</span></span>

### <span data-ttu-id="a8540-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8540-111">-ApplicationGateway</span></span>
<span data-ttu-id="a8540-112">Bu cmdlet 'in URL yol haritası yapılandırmasını ayarladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="a8540-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8540-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a8540-114">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a8540-115">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="a8540-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a8540-116">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="a8540-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a8540-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a8540-118">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a8540-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a8540-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a8540-120">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="a8540-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8540-121">-DefaultProfile</span></span>
<span data-ttu-id="a8540-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8540-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8540-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8540-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a8540-124">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="a8540-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a8540-125">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="a8540-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a8540-126">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="a8540-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a8540-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8540-127">-Name</span></span>
<span data-ttu-id="a8540-128">Bu cmdlet 'in yapılandırmasını ayarladığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="a8540-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a8540-129">-PathRules</span></span>
<span data-ttu-id="a8540-130">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8540-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="a8540-131">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a8540-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="a8540-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8540-132">CommonParameters</span></span>
<span data-ttu-id="a8540-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8540-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8540-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8540-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8540-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8540-135">INPUTS</span></span>

### <span data-ttu-id="a8540-136">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8540-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="a8540-137">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8540-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="a8540-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8540-138">OUTPUTS</span></span>

### <span data-ttu-id="a8540-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8540-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8540-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8540-140">NOTES</span></span>

## <span data-ttu-id="a8540-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8540-141">RELATED LINKS</span></span>

[<span data-ttu-id="a8540-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8540-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8540-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8540-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8540-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8540-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a8540-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a8540-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


