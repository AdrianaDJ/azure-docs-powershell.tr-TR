---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 3885298f58f3bc45b207ea14cdda0935d0724986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590433"
---
# <span data-ttu-id="4d1b6-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d1b6-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4d1b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1b6-103">Arka uç sunucu havuzuna bir URL yolu eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d1b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d1b6-104">SYNTAX</span></span>

### <span data-ttu-id="4d1b6-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d1b6-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d1b6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d1b6-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d1b6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d1b6-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1b6-108">**Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'i arka uç sunucu havuzuna bir URL yol eşlemeleri dizisi ekler.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="4d1b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d1b6-109">EXAMPLES</span></span>

## <span data-ttu-id="4d1b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d1b6-110">PARAMETERS</span></span>

### <span data-ttu-id="4d1b6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1b6-111">-ApplicationGateway</span></span>
<span data-ttu-id="4d1b6-112">Bu cmdlet 'in URL yol haritası yapılandırmasını eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="4d1b6-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d1b6-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4d1b6-114">*Pathrules* parametresinde belirtilen kuralların eşleşmemesi durumunda, yönlendirilecek varsayılan arka uç adres havuzunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4d1b6-115">-Defaultbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="4d1b6-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4d1b6-116">Varsayılan arka uç adres havuzu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="4d1b6-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4d1b6-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4d1b6-118">*Pathrules* parametresinde belirtilen kuralların eşleşmediği durumlarda kullanılacak varsayılan arka uç http ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4d1b6-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4d1b6-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4d1b6-120">Varsayılan arka uç HTTP ayarları KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="4d1b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1b6-121">-DefaultProfile</span></span>
<span data-ttu-id="4d1b6-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1b6-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1b6-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4d1b6-124">Uygulama ağ geçidi varsayılan Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="4d1b6-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4d1b6-125">-Defaultredirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="4d1b6-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4d1b6-126">Uygulama ağ geçidi varsayılan RedirectConfiguration 'ın KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="4d1b6-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4d1b6-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d1b6-127">-Name</span></span>
<span data-ttu-id="4d1b6-128">Bu cmdlet 'in arka uç sunucu havuzuna eklediği URL yol eşlem adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="4d1b6-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4d1b6-129">-PathRules</span></span>
<span data-ttu-id="4d1b6-130">Yol kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="4d1b6-131">Yol kuralları sıralı duyarlı, belirtildikleri sırayla uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="4d1b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1b6-132">CommonParameters</span></span>
<span data-ttu-id="4d1b6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1b6-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1b6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d1b6-135">INPUTS</span></span>

### <span data-ttu-id="4d1b6-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1b6-136">PSApplicationGateway</span></span>
<span data-ttu-id="4d1b6-137">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4d1b6-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4d1b6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d1b6-138">OUTPUTS</span></span>

### <span data-ttu-id="4d1b6-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1b6-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d1b6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d1b6-140">NOTES</span></span>

## <span data-ttu-id="4d1b6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d1b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="4d1b6-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d1b6-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d1b6-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d1b6-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d1b6-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d1b6-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4d1b6-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4d1b6-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


