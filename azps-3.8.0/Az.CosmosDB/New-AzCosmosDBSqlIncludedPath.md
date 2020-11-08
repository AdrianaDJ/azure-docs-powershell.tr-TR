---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103641"
---
# <span data-ttu-id="aa3dd-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="aa3dd-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="aa3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3dd-103">Psıncludedpath türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="aa3dd-104">Set-AzCosmosDBSqlContainer için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="aa3dd-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa3dd-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa3dd-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa3dd-106">DESCRIPTION</span></span>
<span data-ttu-id="aa3dd-107">SQL API 'sinin ıncludedpath 'e karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="aa3dd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa3dd-108">EXAMPLES</span></span>

### <span data-ttu-id="aa3dd-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa3dd-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="aa3dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa3dd-110">PARAMETERS</span></span>

### <span data-ttu-id="aa3dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3dd-111">-DefaultProfile</span></span>
<span data-ttu-id="aa3dd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3dd-113">-Index</span><span class="sxs-lookup"><span data-stu-id="aa3dd-113">-Index</span></span>
<span data-ttu-id="aa3dd-114">Bu yolun dizinlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="aa3dd-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3dd-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="aa3dd-115">-Path</span></span>
<span data-ttu-id="aa3dd-116">Dizin oluşturma davranışının uygulandığı yol.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="aa3dd-117">Dizin yolları genellikle kök ile başlar ve joker karakterle biter (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="aa3dd-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="aa3dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3dd-118">CommonParameters</span></span>
<span data-ttu-id="aa3dd-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3dd-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa3dd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3dd-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa3dd-121">INPUTS</span></span>

### <span data-ttu-id="aa3dd-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aa3dd-122">None</span></span>

## <span data-ttu-id="aa3dd-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa3dd-123">OUTPUTS</span></span>

### <span data-ttu-id="aa3dd-124">Microsoft. Azure. Commands. CosmosDB. modeller. Psıncludedpath</span><span class="sxs-lookup"><span data-stu-id="aa3dd-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="aa3dd-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa3dd-125">NOTES</span></span>

## <span data-ttu-id="aa3dd-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa3dd-126">RELATED LINKS</span></span>
