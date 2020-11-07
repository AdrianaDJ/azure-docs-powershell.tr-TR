---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935646"
---
# <span data-ttu-id="9246f-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9246f-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9246f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9246f-102">SYNOPSIS</span></span>
<span data-ttu-id="9246f-103">Arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="9246f-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9246f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9246f-104">SYNTAX</span></span>

### <span data-ttu-id="9246f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9246f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9246f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9246f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9246f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9246f-107">DESCRIPTION</span></span>
<span data-ttu-id="9246f-108">**Add-AzApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="9246f-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="9246f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9246f-109">EXAMPLES</span></span>

### <span data-ttu-id="9246f-110">2</span><span class="sxs-lookup"><span data-stu-id="9246f-110">1:</span></span>
```

```

## <span data-ttu-id="9246f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9246f-111">PARAMETERS</span></span>

### <span data-ttu-id="9246f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9246f-112">-ApplicationGateway</span></span>
<span data-ttu-id="9246f-113">Bu cmdlet 'in URL yol haritası yapılandırmasını eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="9246f-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9246f-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="9246f-115">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9246f-116">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="9246f-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="9246f-117">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="9246f-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9246f-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="9246f-119">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9246f-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9246f-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="9246f-121">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="9246f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9246f-122">-DefaultProfile</span></span>
<span data-ttu-id="9246f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9246f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9246f-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9246f-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="9246f-125">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="9246f-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9246f-126">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="9246f-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="9246f-127">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="9246f-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9246f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="9246f-128">-Name</span></span>
<span data-ttu-id="9246f-129">Bu cmdlet 'in arka uç sunucu havuzuna eklediği URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="9246f-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="9246f-130">-PathRules</span></span>
<span data-ttu-id="9246f-131">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9246f-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="9246f-132">Yol kuralları sıralı duyarlı, belirtildikleri sırayla uygulanır.</span><span class="sxs-lookup"><span data-stu-id="9246f-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="9246f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9246f-133">CommonParameters</span></span>
<span data-ttu-id="9246f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9246f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9246f-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9246f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9246f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9246f-136">INPUTS</span></span>

### <span data-ttu-id="9246f-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9246f-137">PSApplicationGateway</span></span>
<span data-ttu-id="9246f-138">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9246f-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9246f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9246f-139">OUTPUTS</span></span>

### <span data-ttu-id="9246f-140">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9246f-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9246f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9246f-141">NOTES</span></span>

## <span data-ttu-id="9246f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9246f-142">RELATED LINKS</span></span>

[<span data-ttu-id="9246f-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9246f-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9246f-144">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9246f-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9246f-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9246f-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9246f-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9246f-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


