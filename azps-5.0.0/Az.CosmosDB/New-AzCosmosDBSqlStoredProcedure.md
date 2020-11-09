---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321482"
---
# <span data-ttu-id="b0b53-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b0b53-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b0b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b53-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b53-103">Yeni bir CosmosDB SQL StoredProcedure oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0b53-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b0b53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0b53-104">SYNTAX</span></span>

### <span data-ttu-id="b0b53-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0b53-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b53-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0b53-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b53-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0b53-107">DESCRIPTION</span></span>
<span data-ttu-id="b0b53-108">Yeni bir CosmosDB SQL StoredProcedure oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0b53-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b0b53-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0b53-109">EXAMPLES</span></span>

### <span data-ttu-id="b0b53-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b0b53-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="b0b53-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0b53-111">PARAMETERS</span></span>

### <span data-ttu-id="b0b53-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0b53-112">-AccountName</span></span>
<span data-ttu-id="b0b53-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b0b53-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0b53-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="b0b53-114">-Body</span></span>
<span data-ttu-id="b0b53-115">Saklı yordamın gövdesi.</span><span class="sxs-lookup"><span data-stu-id="b0b53-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="b0b53-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="b0b53-116">-Confirm</span></span>
<span data-ttu-id="b0b53-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b0b53-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b53-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="b0b53-118">-ContainerName</span></span>
<span data-ttu-id="b0b53-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="b0b53-119">Container name.</span></span>

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

### <span data-ttu-id="b0b53-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0b53-120">-DatabaseName</span></span>
<span data-ttu-id="b0b53-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b0b53-121">Database name.</span></span>

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

### <span data-ttu-id="b0b53-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b53-122">-DefaultProfile</span></span>
<span data-ttu-id="b0b53-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0b53-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b53-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0b53-124">-Name</span></span>
<span data-ttu-id="b0b53-125">.</span><span class="sxs-lookup"><span data-stu-id="b0b53-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b0b53-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b0b53-126">-ParentObject</span></span>
<span data-ttu-id="b0b53-127">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b0b53-127">Sql Container object.</span></span>

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

### <span data-ttu-id="b0b53-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b53-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0b53-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b0b53-129">Name of resource group.</span></span>

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

### <span data-ttu-id="b0b53-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b53-130">-WhatIf</span></span>
<span data-ttu-id="b0b53-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0b53-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b53-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b0b53-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b53-133">CommonParameters</span></span>
<span data-ttu-id="b0b53-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0b53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b53-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b0b53-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b53-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0b53-136">INPUTS</span></span>

### <span data-ttu-id="b0b53-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="b0b53-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="b0b53-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0b53-138">OUTPUTS</span></span>

### <span data-ttu-id="b0b53-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b0b53-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="b0b53-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b0b53-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b0b53-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0b53-141">NOTES</span></span>

## <span data-ttu-id="b0b53-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0b53-142">RELATED LINKS</span></span>
