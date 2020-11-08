---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278519"
---
# <span data-ttu-id="8ec67-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8ec67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec67-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec67-103">Uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8ec67-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="8ec67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ec67-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ec67-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec67-106">**Set-AzApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8ec67-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="8ec67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ec67-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec67-108">Örnek 1: uygulama ağ geçidinde güncelleştirme özel hatası</span><span class="sxs-lookup"><span data-stu-id="8ec67-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="8ec67-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını güncelleştirir ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ec67-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="8ec67-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ec67-110">PARAMETERS</span></span>

### <span data-ttu-id="8ec67-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ec67-111">-ApplicationGateway</span></span>
<span data-ttu-id="8ec67-112">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="8ec67-112">The Application Gateway</span></span>

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

### <span data-ttu-id="8ec67-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="8ec67-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="8ec67-114">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="8ec67-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8ec67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec67-115">-DefaultProfile</span></span>
<span data-ttu-id="8ec67-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ec67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec67-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8ec67-117">-StatusCode</span></span>
<span data-ttu-id="8ec67-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="8ec67-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8ec67-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec67-119">CommonParameters</span></span>
<span data-ttu-id="8ec67-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ec67-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec67-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec67-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec67-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ec67-122">INPUTS</span></span>

### <span data-ttu-id="8ec67-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ec67-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ec67-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ec67-124">OUTPUTS</span></span>

### <span data-ttu-id="8ec67-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8ec67-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ec67-126">NOTES</span></span>

## <span data-ttu-id="8ec67-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ec67-127">RELATED LINKS</span></span>

[<span data-ttu-id="8ec67-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8ec67-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8ec67-130">Yeni-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8ec67-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8ec67-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
