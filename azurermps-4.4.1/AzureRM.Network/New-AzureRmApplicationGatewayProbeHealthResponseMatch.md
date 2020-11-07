---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 6b54c300eb6e37544246b785fe30b2a3dcb67b9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764048"
---
# <span data-ttu-id="13e12-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="13e12-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="13e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e12-102">SYNOPSIS</span></span>
<span data-ttu-id="13e12-103">Uygulama ağ geçidi için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13e12-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13e12-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13e12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="13e12-105">DESCRIPTION</span></span>
<span data-ttu-id="13e12-106">**Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet 'i, uygulama ağ geçidi Için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13e12-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="13e12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13e12-107">EXAMPLES</span></span>

### <span data-ttu-id="13e12-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13e12-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="13e12-109">Bu komut, bir parametre olarak ProbeConfig 'e geçirilebilecek bir sağlık yanıtı eşleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13e12-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="13e12-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13e12-110">PARAMETERS</span></span>

### <span data-ttu-id="13e12-111">-Gövde</span><span class="sxs-lookup"><span data-stu-id="13e12-111">-Body</span></span>
<span data-ttu-id="13e12-112">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="13e12-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="13e12-113">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="13e12-113">Default value is empty</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e12-114">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="13e12-114">-StatusCode</span></span>
<span data-ttu-id="13e12-115">İzin verilen sağlıklı durum kodları aralıkları. Sağlıklı durum kodlarının varsayılan aralığı 200-399</span><span class="sxs-lookup"><span data-stu-id="13e12-115">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e12-116">-DefaultProfile</span></span>
<span data-ttu-id="13e12-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13e12-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13e12-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e12-118">CommonParameters</span></span>
<span data-ttu-id="13e12-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13e12-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e12-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e12-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e12-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13e12-121">INPUTS</span></span>

### <span data-ttu-id="13e12-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="13e12-122">None</span></span>

## <span data-ttu-id="13e12-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13e12-123">OUTPUTS</span></span>

### <span data-ttu-id="13e12-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="13e12-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="13e12-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13e12-125">NOTES</span></span>

## <span data-ttu-id="13e12-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13e12-126">RELATED LINKS</span></span>
