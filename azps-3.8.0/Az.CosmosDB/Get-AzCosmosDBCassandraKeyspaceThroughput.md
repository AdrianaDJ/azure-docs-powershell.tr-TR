---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104130"
---
# <span data-ttu-id="6e93b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="6e93b-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="6e93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e93b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e93b-103">Cassandra keyspace 'in üretilen iş değerini alır.</span><span class="sxs-lookup"><span data-stu-id="6e93b-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="6e93b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e93b-104">SYNTAX</span></span>

### <span data-ttu-id="6e93b-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e93b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e93b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e93b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e93b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e93b-107">DESCRIPTION</span></span>
<span data-ttu-id="6e93b-108">**Get-Azcosmosdbcassandrakeyspaceüretiminin** cmdlet 'i, verilen bir keyspace 'e karşılık gelen üretilen iş nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="6e93b-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="6e93b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e93b-109">EXAMPLES</span></span>

### <span data-ttu-id="6e93b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6e93b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="6e93b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e93b-111">PARAMETERS</span></span>

### <span data-ttu-id="6e93b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e93b-112">-AccountName</span></span>
<span data-ttu-id="6e93b-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="6e93b-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e93b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e93b-114">-DefaultProfile</span></span>
<span data-ttu-id="6e93b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e93b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e93b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e93b-116">-InputObject</span></span>
<span data-ttu-id="6e93b-117">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="6e93b-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e93b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e93b-118">-Name</span></span>
<span data-ttu-id="6e93b-119">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6e93b-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="6e93b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e93b-120">-ResourceGroupName</span></span>
<span data-ttu-id="6e93b-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6e93b-121">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e93b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e93b-122">CommonParameters</span></span>
<span data-ttu-id="6e93b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e93b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e93b-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e93b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e93b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e93b-125">INPUTS</span></span>

### <span data-ttu-id="6e93b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6e93b-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6e93b-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e93b-127">OUTPUTS</span></span>

### <span data-ttu-id="6e93b-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6e93b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6e93b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e93b-129">NOTES</span></span>

## <span data-ttu-id="6e93b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e93b-130">RELATED LINKS</span></span>
