---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096038"
---
# <span data-ttu-id="ed792-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="ed792-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="ed792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed792-102">SYNOPSIS</span></span>
<span data-ttu-id="ed792-103">CosmosDB SQL tetikleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="ed792-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="ed792-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed792-104">SYNTAX</span></span>

### <span data-ttu-id="ed792-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed792-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed792-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed792-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed792-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed792-107">DESCRIPTION</span></span>
<span data-ttu-id="ed792-108">**Get-AzCosmosDBSqlTrigger** cmdlet 'i, belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için var olan tüm Cosmosdb SQL tetiklerinin listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName, ContainerName ve triggername için tek bir Cosmosdb SQL tetikleyicisi alır.</span><span class="sxs-lookup"><span data-stu-id="ed792-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="ed792-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed792-109">EXAMPLES</span></span>

### <span data-ttu-id="ed792-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed792-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="ed792-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed792-111">PARAMETERS</span></span>

### <span data-ttu-id="ed792-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed792-112">-AccountName</span></span>
<span data-ttu-id="ed792-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ed792-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ed792-114">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="ed792-114">-ContainerName</span></span>
<span data-ttu-id="ed792-115">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="ed792-115">Container name.</span></span>

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

### <span data-ttu-id="ed792-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed792-116">-DatabaseName</span></span>
<span data-ttu-id="ed792-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ed792-117">Database name.</span></span>

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

### <span data-ttu-id="ed792-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed792-118">-DefaultProfile</span></span>
<span data-ttu-id="ed792-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed792-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed792-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed792-120">-InputObject</span></span>
<span data-ttu-id="ed792-121">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ed792-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed792-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed792-122">-Name</span></span>
<span data-ttu-id="ed792-123">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="ed792-123">Trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed792-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed792-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed792-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed792-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ed792-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed792-126">CommonParameters</span></span>
<span data-ttu-id="ed792-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed792-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed792-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed792-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed792-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed792-129">INPUTS</span></span>

### <span data-ttu-id="ed792-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed792-130">None</span></span>

## <span data-ttu-id="ed792-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed792-131">OUTPUTS</span></span>

### <span data-ttu-id="ed792-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="ed792-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="ed792-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed792-133">NOTES</span></span>

## <span data-ttu-id="ed792-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed792-134">RELATED LINKS</span></span>
