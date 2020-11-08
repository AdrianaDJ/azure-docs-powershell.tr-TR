---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274390"
---
# <span data-ttu-id="f25d7-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f25d7-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f25d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f25d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f25d7-103">Uygulama ağ geçidi için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f25d7-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="f25d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f25d7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f25d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f25d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f25d7-106">**Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet 'i, uygulama ağ geçidi araştırması tarafından kullanılan bir sistem durumu araştırması yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f25d7-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="f25d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f25d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f25d7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f25d7-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="f25d7-109">Bu komut, bir parametre olarak ProbeConfig 'e geçirilebilecek bir sağlık yanıtı eşleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f25d7-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="f25d7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f25d7-110">PARAMETERS</span></span>

### <span data-ttu-id="f25d7-111">-Gövde</span><span class="sxs-lookup"><span data-stu-id="f25d7-111">-Body</span></span>
<span data-ttu-id="f25d7-112">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="f25d7-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f25d7-113">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="f25d7-113">Default value is empty</span></span>

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

### <span data-ttu-id="f25d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25d7-114">-DefaultProfile</span></span>
<span data-ttu-id="f25d7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f25d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f25d7-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f25d7-116">-StatusCode</span></span>
<span data-ttu-id="f25d7-117">İzin verilen sağlıklı durum kodları aralıkları. Sağlıklı durum kodlarının varsayılan aralığı 200-399</span><span class="sxs-lookup"><span data-stu-id="f25d7-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f25d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25d7-118">CommonParameters</span></span>
<span data-ttu-id="f25d7-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f25d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25d7-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f25d7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25d7-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f25d7-121">INPUTS</span></span>

### <span data-ttu-id="f25d7-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f25d7-122">None</span></span>

## <span data-ttu-id="f25d7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f25d7-123">OUTPUTS</span></span>

### <span data-ttu-id="f25d7-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f25d7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f25d7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f25d7-125">NOTES</span></span>

## <span data-ttu-id="f25d7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f25d7-126">RELATED LINKS</span></span>
