---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268343"
---
# <span data-ttu-id="f9518-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f9518-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="f9518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9518-102">SYNOPSIS</span></span>
<span data-ttu-id="f9518-103">Yeni bir CosmosDB SqlUniqueKeyPolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9518-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="f9518-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9518-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9518-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9518-105">DESCRIPTION</span></span>
<span data-ttu-id="f9518-106">**New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet 'i PSSqlUniqueKeyPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9518-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="f9518-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9518-107">EXAMPLES</span></span>

### <span data-ttu-id="f9518-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9518-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="f9518-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9518-109">PARAMETERS</span></span>

### <span data-ttu-id="f9518-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9518-110">-DefaultProfile</span></span>
<span data-ttu-id="f9518-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9518-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9518-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="f9518-112">-UniqueKey</span></span>
<span data-ttu-id="f9518-113">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="f9518-113">Database name.</span></span>

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

### <span data-ttu-id="f9518-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9518-114">CommonParameters</span></span>
<span data-ttu-id="f9518-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9518-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9518-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f9518-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9518-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9518-117">INPUTS</span></span>

### <span data-ttu-id="f9518-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f9518-118">None</span></span>

## <span data-ttu-id="f9518-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9518-119">OUTPUTS</span></span>

### <span data-ttu-id="f9518-120">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="f9518-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="f9518-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9518-121">NOTES</span></span>

## <span data-ttu-id="f9518-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9518-122">RELATED LINKS</span></span>
