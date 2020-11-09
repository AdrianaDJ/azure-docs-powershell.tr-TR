---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321710"
---
# <span data-ttu-id="da7c7-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="da7c7-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="da7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="da7c7-103">Cassandra keyspace 'in üretilen iş değerini alır.</span><span class="sxs-lookup"><span data-stu-id="da7c7-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="da7c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da7c7-104">SYNTAX</span></span>

### <span data-ttu-id="da7c7-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da7c7-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da7c7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da7c7-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da7c7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="da7c7-107">DESCRIPTION</span></span>
<span data-ttu-id="da7c7-108">**Get-Azcosmosdbcassandrakeyspaceüretiminin** cmdlet 'i, verilen bir keyspace 'e karşılık gelen üretilen iş nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="da7c7-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="da7c7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da7c7-109">EXAMPLES</span></span>

### <span data-ttu-id="da7c7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="da7c7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="da7c7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da7c7-111">PARAMETERS</span></span>

### <span data-ttu-id="da7c7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da7c7-112">-AccountName</span></span>
<span data-ttu-id="da7c7-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="da7c7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da7c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7c7-114">-DefaultProfile</span></span>
<span data-ttu-id="da7c7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da7c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7c7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da7c7-116">-InputObject</span></span>
<span data-ttu-id="da7c7-117">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="da7c7-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da7c7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="da7c7-118">-Name</span></span>
<span data-ttu-id="da7c7-119">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="da7c7-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="da7c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="da7c7-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="da7c7-121">Name of resource group.</span></span>

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

### <span data-ttu-id="da7c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7c7-122">CommonParameters</span></span>
<span data-ttu-id="da7c7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da7c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7c7-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da7c7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7c7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da7c7-125">INPUTS</span></span>

### <span data-ttu-id="da7c7-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="da7c7-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="da7c7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da7c7-127">OUTPUTS</span></span>

### <span data-ttu-id="da7c7-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="da7c7-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="da7c7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da7c7-129">NOTES</span></span>

## <span data-ttu-id="da7c7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da7c7-130">RELATED LINKS</span></span>
