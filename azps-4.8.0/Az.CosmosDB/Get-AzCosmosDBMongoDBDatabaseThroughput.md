---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274204"
---
# <span data-ttu-id="b4320-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="b4320-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="b4320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4320-102">SYNOPSIS</span></span>
<span data-ttu-id="b4320-103">MongoDB veritabanının CosmosDB aktarımı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b4320-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="b4320-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4320-104">SYNTAX</span></span>

### <span data-ttu-id="b4320-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4320-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4320-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4320-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4320-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4320-107">DESCRIPTION</span></span>
<span data-ttu-id="b4320-108">**Get-Azcosmosdbmongodbdatabase,**</span><span class="sxs-lookup"><span data-stu-id="b4320-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="b4320-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4320-109">EXAMPLES</span></span>

### <span data-ttu-id="b4320-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4320-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="b4320-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4320-111">PARAMETERS</span></span>

### <span data-ttu-id="b4320-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4320-112">-AccountName</span></span>
<span data-ttu-id="b4320-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b4320-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4320-114">-DefaultProfile</span></span>
<span data-ttu-id="b4320-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4320-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4320-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4320-116">-InputObject</span></span>
<span data-ttu-id="b4320-117">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="b4320-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4320-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4320-118">-Name</span></span>
<span data-ttu-id="b4320-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b4320-119">Database name.</span></span>

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

### <span data-ttu-id="b4320-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4320-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4320-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b4320-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b4320-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4320-122">CommonParameters</span></span>
<span data-ttu-id="b4320-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4320-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4320-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4320-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4320-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4320-125">INPUTS</span></span>

### <span data-ttu-id="b4320-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4320-126">None</span></span>

## <span data-ttu-id="b4320-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4320-127">OUTPUTS</span></span>

### <span data-ttu-id="b4320-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b4320-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b4320-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4320-129">NOTES</span></span>

## <span data-ttu-id="b4320-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4320-130">RELATED LINKS</span></span>
