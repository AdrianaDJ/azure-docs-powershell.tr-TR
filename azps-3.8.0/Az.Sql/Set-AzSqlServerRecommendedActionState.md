---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937990"
---
# <span data-ttu-id="07892-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="07892-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="07892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07892-102">SYNOPSIS</span></span>
<span data-ttu-id="07892-103">Bir Azure SQL Server önerilen eyleminin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="07892-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="07892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07892-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07892-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07892-105">DESCRIPTION</span></span>
<span data-ttu-id="07892-106">**Set-AzSqlServerRecommendedActionState** cmdlet 'ı BIR Azure SQL Server önerilen eyleminin durumu.</span><span class="sxs-lookup"><span data-stu-id="07892-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="07892-107">Bu cmdlet, yeni duruma göre önerilen eylemi uygular, geri alır veya atar.</span><span class="sxs-lookup"><span data-stu-id="07892-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="07892-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07892-108">EXAMPLES</span></span>

### <span data-ttu-id="07892-109">Example1: önerilen eylemin durumunu Beklemede olarak güncelleyin</span><span class="sxs-lookup"><span data-stu-id="07892-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="07892-110">"IR_ \[ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893" adlı sunucu tarafından önerilen eylemin durumunu \] \[ \] "beklemede" olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="07892-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="07892-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07892-111">PARAMETERS</span></span>

### <span data-ttu-id="07892-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="07892-112">-AdvisorName</span></span>
<span data-ttu-id="07892-113">Önerilen eylemi içeren Advisor adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07892-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="07892-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07892-114">-DefaultProfile</span></span>
<span data-ttu-id="07892-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="07892-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07892-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="07892-116">-RecommendedActionName</span></span>
<span data-ttu-id="07892-117">Bu cmdlet 'in durumu güncelleştirdiği önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07892-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="07892-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07892-118">-ResourceGroupName</span></span>
<span data-ttu-id="07892-119">Sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07892-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="07892-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07892-120">-ServerName</span></span>
<span data-ttu-id="07892-121">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07892-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="07892-122">Durumlu</span><span class="sxs-lookup"><span data-stu-id="07892-122">-State</span></span>
<span data-ttu-id="07892-123">Bu cmdlet 'in önerilen eylem durumunu güncelleştirdiği yeni değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="07892-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="07892-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07892-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07892-125">Etkin</span><span class="sxs-lookup"><span data-stu-id="07892-125">Active</span></span>
- <span data-ttu-id="07892-126">Bekley</span><span class="sxs-lookup"><span data-stu-id="07892-126">Pending</span></span>
- <span data-ttu-id="07892-127">Pendinggeri döndür</span><span class="sxs-lookup"><span data-stu-id="07892-127">PendingRevert</span></span>
- <span data-ttu-id="07892-128">Yankı Iptal edildi</span><span class="sxs-lookup"><span data-stu-id="07892-128">RevertCancelled</span></span>
- <span data-ttu-id="07892-129">Edildi</span><span class="sxs-lookup"><span data-stu-id="07892-129">Ignored</span></span>
- <span data-ttu-id="07892-130">Lemezse</span><span class="sxs-lookup"><span data-stu-id="07892-130">Resolved</span></span>

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

### <span data-ttu-id="07892-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="07892-131">-Confirm</span></span>
<span data-ttu-id="07892-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07892-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07892-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07892-133">-WhatIf</span></span>
<span data-ttu-id="07892-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07892-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07892-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07892-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07892-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07892-136">CommonParameters</span></span>
<span data-ttu-id="07892-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07892-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07892-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07892-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07892-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07892-139">INPUTS</span></span>

### <span data-ttu-id="07892-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07892-140">System.String</span></span>

### <span data-ttu-id="07892-141">Microsoft. Azure. Commands. Sql. RecommendedAction. cmdlet. RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="07892-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="07892-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07892-142">OUTPUTS</span></span>

### <span data-ttu-id="07892-143">Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="07892-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="07892-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07892-144">NOTES</span></span>
* <span data-ttu-id="07892-145">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="07892-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="07892-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07892-146">RELATED LINKS</span></span>

[<span data-ttu-id="07892-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="07892-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="07892-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="07892-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="07892-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="07892-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="07892-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="07892-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="07892-151">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="07892-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
