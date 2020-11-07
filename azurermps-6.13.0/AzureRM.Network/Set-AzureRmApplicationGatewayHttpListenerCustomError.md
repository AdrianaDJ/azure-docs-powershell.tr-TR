---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761964"
---
# <span data-ttu-id="750d8-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="750d8-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="750d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="750d8-102">SYNOPSIS</span></span>
<span data-ttu-id="750d8-103">Uygulama ağ geçidinin http dinleyicisinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="750d8-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="750d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="750d8-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="750d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="750d8-105">DESCRIPTION</span></span>
<span data-ttu-id="750d8-106">**Set-AzureRmApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinin http dinleyicisinde özel bir hatayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="750d8-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="750d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="750d8-107">EXAMPLES</span></span>

### <span data-ttu-id="750d8-108">Örnek 1: http dinleyicisinde özel bir hatayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="750d8-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="750d8-109">Bu komut, http dinleyicisi $listener 502 özel hatasını güncelleştirir ve güncelleştirilmiş dinleyiciyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="750d8-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="750d8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="750d8-110">PARAMETERS</span></span>

### <span data-ttu-id="750d8-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="750d8-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="750d8-112">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="750d8-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="750d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750d8-113">-DefaultProfile</span></span>
<span data-ttu-id="750d8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="750d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750d8-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="750d8-115">-HttpListener</span></span>
<span data-ttu-id="750d8-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="750d8-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="750d8-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="750d8-117">-StatusCode</span></span>
<span data-ttu-id="750d8-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="750d8-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="750d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750d8-119">CommonParameters</span></span>
<span data-ttu-id="750d8-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="750d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="750d8-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="750d8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750d8-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="750d8-122">INPUTS</span></span>

### <span data-ttu-id="750d8-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="750d8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="750d8-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="750d8-124">OUTPUTS</span></span>

### <span data-ttu-id="750d8-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="750d8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="750d8-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="750d8-126">NOTES</span></span>

## <span data-ttu-id="750d8-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="750d8-127">RELATED LINKS</span></span>
