---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: da6acfddcee30861b73145d7d8e66871de02568d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096826"
---
# <span data-ttu-id="4d1d9-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1d9-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4d1d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1d9-103">Varolan bir uygulama ağ geçidinde yeniden yönlendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="4d1d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d1d9-104">SYNTAX</span></span>

### <span data-ttu-id="4d1d9-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d1d9-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d1d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4d1d9-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d1d9-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="4d1d9-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d1d9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d1d9-108">DESCRIPTION</span></span>
<span data-ttu-id="4d1d9-109">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet 'i yeniden yönlendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="4d1d9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d1d9-110">EXAMPLES</span></span>

### <span data-ttu-id="4d1d9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d1d9-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="4d1d9-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4d1d9-113">İkinci komut, uygulama ağ geçidinin yeniden yönlendirme yapılandırmasını kalıcı olarak yeniden yönlendirmek ve hedef URL 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="4d1d9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d1d9-114">PARAMETERS</span></span>

### <span data-ttu-id="4d1d9-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1d9-115">-ApplicationGateway</span></span>
<span data-ttu-id="4d1d9-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1d9-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4d1d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1d9-117">-DefaultProfile</span></span>
<span data-ttu-id="4d1d9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1d9-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="4d1d9-119">-IncludePath</span></span>
<span data-ttu-id="4d1d9-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-120">Include path in the redirected url.</span></span>
<span data-ttu-id="4d1d9-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1d9-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="4d1d9-122">-IncludeQueryString</span></span>
<span data-ttu-id="4d1d9-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="4d1d9-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1d9-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d1d9-125">-Name</span></span>
<span data-ttu-id="4d1d9-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="4d1d9-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="4d1d9-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="4d1d9-127">-RedirectType</span></span>
<span data-ttu-id="4d1d9-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="4d1d9-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1d9-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="4d1d9-129">-TargetListener</span></span>
<span data-ttu-id="4d1d9-130">İsteğin yönlendirileceği HTTP dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d1d9-130">HTTP listener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1d9-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="4d1d9-131">-TargetListenerID</span></span>
<span data-ttu-id="4d1d9-132">İsteğin yönlendirileceği HTTP dinleyicisinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="4d1d9-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="4d1d9-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4d1d9-133">-TargetUrl</span></span>
<span data-ttu-id="4d1d9-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="4d1d9-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d1d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1d9-135">CommonParameters</span></span>
<span data-ttu-id="4d1d9-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d1d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1d9-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1d9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1d9-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d1d9-138">INPUTS</span></span>

### <span data-ttu-id="4d1d9-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1d9-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d1d9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d1d9-140">OUTPUTS</span></span>

### <span data-ttu-id="4d1d9-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d1d9-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d1d9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d1d9-142">NOTES</span></span>

## <span data-ttu-id="4d1d9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d1d9-143">RELATED LINKS</span></span>

[<span data-ttu-id="4d1d9-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1d9-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4d1d9-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1d9-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4d1d9-146">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1d9-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4d1d9-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d1d9-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
