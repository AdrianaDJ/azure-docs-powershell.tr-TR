---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpathindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPathIndex.md
ms.openlocfilehash: f6bd378ac39c0e00975616b08d3bb9c14358d5d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274625"
---
# <span data-ttu-id="ddfa6-101">New-AzCosmosDBSqlIncludedPathIndex</span><span class="sxs-lookup"><span data-stu-id="ddfa6-101">New-AzCosmosDBSqlIncludedPathIndex</span></span>

## <span data-ttu-id="ddfa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfa6-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfa6-103">Psındexes türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-103">Creates a new object of type PSIndexes.</span></span> <span data-ttu-id="ddfa6-104">Set-Azcosmosdbsqlıncludedpath için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIncludedPath.</span></span>

## <span data-ttu-id="ddfa6-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddfa6-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPathIndex -DataType <String> [-Precision <Int32>] -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddfa6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddfa6-106">DESCRIPTION</span></span>
<span data-ttu-id="ddfa6-107">SQL API 'sinin ıncludedpath'in dizinlerine karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-107">Object corresponding to Sql API's IncludedPath's Indexes.</span></span>

## <span data-ttu-id="ddfa6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddfa6-108">EXAMPLES</span></span>

### <span data-ttu-id="ddfa6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ddfa6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
DataType Precision Kind
-------- --------- ----
String          -1 Hash
```

## <span data-ttu-id="ddfa6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddfa6-110">PARAMETERS</span></span>

### <span data-ttu-id="ddfa6-111">-Veri türü</span><span class="sxs-lookup"><span data-stu-id="ddfa6-111">-DataType</span></span>
<span data-ttu-id="ddfa6-112">Dizin oluşturma davranışı uygulandığı veri türü.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-112">Datatype for which the indexing behavior is applied to.</span></span>
<span data-ttu-id="ddfa6-113">Olası değerler: ' dize ', ' sayı ', ' nokta ', ' Çokgen ', ' LineString ', ' MultiPolygon '</span><span class="sxs-lookup"><span data-stu-id="ddfa6-113">Possible values include: 'String', 'Number', 'Point', 'Polygon', 'LineString', 'MultiPolygon'</span></span>

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

### <span data-ttu-id="ddfa6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfa6-114">-DefaultProfile</span></span>
<span data-ttu-id="ddfa6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddfa6-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="ddfa6-116">-Kind</span></span>
<span data-ttu-id="ddfa6-117">Dizinin türünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-117">Indicates the type of index.</span></span>
<span data-ttu-id="ddfa6-118">Olası değerler: ' hash ', ' Range ', ' uzamsal '</span><span class="sxs-lookup"><span data-stu-id="ddfa6-118">Possible values include: 'Hash', 'Range', 'Spatial'</span></span>

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

### <span data-ttu-id="ddfa6-119">-Precision</span><span class="sxs-lookup"><span data-stu-id="ddfa6-119">-Precision</span></span>
<span data-ttu-id="ddfa6-120">Dizinin duyarlığı.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-120">The precision of the index.</span></span>
<span data-ttu-id="ddfa6-121">-1 en yüksek duyarlığa.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-121">-1 is maximum precision.</span></span>

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

### <span data-ttu-id="ddfa6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfa6-122">CommonParameters</span></span>
<span data-ttu-id="ddfa6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfa6-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddfa6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfa6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddfa6-125">INPUTS</span></span>

### <span data-ttu-id="ddfa6-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ddfa6-126">None</span></span>

## <span data-ttu-id="ddfa6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddfa6-127">OUTPUTS</span></span>

### <span data-ttu-id="ddfa6-128">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexes</span><span class="sxs-lookup"><span data-stu-id="ddfa6-128">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes</span></span>

## <span data-ttu-id="ddfa6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddfa6-129">NOTES</span></span>

## <span data-ttu-id="ddfa6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddfa6-130">RELATED LINKS</span></span>
