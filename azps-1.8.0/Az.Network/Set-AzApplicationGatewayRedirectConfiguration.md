---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760044"
---
# <span data-ttu-id="e1527-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1527-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e1527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1527-102">SYNOPSIS</span></span>
<span data-ttu-id="e1527-103">Varolan bir uygulama ağ geçidinde yeniden yönlendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e1527-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="e1527-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1527-104">SYNTAX</span></span>

### <span data-ttu-id="e1527-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e1527-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1527-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e1527-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1527-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e1527-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1527-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1527-108">DESCRIPTION</span></span>
<span data-ttu-id="e1527-109">**Set-AzApplicationGatewayRequestRoutingRule** cmdlet 'i yeniden yönlendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e1527-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="e1527-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1527-110">EXAMPLES</span></span>

### <span data-ttu-id="e1527-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1527-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="e1527-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e1527-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1527-113">İkinci komut, uygulama ağ geçidinin yeniden yönlendirme yapılandırmasını kalıcı olarak yeniden yönlendirmek ve hedef URL 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="e1527-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="e1527-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1527-114">PARAMETERS</span></span>

### <span data-ttu-id="e1527-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1527-115">-ApplicationGateway</span></span>
<span data-ttu-id="e1527-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1527-116">The applicationGateway</span></span>

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

### <span data-ttu-id="e1527-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1527-117">-DefaultProfile</span></span>
<span data-ttu-id="e1527-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1527-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1527-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e1527-119">-IncludePath</span></span>
<span data-ttu-id="e1527-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e1527-120">Include path in the redirected url.</span></span>
<span data-ttu-id="e1527-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="e1527-121">Default is true.</span></span>

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

### <span data-ttu-id="e1527-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="e1527-122">-IncludeQueryString</span></span>
<span data-ttu-id="e1527-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e1527-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="e1527-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="e1527-124">Default is true.</span></span>

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

### <span data-ttu-id="e1527-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1527-125">-Name</span></span>
<span data-ttu-id="e1527-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="e1527-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e1527-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e1527-127">-RedirectType</span></span>
<span data-ttu-id="e1527-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="e1527-128">The type of redirect</span></span>

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

### <span data-ttu-id="e1527-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e1527-129">-TargetListener</span></span>
<span data-ttu-id="e1527-130">İsteğin yönlendirileceği HTTP dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="e1527-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="e1527-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="e1527-131">-TargetListenerID</span></span>
<span data-ttu-id="e1527-132">İsteğin yönlendirileceği HTTP dinleyicisinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="e1527-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="e1527-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e1527-133">-TargetUrl</span></span>
<span data-ttu-id="e1527-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="e1527-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="e1527-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1527-135">CommonParameters</span></span>
<span data-ttu-id="e1527-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1527-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1527-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1527-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1527-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1527-138">INPUTS</span></span>

### <span data-ttu-id="e1527-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1527-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1527-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1527-140">OUTPUTS</span></span>

### <span data-ttu-id="e1527-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1527-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1527-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1527-142">NOTES</span></span>

## <span data-ttu-id="e1527-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1527-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1527-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1527-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e1527-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1527-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e1527-146">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1527-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e1527-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1527-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
