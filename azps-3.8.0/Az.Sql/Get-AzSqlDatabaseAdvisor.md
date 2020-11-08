---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097043"
---
# <span data-ttu-id="d8afc-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="d8afc-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="d8afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8afc-102">SYNOPSIS</span></span>
<span data-ttu-id="d8afc-103">Bir Azure SQL veritabanı için bir veya daha fazla danışmanları alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="d8afc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8afc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8afc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8afc-105">DESCRIPTION</span></span>
<span data-ttu-id="d8afc-106">**Get-AzSqlDatabaseAdvisor** cmdlet 'ı BIR Azure SQL veritabanı için bir veya birden çok Azure SQL veritabanı danışmanını alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="d8afc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8afc-107">EXAMPLES</span></span>

### <span data-ttu-id="d8afc-108">Örnek 1: belirtilen veritabanının tüm danışmanlarının listesi</span><span class="sxs-lookup"><span data-stu-id="d8afc-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="d8afc-109">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucuya ait olan WIRunner adlı veritabanının tüm danışmanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="d8afc-110">Örnek 2: belirtilen veritabanı için tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="d8afc-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="d8afc-111">Bu komut, WIRunner adlı veritabanı için CreateIndex adındaki Danışmanı alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="d8afc-112">Örnek 3: yanıtta verilen önerilen eylemlerle birlikte tüm danışmanları listeleyin</span><span class="sxs-lookup"><span data-stu-id="d8afc-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="d8afc-113">Bu komut, ' WIRunner ' adlı veritabanının, yanıtta verilen önerilen eylemlerle birlikte tüm danışmanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="d8afc-114">Komut *ExpandRecommendedActions* parametresini kullandığından, cmdlet, yanıttaki önerilen eylemleri alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="d8afc-115">Örnek 4: yanıta dahil olan önerilen eylemlerle tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="d8afc-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="d8afc-116">Bu komut, WIRunner adlı veritabanından, yanıtın içerdiği önerilen eylemleri içeren CreateIndex adındaki Danışmanı alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="d8afc-117">Komut *ExpandRecommendedActions* parametresini kullandığından, cmdlet, yanıttaki önerilen eylemleri alır.</span><span class="sxs-lookup"><span data-stu-id="d8afc-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="d8afc-118">Örnek 5: filtreleme kullanarak belirtilen veritabanının tüm danışmanlarının listesi</span><span class="sxs-lookup"><span data-stu-id="d8afc-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="d8afc-119">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucuya ait olan WIRunner adlı veritabanının tüm danışmanlarının listesini alır ve "d" harfiyle başlar.</span><span class="sxs-lookup"><span data-stu-id="d8afc-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="d8afc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8afc-120">PARAMETERS</span></span>

### <span data-ttu-id="d8afc-121">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="d8afc-121">-AdvisorName</span></span>
<span data-ttu-id="d8afc-122">Bu cmdlet 'in aldığı danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8afc-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d8afc-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8afc-123">-DatabaseName</span></span>
<span data-ttu-id="d8afc-124">Bu cmdlet 'in Danışmanı istediği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8afc-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="d8afc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8afc-125">-DefaultProfile</span></span>
<span data-ttu-id="d8afc-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8afc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8afc-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="d8afc-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="d8afc-128">Bu cmdlet 'in yanıttaki önerilen eylemleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8afc-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8afc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8afc-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8afc-130">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8afc-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d8afc-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8afc-131">-ServerName</span></span>
<span data-ttu-id="d8afc-132">Veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8afc-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="d8afc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8afc-133">CommonParameters</span></span>
<span data-ttu-id="d8afc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8afc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8afc-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8afc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8afc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8afc-136">INPUTS</span></span>

### <span data-ttu-id="d8afc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d8afc-137">System.String</span></span>

### <span data-ttu-id="d8afc-138">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d8afc-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d8afc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8afc-139">OUTPUTS</span></span>

### <span data-ttu-id="d8afc-140">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqldatabasedanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="d8afc-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="d8afc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8afc-141">NOTES</span></span>
* <span data-ttu-id="d8afc-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="d8afc-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="d8afc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8afc-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8afc-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="d8afc-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="d8afc-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="d8afc-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="d8afc-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="d8afc-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="d8afc-147">Set-Azsqldatabasedanışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="d8afc-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="d8afc-148">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="d8afc-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
