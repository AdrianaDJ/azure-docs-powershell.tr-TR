---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109755"
---
# <span data-ttu-id="2d379-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d379-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="2d379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d379-102">SYNOPSIS</span></span>
<span data-ttu-id="2d379-103">Yeni bir CosmosDB Cassandra küme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d379-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="2d379-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d379-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d379-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d379-105">DESCRIPTION</span></span>
<span data-ttu-id="2d379-106">**New-AzCosmosDBCassandraClusterKey** yeni bir Cosmosdb Cassandra küme anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d379-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="2d379-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d379-107">EXAMPLES</span></span>

### <span data-ttu-id="2d379-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d379-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="2d379-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d379-109">PARAMETERS</span></span>

### <span data-ttu-id="2d379-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d379-110">-DefaultProfile</span></span>
<span data-ttu-id="2d379-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d379-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d379-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d379-112">-Name</span></span>
<span data-ttu-id="2d379-113">Cassandra küme anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="2d379-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="2d379-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2d379-114">-OrderBy</span></span>
<span data-ttu-id="2d379-115">Cassandra küme anahtarının sıralaması.</span><span class="sxs-lookup"><span data-stu-id="2d379-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="2d379-116">Olası değerler: ' ASC ', ' DESC '</span><span class="sxs-lookup"><span data-stu-id="2d379-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="2d379-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d379-117">CommonParameters</span></span>
<span data-ttu-id="2d379-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d379-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d379-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2d379-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d379-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d379-120">INPUTS</span></span>

### <span data-ttu-id="2d379-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2d379-121">None</span></span>

## <span data-ttu-id="2d379-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d379-122">OUTPUTS</span></span>

### <span data-ttu-id="2d379-123">Microsoft. Azure. Commands. CosmosDB. modeller. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d379-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="2d379-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d379-124">NOTES</span></span>

## <span data-ttu-id="2d379-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d379-125">RELATED LINKS</span></span>
