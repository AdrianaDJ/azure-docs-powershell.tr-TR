---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098019"
---
# <span data-ttu-id="ff77b-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ff77b-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="ff77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff77b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff77b-103">Add-AzVirtualHubRouteTable komutuna parametre olarak geçirilebilecek bir VirtualHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff77b-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="ff77b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff77b-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff77b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff77b-105">DESCRIPTION</span></span>
<span data-ttu-id="ff77b-106">VirtualHubRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff77b-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="ff77b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff77b-107">EXAMPLES</span></span>

### <span data-ttu-id="ff77b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff77b-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="ff77b-109">Yukarıdaki komut, bir VirtualHubRouteTable kaynağına eklenebilir ve bir VirtualHub 'a ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ff77b-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="ff77b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff77b-110">PARAMETERS</span></span>

### <span data-ttu-id="ff77b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff77b-111">-DefaultProfile</span></span>
<span data-ttu-id="ff77b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff77b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff77b-113">-Hedef</span><span class="sxs-lookup"><span data-stu-id="ff77b-113">-Destination</span></span>
<span data-ttu-id="ff77b-114">Hedef listesi.</span><span class="sxs-lookup"><span data-stu-id="ff77b-114">List of Destinations.</span></span>

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

### <span data-ttu-id="ff77b-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="ff77b-115">-DestinationType</span></span>
<span data-ttu-id="ff77b-116">Hedef türü.</span><span class="sxs-lookup"><span data-stu-id="ff77b-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="ff77b-117">-Sonraki</span><span class="sxs-lookup"><span data-stu-id="ff77b-117">-NextHop</span></span>
<span data-ttu-id="ff77b-118">Sonraki atlamalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="ff77b-118">List of Next hops.</span></span>

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

### <span data-ttu-id="ff77b-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="ff77b-119">-NextHopType</span></span>
<span data-ttu-id="ff77b-120">Sonraki atlama türü.</span><span class="sxs-lookup"><span data-stu-id="ff77b-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="ff77b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff77b-121">CommonParameters</span></span>
<span data-ttu-id="ff77b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff77b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff77b-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff77b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff77b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff77b-124">INPUTS</span></span>

### <span data-ttu-id="ff77b-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ff77b-125">None</span></span>

## <span data-ttu-id="ff77b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff77b-126">OUTPUTS</span></span>

### <span data-ttu-id="ff77b-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="ff77b-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="ff77b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff77b-128">NOTES</span></span>

## <span data-ttu-id="ff77b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff77b-129">RELATED LINKS</span></span>
