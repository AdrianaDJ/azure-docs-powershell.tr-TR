---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933687"
---
# <span data-ttu-id="c0d23-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="c0d23-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="c0d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d23-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d23-103">**Önemli: Bu cmdlet kullanım dışıdır, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) .**</span><span class="sxs-lookup"><span data-stu-id="c0d23-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="c0d23-104">Bir Azure SQL veritabanının denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c0d23-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="c0d23-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0d23-105">SYNTAX</span></span>

### <span data-ttu-id="c0d23-106">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0d23-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="c0d23-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-108">Günlük çözümlemesi</span><span class="sxs-lookup"><span data-stu-id="c0d23-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="c0d23-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="c0d23-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d23-111">Loganalyzer Ticsbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="c0d23-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d23-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0d23-112">DESCRIPTION</span></span>
<span data-ttu-id="c0d23-113">**Get-AzSqlDatabaseAuditing** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="c0d23-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="c0d23-114">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c0d23-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c0d23-115">Denetim günlükleri hedefi, aşağıdaki Switch parametrelerinden biri belirtilerek belirlenir: BlobStorage, LogAnalytics veya EventHub (hiçbiri belirtilmemişse, varsayılan BlobStorage olur).</span><span class="sxs-lookup"><span data-stu-id="c0d23-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="c0d23-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0d23-116">EXAMPLES</span></span>

### <span data-ttu-id="c0d23-117">Örnek 1: Azure SQL veritabanının BLOB depolama denetimi ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c0d23-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="c0d23-118">Örnek 2: Azure SQL veritabanının BLOB depolama denetimi ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c0d23-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="c0d23-119">Örnek 3: bir Azure SQL veritabanının BLOB depolama denetimi ayarları</span><span class="sxs-lookup"><span data-stu-id="c0d23-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="c0d23-120">Örnek 4: Azure SQL veritabanının Olay Hub denetimini alma</span><span class="sxs-lookup"><span data-stu-id="c0d23-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="c0d23-121">Örnek 5: bir Azure SQL veritabanının Olay Hub denetimini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c0d23-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="c0d23-122">Örnek 6: Azure SQL veritabanının Log Analytics denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c0d23-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="c0d23-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0d23-123">PARAMETERS</span></span>

### <span data-ttu-id="c0d23-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="c0d23-124">-BlobStorage</span></span>
<span data-ttu-id="c0d23-125">Denetim günlükleri hedefinin blob depolaması olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="c0d23-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0d23-126">-DatabaseName</span></span>
<span data-ttu-id="c0d23-127">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="c0d23-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d23-128">-DefaultProfile</span></span>
<span data-ttu-id="c0d23-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0d23-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d23-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c0d23-130">-EventHub</span></span>
<span data-ttu-id="c0d23-131">Denetim günlükleri hedefinin Olay Hub olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="c0d23-131">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0d23-132">-InputObject</span></span>
<span data-ttu-id="c0d23-133">Denetim ilkesini yönetmek için veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c0d23-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="c0d23-134">-LogAnalytics</span></span>
<span data-ttu-id="c0d23-135">Denetim günlükleri hedefinin Günlük Analizi olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="c0d23-135">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d23-136">-ResourceGroupName</span></span>
<span data-ttu-id="c0d23-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c0d23-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c0d23-138">-ServerName</span></span>
<span data-ttu-id="c0d23-139">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="c0d23-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0d23-140">-Confirm</span></span>
<span data-ttu-id="c0d23-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0d23-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d23-142">-WhatIf</span></span>
<span data-ttu-id="c0d23-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0d23-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0d23-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0d23-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d23-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d23-145">CommonParameters</span></span>
<span data-ttu-id="c0d23-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0d23-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d23-147">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0d23-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d23-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0d23-148">INPUTS</span></span>

### <span data-ttu-id="c0d23-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d23-149">System.String</span></span>

### <span data-ttu-id="c0d23-150">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="c0d23-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="c0d23-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0d23-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0d23-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0d23-152">OUTPUTS</span></span>

### <span data-ttu-id="c0d23-153">Microsoft. Azure. Commands. Sql. Auditing. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="c0d23-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="c0d23-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0d23-154">NOTES</span></span>

## <span data-ttu-id="c0d23-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0d23-155">RELATED LINKS</span></span>
