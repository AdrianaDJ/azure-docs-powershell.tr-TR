---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764051"
---
# <span data-ttu-id="3e25f-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e25f-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="3e25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e25f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e25f-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3e25f-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e25f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e25f-104">SYNTAX</span></span>

### <span data-ttu-id="3e25f-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3e25f-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e25f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3e25f-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e25f-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="3e25f-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e25f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e25f-108">DESCRIPTION</span></span>
<span data-ttu-id="3e25f-109">**Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3e25f-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="3e25f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e25f-110">EXAMPLES</span></span>

### <span data-ttu-id="3e25f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3e25f-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="3e25f-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3e25f-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3e25f-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="3e25f-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="3e25f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e25f-114">PARAMETERS</span></span>

### <span data-ttu-id="3e25f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e25f-115">-ApplicationGateway</span></span>
<span data-ttu-id="3e25f-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e25f-116">The applicationGateway</span></span>

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

### <span data-ttu-id="3e25f-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="3e25f-117">-IncludePath</span></span>
<span data-ttu-id="3e25f-118">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3e25f-118">Include path in the redirected url.</span></span>
<span data-ttu-id="3e25f-119">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="3e25f-119">Default is true.</span></span>

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

### <span data-ttu-id="3e25f-120">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="3e25f-120">-IncludeQueryString</span></span>
<span data-ttu-id="3e25f-121">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3e25f-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="3e25f-122">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="3e25f-122">Default is true.</span></span>

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

### <span data-ttu-id="3e25f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e25f-123">-Name</span></span>
<span data-ttu-id="3e25f-124">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="3e25f-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="3e25f-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="3e25f-125">-RedirectType</span></span>
<span data-ttu-id="3e25f-126">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="3e25f-126">The type of redirect</span></span>

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

### <span data-ttu-id="3e25f-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="3e25f-127">-TargetListener</span></span>
<span data-ttu-id="3e25f-128">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="3e25f-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="3e25f-129">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="3e25f-129">-TargetListenerID</span></span>
<span data-ttu-id="3e25f-130">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3e25f-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="3e25f-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="3e25f-131">-TargetUrl</span></span>
<span data-ttu-id="3e25f-132">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="3e25f-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="3e25f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e25f-133">-DefaultProfile</span></span>
<span data-ttu-id="3e25f-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e25f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e25f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e25f-135">CommonParameters</span></span>
<span data-ttu-id="3e25f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e25f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e25f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e25f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e25f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e25f-138">INPUTS</span></span>

### <span data-ttu-id="3e25f-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e25f-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e25f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e25f-140">OUTPUTS</span></span>

### <span data-ttu-id="3e25f-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3e25f-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3e25f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e25f-142">NOTES</span></span>

## <span data-ttu-id="3e25f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e25f-143">RELATED LINKS</span></span>

