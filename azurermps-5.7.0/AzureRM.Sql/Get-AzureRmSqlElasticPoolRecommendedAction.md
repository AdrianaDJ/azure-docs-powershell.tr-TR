---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: c6a3a03c71a9b240256bc30eced51929d804cdc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588749"
---
# <span data-ttu-id="0afb4-101">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0afb4-101">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="0afb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afb4-102">SYNOPSIS</span></span>
<span data-ttu-id="0afb4-103">Bir Azure SQL esnek havuz Danışmanı için bir veya daha fazla önerilen eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="0afb4-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0afb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0afb4-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0afb4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0afb4-105">DESCRIPTION</span></span>
<span data-ttu-id="0afb4-106">**Get-AzureRmSqlElasticPoolRecommendedAction** cmdlet 'ı BIR Azure SQL esnek havuz Danışmanı için önerilen bir veya birden çok eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="0afb4-106">The **Get-AzureRmSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="0afb4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0afb4-107">EXAMPLES</span></span>

### <span data-ttu-id="0afb4-108">Örnek 1: bir danışman için önerilen tüm eylemleri listeleme</span><span class="sxs-lookup"><span data-stu-id="0afb4-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM

ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="0afb4-109">Bu komut, WIRunnerPool adlı elastik havuz için sağlanan CreateIndex adındaki tüm önerilen eylemlerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0afb4-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="0afb4-110">Örnek 2: bir danışman için önerilen eylemi edinme</span><span class="sxs-lookup"><span data-stu-id="0afb4-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="0afb4-111">Bu komut, \[ CreateIndex adındaki test_schema IR_ \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 adlı önerilen eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="0afb4-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="0afb4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0afb4-112">PARAMETERS</span></span>

### <span data-ttu-id="0afb4-113">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="0afb4-113">-AdvisorName</span></span>
<span data-ttu-id="0afb4-114">Bu cmdlet 'in önerilen eylemleri istediği bir danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0afb4-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="0afb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afb4-115">-DefaultProfile</span></span>
<span data-ttu-id="0afb4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0afb4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0afb4-117">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="0afb4-117">-ElasticPoolName</span></span>
<span data-ttu-id="0afb4-118">Bu cmdlet 'in önerilen eylemleri istediği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0afb4-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="0afb4-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="0afb4-119">-RecommendedActionName</span></span>
<span data-ttu-id="0afb4-120">Bu cmdlet 'in aldığı önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0afb4-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="0afb4-122">Bu esnek havuzu içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0afb4-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="0afb4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0afb4-123">-ServerName</span></span>
<span data-ttu-id="0afb4-124">Elastik havuzun bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0afb4-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="0afb4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afb4-125">CommonParameters</span></span>
<span data-ttu-id="0afb4-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0afb4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afb4-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afb4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afb4-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0afb4-128">INPUTS</span></span>

### <span data-ttu-id="0afb4-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0afb4-129">None</span></span>
<span data-ttu-id="0afb4-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0afb4-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0afb4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0afb4-131">OUTPUTS</span></span>

### <span data-ttu-id="0afb4-132">Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="0afb4-132">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="0afb4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0afb4-133">NOTES</span></span>
* <span data-ttu-id="0afb4-134">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, SQL, elappool, MSSQL, danışman, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="0afb4-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="0afb4-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0afb4-135">RELATED LINKS</span></span>

[<span data-ttu-id="0afb4-136">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0afb4-136">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="0afb4-137">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="0afb4-137">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="0afb4-138">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0afb4-138">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="0afb4-139">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="0afb4-139">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="0afb4-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0afb4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
