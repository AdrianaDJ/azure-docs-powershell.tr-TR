---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765033"
---
# <span data-ttu-id="b21cd-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b21cd-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="b21cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b21cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b21cd-103">Bir Azure SQL Server önerilen eyleminin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b21cd-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b21cd-105">DESCRIPTION</span></span>
<span data-ttu-id="b21cd-106">**Set-AzureRmSqlServerRecommendedActionState** cmdlet 'ı BIR Azure SQL Server önerilen eyleminin durumu.</span><span class="sxs-lookup"><span data-stu-id="b21cd-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="b21cd-107">Bu cmdlet, yeni duruma göre önerilen eylemi uygular, geri alır veya atar.</span><span class="sxs-lookup"><span data-stu-id="b21cd-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="b21cd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b21cd-108">EXAMPLES</span></span>

### <span data-ttu-id="b21cd-109">Example1: önerilen eylemin durumunu Beklemede olarak güncelleyin</span><span class="sxs-lookup"><span data-stu-id="b21cd-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="b21cd-110">"IR_ \[ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893" adlı sunucu tarafından önerilen eylemin durumunu \] \[ \] "beklemede" olarak güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b21cd-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="b21cd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b21cd-111">PARAMETERS</span></span>

### <span data-ttu-id="b21cd-112">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="b21cd-112">-AdvisorName</span></span>
<span data-ttu-id="b21cd-113">Önerilen eylemi içeren Advisor adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="b21cd-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b21cd-114">-RecommendedActionName</span></span>
<span data-ttu-id="b21cd-115">Bu cmdlet 'in durumu güncelleştirdiği önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="b21cd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b21cd-116">-ResourceGroupName</span></span>
<span data-ttu-id="b21cd-117">Sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="b21cd-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b21cd-118">-ServerName</span></span>
<span data-ttu-id="b21cd-119">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b21cd-120">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b21cd-120">-State</span></span>
<span data-ttu-id="b21cd-121">Bu cmdlet 'in önerilen eylem durumunu güncelleştirdiği yeni değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="b21cd-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b21cd-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b21cd-123">Etkin</span><span class="sxs-lookup"><span data-stu-id="b21cd-123">Active</span></span>
- <span data-ttu-id="b21cd-124">Bekley</span><span class="sxs-lookup"><span data-stu-id="b21cd-124">Pending</span></span>
- <span data-ttu-id="b21cd-125">Pendinggeri döndür</span><span class="sxs-lookup"><span data-stu-id="b21cd-125">PendingRevert</span></span>
- <span data-ttu-id="b21cd-126">Yankı Iptal edildi</span><span class="sxs-lookup"><span data-stu-id="b21cd-126">RevertCancelled</span></span>
- <span data-ttu-id="b21cd-127">Edildi</span><span class="sxs-lookup"><span data-stu-id="b21cd-127">Ignored</span></span>
- <span data-ttu-id="b21cd-128">Lemezse</span><span class="sxs-lookup"><span data-stu-id="b21cd-128">Resolved</span></span>

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

### <span data-ttu-id="b21cd-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b21cd-129">-Confirm</span></span>
<span data-ttu-id="b21cd-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b21cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21cd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21cd-131">-WhatIf</span></span>
<span data-ttu-id="b21cd-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b21cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21cd-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b21cd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21cd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21cd-134">-DefaultProfile</span></span>
<span data-ttu-id="b21cd-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b21cd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21cd-136">CommonParameters</span></span>
<span data-ttu-id="b21cd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b21cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21cd-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21cd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21cd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b21cd-139">INPUTS</span></span>

## <span data-ttu-id="b21cd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b21cd-140">OUTPUTS</span></span>

### <span data-ttu-id="b21cd-141">Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b21cd-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="b21cd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b21cd-142">NOTES</span></span>
* <span data-ttu-id="b21cd-143">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b21cd-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b21cd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b21cd-144">RELATED LINKS</span></span>

[<span data-ttu-id="b21cd-145">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b21cd-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="b21cd-146">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b21cd-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="b21cd-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b21cd-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="b21cd-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b21cd-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="b21cd-149">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b21cd-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
