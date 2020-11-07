---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758803"
---
# <span data-ttu-id="a792a-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a792a-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="a792a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a792a-102">SYNOPSIS</span></span>
<span data-ttu-id="a792a-103">Azure SQL veritabanı için denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a792a-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="a792a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a792a-104">SYNTAX</span></span>

### <span data-ttu-id="a792a-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a792a-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-106">Storageaccountsubscriptionıdset</span><span class="sxs-lookup"><span data-stu-id="a792a-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="a792a-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-108">Günlük çözümlemesi</span><span class="sxs-lookup"><span data-stu-id="a792a-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a792a-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-110">Storageaccountsubscriptionıdbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="a792a-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a792a-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a792a-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a792a-112">Loganalyzer Ticsbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="a792a-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a792a-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="a792a-113">DESCRIPTION</span></span>
<span data-ttu-id="a792a-114">**Set-AzSqlDatabaseAuditing** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a792a-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="a792a-115">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a792a-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a792a-116">Denetim günlükleri hedefi, aşağıdaki Switch parametrelerinden biri belirtilerek belirlenir: BlobStorage, LogAnalytics veya EventHub (hiçbiri belirtilmemişse, varsayılan BlobStorage olur).</span><span class="sxs-lookup"><span data-stu-id="a792a-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="a792a-117">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a792a-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="a792a-118">Denetim günlükleri hedefi BLOB depolama olduğunda, denetim günlüklerinin depolama hesabını belirlemek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a792a-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="a792a-119">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a792a-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="a792a-120">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , veritabanı tanımlayıcılarına ek olarak geçerli denetleme ayarlarını açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a792a-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="a792a-121">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="a792a-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="a792a-122">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a792a-122">EXAMPLES</span></span>

### <span data-ttu-id="a792a-123">Örnek 1: Azure SQL veritabanının BLOB depolama denetimi ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a792a-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="a792a-124">Örnek 2: Azure SQL veritabanının BLOB depolama denetimi ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a792a-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="a792a-125">Örnek 3: farklı bir abonelikten depolama hesabı kullanarak Azure SQL veritabanının BLOB depolama alanı Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a792a-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="a792a-126">Örnek 4: bir T-SQL koşulunu kullanarak, Gelişmiş filtreleme ile bir Azure SQL veritabanının BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a792a-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="a792a-127">Örnek 5: bir Azure SQL veritabanının BLOB depolama alanı denetleme ilkesinden Gelişmiş filtreleme ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a792a-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="a792a-128">Örnek 6: bir Azure SQL veritabanının Olay Hub denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a792a-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="a792a-129">Örnek 7: Azure SQL veritabanının Olay Hub denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a792a-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="a792a-130">Örnek 8: Azure SQL veritabanının Log Analytics denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a792a-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="a792a-131">Örnek 9: Azure SQL veritabanının Log Analytics denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a792a-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="a792a-132">Örnek 10: Azure SQL veritabanının günlük Analizi denetim ilkesini ardışık düzen aracılığıyla devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a792a-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="a792a-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a792a-133">PARAMETERS</span></span>

