---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321585"
---
# <span data-ttu-id="99121-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="99121-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="99121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99121-102">SYNOPSIS</span></span>
<span data-ttu-id="99121-103">Yeni bir CosmosDB Cassandra şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99121-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="99121-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99121-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99121-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99121-105">DESCRIPTION</span></span>
<span data-ttu-id="99121-106">**New-AzCosmosDBCassandraSchema** , yeni bir Cosmosdb Cassandra şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99121-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="99121-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99121-107">EXAMPLES</span></span>

### <span data-ttu-id="99121-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99121-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="99121-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99121-109">PARAMETERS</span></span>

### <span data-ttu-id="99121-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="99121-110">-ClusterKey</span></span>
<span data-ttu-id="99121-111">PSClusterKey nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="99121-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99121-112">Sütunlu</span><span class="sxs-lookup"><span data-stu-id="99121-112">-Column</span></span>
<span data-ttu-id="99121-113">PSColumn nesnesi.</span><span class="sxs-lookup"><span data-stu-id="99121-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99121-114">-DefaultProfile</span></span>
<span data-ttu-id="99121-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99121-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99121-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="99121-116">-PartitionKey</span></span>
<span data-ttu-id="99121-117">Bölüm anahtarlarını içeren dizeler dizisi.</span><span class="sxs-lookup"><span data-stu-id="99121-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99121-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99121-118">CommonParameters</span></span>
<span data-ttu-id="99121-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99121-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99121-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99121-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99121-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99121-121">INPUTS</span></span>

### <span data-ttu-id="99121-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99121-122">None</span></span>

## <span data-ttu-id="99121-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99121-123">OUTPUTS</span></span>

### <span data-ttu-id="99121-124">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="99121-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="99121-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99121-125">NOTES</span></span>

## <span data-ttu-id="99121-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99121-126">RELATED LINKS</span></span>
