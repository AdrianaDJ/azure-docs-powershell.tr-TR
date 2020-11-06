---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 853702ab34a6a9dab7e90f2335f99deb7155a837
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591893"
---
# <span data-ttu-id="c9253-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="c9253-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="c9253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9253-102">SYNOPSIS</span></span>
<span data-ttu-id="c9253-103">Bir Azure SQL veritabanı için bir veya daha fazla danışmanları alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9253-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9253-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9253-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9253-105">DESCRIPTION</span></span>
<span data-ttu-id="c9253-106">**Get-AzureRmSqlDatabaseAdvisor** cmdlet 'i, BIR Azure SQL veritabanı için bir veya birden çok Azure SQL veritabanı danışmanını alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="c9253-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9253-107">EXAMPLES</span></span>

### <span data-ttu-id="c9253-108">Örnek 1: belirtilen veritabanının tüm danışmanlarının listesi</span><span class="sxs-lookup"><span data-stu-id="c9253-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="c9253-109">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucuya ait olan WIRunner adlı veritabanının tüm danışmanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="c9253-110">Örnek 2: belirtilen veritabanı için tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="c9253-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="c9253-111">Bu komut, WIRunner adlı veritabanı için CreateIndex adındaki Danışmanı alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="c9253-112">Örnek 3: yanıtta verilen önerilen eylemlerle birlikte tüm danışmanları listeleyin</span><span class="sxs-lookup"><span data-stu-id="c9253-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="c9253-113">Bu komut, ' WIRunner ' adlı veritabanının, yanıtta verilen önerilen eylemlerle birlikte tüm danışmanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="c9253-114">Komut *ExpandRecommendedActions* parametresini kullandığından, cmdlet, yanıttaki önerilen eylemleri alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="c9253-115">Örnek 4: yanıta dahil olan önerilen eylemlerle tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="c9253-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="c9253-116">Bu komut, WIRunner adlı veritabanından, yanıtın içerdiği önerilen eylemleri içeren CreateIndex adındaki Danışmanı alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="c9253-117">Komut *ExpandRecommendedActions* parametresini kullandığından, cmdlet, yanıttaki önerilen eylemleri alır.</span><span class="sxs-lookup"><span data-stu-id="c9253-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="c9253-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9253-118">PARAMETERS</span></span>

### <span data-ttu-id="c9253-119">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="c9253-119">-AdvisorName</span></span>
<span data-ttu-id="c9253-120">Bu cmdlet 'in aldığı danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9253-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c9253-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9253-121">-DatabaseName</span></span>
<span data-ttu-id="c9253-122">Bu cmdlet 'in Danışmanı istediği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9253-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="c9253-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9253-123">-DefaultProfile</span></span>
<span data-ttu-id="c9253-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c9253-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9253-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="c9253-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="c9253-126">Bu cmdlet 'in yanıttaki önerilen eylemleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9253-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="c9253-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9253-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9253-128">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9253-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="c9253-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9253-129">-ServerName</span></span>
<span data-ttu-id="c9253-130">Veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9253-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="c9253-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9253-131">CommonParameters</span></span>
<span data-ttu-id="c9253-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9253-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9253-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9253-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9253-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9253-134">INPUTS</span></span>

### <span data-ttu-id="c9253-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c9253-135">System.String</span></span>

### <span data-ttu-id="c9253-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9253-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9253-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9253-137">OUTPUTS</span></span>

### <span data-ttu-id="c9253-138">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqldatabasedanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="c9253-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="c9253-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9253-139">NOTES</span></span>
* <span data-ttu-id="c9253-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="c9253-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="c9253-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9253-141">RELATED LINKS</span></span>

[<span data-ttu-id="c9253-142">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c9253-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="c9253-143">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c9253-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="c9253-144">Get-AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c9253-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="c9253-145">Set-Azurermsqldatabasedanışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="c9253-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c9253-146">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c9253-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
