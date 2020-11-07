---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760394"
---
# <span data-ttu-id="17389-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="17389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17389-102">SYNOPSIS</span></span>
<span data-ttu-id="17389-103">Uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17389-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="17389-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17389-104">SYNTAX</span></span>

### <span data-ttu-id="17389-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="17389-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17389-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="17389-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17389-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="17389-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17389-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17389-108">DESCRIPTION</span></span>
<span data-ttu-id="17389-109">**Yeni-AzApplicationGatewayRedirectConfiguration** cmdlet 'i bir uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17389-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="17389-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17389-110">EXAMPLES</span></span>

### <span data-ttu-id="17389-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17389-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="17389-112">Bu komut, Redirect01 adlı bir yönlendirme yapılandırması oluşturur ve sonucu $RedirectConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="17389-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="17389-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17389-113">PARAMETERS</span></span>

### <span data-ttu-id="17389-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17389-114">-DefaultProfile</span></span>
<span data-ttu-id="17389-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17389-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17389-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="17389-116">-IncludePath</span></span>
<span data-ttu-id="17389-117">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="17389-117">Include path in the redirected url.</span></span>
<span data-ttu-id="17389-118">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="17389-118">Default is true.</span></span>

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

### <span data-ttu-id="17389-119">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="17389-119">-IncludeQueryString</span></span>
<span data-ttu-id="17389-120">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="17389-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="17389-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="17389-121">Default is true.</span></span>

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

### <span data-ttu-id="17389-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="17389-122">-Name</span></span>
<span data-ttu-id="17389-123">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="17389-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="17389-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="17389-124">-RedirectType</span></span>
<span data-ttu-id="17389-125">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="17389-125">The type of redirect</span></span>

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

### <span data-ttu-id="17389-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="17389-126">-TargetListener</span></span>
<span data-ttu-id="17389-127">İsteğin yönlendirileceği HTTP dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="17389-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="17389-128">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="17389-128">-TargetListenerID</span></span>
<span data-ttu-id="17389-129">İsteğin yönlendirileceği HTTP dinleyicisinin KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="17389-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="17389-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="17389-130">-TargetUrl</span></span>
<span data-ttu-id="17389-131">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="17389-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="17389-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17389-132">CommonParameters</span></span>
<span data-ttu-id="17389-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17389-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17389-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17389-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17389-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17389-135">INPUTS</span></span>

### <span data-ttu-id="17389-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="17389-136">None</span></span>

## <span data-ttu-id="17389-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17389-137">OUTPUTS</span></span>

### <span data-ttu-id="17389-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="17389-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17389-139">NOTES</span></span>

## <span data-ttu-id="17389-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17389-140">RELATED LINKS</span></span>

[<span data-ttu-id="17389-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17389-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17389-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="17389-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="17389-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
