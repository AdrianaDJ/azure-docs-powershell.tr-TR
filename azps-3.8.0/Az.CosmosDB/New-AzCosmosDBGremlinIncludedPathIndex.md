---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIncludedPathIndex.md
ms.openlocfilehash: 5d85baaa308b3a0c58f09f40797c3bb2dca4fabe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097563"
---
# <span data-ttu-id="bb3b1-101">New-AzCosmosDBGremlinIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="bb3b1-101">New-AzCosmosDBGremlinIncludedPathIndex</span></span>

## <span data-ttu-id="bb3b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3b1-103">Psındexes türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="bb3b1-104">Set-Azcosmosdbgremlinıncludedpath için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinIncludedPath.</span></span>

## <span data-ttu-id="bb3b1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb3b1-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb3b1-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb3b1-106">DESCRIPTION</span></span>
<span data-ttu-id="bb3b1-107">API 'nin ıncludedpath's Indexes 'a karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-107">Object corresponding to Gremlin API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="bb3b1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb3b1-108">EXAMPLES</span></span>

### <span data-ttu-id="bb3b1-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb3b1-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash

DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="bb3b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb3b1-110">PARAMETERS</span></span>

### <span data-ttu-id="bb3b1-111">-Veri türü</span><span class="sxs-lookup"><span data-stu-id="bb3b1-111">-DataType</span></span>
<span data-ttu-id="bb3b1-112">Dizin oluşturma davranışı uygulandığı veri türü.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="bb3b1-113">Olası değerler: ' dize ', ' sayı ', ' nokta ', ' Çokgen ', ' LineString ', ' MultiPolygon '</span><span class="sxs-lookup"><span data-stu-id="bb3b1-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="bb3b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3b1-114">-DefaultProfile</span></span>
<span data-ttu-id="bb3b1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3b1-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="bb3b1-116">-Kind</span></span>
<span data-ttu-id="bb3b1-117">Dizinin türünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-117">Indicates the type of index.</span></span>
<span data-ttu-id="bb3b1-118">Olası değerler: ' hash ', ' Range ', ' uzamsal '</span><span class="sxs-lookup"><span data-stu-id="bb3b1-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="bb3b1-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="bb3b1-119">-Precision</span></span>
<span data-ttu-id="bb3b1-120">Dizinin duyarlığı.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-120">The precision of the index.</span></span>
<span data-ttu-id="bb3b1-121">-1 en yüksek duyarlığa.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-121">-1 is maximum precision.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb3b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3b1-122">CommonParameters</span></span>
<span data-ttu-id="bb3b1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3b1-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb3b1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3b1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb3b1-125">INPUTS</span></span>

### <span data-ttu-id="bb3b1-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb3b1-126">None</span></span>

## <span data-ttu-id="bb3b1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb3b1-127">OUTPUTS</span></span>

### <span data-ttu-id="bb3b1-128">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexes</span><span class="sxs-lookup"><span data-stu-id="bb3b1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="bb3b1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb3b1-129">NOTES</span></span>

## <span data-ttu-id="bb3b1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb3b1-130">RELATED LINKS</span></span>
