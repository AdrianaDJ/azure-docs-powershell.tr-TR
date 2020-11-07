---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerRecommendedAction.md
ms.openlocfilehash: 7a9493b5dbc1149bd4afa9298ce69c6ebd5fbe2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764108"
---
# <span data-ttu-id="49254-101">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="49254-101">Get-AzureRmSqlServerRecommendedAction</span></span>

## <span data-ttu-id="49254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49254-102">SYNOPSIS</span></span>
<span data-ttu-id="49254-103">Bir Azure SQL Server Danışmanı için önerilen bir veya birden çok eylemi getirir.</span><span class="sxs-lookup"><span data-stu-id="49254-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49254-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49254-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -AdvisorName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49254-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49254-105">DESCRIPTION</span></span>
<span data-ttu-id="49254-106">**Get-AzureRmSqlServerRecommendedAction** cmdlet 'ı BIR Azure SQL Server Danışmanı için önerilen bir veya birden çok eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="49254-106">The **Get-AzureRmSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="49254-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49254-107">EXAMPLES</span></span>

### <span data-ttu-id="49254-108">Örnek 1: belirli bir danışman için önerilen tüm eylemlerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="49254-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzureRmSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="49254-109">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucuda bulunan CreateIndex adındaki SQL Server Danışmanı için önerilen tüm eylemlerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="49254-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="49254-110">Örnek 2: bir danışman için önerilen eylemi edinme</span><span class="sxs-lookup"><span data-stu-id="49254-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="49254-111">Bu komut \[ \] \[ \] , createındex adındaki Advisor _6C7AE8CC9C87E7FD5893 test_table_0 test_schema IR_</span><span class="sxs-lookup"><span data-stu-id="49254-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="49254-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49254-112">PARAMETERS</span></span>

### <span data-ttu-id="49254-113">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="49254-113">-AdvisorName</span></span>
<span data-ttu-id="49254-114">Bu cmdlet 'in eylem istediği danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49254-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="49254-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49254-115">-DefaultProfile</span></span>
<span data-ttu-id="49254-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="49254-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49254-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="49254-117">-RecommendedActionName</span></span>
<span data-ttu-id="49254-118">Bu cmdlet 'in aldığı önerilen eylemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49254-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49254-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49254-119">-ResourceGroupName</span></span>
<span data-ttu-id="49254-120">Bu sunucunun bulunduğu sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49254-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="49254-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="49254-121">-ServerName</span></span>
<span data-ttu-id="49254-122">Danışmanın ait olduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49254-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="49254-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49254-123">CommonParameters</span></span>
<span data-ttu-id="49254-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49254-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49254-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49254-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49254-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49254-126">INPUTS</span></span>

### <span data-ttu-id="49254-127">System. String</span><span class="sxs-lookup"><span data-stu-id="49254-127">System.String</span></span>

## <span data-ttu-id="49254-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49254-128">OUTPUTS</span></span>

### <span data-ttu-id="49254-129">Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="49254-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="49254-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49254-130">NOTES</span></span>
* <span data-ttu-id="49254-131">Anahtar sözcükler: Azure, azurerm, ARM, Resource, yönetim, Manager, SQL, Server, MSSQL, Advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="49254-131">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="49254-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49254-132">RELATED LINKS</span></span>

[<span data-ttu-id="49254-133">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="49254-133">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="49254-134">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="49254-134">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="49254-135">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="49254-135">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="49254-136">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="49254-136">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="49254-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="49254-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
