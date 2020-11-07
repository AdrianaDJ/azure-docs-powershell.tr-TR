---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 01f7daf47fa62e346dc7323ee5978f81f5797e29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764946"
---
# <span data-ttu-id="1b776-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b776-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1b776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b776-102">SYNOPSIS</span></span>
<span data-ttu-id="1b776-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1b776-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b776-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b776-104">SYNTAX</span></span>

### <span data-ttu-id="1b776-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1b776-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b776-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b776-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b776-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="1b776-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b776-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b776-108">DESCRIPTION</span></span>
<span data-ttu-id="1b776-109">**Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="1b776-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="1b776-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b776-110">EXAMPLES</span></span>

### <span data-ttu-id="1b776-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b776-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="1b776-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1b776-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1b776-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="1b776-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="1b776-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b776-114">PARAMETERS</span></span>

### <span data-ttu-id="1b776-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b776-115">-ApplicationGateway</span></span>
<span data-ttu-id="1b776-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b776-116">The applicationGateway</span></span>

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

### <span data-ttu-id="1b776-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b776-117">-DefaultProfile</span></span>
<span data-ttu-id="1b776-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b776-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b776-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="1b776-119">-IncludePath</span></span>
<span data-ttu-id="1b776-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1b776-120">Include path in the redirected url.</span></span>
<span data-ttu-id="1b776-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="1b776-121">Default is true.</span></span>

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

### <span data-ttu-id="1b776-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="1b776-122">-IncludeQueryString</span></span>
<span data-ttu-id="1b776-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1b776-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="1b776-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="1b776-124">Default is true.</span></span>

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

### <span data-ttu-id="1b776-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b776-125">-Name</span></span>
<span data-ttu-id="1b776-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="1b776-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="1b776-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="1b776-127">-RedirectType</span></span>
<span data-ttu-id="1b776-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="1b776-128">The type of redirect</span></span>

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

### <span data-ttu-id="1b776-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="1b776-129">-TargetListener</span></span>
<span data-ttu-id="1b776-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="1b776-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="1b776-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="1b776-131">-TargetListenerID</span></span>
<span data-ttu-id="1b776-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="1b776-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="1b776-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="1b776-133">-TargetUrl</span></span>
<span data-ttu-id="1b776-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="1b776-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="1b776-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b776-135">CommonParameters</span></span>
<span data-ttu-id="1b776-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b776-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b776-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b776-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b776-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b776-138">INPUTS</span></span>

### <span data-ttu-id="1b776-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b776-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1b776-140">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b776-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1b776-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b776-141">OUTPUTS</span></span>

### <span data-ttu-id="1b776-142">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b776-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b776-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b776-143">NOTES</span></span>

## <span data-ttu-id="1b776-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b776-144">RELATED LINKS</span></span>
