---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275089"
---
# <span data-ttu-id="b82fe-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="b82fe-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="b82fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b82fe-103">PSCompositePath türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b82fe-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="b82fe-104">Set-AzCosmosDBSqlContainer için parametre değeri olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="b82fe-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="b82fe-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b82fe-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82fe-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="b82fe-106">DESCRIPTION</span></span>
<span data-ttu-id="b82fe-107">SQL API 'nın CompositePath 'e karşılık gelen nesne.</span><span class="sxs-lookup"><span data-stu-id="b82fe-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="b82fe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b82fe-108">EXAMPLES</span></span>

### <span data-ttu-id="b82fe-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b82fe-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="b82fe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b82fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b82fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82fe-111">-DefaultProfile</span></span>
<span data-ttu-id="b82fe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b82fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b82fe-113">-Düzen</span><span class="sxs-lookup"><span data-stu-id="b82fe-113">-Order</span></span>
<span data-ttu-id="b82fe-114">Bileşik yollar için sıralama düzenini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b82fe-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="b82fe-115">Olası değerler: ' artan ', ' azalan '</span><span class="sxs-lookup"><span data-stu-id="b82fe-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="b82fe-116">-Yol</span><span class="sxs-lookup"><span data-stu-id="b82fe-116">-Path</span></span>
<span data-ttu-id="b82fe-117">Dizin oluşturma davranışının uygulandığı yol.</span><span class="sxs-lookup"><span data-stu-id="b82fe-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="b82fe-118">Dizin yolları genellikle kök ile başlar ve joker karakterle biter (/path/\*)</span><span class="sxs-lookup"><span data-stu-id="b82fe-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="b82fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82fe-119">CommonParameters</span></span>
<span data-ttu-id="b82fe-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b82fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82fe-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b82fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82fe-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b82fe-122">INPUTS</span></span>

### <span data-ttu-id="b82fe-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b82fe-123">None</span></span>

## <span data-ttu-id="b82fe-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b82fe-124">OUTPUTS</span></span>

### <span data-ttu-id="b82fe-125">Microsoft. Azure. Commands. CosmosDB. modeller. PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="b82fe-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="b82fe-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b82fe-126">NOTES</span></span>

## <span data-ttu-id="b82fe-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b82fe-127">RELATED LINKS</span></span>
