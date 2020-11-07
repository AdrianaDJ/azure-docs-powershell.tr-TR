---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 1816b7407ec1d36f8eb5fd213484e22a9e89998c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938965"
---
# <span data-ttu-id="e7174-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7174-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e7174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7174-102">SYNOPSIS</span></span>
<span data-ttu-id="e7174-103">Uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e7174-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7174-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7174-104">SYNTAX</span></span>

### <span data-ttu-id="e7174-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7174-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7174-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e7174-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7174-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e7174-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7174-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7174-108">DESCRIPTION</span></span>
<span data-ttu-id="e7174-109">**Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidine yeniden yönlendirme yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e7174-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="e7174-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7174-110">EXAMPLES</span></span>

### <span data-ttu-id="e7174-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7174-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="e7174-112">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e7174-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e7174-113">İkinci komut, yönlendirme yapılandırmasını uygulama ağ geçidine ekler.</span><span class="sxs-lookup"><span data-stu-id="e7174-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="e7174-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7174-114">PARAMETERS</span></span>

### <span data-ttu-id="e7174-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7174-115">-ApplicationGateway</span></span>
<span data-ttu-id="e7174-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7174-116">The applicationGateway</span></span>

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

### <span data-ttu-id="e7174-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7174-117">-DefaultProfile</span></span>
<span data-ttu-id="e7174-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7174-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7174-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e7174-119">-IncludePath</span></span>
<span data-ttu-id="e7174-120">Yeniden yönlendirilen URL 'ye yol ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7174-120">Include path in the redirected url.</span></span>
<span data-ttu-id="e7174-121">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="e7174-121">Default is true.</span></span>

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

### <span data-ttu-id="e7174-122">-Includequerystring</span><span class="sxs-lookup"><span data-stu-id="e7174-122">-IncludeQueryString</span></span>
<span data-ttu-id="e7174-123">Yeniden yönlendirilen URL 'ye sorgu dizesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e7174-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="e7174-124">Varsayılan doğrudur.</span><span class="sxs-lookup"><span data-stu-id="e7174-124">Default is true.</span></span>

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

### <span data-ttu-id="e7174-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7174-125">-Name</span></span>
<span data-ttu-id="e7174-126">Yönlendirme yapılandırmasının adı</span><span class="sxs-lookup"><span data-stu-id="e7174-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e7174-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e7174-127">-RedirectType</span></span>
<span data-ttu-id="e7174-128">Yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="e7174-128">The type of redirect</span></span>

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

### <span data-ttu-id="e7174-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e7174-129">-TargetListener</span></span>
<span data-ttu-id="e7174-130">HTTPListener</span><span class="sxs-lookup"><span data-stu-id="e7174-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="e7174-131">-Targetlistenerıd</span><span class="sxs-lookup"><span data-stu-id="e7174-131">-TargetListenerID</span></span>
<span data-ttu-id="e7174-132">İsteği yönlendirme KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="e7174-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="e7174-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e7174-133">-TargetUrl</span></span>
<span data-ttu-id="e7174-134">Hedef URL fo yeniden yönlendirmesi</span><span class="sxs-lookup"><span data-stu-id="e7174-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="e7174-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7174-135">CommonParameters</span></span>
<span data-ttu-id="e7174-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7174-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7174-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7174-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7174-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7174-138">INPUTS</span></span>

### <span data-ttu-id="e7174-139">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7174-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7174-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7174-140">OUTPUTS</span></span>

### <span data-ttu-id="e7174-141">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7174-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7174-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7174-142">NOTES</span></span>

## <span data-ttu-id="e7174-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7174-143">RELATED LINKS</span></span>

