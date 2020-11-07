---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935650"
---
# <span data-ttu-id="0effe-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0effe-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="0effe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0effe-102">SYNOPSIS</span></span>
<span data-ttu-id="0effe-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0effe-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="0effe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0effe-104">SYNTAX</span></span>

### <span data-ttu-id="0effe-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="0effe-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0effe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0effe-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0effe-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="0effe-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0effe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0effe-108">DESCRIPTION</span></span>
<span data-ttu-id="0effe-109">**Add-AzApplicationGatewayRedirectConfiguration** cmdlet 'ı, uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0effe-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="0effe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0effe-110">EXAMPLES</span></span>

### <span data-ttu-id="0effe-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0effe-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="0effe-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0effe-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0effe-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="0effe-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="0effe-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0effe-114">PARAMETERS</span></span>

### <span data-ttu-id="0effe-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0effe-115">-ApplicationGateway</span></span>
<span data-ttu-id="0effe-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0effe-116">The applicationGateway</span></span>

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

### <span data-ttu-id="0effe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0effe-117">-DefaultProfile</span></span>
<span data-ttu-id="0effe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0effe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0effe-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="0effe-119">-IncludePath</span></span>
<span data-ttu-id="0effe-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0effe-120">Include path in the redirected url.</span></span>
<span data-ttu-id="0effe-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="0effe-121">Default is true.</span></span>

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

### <span data-ttu-id="0effe-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="0effe-122">-IncludeQueryString</span></span>
<span data-ttu-id="0effe-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0effe-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="0effe-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="0effe-124">Default is true.</span></span>

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

### <span data-ttu-id="0effe-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0effe-125">-Name</span></span>
<span data-ttu-id="0effe-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="0effe-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="0effe-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="0effe-127">-RedirectType</span></span>
<span data-ttu-id="0effe-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="0effe-128">The type of redirect</span></span>

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

### <span data-ttu-id="0effe-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="0effe-129">-TargetListener</span></span>
<span data-ttu-id="0effe-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="0effe-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="0effe-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="0effe-131">-TargetListenerID</span></span>
<span data-ttu-id="0effe-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="0effe-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="0effe-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="0effe-133">-TargetUrl</span></span>
<span data-ttu-id="0effe-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="0effe-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="0effe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0effe-135">CommonParameters</span></span>
<span data-ttu-id="0effe-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0effe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0effe-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0effe-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0effe-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0effe-138">INPUTS</span></span>

### <span data-ttu-id="0effe-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0effe-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0effe-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0effe-140">OUTPUTS</span></span>

### <span data-ttu-id="0effe-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0effe-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0effe-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0effe-142">NOTES</span></span>

## <span data-ttu-id="0effe-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0effe-143">RELATED LINKS</span></span>