### <span data-ttu-id="a792a-134">-Iş</span><span class="sxs-lookup"><span data-stu-id="a792a-134">-AsJob</span></span>
<span data-ttu-id="a792a-135">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a792a-135">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="a792a-136">-AuditAction</span></span>
<span data-ttu-id="a792a-137">Denetim eylemleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="a792a-137">The set of audit actions.</span></span>  
<span data-ttu-id="a792a-138">Denetlenecek desteklenen eylemler:</span><span class="sxs-lookup"><span data-stu-id="a792a-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="a792a-139">SEÇMESINI</span><span class="sxs-lookup"><span data-stu-id="a792a-139">SELECT</span></span>  
<span data-ttu-id="a792a-140">GÜNCELLEŞTIREMEDI</span><span class="sxs-lookup"><span data-stu-id="a792a-140">UPDATE</span></span>  
<span data-ttu-id="a792a-141">EKLEMEYE</span><span class="sxs-lookup"><span data-stu-id="a792a-141">INSERT</span></span>  
<span data-ttu-id="a792a-142">SILME</span><span class="sxs-lookup"><span data-stu-id="a792a-142">DELETE</span></span>  
<span data-ttu-id="a792a-143">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="a792a-143">EXECUTE</span></span>  
<span data-ttu-id="a792a-144">ALıP</span><span class="sxs-lookup"><span data-stu-id="a792a-144">RECEIVE</span></span>  
<span data-ttu-id="a792a-145">Bir eylemin denetlenmesi için genel forma başvurur: [nesne] ÜZERINDEKI [eylem], yukarıdaki biçimde, tablo, görünüm veya saklı yordam gibi bir nesneye veya tüm veritabanı veya şemaya başvuruda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="a792a-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="a792a-146">Son durumlarda, sırasıyla formlar VERITABANı: [dbname] ve şema:: [SchemaName] kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a792a-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="a792a-147">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="a792a-147">For example:</span></span>  
<span data-ttu-id="a792a-148">Dbo. myTable ' de genel olarak seçme</span><span class="sxs-lookup"><span data-stu-id="a792a-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="a792a-149">VERITABANıNDA SELECT:: myDatabase on The Public by</span><span class="sxs-lookup"><span data-stu-id="a792a-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="a792a-150">ŞEMAYı seçme:: mySchema-public ile</span><span class="sxs-lookup"><span data-stu-id="a792a-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="a792a-151">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="a792a-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-152">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="a792a-152">-AuditActionGroup</span></span>
<span data-ttu-id="a792a-153">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="a792a-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="a792a-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a792a-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="a792a-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a792a-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="a792a-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a792a-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="a792a-157">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="a792a-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="a792a-158">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="a792a-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="a792a-159">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="a792a-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="a792a-160">-BlobStorage</span></span>
<span data-ttu-id="a792a-161">Denetim günlükleri hedefinin blob depolaması olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="a792a-161">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a792a-162">-DatabaseName</span></span>
<span data-ttu-id="a792a-163">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="a792a-163">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a792a-164">-DefaultProfile</span></span>
<span data-ttu-id="a792a-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a792a-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a792a-166">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a792a-166">-EventHub</span></span>
<span data-ttu-id="a792a-167">Denetim günlükleri hedefinin Olay Hub olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="a792a-167">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="a792a-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="a792a-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="a792a-169">Olay Merkezi yetkilendirme kuralı için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a792a-169">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="a792a-170">-EventHubName</span></span>
<span data-ttu-id="a792a-171">Olay Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="a792a-171">The name of the event hub.</span></span> <span data-ttu-id="a792a-172">EventHubAuthorizationRuleResourceId sağlama sırasında hiçbiri belirtilmemişse, varsayılan olay hub 'ı seçilir.</span><span class="sxs-lookup"><span data-stu-id="a792a-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-173">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a792a-173">-InputObject</span></span>
<span data-ttu-id="a792a-174">Denetim ilkesini yönetmek için veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a792a-174">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="a792a-175">-LogAnalytics</span></span>
<span data-ttu-id="a792a-176">Denetim günlükleri hedefinin Günlük Analizi olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="a792a-176">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="a792a-177">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a792a-177">-PassThru</span></span>
<span data-ttu-id="a792a-178">Cmdlet 'in yürütülmesinin sonunda denetim ilkesinin çıktısının çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="a792a-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-179">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="a792a-179">-PredicateExpression</span></span>
<span data-ttu-id="a792a-180">Denetim günlüklerini filtrelemek için kullanılan T-SQL koşulu (WHERE yan tümcesi).</span><span class="sxs-lookup"><span data-stu-id="a792a-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="a792a-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a792a-181">-ResourceGroupName</span></span>
<span data-ttu-id="a792a-182">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a792a-182">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-183">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a792a-183">-RetentionInDays</span></span>
<span data-ttu-id="a792a-184">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="a792a-184">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a792a-185">-ServerName</span></span>
<span data-ttu-id="a792a-186">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="a792a-186">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-187">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a792a-187">-State</span></span>
<span data-ttu-id="a792a-188">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="a792a-188">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a792a-189">-StorageAccountName</span></span>
<span data-ttu-id="a792a-190">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a792a-190">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-191">-Storageaccountsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a792a-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="a792a-192">Depolama hesabı abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="a792a-192">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a792a-193">-StorageKeyType</span></span>
<span data-ttu-id="a792a-194">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a792a-194">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a792a-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="a792a-196">Denetim günlükleri göndermek istediğiniz bir Log Analytics çalışma alanı için çalışma alanı KIMLIĞI (Log Analytics çalışma alanının kaynak KIMLIĞI).</span><span class="sxs-lookup"><span data-stu-id="a792a-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="a792a-197">Örnek:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="a792a-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a792a-198">-Onay</span><span class="sxs-lookup"><span data-stu-id="a792a-198">-Confirm</span></span>
<span data-ttu-id="a792a-199">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a792a-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a792a-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a792a-200">-WhatIf</span></span>
<span data-ttu-id="a792a-201">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a792a-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a792a-202">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a792a-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a792a-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a792a-203">CommonParameters</span></span>
<span data-ttu-id="a792a-204">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a792a-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a792a-205">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a792a-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a792a-206">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a792a-206">INPUTS</span></span>

### <span data-ttu-id="a792a-207">System. String</span><span class="sxs-lookup"><span data-stu-id="a792a-207">System.String</span></span>

### <span data-ttu-id="a792a-208">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="a792a-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="a792a-209">Microsoft. Azure. Commands. Sql. Auditing. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="a792a-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="a792a-210">System. String []</span><span class="sxs-lookup"><span data-stu-id="a792a-210">System.String[]</span></span>

### <span data-ttu-id="a792a-211">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a792a-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a792a-212">System. Guid</span><span class="sxs-lookup"><span data-stu-id="a792a-212">System.Guid</span></span>

### <span data-ttu-id="a792a-213">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a792a-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a792a-214">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a792a-214">OUTPUTS</span></span>

### <span data-ttu-id="a792a-215">Microsoft. Azure. Commands. Sql. Auditing. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a792a-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="a792a-216">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a792a-216">NOTES</span></span>

## <span data-ttu-id="a792a-217">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a792a-217">RELATED LINKS</span></span>
