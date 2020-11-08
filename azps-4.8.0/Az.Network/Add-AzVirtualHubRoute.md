---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108943"
---
# <span data-ttu-id="2a166-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2a166-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="2a166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a166-102">SYNOPSIS</span></span>
<span data-ttu-id="2a166-103">Add-AzVirtualHubRouteTable komutuna parametre olarak geçirilebilecek bir VirtualHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a166-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="2a166-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a166-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a166-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a166-105">DESCRIPTION</span></span>
<span data-ttu-id="2a166-106">VirtualHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a166-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="2a166-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a166-107">EXAMPLES</span></span>

### <span data-ttu-id="2a166-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a166-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="2a166-109">Yukarıdaki komut, bir VirtualHubRouteTable kaynağına eklenebilir ve bir VirtualHub 'a ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2a166-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="2a166-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a166-110">PARAMETERS</span></span>

### <span data-ttu-id="2a166-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a166-111">-DefaultProfile</span></span>
<span data-ttu-id="2a166-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a166-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a166-113">-Hedef</span><span class="sxs-lookup"><span data-stu-id="2a166-113">-Destination</span></span>
<span data-ttu-id="2a166-114">Hedef listesi.</span><span class="sxs-lookup"><span data-stu-id="2a166-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a166-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="2a166-115">-DestinationType</span></span>
<span data-ttu-id="2a166-116">Hedef türü.</span><span class="sxs-lookup"><span data-stu-id="2a166-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="2a166-117">-Sonraki</span><span class="sxs-lookup"><span data-stu-id="2a166-117">-NextHop</span></span>
<span data-ttu-id="2a166-118">Sonraki atlamalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="2a166-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a166-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="2a166-119">-NextHopType</span></span>
<span data-ttu-id="2a166-120">Sonraki atlama türü.</span><span class="sxs-lookup"><span data-stu-id="2a166-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="2a166-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a166-121">CommonParameters</span></span>
<span data-ttu-id="2a166-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a166-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a166-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a166-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a166-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a166-124">INPUTS</span></span>

### <span data-ttu-id="2a166-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a166-125">None</span></span>

## <span data-ttu-id="2a166-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a166-126">OUTPUTS</span></span>

### <span data-ttu-id="2a166-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2a166-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="2a166-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a166-128">NOTES</span></span>

## <span data-ttu-id="2a166-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a166-129">RELATED LINKS</span></span>
