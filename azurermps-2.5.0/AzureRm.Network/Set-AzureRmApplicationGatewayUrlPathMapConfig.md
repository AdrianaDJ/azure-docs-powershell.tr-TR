---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939695"
---
# <span data-ttu-id="d98d5-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d98d5-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d98d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d98d5-103">Arka uç sunucu havuzuna ait bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d98d5-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d98d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d98d5-104">SYNTAX</span></span>

### <span data-ttu-id="d98d5-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d98d5-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d98d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d98d5-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d98d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d98d5-107">DESCRIPTION</span></span>
<span data-ttu-id="d98d5-108">**Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna AIT bir URL yolu eşlemeleri dizisinin yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d98d5-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d98d5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d98d5-109">EXAMPLES</span></span>

### <span data-ttu-id="d98d5-110">2</span><span class="sxs-lookup"><span data-stu-id="d98d5-110">1:</span></span>
```

```

## <span data-ttu-id="d98d5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d98d5-111">PARAMETERS</span></span>

### <span data-ttu-id="d98d5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d98d5-112">-ApplicationGateway</span></span>
<span data-ttu-id="d98d5-113">Bu cmdlet 'in URL yol haritası yapılandırmasını ayarladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d98d5-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d98d5-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d98d5-115">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d98d5-116">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="d98d5-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d98d5-117">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d98d5-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d98d5-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d98d5-119">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d98d5-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d98d5-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d98d5-121">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d98d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98d5-122">-DefaultProfile</span></span>
<span data-ttu-id="d98d5-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d98d5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d98d5-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d98d5-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d98d5-125">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="d98d5-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d98d5-126">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="d98d5-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d98d5-127">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="d98d5-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d98d5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d98d5-128">-Name</span></span>
<span data-ttu-id="d98d5-129">Bu cmdlet 'in yapılandırmasını ayarladığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="d98d5-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d98d5-130">-PathRules</span></span>
<span data-ttu-id="d98d5-131">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d98d5-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="d98d5-132">Yol kurallarının, belirtildikleri sırayla uygulandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d98d5-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d98d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98d5-133">CommonParameters</span></span>
<span data-ttu-id="d98d5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d98d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98d5-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98d5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98d5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d98d5-136">INPUTS</span></span>

### <span data-ttu-id="d98d5-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d98d5-137">PSApplicationGateway</span></span>
<span data-ttu-id="d98d5-138">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d98d5-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d98d5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d98d5-139">OUTPUTS</span></span>

### <span data-ttu-id="d98d5-140">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d98d5-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d98d5-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d98d5-141">NOTES</span></span>

## <span data-ttu-id="d98d5-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d98d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="d98d5-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d98d5-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d98d5-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d98d5-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d98d5-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d98d5-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d98d5-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d98d5-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


