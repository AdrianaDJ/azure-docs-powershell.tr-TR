---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1d470870d27001a07302240dba1abd7e56153d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104107"
---
# <span data-ttu-id="79c1c-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="79c1c-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="79c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="79c1c-103">MongoDB veritabanının CosmosDB aktarımı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="79c1c-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="79c1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79c1c-104">SYNTAX</span></span>

### <span data-ttu-id="79c1c-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79c1c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79c1c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c1c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c1c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79c1c-107">DESCRIPTION</span></span>
<span data-ttu-id="79c1c-108">**Get-Azcosmosdbmongodbdatabase,**</span><span class="sxs-lookup"><span data-stu-id="79c1c-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="79c1c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79c1c-109">EXAMPLES</span></span>

### <span data-ttu-id="79c1c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79c1c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="79c1c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79c1c-111">PARAMETERS</span></span>

### <span data-ttu-id="79c1c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79c1c-112">-AccountName</span></span>
<span data-ttu-id="79c1c-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="79c1c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="79c1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c1c-114">-DefaultProfile</span></span>
<span data-ttu-id="79c1c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79c1c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c1c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c1c-116">-InputObject</span></span>
<span data-ttu-id="79c1c-117">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="79c1c-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c1c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="79c1c-118">-Name</span></span>
<span data-ttu-id="79c1c-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="79c1c-119">Database name.</span></span>

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

### <span data-ttu-id="79c1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="79c1c-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="79c1c-121">Name of resource group.</span></span>

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

### <span data-ttu-id="79c1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c1c-122">CommonParameters</span></span>
<span data-ttu-id="79c1c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79c1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c1c-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79c1c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c1c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79c1c-125">INPUTS</span></span>

### <span data-ttu-id="79c1c-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="79c1c-126">None</span></span>

## <span data-ttu-id="79c1c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79c1c-127">OUTPUTS</span></span>

### <span data-ttu-id="79c1c-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="79c1c-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="79c1c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79c1c-129">NOTES</span></span>

## <span data-ttu-id="79c1c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79c1c-130">RELATED LINKS</span></span>
