---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b6bfe8b7064324dea353543e0e9debe77e4b2edd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104788"
---
# <span data-ttu-id="d3a65-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d3a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a65-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a65-103">Uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3a65-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="d3a65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3a65-104">SYNTAX</span></span>

### <span data-ttu-id="d3a65-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d3a65-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a65-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d3a65-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a65-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="d3a65-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3a65-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3a65-108">DESCRIPTION</span></span>
<span data-ttu-id="d3a65-109">**Yeni-AzApplicationGatewayRedirectConfiguration** cmdlet 'i bir uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3a65-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="d3a65-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3a65-110">EXAMPLES</span></span>

### <span data-ttu-id="d3a65-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3a65-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="d3a65-112">Bu komut, Redirect01 adlı bir yönlendirme yapılandırması oluşturur ve sonucu $RedirectConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d3a65-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="d3a65-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3a65-113">PARAMETERS</span></span>

### <span data-ttu-id="d3a65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a65-114">-DefaultProfile</span></span>
<span data-ttu-id="d3a65-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3a65-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3a65-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="d3a65-116">-IncludePath</span></span>
<span data-ttu-id="d3a65-117">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d3a65-117">Include path in the redirected url.</span></span>
<span data-ttu-id="d3a65-118">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="d3a65-118">Default is true.</span></span>

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

### <span data-ttu-id="d3a65-119">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="d3a65-119">-IncludeQueryString</span></span>
<span data-ttu-id="d3a65-120">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d3a65-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="d3a65-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="d3a65-121">Default is true.</span></span>

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

### <span data-ttu-id="d3a65-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3a65-122">-Name</span></span>
<span data-ttu-id="d3a65-123">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="d3a65-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="d3a65-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="d3a65-124">-RedirectType</span></span>
<span data-ttu-id="d3a65-125">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="d3a65-125">The type of redirect</span></span>

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

### <span data-ttu-id="d3a65-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="d3a65-126">-TargetListener</span></span>
<span data-ttu-id="d3a65-127">İsteğin yönlendirileceği HTTP dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3a65-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="d3a65-128">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="d3a65-128">-TargetListenerID</span></span>
<span data-ttu-id="d3a65-129">İsteğin yönlendirileceği HTTP dinleyicisinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="d3a65-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="d3a65-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="d3a65-130">-TargetUrl</span></span>
<span data-ttu-id="d3a65-131">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="d3a65-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="d3a65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a65-132">CommonParameters</span></span>
<span data-ttu-id="d3a65-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3a65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a65-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a65-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a65-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3a65-135">INPUTS</span></span>

### <span data-ttu-id="d3a65-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3a65-136">None</span></span>

## <span data-ttu-id="d3a65-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3a65-137">OUTPUTS</span></span>

### <span data-ttu-id="d3a65-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d3a65-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3a65-139">NOTES</span></span>

## <span data-ttu-id="d3a65-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3a65-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3a65-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d3a65-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d3a65-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="d3a65-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a65-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
