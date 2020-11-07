---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762700"
---
# <span data-ttu-id="f2f87-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2f87-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f2f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f87-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f87-103">Varolan bir uygulama ağ geçidinde yeniden yönlendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f2f87-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2f87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2f87-104">SYNTAX</span></span>

### <span data-ttu-id="f2f87-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f2f87-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2f87-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f87-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="f2f87-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f87-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2f87-108">DESCRIPTION</span></span>
<span data-ttu-id="f2f87-109">**Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i yeniden yönlendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f2f87-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="f2f87-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2f87-110">EXAMPLES</span></span>

### <span data-ttu-id="f2f87-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2f87-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="f2f87-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f2f87-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f2f87-113">İkinci komut, uygulama ağ geçidinin yeniden yönlendirme yapılandırmasını kalıcı olarak yeniden yönlendirmek ve hedef URL 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2f87-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="f2f87-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2f87-114">PARAMETERS</span></span>

### <span data-ttu-id="f2f87-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f87-115">-ApplicationGateway</span></span>
<span data-ttu-id="f2f87-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f87-116">The applicationGateway</span></span>

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

### <span data-ttu-id="f2f87-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="f2f87-117">-IncludePath</span></span>
<span data-ttu-id="f2f87-118">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f2f87-118">Include path in the redirected url.</span></span>
<span data-ttu-id="f2f87-119">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="f2f87-119">Default is true.</span></span>

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

### <span data-ttu-id="f2f87-120">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="f2f87-120">-IncludeQueryString</span></span>
<span data-ttu-id="f2f87-121">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f2f87-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="f2f87-122">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="f2f87-122">Default is true.</span></span>

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

### <span data-ttu-id="f2f87-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2f87-123">-Name</span></span>
<span data-ttu-id="f2f87-124">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="f2f87-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="f2f87-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="f2f87-125">-RedirectType</span></span>
<span data-ttu-id="f2f87-126">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="f2f87-126">The type of redirect</span></span>

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

### <span data-ttu-id="f2f87-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="f2f87-127">-TargetListener</span></span>
<span data-ttu-id="f2f87-128">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="f2f87-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="f2f87-129">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="f2f87-129">-TargetListenerID</span></span>
<span data-ttu-id="f2f87-130">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="f2f87-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="f2f87-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="f2f87-131">-TargetUrl</span></span>
<span data-ttu-id="f2f87-132">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="f2f87-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="f2f87-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f87-133">-DefaultProfile</span></span>
<span data-ttu-id="f2f87-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2f87-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f87-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f87-135">CommonParameters</span></span>
<span data-ttu-id="f2f87-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2f87-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f87-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f87-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f87-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2f87-138">INPUTS</span></span>

### <span data-ttu-id="f2f87-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f87-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2f87-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2f87-140">OUTPUTS</span></span>

### <span data-ttu-id="f2f87-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f87-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2f87-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2f87-142">NOTES</span></span>

## <span data-ttu-id="f2f87-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2f87-143">RELATED LINKS</span></span>

