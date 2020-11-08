---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103631"
---
# <span data-ttu-id="827a2-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="827a2-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="827a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="827a2-102">SYNOPSIS</span></span>
<span data-ttu-id="827a2-103">Yeni bir CosmosDB SqlUniqueKeyPolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="827a2-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="827a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="827a2-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="827a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="827a2-105">DESCRIPTION</span></span>
<span data-ttu-id="827a2-106">**New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet 'i PSSqlUniqueKeyPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="827a2-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="827a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="827a2-107">EXAMPLES</span></span>

### <span data-ttu-id="827a2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="827a2-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="827a2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="827a2-109">PARAMETERS</span></span>

### <span data-ttu-id="827a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827a2-110">-DefaultProfile</span></span>
<span data-ttu-id="827a2-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="827a2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="827a2-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="827a2-112">-UniqueKey</span></span>
<span data-ttu-id="827a2-113">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="827a2-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827a2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827a2-114">CommonParameters</span></span>
<span data-ttu-id="827a2-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="827a2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827a2-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="827a2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827a2-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="827a2-117">INPUTS</span></span>

### <span data-ttu-id="827a2-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="827a2-118">None</span></span>

## <span data-ttu-id="827a2-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="827a2-119">OUTPUTS</span></span>

### <span data-ttu-id="827a2-120">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="827a2-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="827a2-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="827a2-121">NOTES</span></span>

## <span data-ttu-id="827a2-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="827a2-122">RELATED LINKS</span></span>
