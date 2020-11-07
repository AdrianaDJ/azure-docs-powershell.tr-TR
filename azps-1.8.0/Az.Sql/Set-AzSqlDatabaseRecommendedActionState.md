---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 49ea5796e8f2b03fe67a6c40ab42dc7f1c2481e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758791"
---
# <span data-ttu-id="75544-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="75544-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="75544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75544-102">SYNOPSIS</span></span>
<span data-ttu-id="75544-103">Bir Azure SQL veritabanı önerilen eyleminin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75544-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="75544-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75544-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75544-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75544-105">DESCRIPTION</span></span>
<span data-ttu-id="75544-106">**Set-AzSqlDatabaseRecommendedActionState** cmdlet 'i, BIR Azure SQL veritabanı önerilen eyleminin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75544-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="75544-107">Bu, önerilen bir eylemin yeni duruma göre uygulanmasını, geri döndürüldüğünü veya atılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="75544-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="75544-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75544-108">EXAMPLES</span></span>

### <span data-ttu-id="75544-109">Örnek 1: beklemede olan önerilen bir eylem durumunu uygulama</span><span class="sxs-lookup"><span data-stu-id="75544-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="75544-110">Bu komut, \[ \] \[ \] wirunner adlı veritabanına ait olan IR_ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 adlı önerilen eylemin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="75544-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="75544-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75544-111">PARAMETERS</span></span>

### <span data-ttu-id="75544-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="75544-112">-AdvisorName</span></span>
<span data-ttu-id="75544-113">Bu önerilen eylemin ait olduğu danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75544-114">-DatabaseName</span></span>
<span data-ttu-id="75544-115">Bu cmdlet 'in önerilen eylem durumunu ayarladığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75544-116">-DefaultProfile</span></span>
<span data-ttu-id="75544-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="75544-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75544-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="75544-118">-RecommendedActionName</span></span>
<span data-ttu-id="75544-119">Durumu güncelleştirilen önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-119">Specifies the name of the recommended action for which state is being updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75544-120">-ResourceGroupName</span></span>
<span data-ttu-id="75544-121">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-121">Specifies the name of the resource group of the server that contains this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="75544-122">-ServerName</span></span>
<span data-ttu-id="75544-123">Veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-123">Specifies the name of the server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-124">Durumlu</span><span class="sxs-lookup"><span data-stu-id="75544-124">-State</span></span>
<span data-ttu-id="75544-125">Bu cmdlet 'in önerilen eylem durumunu güncelleştirdiği yeni değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="75544-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="75544-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75544-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75544-127">Etkin</span><span class="sxs-lookup"><span data-stu-id="75544-127">Active</span></span>
- <span data-ttu-id="75544-128">Bekley</span><span class="sxs-lookup"><span data-stu-id="75544-128">Pending</span></span>
- <span data-ttu-id="75544-129">Pendinggeri döndür</span><span class="sxs-lookup"><span data-stu-id="75544-129">PendingRevert</span></span>
- <span data-ttu-id="75544-130">Yankı Iptal edildi</span><span class="sxs-lookup"><span data-stu-id="75544-130">RevertCancelled</span></span>
- <span data-ttu-id="75544-131">Edildi</span><span class="sxs-lookup"><span data-stu-id="75544-131">Ignored</span></span>
- <span data-ttu-id="75544-132">Lemezse</span><span class="sxs-lookup"><span data-stu-id="75544-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75544-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="75544-133">-Confirm</span></span>
<span data-ttu-id="75544-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75544-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75544-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75544-135">-WhatIf</span></span>
<span data-ttu-id="75544-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75544-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75544-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75544-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75544-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75544-138">CommonParameters</span></span>
<span data-ttu-id="75544-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75544-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75544-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75544-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75544-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75544-141">INPUTS</span></span>

### <span data-ttu-id="75544-142">System. String</span><span class="sxs-lookup"><span data-stu-id="75544-142">System.String</span></span>

### <span data-ttu-id="75544-143">Microsoft. Azure. Commands. Sql. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="75544-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="75544-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75544-144">OUTPUTS</span></span>

### <span data-ttu-id="75544-145">Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="75544-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="75544-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75544-146">NOTES</span></span>
* <span data-ttu-id="75544-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL, danışman, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="75544-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="75544-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75544-148">RELATED LINKS</span></span>

[<span data-ttu-id="75544-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="75544-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="75544-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="75544-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="75544-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="75544-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="75544-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="75544-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="75544-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="75544-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="75544-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="75544-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="75544-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="75544-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="75544-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="75544-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="75544-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="75544-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="75544-158">Set-Azsqlserverdanışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="75544-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="75544-159">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="75544-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)