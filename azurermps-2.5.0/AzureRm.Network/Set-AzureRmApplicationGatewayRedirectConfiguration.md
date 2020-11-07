---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: c851e075c4963477d8b8f6b18440780735c74f32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939694"
---
# <span data-ttu-id="14ed5-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14ed5-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="14ed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="14ed5-103">Varolan bir uygulama ağ geçidinde yeniden yönlendirme yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="14ed5-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14ed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14ed5-104">SYNTAX</span></span>

### <span data-ttu-id="14ed5-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="14ed5-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ed5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14ed5-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ed5-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="14ed5-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ed5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="14ed5-108">DESCRIPTION</span></span>
<span data-ttu-id="14ed5-109">**Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i yeniden yönlendirme yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="14ed5-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="14ed5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14ed5-110">EXAMPLES</span></span>

### <span data-ttu-id="14ed5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14ed5-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="14ed5-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="14ed5-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="14ed5-113">İkinci komut, uygulama ağ geçidinin yeniden yönlendirme yapılandırmasını kalıcı olarak yeniden yönlendirmek ve hedef URL 'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="14ed5-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="14ed5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14ed5-114">PARAMETERS</span></span>

### <span data-ttu-id="14ed5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ed5-115">-ApplicationGateway</span></span>
<span data-ttu-id="14ed5-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ed5-116">The applicationGateway</span></span>

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

### <span data-ttu-id="14ed5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ed5-117">-DefaultProfile</span></span>
<span data-ttu-id="14ed5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14ed5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14ed5-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="14ed5-119">-IncludePath</span></span>
<span data-ttu-id="14ed5-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="14ed5-120">Include path in the redirected url.</span></span>
<span data-ttu-id="14ed5-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="14ed5-121">Default is true.</span></span>

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

### <span data-ttu-id="14ed5-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="14ed5-122">-IncludeQueryString</span></span>
<span data-ttu-id="14ed5-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="14ed5-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="14ed5-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="14ed5-124">Default is true.</span></span>

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

### <span data-ttu-id="14ed5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="14ed5-125">-Name</span></span>
<span data-ttu-id="14ed5-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="14ed5-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="14ed5-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="14ed5-127">-RedirectType</span></span>
<span data-ttu-id="14ed5-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="14ed5-128">The type of redirect</span></span>

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

### <span data-ttu-id="14ed5-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="14ed5-129">-TargetListener</span></span>
<span data-ttu-id="14ed5-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="14ed5-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="14ed5-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="14ed5-131">-TargetListenerID</span></span>
<span data-ttu-id="14ed5-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="14ed5-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="14ed5-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="14ed5-133">-TargetUrl</span></span>
<span data-ttu-id="14ed5-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="14ed5-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="14ed5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ed5-135">CommonParameters</span></span>
<span data-ttu-id="14ed5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14ed5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ed5-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ed5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ed5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14ed5-138">INPUTS</span></span>

### <span data-ttu-id="14ed5-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ed5-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14ed5-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14ed5-140">OUTPUTS</span></span>

### <span data-ttu-id="14ed5-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14ed5-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14ed5-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14ed5-142">NOTES</span></span>

## <span data-ttu-id="14ed5-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14ed5-143">RELATED LINKS</span></span>

