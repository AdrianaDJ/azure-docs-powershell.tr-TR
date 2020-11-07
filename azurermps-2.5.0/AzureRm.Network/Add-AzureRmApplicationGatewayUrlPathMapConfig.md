---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939355"
---
# <span data-ttu-id="12cbb-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12cbb-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="12cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="12cbb-103">Arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="12cbb-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12cbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12cbb-104">SYNTAX</span></span>

### <span data-ttu-id="12cbb-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="12cbb-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12cbb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="12cbb-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12cbb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="12cbb-108">**Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="12cbb-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="12cbb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="12cbb-110">2</span><span class="sxs-lookup"><span data-stu-id="12cbb-110">1:</span></span>
```

```

## <span data-ttu-id="12cbb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12cbb-111">PARAMETERS</span></span>

### <span data-ttu-id="12cbb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12cbb-112">-ApplicationGateway</span></span>
<span data-ttu-id="12cbb-113">Bu cmdlet 'in URL yol haritası yapılandırmasını eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="12cbb-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12cbb-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="12cbb-115">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="12cbb-116">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="12cbb-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="12cbb-117">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="12cbb-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="12cbb-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="12cbb-119">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="12cbb-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="12cbb-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="12cbb-121">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="12cbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cbb-122">-DefaultProfile</span></span>
<span data-ttu-id="12cbb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12cbb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12cbb-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="12cbb-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="12cbb-125">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="12cbb-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="12cbb-126">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="12cbb-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="12cbb-127">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="12cbb-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="12cbb-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="12cbb-128">-Name</span></span>
<span data-ttu-id="12cbb-129">Bu cmdlet 'in arka uç sunucu havuzuna eklediği URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="12cbb-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="12cbb-130">-PathRules</span></span>
<span data-ttu-id="12cbb-131">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12cbb-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="12cbb-132">Yol kuralları sıralı duyarlı, belirtildikleri sırayla uygulanır.</span><span class="sxs-lookup"><span data-stu-id="12cbb-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="12cbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cbb-133">CommonParameters</span></span>
<span data-ttu-id="12cbb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12cbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cbb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cbb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cbb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12cbb-136">INPUTS</span></span>

### <span data-ttu-id="12cbb-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12cbb-137">PSApplicationGateway</span></span>
<span data-ttu-id="12cbb-138">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="12cbb-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="12cbb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12cbb-139">OUTPUTS</span></span>

### <span data-ttu-id="12cbb-140">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12cbb-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12cbb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12cbb-141">NOTES</span></span>

## <span data-ttu-id="12cbb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12cbb-142">RELATED LINKS</span></span>

[<span data-ttu-id="12cbb-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12cbb-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="12cbb-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12cbb-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="12cbb-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12cbb-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="12cbb-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="12cbb-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


