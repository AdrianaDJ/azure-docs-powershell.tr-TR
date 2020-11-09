---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321578"
---
# <span data-ttu-id="1dcba-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="1dcba-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="1dcba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcba-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcba-103">PSCompositePath türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1dcba-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="1dcba-104">Set-AzCosmosDBGremlinGraph için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="1dcba-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="1dcba-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1dcba-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dcba-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1dcba-106">DESCRIPTION</span></span>
<span data-ttu-id="1dcba-107">Gremlın API 'sinin CompositePath 'e karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="1dcba-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="1dcba-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1dcba-108">EXAMPLES</span></span>

### <span data-ttu-id="1dcba-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1dcba-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="1dcba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1dcba-110">PARAMETERS</span></span>

### <span data-ttu-id="1dcba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcba-111">-DefaultProfile</span></span>
<span data-ttu-id="1dcba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1dcba-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dcba-113">-Düzen</span><span class="sxs-lookup"><span data-stu-id="1dcba-113">-Order</span></span>
<span data-ttu-id="1dcba-114">Bileşik yollar için sıralama düzenini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1dcba-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="1dcba-115">Olası değerler: ' artan ', ' azalan '</span><span class="sxs-lookup"><span data-stu-id="1dcba-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="1dcba-116">-Yol</span><span class="sxs-lookup"><span data-stu-id="1dcba-116">-Path</span></span>
<span data-ttu-id="1dcba-117">Dizin oluşturma davranışının uygulandığı yol.</span><span class="sxs-lookup"><span data-stu-id="1dcba-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="1dcba-118">Dizin yolları genellikle kök ile başlar ve joker karakterle biter (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="1dcba-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="1dcba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcba-119">CommonParameters</span></span>
<span data-ttu-id="1dcba-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1dcba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcba-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1dcba-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcba-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1dcba-122">INPUTS</span></span>

### <span data-ttu-id="1dcba-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1dcba-123">None</span></span>

## <span data-ttu-id="1dcba-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1dcba-124">OUTPUTS</span></span>

### <span data-ttu-id="1dcba-125">Microsoft. Azure. Commands. CosmosDB. modeller. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="1dcba-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="1dcba-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1dcba-126">NOTES</span></span>

## <span data-ttu-id="1dcba-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1dcba-127">RELATED LINKS</span></span>
