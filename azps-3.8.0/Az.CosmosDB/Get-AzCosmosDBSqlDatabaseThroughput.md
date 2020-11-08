---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096040"
---
# <span data-ttu-id="41705-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="41705-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="41705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41705-102">SYNOPSIS</span></span>
<span data-ttu-id="41705-103">CosmosDB SQL veritabanına karşılık gelen üretilen iş ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="41705-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="41705-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41705-104">SYNTAX</span></span>

### <span data-ttu-id="41705-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41705-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41705-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41705-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41705-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="41705-107">DESCRIPTION</span></span>
<span data-ttu-id="41705-108">**Get-Azcosmosdbsqldatabaseüretilen** iş cmdlet 'ı Cosmosdb SQL veritabanına karşılık gelen üretilen iş ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="41705-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="41705-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41705-109">EXAMPLES</span></span>

### <span data-ttu-id="41705-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="41705-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="41705-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41705-111">PARAMETERS</span></span>

### <span data-ttu-id="41705-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41705-112">-AccountName</span></span>
<span data-ttu-id="41705-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="41705-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="41705-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41705-114">-DefaultProfile</span></span>
<span data-ttu-id="41705-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41705-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41705-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41705-116">-InputObject</span></span>
<span data-ttu-id="41705-117">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="41705-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="41705-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="41705-118">-Name</span></span>
<span data-ttu-id="41705-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="41705-119">Database name.</span></span>

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

### <span data-ttu-id="41705-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41705-120">-ResourceGroupName</span></span>
<span data-ttu-id="41705-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="41705-121">Name of resource group.</span></span>

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

### <span data-ttu-id="41705-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41705-122">CommonParameters</span></span>
<span data-ttu-id="41705-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41705-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41705-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41705-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41705-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41705-125">INPUTS</span></span>

### <span data-ttu-id="41705-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="41705-126">None</span></span>

## <span data-ttu-id="41705-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41705-127">OUTPUTS</span></span>

### <span data-ttu-id="41705-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="41705-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="41705-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41705-129">NOTES</span></span>

## <span data-ttu-id="41705-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41705-130">RELATED LINKS</span></span>
