---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlspatialspec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlSpatialSpec.md
ms.openlocfilehash: 0d205c7de9f4515c153f3662d3fededee48793eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274620"
---
# <span data-ttu-id="13ab6-101">New-AzCosmosDBSqlSpatialSpec</span><span class="sxs-lookup"><span data-stu-id="13ab6-101">New-AzCosmosDBSqlSpatialSpec</span></span>

## <span data-ttu-id="13ab6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="13ab6-103">Psshaalspec türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13ab6-103">Creates a new object of type PSSpatialSpec.</span></span> <span data-ttu-id="13ab6-104">Set-AzCosmosDBSqlIndexingPolicy için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="13ab6-104">It can be passed as a parameter value for Set-AzCosmosDBSqlIndexingPolicy.</span></span>

## <span data-ttu-id="13ab6-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13ab6-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlSpatialSpec -Path <String> -Type <String[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ab6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="13ab6-106">DESCRIPTION</span></span>
<span data-ttu-id="13ab6-107">SQL API 'sinin SpatialSpec 'e karşılık gelen nesneyi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13ab6-107">Creates Object corresponding to Sql API's SpatialSpec.</span></span>

## <span data-ttu-id="13ab6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13ab6-108">EXAMPLES</span></span>

### <span data-ttu-id="13ab6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13ab6-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlSpatialSpec -Path "/abc" -Type String
Path Types
---- -----
/abc {String}
```

## <span data-ttu-id="13ab6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13ab6-110">PARAMETERS</span></span>

### <span data-ttu-id="13ab6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ab6-111">-DefaultProfile</span></span>
<span data-ttu-id="13ab6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13ab6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ab6-113">-Yol</span><span class="sxs-lookup"><span data-stu-id="13ab6-113">-Path</span></span>
<span data-ttu-id="13ab6-114">JSON belgesinde dizine eklenecek yol.</span><span class="sxs-lookup"><span data-stu-id="13ab6-114">Path in JSON document to index.</span></span>

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

### <span data-ttu-id="13ab6-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="13ab6-115">-Type</span></span>
<span data-ttu-id="13ab6-116">Kabul edilebilir değerler içeren dizeler dizisi: nokta, LineString, Çokgen, MultiPolygon.</span><span class="sxs-lookup"><span data-stu-id="13ab6-116">Array of strings with acceptable values: Point, LineString, Polygon, MultiPolygon.</span></span>
<span data-ttu-id="13ab6-117">Yolların uzamsal türünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="13ab6-117">Represent's paths spatial type.</span></span>

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

### <span data-ttu-id="13ab6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ab6-118">CommonParameters</span></span>
<span data-ttu-id="13ab6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13ab6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ab6-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="13ab6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ab6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13ab6-121">INPUTS</span></span>

### <span data-ttu-id="13ab6-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="13ab6-122">None</span></span>

## <span data-ttu-id="13ab6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13ab6-123">OUTPUTS</span></span>

### <span data-ttu-id="13ab6-124">Microsoft. Azure. Commands. CosmosDB. modeller. Psshaalspec</span><span class="sxs-lookup"><span data-stu-id="13ab6-124">Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec</span></span>

## <span data-ttu-id="13ab6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13ab6-125">NOTES</span></span>

## <span data-ttu-id="13ab6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13ab6-126">RELATED LINKS</span></span>
