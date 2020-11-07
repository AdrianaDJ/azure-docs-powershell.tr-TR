---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bf187375ba625e40c147f7862d9faf4e0706f844
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938230"
---
# <span data-ttu-id="7c0a8-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0a8-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7c0a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0a8-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="7c0a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c0a8-104">SYNTAX</span></span>

### <span data-ttu-id="7c0a8-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7c0a8-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c0a8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7c0a8-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c0a8-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="7c0a8-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c0a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c0a8-108">DESCRIPTION</span></span>
<span data-ttu-id="7c0a8-109">**Add-AzApplicationGatewayRedirectConfiguration** cmdlet 'ı, uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="7c0a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c0a8-110">EXAMPLES</span></span>

### <span data-ttu-id="7c0a8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7c0a8-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="7c0a8-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7c0a8-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="7c0a8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c0a8-114">PARAMETERS</span></span>

### <span data-ttu-id="7c0a8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c0a8-115">-ApplicationGateway</span></span>
<span data-ttu-id="7c0a8-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c0a8-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7c0a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0a8-117">-DefaultProfile</span></span>
<span data-ttu-id="7c0a8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c0a8-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="7c0a8-119">-IncludePath</span></span>
<span data-ttu-id="7c0a8-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-120">Include path in the redirected url.</span></span>
<span data-ttu-id="7c0a8-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-121">Default is true.</span></span>

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

### <span data-ttu-id="7c0a8-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="7c0a8-122">-IncludeQueryString</span></span>
<span data-ttu-id="7c0a8-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="7c0a8-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-124">Default is true.</span></span>

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

### <span data-ttu-id="7c0a8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c0a8-125">-Name</span></span>
<span data-ttu-id="7c0a8-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="7c0a8-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="7c0a8-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="7c0a8-127">-RedirectType</span></span>
<span data-ttu-id="7c0a8-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="7c0a8-128">The type of redirect</span></span>

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

### <span data-ttu-id="7c0a8-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="7c0a8-129">-TargetListener</span></span>
<span data-ttu-id="7c0a8-130">İsteğin yönlendirileceği HTTP dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="7c0a8-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="7c0a8-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="7c0a8-131">-TargetListenerID</span></span>
<span data-ttu-id="7c0a8-132">İsteğin yönlendirileceği HTTP dinleyicisinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="7c0a8-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="7c0a8-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="7c0a8-133">-TargetUrl</span></span>
<span data-ttu-id="7c0a8-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="7c0a8-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="7c0a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0a8-135">CommonParameters</span></span>
<span data-ttu-id="7c0a8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0a8-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c0a8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0a8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c0a8-138">INPUTS</span></span>

### <span data-ttu-id="7c0a8-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c0a8-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c0a8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c0a8-140">OUTPUTS</span></span>

### <span data-ttu-id="7c0a8-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c0a8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c0a8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c0a8-142">NOTES</span></span>

## <span data-ttu-id="7c0a8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c0a8-143">RELATED LINKS</span></span>

[<span data-ttu-id="7c0a8-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0a8-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7c0a8-145">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0a8-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7c0a8-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0a8-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7c0a8-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c0a8-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
