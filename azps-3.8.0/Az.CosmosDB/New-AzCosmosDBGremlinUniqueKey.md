---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096391"
---
# <span data-ttu-id="b4846-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b4846-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="b4846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4846-102">SYNOPSIS</span></span>
<span data-ttu-id="b4846-103">Yeni bir CosmosDB UniqueKeyPolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4846-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="b4846-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4846-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4846-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4846-105">DESCRIPTION</span></span>
<span data-ttu-id="b4846-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet 'i PSUniqueKeyPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4846-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="b4846-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4846-107">EXAMPLES</span></span>

### <span data-ttu-id="b4846-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4846-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="b4846-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4846-109">PARAMETERS</span></span>

### <span data-ttu-id="b4846-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4846-110">-DefaultProfile</span></span>
<span data-ttu-id="b4846-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4846-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4846-112">-Yol</span><span class="sxs-lookup"><span data-stu-id="b4846-112">-Path</span></span>
<span data-ttu-id="b4846-113">Yol değerleri dizesi dizisi</span><span class="sxs-lookup"><span data-stu-id="b4846-113">Array of string of path values</span></span>

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

### <span data-ttu-id="b4846-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4846-114">CommonParameters</span></span>
<span data-ttu-id="b4846-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4846-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4846-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4846-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4846-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4846-117">INPUTS</span></span>

### <span data-ttu-id="b4846-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4846-118">None</span></span>

## <span data-ttu-id="b4846-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4846-119">OUTPUTS</span></span>

### <span data-ttu-id="b4846-120">Microsoft. Azure. Commands. CosmosDB. modeller. PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="b4846-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="b4846-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4846-121">NOTES</span></span>

## <span data-ttu-id="b4846-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4846-122">RELATED LINKS</span></span>
