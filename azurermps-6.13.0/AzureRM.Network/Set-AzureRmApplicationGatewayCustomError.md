---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590128"
---
# <span data-ttu-id="fb6f1-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="fb6f1-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="fb6f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6f1-103">Uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb6f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb6f1-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb6f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6f1-106">**Set-AzureRmApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="fb6f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb6f1-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6f1-108">Örnek 1: uygulama ağ geçidinde güncelleştirme özel hatası</span><span class="sxs-lookup"><span data-stu-id="fb6f1-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="fb6f1-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını güncelleştirir ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="fb6f1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb6f1-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6f1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb6f1-111">-ApplicationGateway</span></span>
<span data-ttu-id="fb6f1-112">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="fb6f1-112">The Application Gateway</span></span>

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

### <span data-ttu-id="fb6f1-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="fb6f1-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="fb6f1-114">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fb6f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6f1-115">-DefaultProfile</span></span>
<span data-ttu-id="fb6f1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6f1-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="fb6f1-117">-StatusCode</span></span>
<span data-ttu-id="fb6f1-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="fb6f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6f1-119">CommonParameters</span></span>
<span data-ttu-id="fb6f1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb6f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6f1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6f1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6f1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb6f1-122">INPUTS</span></span>

### <span data-ttu-id="fb6f1-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb6f1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb6f1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb6f1-124">OUTPUTS</span></span>

### <span data-ttu-id="fb6f1-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb6f1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb6f1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb6f1-126">NOTES</span></span>

## <span data-ttu-id="fb6f1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb6f1-127">RELATED LINKS</span></span>
