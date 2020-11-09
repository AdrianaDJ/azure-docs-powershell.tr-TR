---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321590"
---
# <span data-ttu-id="56322-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="56322-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="56322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56322-102">SYNOPSIS</span></span>
<span data-ttu-id="56322-103">Yeni bir CosmosDB Cassandra sütunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56322-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="56322-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56322-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56322-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56322-105">DESCRIPTION</span></span>
<span data-ttu-id="56322-106">**New-AzCosmosDBCassandraColumn** yeni bir Cosmosdb Cassandra sütunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56322-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="56322-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56322-107">EXAMPLES</span></span>

### <span data-ttu-id="56322-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56322-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="56322-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56322-109">PARAMETERS</span></span>

### <span data-ttu-id="56322-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56322-110">-DefaultProfile</span></span>
<span data-ttu-id="56322-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56322-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56322-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="56322-112">-Name</span></span>
<span data-ttu-id="56322-113">Cassandra sütununun adı.</span><span class="sxs-lookup"><span data-stu-id="56322-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="56322-114">-Tür</span><span class="sxs-lookup"><span data-stu-id="56322-114">-Type</span></span>
<span data-ttu-id="56322-115">Cassandra sütunu türü.</span><span class="sxs-lookup"><span data-stu-id="56322-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="56322-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56322-116">CommonParameters</span></span>
<span data-ttu-id="56322-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56322-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56322-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56322-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56322-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56322-119">INPUTS</span></span>

### <span data-ttu-id="56322-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="56322-120">None</span></span>

## <span data-ttu-id="56322-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56322-121">OUTPUTS</span></span>

### <span data-ttu-id="56322-122">Microsoft. Azure. Commands. CosmosDB. modeller. PSColumn</span><span class="sxs-lookup"><span data-stu-id="56322-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="56322-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56322-123">NOTES</span></span>

## <span data-ttu-id="56322-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56322-124">RELATED LINKS</span></span>
