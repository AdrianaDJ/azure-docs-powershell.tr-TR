---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096886"
---
# <span data-ttu-id="f1f46-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f1f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f46-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f46-103">Uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1f46-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f1f46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1f46-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1f46-105">DESCRIPTION</span></span>
<span data-ttu-id="f1f46-106">**Set-AzApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1f46-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="f1f46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1f46-107">EXAMPLES</span></span>

### <span data-ttu-id="f1f46-108">Örnek 1: uygulama ağ geçidinde güncelleştirme özel hatası</span><span class="sxs-lookup"><span data-stu-id="f1f46-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="f1f46-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını güncelleştirir ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1f46-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="f1f46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1f46-110">PARAMETERS</span></span>

### <span data-ttu-id="f1f46-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1f46-111">-ApplicationGateway</span></span>
<span data-ttu-id="f1f46-112">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="f1f46-112">The Application Gateway</span></span>

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

### <span data-ttu-id="f1f46-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f1f46-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f1f46-114">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="f1f46-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f1f46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f46-115">-DefaultProfile</span></span>
<span data-ttu-id="f1f46-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1f46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f46-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1f46-117">-StatusCode</span></span>
<span data-ttu-id="f1f46-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="f1f46-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="f1f46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f46-119">CommonParameters</span></span>
<span data-ttu-id="f1f46-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1f46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f46-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f46-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f46-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1f46-122">INPUTS</span></span>

### <span data-ttu-id="f1f46-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1f46-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1f46-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1f46-124">OUTPUTS</span></span>

### <span data-ttu-id="f1f46-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f1f46-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1f46-126">NOTES</span></span>

## <span data-ttu-id="f1f46-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1f46-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1f46-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1f46-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1f46-130">Yeni-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f1f46-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f1f46-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
