---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764355"
---
# <span data-ttu-id="30b3f-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="30b3f-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="30b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="30b3f-103">Uygulama ağ geçidinin http dinleyicisine özel hata ekler.</span><span class="sxs-lookup"><span data-stu-id="30b3f-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30b3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30b3f-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30b3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="30b3f-106">**Add-AzureRmApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinin http dinleyicisine özel bir hata ekler.</span><span class="sxs-lookup"><span data-stu-id="30b3f-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="30b3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="30b3f-108">Örnek 1: http dinleyici düzeyine özel hata ekler</span><span class="sxs-lookup"><span data-stu-id="30b3f-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="30b3f-109">Bu komut http dinleyicisi $listener olarak http dinleyicisi için özel bir hata 502.</span><span class="sxs-lookup"><span data-stu-id="30b3f-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="30b3f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30b3f-110">PARAMETERS</span></span>

### <span data-ttu-id="30b3f-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="30b3f-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="30b3f-112">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="30b3f-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="30b3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b3f-113">-DefaultProfile</span></span>
<span data-ttu-id="30b3f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30b3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30b3f-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="30b3f-115">-HttpListener</span></span>
<span data-ttu-id="30b3f-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="30b3f-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="30b3f-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="30b3f-117">-StatusCode</span></span>
<span data-ttu-id="30b3f-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="30b3f-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="30b3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b3f-119">CommonParameters</span></span>
<span data-ttu-id="30b3f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30b3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="30b3f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30b3f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b3f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30b3f-122">INPUTS</span></span>

### <span data-ttu-id="30b3f-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30b3f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="30b3f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30b3f-124">OUTPUTS</span></span>

### <span data-ttu-id="30b3f-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="30b3f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="30b3f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30b3f-126">NOTES</span></span>

## <span data-ttu-id="30b3f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30b3f-127">RELATED LINKS</span></span>
