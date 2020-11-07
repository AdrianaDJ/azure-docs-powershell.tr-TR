---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935425"
---
# <span data-ttu-id="3df01-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="3df01-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="3df01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df01-102">SYNOPSIS</span></span>
<span data-ttu-id="3df01-103">Uygulama ağ geçidi için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3df01-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="3df01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3df01-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3df01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3df01-105">DESCRIPTION</span></span>
<span data-ttu-id="3df01-106">**Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet 'i, uygulama ağ geçidi araştırması tarafından kullanılan bir sistem durumu araştırması yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3df01-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="3df01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3df01-107">EXAMPLES</span></span>

### <span data-ttu-id="3df01-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3df01-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="3df01-109">Bu komut, bir parametre olarak ProbeConfig 'e geçirilebilecek bir sağlık yanıtı eşleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3df01-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="3df01-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3df01-110">PARAMETERS</span></span>

### <span data-ttu-id="3df01-111">-Gövde</span><span class="sxs-lookup"><span data-stu-id="3df01-111">-Body</span></span>
<span data-ttu-id="3df01-112">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="3df01-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="3df01-113">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="3df01-113">Default value is empty</span></span>

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

### <span data-ttu-id="3df01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df01-114">-DefaultProfile</span></span>
<span data-ttu-id="3df01-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3df01-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3df01-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3df01-116">-StatusCode</span></span>
<span data-ttu-id="3df01-117">İzin verilen sağlıklı durum kodları aralıkları. Sağlıklı durum kodlarının varsayılan aralığı 200-399</span><span class="sxs-lookup"><span data-stu-id="3df01-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="3df01-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df01-118">CommonParameters</span></span>
<span data-ttu-id="3df01-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3df01-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df01-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df01-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df01-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3df01-121">INPUTS</span></span>

### <span data-ttu-id="3df01-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3df01-122">None</span></span>

## <span data-ttu-id="3df01-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3df01-123">OUTPUTS</span></span>

### <span data-ttu-id="3df01-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="3df01-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="3df01-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3df01-125">NOTES</span></span>

## <span data-ttu-id="3df01-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3df01-126">RELATED LINKS</span></span>

