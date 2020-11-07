---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: c98d36e7f08d16f12581c340b875e26f5a393f1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931929"
---
# <span data-ttu-id="eaa46-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="eaa46-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="eaa46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa46-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa46-103">Uygulama ağ geçidi için sistem durumu araştırması tarafından kullanılan bir sistem durumu araştırma yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaa46-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="eaa46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaa46-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaa46-105">DESCRIPTION</span></span>
<span data-ttu-id="eaa46-106">**Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet 'i, uygulama ağ geçidi araştırması tarafından kullanılan bir sistem durumu araştırması yanıtı eşleştirmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaa46-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="eaa46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaa46-107">EXAMPLES</span></span>

### <span data-ttu-id="eaa46-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eaa46-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="eaa46-109">Bu komut, bir parametre olarak ProbeConfig 'e geçirilebilecek bir sağlık yanıtı eşleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaa46-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="eaa46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaa46-110">PARAMETERS</span></span>

### <span data-ttu-id="eaa46-111">-Gövde</span><span class="sxs-lookup"><span data-stu-id="eaa46-111">-Body</span></span>
<span data-ttu-id="eaa46-112">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="eaa46-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="eaa46-113">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="eaa46-113">Default value is empty</span></span>

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

### <span data-ttu-id="eaa46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa46-114">-DefaultProfile</span></span>
<span data-ttu-id="eaa46-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eaa46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaa46-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="eaa46-116">-StatusCode</span></span>
<span data-ttu-id="eaa46-117">İzin verilen sağlıklı durum kodları aralıkları. Sağlıklı durum kodlarının varsayılan aralığı 200-399</span><span class="sxs-lookup"><span data-stu-id="eaa46-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="eaa46-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa46-118">CommonParameters</span></span>
<span data-ttu-id="eaa46-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaa46-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa46-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa46-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa46-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaa46-121">INPUTS</span></span>

### <span data-ttu-id="eaa46-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eaa46-122">None</span></span>

## <span data-ttu-id="eaa46-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaa46-123">OUTPUTS</span></span>

### <span data-ttu-id="eaa46-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="eaa46-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="eaa46-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaa46-125">NOTES</span></span>

## <span data-ttu-id="eaa46-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaa46-126">RELATED LINKS</span></span>
