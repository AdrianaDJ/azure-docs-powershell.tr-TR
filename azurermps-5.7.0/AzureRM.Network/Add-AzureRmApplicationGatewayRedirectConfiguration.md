---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 73d60d86110893005e72152c08e82d4152b1c482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587543"
---
# <span data-ttu-id="18416-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="18416-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="18416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18416-102">SYNOPSIS</span></span>
<span data-ttu-id="18416-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="18416-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18416-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18416-104">SYNTAX</span></span>

### <span data-ttu-id="18416-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="18416-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18416-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="18416-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18416-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="18416-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18416-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18416-108">DESCRIPTION</span></span>
<span data-ttu-id="18416-109">**Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="18416-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="18416-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18416-110">EXAMPLES</span></span>

### <span data-ttu-id="18416-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18416-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="18416-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="18416-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="18416-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="18416-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="18416-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18416-114">PARAMETERS</span></span>

### <span data-ttu-id="18416-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18416-115">-ApplicationGateway</span></span>
<span data-ttu-id="18416-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18416-116">The applicationGateway</span></span>

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

### <span data-ttu-id="18416-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18416-117">-DefaultProfile</span></span>
<span data-ttu-id="18416-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18416-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18416-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="18416-119">-IncludePath</span></span>
<span data-ttu-id="18416-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="18416-120">Include path in the redirected url.</span></span>
<span data-ttu-id="18416-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="18416-121">Default is true.</span></span>

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

### <span data-ttu-id="18416-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="18416-122">-IncludeQueryString</span></span>
<span data-ttu-id="18416-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="18416-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="18416-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="18416-124">Default is true.</span></span>

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

### <span data-ttu-id="18416-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="18416-125">-Name</span></span>
<span data-ttu-id="18416-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="18416-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="18416-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="18416-127">-RedirectType</span></span>
<span data-ttu-id="18416-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="18416-128">The type of redirect</span></span>

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

### <span data-ttu-id="18416-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="18416-129">-TargetListener</span></span>
<span data-ttu-id="18416-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="18416-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="18416-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="18416-131">-TargetListenerID</span></span>
<span data-ttu-id="18416-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="18416-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="18416-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="18416-133">-TargetUrl</span></span>
<span data-ttu-id="18416-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="18416-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="18416-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18416-135">CommonParameters</span></span>
<span data-ttu-id="18416-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18416-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18416-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18416-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18416-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18416-138">INPUTS</span></span>

### <span data-ttu-id="18416-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18416-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18416-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18416-140">OUTPUTS</span></span>

### <span data-ttu-id="18416-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18416-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18416-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18416-142">NOTES</span></span>

## <span data-ttu-id="18416-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18416-143">RELATED LINKS</span></span>

