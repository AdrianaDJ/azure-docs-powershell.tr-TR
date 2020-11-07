---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
ms.openlocfilehash: a77119e653f3d4e6155fbe98e85a583eca50c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763792"
---
# <span data-ttu-id="e224f-101">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="e224f-101">Get-AzureRmSqlServerAdvisor</span></span>

## <span data-ttu-id="e224f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e224f-102">SYNOPSIS</span></span>
<span data-ttu-id="e224f-103">Bir Azure SQL Server için bir veya daha fazla danışmanları alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e224f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e224f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e224f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e224f-105">DESCRIPTION</span></span>
<span data-ttu-id="e224f-106">**Get-AzureRmSqlServerAdvisor** cmdlet 'i, BIR Azure SQL Server için bir veya daha fazla Azure SQL Server danışmanını alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-106">The **Get-AzureRmSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="e224f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e224f-107">EXAMPLES</span></span>

### <span data-ttu-id="e224f-108">Örnek 1: sunucunun tüm danışmanlarının listesi</span><span class="sxs-lookup"><span data-stu-id="e224f-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="e224f-109">Bu komut, WIRunnersProd adlı kaynak grubuna ait olan Wi-Runner-Avustralya-Doğu adlı sunucunun tüm danışmanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="e224f-110">Örnek 2: sunucu için tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="e224f-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="e224f-111">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucu için CreateIndex adındaki Danışmanı alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="e224f-112">Örnek 3: yanıtta verilen önerilen eylemlerle birlikte tüm danışmanları listeleyin</span><span class="sxs-lookup"><span data-stu-id="e224f-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="e224f-113">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucunun tüm danışmanları alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="e224f-114">Komut *ExpandRecommendedActions* parametresini kullandığından, cmdlet yanıtın içerdiği önerilen eylemleri alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="e224f-115">Örnek 4: yanıta dahil olan önerilen eylemlerle tek bir danışman alma</span><span class="sxs-lookup"><span data-stu-id="e224f-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="e224f-116">Bu komut, Wi-Runner-Avustralya-Doğu adlı sunucudan, yanıta dahil edilen önerilen eylemlerle birlikte CreateIndex adındaki Advisor 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="e224f-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="e224f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e224f-117">PARAMETERS</span></span>

### <span data-ttu-id="e224f-118">-Danışmanlar veya ad</span><span class="sxs-lookup"><span data-stu-id="e224f-118">-AdvisorName</span></span>
<span data-ttu-id="e224f-119">Bu cmdlet 'in aldığı danışman adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e224f-119">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e224f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e224f-120">-DefaultProfile</span></span>
<span data-ttu-id="e224f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e224f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e224f-122">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="e224f-122">-ExpandRecommendedActions</span></span>
<span data-ttu-id="e224f-123">Cmdlet 'in yanıta dahil olan danışmanlar için önerilen eylemleri içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e224f-123">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="e224f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e224f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e224f-125">Sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e224f-125">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="e224f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e224f-126">-ServerName</span></span>
<span data-ttu-id="e224f-127">Bu cmdlet 'in istediği danışman için sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e224f-127">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="e224f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e224f-128">CommonParameters</span></span>
<span data-ttu-id="e224f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e224f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e224f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e224f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e224f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e224f-131">INPUTS</span></span>

### <span data-ttu-id="e224f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e224f-132">System.String</span></span>

### <span data-ttu-id="e224f-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e224f-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e224f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e224f-134">OUTPUTS</span></span>

### <span data-ttu-id="e224f-135">Microsoft. Azure. Commands. Sql. Advisor. model. Azuressqlserverdanışmanlar Ormodel</span><span class="sxs-lookup"><span data-stu-id="e224f-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="e224f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e224f-136">NOTES</span></span>
* <span data-ttu-id="e224f-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, Server, MSSQL, danışman</span><span class="sxs-lookup"><span data-stu-id="e224f-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="e224f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e224f-138">RELATED LINKS</span></span>

[<span data-ttu-id="e224f-139">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="e224f-139">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="e224f-140">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e224f-140">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="e224f-141">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e224f-141">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="e224f-142">Set-Azurermsqlserverdanışmanlar Orautoexecutestatus</span><span class="sxs-lookup"><span data-stu-id="e224f-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="e224f-143">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="e224f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

