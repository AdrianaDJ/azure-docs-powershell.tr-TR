---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 424dd1c13dbc6d860bec05da84704caba96735af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097338"
---
# <span data-ttu-id="e5260-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e5260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5260-102">SYNOPSIS</span></span>
<span data-ttu-id="e5260-103">Uygulama ağ geçidine özel bir hata ekler.</span><span class="sxs-lookup"><span data-stu-id="e5260-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e5260-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5260-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5260-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5260-105">DESCRIPTION</span></span>
<span data-ttu-id="e5260-106">**Add-AzApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidine özel bir hata ekler.</span><span class="sxs-lookup"><span data-stu-id="e5260-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e5260-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5260-107">EXAMPLES</span></span>

### <span data-ttu-id="e5260-108">Örnek 1: uygulama ağ geçidi düzeyine özel hata ekler</span><span class="sxs-lookup"><span data-stu-id="e5260-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e5260-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını ekler ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5260-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="e5260-110">Örnek 2: uygulama ağ geçidi dinleyici düzeyine özel hata ekler</span><span class="sxs-lookup"><span data-stu-id="e5260-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e5260-111">Bu komut, dinleyici düzeyindeki $appgw uygulama ağ geçidi 'ne http durum kodu 502 özel hatasını ekler ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5260-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="e5260-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5260-112">PARAMETERS</span></span>

### <span data-ttu-id="e5260-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5260-113">-ApplicationGateway</span></span>
<span data-ttu-id="e5260-114">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="e5260-114">The Application Gateway</span></span>

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

### <span data-ttu-id="e5260-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e5260-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e5260-116">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="e5260-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e5260-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5260-117">-DefaultProfile</span></span>
<span data-ttu-id="e5260-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5260-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5260-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e5260-119">-StatusCode</span></span>
<span data-ttu-id="e5260-120">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="e5260-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e5260-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5260-121">CommonParameters</span></span>
<span data-ttu-id="e5260-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5260-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5260-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5260-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5260-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5260-124">INPUTS</span></span>

### <span data-ttu-id="e5260-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5260-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5260-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5260-126">OUTPUTS</span></span>

### <span data-ttu-id="e5260-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e5260-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5260-128">NOTES</span></span>

## <span data-ttu-id="e5260-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5260-129">RELATED LINKS</span></span>

[<span data-ttu-id="e5260-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e5260-131">Yeni-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e5260-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e5260-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e5260-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
