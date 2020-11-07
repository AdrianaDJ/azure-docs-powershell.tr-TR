---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 9a37bd3769fa7078e0d215b2d6c2452c4fc64bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765101"
---
# <span data-ttu-id="cb5ef-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb5ef-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="cb5ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5ef-103">Varolan bir uygulama ağ geçidinde yeniden yönlendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb5ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb5ef-104">SYNTAX</span></span>

### <span data-ttu-id="cb5ef-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cb5ef-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cb5ef-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5ef-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="cb5ef-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb5ef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb5ef-108">DESCRIPTION</span></span>
<span data-ttu-id="cb5ef-109">**Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i yeniden yönlendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="cb5ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb5ef-110">EXAMPLES</span></span>

### <span data-ttu-id="cb5ef-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb5ef-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="cb5ef-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cb5ef-113">İkinci komut, uygulama ağ geçidinin yeniden yönlendirme yapılandırmasını kalıcı olarak yeniden yönlendirmek ve hedef URL 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="cb5ef-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb5ef-114">PARAMETERS</span></span>

### <span data-ttu-id="cb5ef-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb5ef-115">-ApplicationGateway</span></span>
<span data-ttu-id="cb5ef-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb5ef-116">The applicationGateway</span></span>

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

### <span data-ttu-id="cb5ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5ef-117">-DefaultProfile</span></span>
<span data-ttu-id="cb5ef-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb5ef-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="cb5ef-119">-IncludePath</span></span>
<span data-ttu-id="cb5ef-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-120">Include path in the redirected url.</span></span>
<span data-ttu-id="cb5ef-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5ef-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="cb5ef-122">-IncludeQueryString</span></span>
<span data-ttu-id="cb5ef-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="cb5ef-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5ef-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb5ef-125">-Name</span></span>
<span data-ttu-id="cb5ef-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="cb5ef-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="cb5ef-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="cb5ef-127">-RedirectType</span></span>
<span data-ttu-id="cb5ef-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="cb5ef-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5ef-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="cb5ef-129">-TargetListener</span></span>
<span data-ttu-id="cb5ef-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="cb5ef-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5ef-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="cb5ef-131">-TargetListenerID</span></span>
<span data-ttu-id="cb5ef-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="cb5ef-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="cb5ef-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="cb5ef-133">-TargetUrl</span></span>
<span data-ttu-id="cb5ef-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="cb5ef-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5ef-135">CommonParameters</span></span>
<span data-ttu-id="cb5ef-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb5ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5ef-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5ef-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5ef-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb5ef-138">INPUTS</span></span>

### <span data-ttu-id="cb5ef-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb5ef-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb5ef-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb5ef-140">OUTPUTS</span></span>

### <span data-ttu-id="cb5ef-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb5ef-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb5ef-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb5ef-142">NOTES</span></span>

## <span data-ttu-id="cb5ef-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb5ef-143">RELATED LINKS</span></span>
