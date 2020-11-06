---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588058"
---
# <span data-ttu-id="568f6-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="568f6-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="568f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568f6-102">SYNOPSIS</span></span>
<span data-ttu-id="568f6-103">Uygulama ağ geçidi 'nin http dinleyicisinde özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="568f6-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="568f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="568f6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="568f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="568f6-105">DESCRIPTION</span></span>
<span data-ttu-id="568f6-106">**Remove-AzureRmApplicationGatewayCustomError** cmdlet 'i, uygulama ağ geçidinin http dinleyicisinde özel bir hatayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="568f6-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="568f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="568f6-107">EXAMPLES</span></span>

### <span data-ttu-id="568f6-108">Örnek 1: http dinleyicisinin özel hatasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="568f6-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="568f6-109">Bu komut http dinleyici $listener 502 özel hatasını kaldırır ve güncelleştirilmiş dinleyiciyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="568f6-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="568f6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="568f6-110">PARAMETERS</span></span>

### <span data-ttu-id="568f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568f6-111">-DefaultProfile</span></span>
<span data-ttu-id="568f6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="568f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="568f6-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="568f6-113">-HttpListener</span></span>
<span data-ttu-id="568f6-114">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="568f6-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="568f6-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="568f6-115">-StatusCode</span></span>
<span data-ttu-id="568f6-116">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="568f6-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="568f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568f6-117">CommonParameters</span></span>
<span data-ttu-id="568f6-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="568f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="568f6-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="568f6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568f6-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="568f6-120">INPUTS</span></span>

### <span data-ttu-id="568f6-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="568f6-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="568f6-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="568f6-122">OUTPUTS</span></span>

### <span data-ttu-id="568f6-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="568f6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="568f6-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="568f6-124">NOTES</span></span>

## <span data-ttu-id="568f6-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="568f6-125">RELATED LINKS</span></span>
