---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935422"
---
# <span data-ttu-id="29e4e-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29e4e-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="29e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="29e4e-103">Uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29e4e-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="29e4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29e4e-104">SYNTAX</span></span>

### <span data-ttu-id="29e4e-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="29e4e-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e4e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29e4e-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e4e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="29e4e-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29e4e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="29e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="29e4e-109">**Yeni-AzApplicationGatewayRedirectConfiguration** cmdlet 'i bir uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29e4e-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="29e4e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29e4e-110">EXAMPLES</span></span>

### <span data-ttu-id="29e4e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29e4e-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="29e4e-112">Bu komut, Redirect01 adlı bir yönlendirme yapılandırması oluşturur ve sonucu $RedirectConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="29e4e-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="29e4e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29e4e-113">PARAMETERS</span></span>

### <span data-ttu-id="29e4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e4e-114">-DefaultProfile</span></span>
<span data-ttu-id="29e4e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29e4e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29e4e-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="29e4e-116">-IncludePath</span></span>
<span data-ttu-id="29e4e-117">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="29e4e-117">Include path in the redirected url.</span></span>
<span data-ttu-id="29e4e-118">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="29e4e-118">Default is true.</span></span>

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

### <span data-ttu-id="29e4e-119">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="29e4e-119">-IncludeQueryString</span></span>
<span data-ttu-id="29e4e-120">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="29e4e-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="29e4e-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="29e4e-121">Default is true.</span></span>

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

### <span data-ttu-id="29e4e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="29e4e-122">-Name</span></span>
<span data-ttu-id="29e4e-123">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="29e4e-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="29e4e-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="29e4e-124">-RedirectType</span></span>
<span data-ttu-id="29e4e-125">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="29e4e-125">The type of redirect</span></span>

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

### <span data-ttu-id="29e4e-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="29e4e-126">-TargetListener</span></span>
<span data-ttu-id="29e4e-127">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="29e4e-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="29e4e-128">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="29e4e-128">-TargetListenerID</span></span>
<span data-ttu-id="29e4e-129">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="29e4e-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="29e4e-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="29e4e-130">-TargetUrl</span></span>
<span data-ttu-id="29e4e-131">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="29e4e-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="29e4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e4e-132">CommonParameters</span></span>
<span data-ttu-id="29e4e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29e4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e4e-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e4e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e4e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29e4e-135">INPUTS</span></span>

### <span data-ttu-id="29e4e-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="29e4e-136">None</span></span>

## <span data-ttu-id="29e4e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29e4e-137">OUTPUTS</span></span>

### <span data-ttu-id="29e4e-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="29e4e-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="29e4e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29e4e-139">NOTES</span></span>

## <span data-ttu-id="29e4e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29e4e-140">RELATED LINKS</span></span>

