---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593532"
---
# <span data-ttu-id="2757b-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2757b-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2757b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2757b-102">SYNOPSIS</span></span>
<span data-ttu-id="2757b-103">Uygulama ağ geçidi için yeniden yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2757b-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2757b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2757b-104">SYNTAX</span></span>

### <span data-ttu-id="2757b-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2757b-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2757b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2757b-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2757b-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="2757b-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2757b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2757b-108">DESCRIPTION</span></span>
<span data-ttu-id="2757b-109">**New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'i bir uygulama ağ geçidi için Yönlendirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2757b-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="2757b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2757b-110">EXAMPLES</span></span>

### <span data-ttu-id="2757b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2757b-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="2757b-112">Bu komut, Redirect01 adlı bir yönlendirme yapılandırması oluşturur ve sonucu $RedirectConfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2757b-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="2757b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2757b-113">PARAMETERS</span></span>

### <span data-ttu-id="2757b-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="2757b-114">-IncludePath</span></span>
<span data-ttu-id="2757b-115">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2757b-115">Include path in the redirected url.</span></span>
<span data-ttu-id="2757b-116">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="2757b-116">Default is true.</span></span>

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

### <span data-ttu-id="2757b-117">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="2757b-117">-IncludeQueryString</span></span>
<span data-ttu-id="2757b-118">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2757b-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="2757b-119">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="2757b-119">Default is true.</span></span>

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

### <span data-ttu-id="2757b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2757b-120">-Name</span></span>
<span data-ttu-id="2757b-121">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="2757b-121">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="2757b-122">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="2757b-122">-RedirectType</span></span>
<span data-ttu-id="2757b-123">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="2757b-123">The type of redirect</span></span>

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

### <span data-ttu-id="2757b-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="2757b-124">-TargetListener</span></span>
<span data-ttu-id="2757b-125">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="2757b-125">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="2757b-126">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="2757b-126">-TargetListenerID</span></span>
<span data-ttu-id="2757b-127">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2757b-127">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="2757b-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="2757b-128">-TargetUrl</span></span>
<span data-ttu-id="2757b-129">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="2757b-129">Target URL fo redirection</span></span>

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

### <span data-ttu-id="2757b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2757b-130">-DefaultProfile</span></span>
<span data-ttu-id="2757b-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2757b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2757b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2757b-132">CommonParameters</span></span>
<span data-ttu-id="2757b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2757b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2757b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2757b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2757b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2757b-135">INPUTS</span></span>

### <span data-ttu-id="2757b-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2757b-136">None</span></span>

## <span data-ttu-id="2757b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2757b-137">OUTPUTS</span></span>

### <span data-ttu-id="2757b-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2757b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2757b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2757b-139">NOTES</span></span>

## <span data-ttu-id="2757b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2757b-140">RELATED LINKS</span></span>

