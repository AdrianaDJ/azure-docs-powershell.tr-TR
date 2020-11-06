---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590178"
---
# <span data-ttu-id="88d84-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="88d84-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="88d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88d84-102">SYNOPSIS</span></span>
<span data-ttu-id="88d84-103">Uygulama ağ geçidi 'nin http dinleyicisinde özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="88d84-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88d84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88d84-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88d84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88d84-105">DESCRIPTION</span></span>
<span data-ttu-id="88d84-106">**Get-AzureRmApplicationGatewayCustomError** cmdlet 'i, bir uygulama ağ geçidinin http dinleyicisinde özel hatalar alır.</span><span class="sxs-lookup"><span data-stu-id="88d84-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="88d84-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88d84-107">EXAMPLES</span></span>

### <span data-ttu-id="88d84-108">Örnek 1: http dinleyicisinde özel hata alır</span><span class="sxs-lookup"><span data-stu-id="88d84-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="88d84-109">Bu komut HTTP dinleyicisinin $listener 502 http dinleyicisi özel hatasını alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="88d84-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="88d84-110">Örnek 2: http dinleyicisinde tüm özel hataların listesini alır</span><span class="sxs-lookup"><span data-stu-id="88d84-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="88d84-111">Bu komut, http dinleyici $listener tüm özel hataların listesini alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="88d84-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="88d84-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88d84-112">PARAMETERS</span></span>

### <span data-ttu-id="88d84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d84-113">-DefaultProfile</span></span>
<span data-ttu-id="88d84-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88d84-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88d84-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="88d84-115">-HttpListener</span></span>
<span data-ttu-id="88d84-116">Uygulama ağ geçidi http dinleyicisi</span><span class="sxs-lookup"><span data-stu-id="88d84-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="88d84-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="88d84-117">-StatusCode</span></span>
<span data-ttu-id="88d84-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="88d84-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88d84-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d84-119">CommonParameters</span></span>
<span data-ttu-id="88d84-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88d84-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88d84-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d84-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d84-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88d84-122">INPUTS</span></span>

### <span data-ttu-id="88d84-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88d84-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="88d84-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88d84-124">OUTPUTS</span></span>

### <span data-ttu-id="88d84-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="88d84-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="88d84-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88d84-126">NOTES</span></span>

## <span data-ttu-id="88d84-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88d84-127">RELATED LINKS</span></span>
