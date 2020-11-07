---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
ms.openlocfilehash: 8781b52c3ed50a2a533b90815f1637ebcfe6df52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938789"
---
# <span data-ttu-id="7afda-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7afda-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7afda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7afda-102">SYNOPSIS</span></span>
<span data-ttu-id="7afda-103">Uygulama ağ geçidi için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7afda-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7afda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7afda-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7afda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7afda-105">DESCRIPTION</span></span>
<span data-ttu-id="7afda-106">**Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet 'i, uygulama ağ geçidi Için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7afda-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="7afda-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7afda-107">EXAMPLES</span></span>

### <span data-ttu-id="7afda-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7afda-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="7afda-109">Bu komut, bir parametre olarak ProbeConfig 'e geçirilebilecek bir sağlık yanıtı eşleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7afda-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="7afda-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7afda-110">PARAMETERS</span></span>

### <span data-ttu-id="7afda-111">-Gövde</span><span class="sxs-lookup"><span data-stu-id="7afda-111">-Body</span></span>
<span data-ttu-id="7afda-112">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="7afda-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="7afda-113">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="7afda-113">Default value is empty</span></span>

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

### <span data-ttu-id="7afda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afda-114">-DefaultProfile</span></span>
<span data-ttu-id="7afda-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7afda-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7afda-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7afda-116">-StatusCode</span></span>
<span data-ttu-id="7afda-117">İzin verilen sağlıklı durum kodları aralıkları. Sağlıklı durum kodlarının varsayılan aralığı 200-399</span><span class="sxs-lookup"><span data-stu-id="7afda-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="7afda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afda-118">CommonParameters</span></span>
<span data-ttu-id="7afda-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7afda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afda-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7afda-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afda-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7afda-121">INPUTS</span></span>

### <span data-ttu-id="7afda-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7afda-122">None</span></span>

## <span data-ttu-id="7afda-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7afda-123">OUTPUTS</span></span>

### <span data-ttu-id="7afda-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7afda-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7afda-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7afda-125">NOTES</span></span>

## <span data-ttu-id="7afda-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7afda-126">RELATED LINKS</span></span>

