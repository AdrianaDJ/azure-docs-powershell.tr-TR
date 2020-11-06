---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 992dc949ec4c17529415beeeb2cf2a831d4d2a68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588698"
---
# <span data-ttu-id="43444-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="43444-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="43444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43444-102">SYNOPSIS</span></span>
<span data-ttu-id="43444-103">Bir Azure SQL esnek havuzu önerilen eyleminin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="43444-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43444-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43444-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43444-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43444-105">DESCRIPTION</span></span>
<span data-ttu-id="43444-106">**Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet 'ı Azure SQL esnek havuzunun önerilen eyleminin durumu.</span><span class="sxs-lookup"><span data-stu-id="43444-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="43444-107">Bu cmdlet, önerilen bir eylemi uygular veya yeni duruma göre atılır.</span><span class="sxs-lookup"><span data-stu-id="43444-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="43444-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43444-108">EXAMPLES</span></span>

### <span data-ttu-id="43444-109">Örnek 1: önerilen bir eylemin durumunu Beklemede olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="43444-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="43444-110">Bu komut, IR_ \[ test_schema \] _ \[ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 adındaki elastik havuz önerilen eyleminin bekleme durumunu güncelleştirir \] .</span><span class="sxs-lookup"><span data-stu-id="43444-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="43444-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43444-111">PARAMETERS</span></span>

### <span data-ttu-id="43444-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="43444-112">-AdvisorName</span></span>
<span data-ttu-id="43444-113">Bu önerilen eylemin ait olduğu danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43444-114">-DefaultProfile</span></span>
<span data-ttu-id="43444-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="43444-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43444-116">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="43444-116">-ElasticPoolName</span></span>
<span data-ttu-id="43444-117">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="43444-118">-RecommendedActionName</span></span>
<span data-ttu-id="43444-119">Bu cmdlet 'in durumu güncelleştirdiği önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43444-120">-ResourceGroupName</span></span>
<span data-ttu-id="43444-121">Bu esnek havuzu içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43444-122">-ServerName</span></span>
<span data-ttu-id="43444-123">Elastik havuzun bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-124">Durumlu</span><span class="sxs-lookup"><span data-stu-id="43444-124">-State</span></span>
<span data-ttu-id="43444-125">Bu cmdlet 'in önerilen eylem durumunu güncelleştirdiği değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="43444-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="43444-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="43444-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43444-127">Etkin</span><span class="sxs-lookup"><span data-stu-id="43444-127">Active</span></span>
- <span data-ttu-id="43444-128">Bekley</span><span class="sxs-lookup"><span data-stu-id="43444-128">Pending</span></span>
- <span data-ttu-id="43444-129">Pendinggeri döndür</span><span class="sxs-lookup"><span data-stu-id="43444-129">PendingRevert</span></span>
- <span data-ttu-id="43444-130">Yankı Iptal edildi</span><span class="sxs-lookup"><span data-stu-id="43444-130">RevertCancelled</span></span>
- <span data-ttu-id="43444-131">Edildi</span><span class="sxs-lookup"><span data-stu-id="43444-131">Ignored</span></span>
- <span data-ttu-id="43444-132">Lemezse</span><span class="sxs-lookup"><span data-stu-id="43444-132">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43444-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="43444-133">-Confirm</span></span>
<span data-ttu-id="43444-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43444-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43444-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43444-135">-WhatIf</span></span>
<span data-ttu-id="43444-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43444-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43444-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43444-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43444-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43444-138">CommonParameters</span></span>
<span data-ttu-id="43444-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43444-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43444-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43444-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43444-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43444-141">INPUTS</span></span>

### <span data-ttu-id="43444-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43444-142">None</span></span>
<span data-ttu-id="43444-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="43444-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43444-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43444-144">OUTPUTS</span></span>

## <span data-ttu-id="43444-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43444-145">NOTES</span></span>
* <span data-ttu-id="43444-146">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, SQL, elappool, MSSQL, danışman, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="43444-146">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="43444-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43444-147">RELATED LINKS</span></span>

[<span data-ttu-id="43444-148">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="43444-148">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="43444-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="43444-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="43444-150">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="43444-150">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="43444-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="43444-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
