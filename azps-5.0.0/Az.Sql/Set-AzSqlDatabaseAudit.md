---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278801"
---
# <span data-ttu-id="7f46f-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7f46f-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="7f46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f46f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f46f-103">Azure SQL veritabanı için denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="7f46f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f46f-104">SYNTAX</span></span>

### <span data-ttu-id="7f46f-105">DatabaseParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f46f-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f46f-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f46f-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f46f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f46f-107">DESCRIPTION</span></span>
<span data-ttu-id="7f46f-108">**Set-AzSqlDatabaseAudit** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7f46f-109">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7f46f-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7f46f-110">BLOB depolama alanı denetim günlükleri için bir hedef olduğunda, denetim günlüklerinin depolama hesabını belirlemek için *Storageaccountresourceıd* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f46f-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7f46f-111">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f46f-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="7f46f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f46f-112">EXAMPLES</span></span>

### <span data-ttu-id="7f46f-113">Örnek 1: Azure SQL veritabanının BLOB depolama denetimi ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7f46f-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="7f46f-114">Örnek 2: Azure SQL veritabanının BLOB depolama denetimi ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f46f-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7f46f-115">Örnek 3: bir T-SQL koşulunu kullanarak, Gelişmiş filtreleme ile bir Azure SQL veritabanının BLOB depolama alanı Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7f46f-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="7f46f-116">Örnek 4: bir Azure SQL veritabanının denetim ilkesinden Gelişmiş filtreleme ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7f46f-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="7f46f-117">Örnek 5: Azure SQL veritabanının Olay Hub denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7f46f-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7f46f-118">Örnek 6: Azure SQL veritabanının Olay Hub denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f46f-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="7f46f-119">Örnek 7: Azure SQL veritabanının Log Analytics denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7f46f-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7f46f-120">Örnek 8: Azure SQL veritabanının Log Analytics denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f46f-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7f46f-121">Örnek 9: bir Azure SQL veritabanının günlük Analizi denetim ilkesini ardışık düzen aracılığıyla devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7f46f-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7f46f-122">Örnek 10: Azure SQL veritabanının kayıtlarını BLOB depolama alanına göndermeyi devre dışı bırakın ve bunları günlük Analizi 'ne göndermeyi etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7f46f-123">Örnek 11: Azure SQL veritabanının denetim kayıtlarını BLOB depolama, Olay Hub 'ı ve Log Analytics 'e göndermeyi etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="7f46f-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="7f46f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f46f-124">PARAMETERS</span></span>

### <span data-ttu-id="7f46f-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7f46f-125">-AuditAction</span></span>
<span data-ttu-id="7f46f-126">Denetim eylemleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="7f46f-126">The set of audit actions.</span></span>  
<span data-ttu-id="7f46f-127">Denetlenecek desteklenen eylemler:</span><span class="sxs-lookup"><span data-stu-id="7f46f-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="7f46f-128">SEÇMESINI</span><span class="sxs-lookup"><span data-stu-id="7f46f-128">SELECT</span></span>  
<span data-ttu-id="7f46f-129">GÜNCELLEŞTIREMEDI</span><span class="sxs-lookup"><span data-stu-id="7f46f-129">UPDATE</span></span>  
<span data-ttu-id="7f46f-130">EKLEMEYE</span><span class="sxs-lookup"><span data-stu-id="7f46f-130">INSERT</span></span>  
<span data-ttu-id="7f46f-131">SILME</span><span class="sxs-lookup"><span data-stu-id="7f46f-131">DELETE</span></span>  
<span data-ttu-id="7f46f-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="7f46f-132">EXECUTE</span></span>  
<span data-ttu-id="7f46f-133">ALıP</span><span class="sxs-lookup"><span data-stu-id="7f46f-133">RECEIVE</span></span>  
<span data-ttu-id="7f46f-134">BULUNUYOR</span><span class="sxs-lookup"><span data-stu-id="7f46f-134">REFERENCES</span></span>  
<span data-ttu-id="7f46f-135">Denetlenecek eylemi tanımlayan genel form: [nesne] ÜZERINDEKI [eylem], yukarıdaki biçimde, tablo, görünüm veya saklı yordam gibi bir nesneye ya da tüm veritabanı veya şemaya başvuruda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="7f46f-136">Son durumlarda, sırasıyla formlar VERITABANı: [dbname] ve şema:: [SchemaName] kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7f46f-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="7f46f-137">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7f46f-137">For example:</span></span>  
<span data-ttu-id="7f46f-138">Dbo. myTable ' de genel olarak seçme</span><span class="sxs-lookup"><span data-stu-id="7f46f-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="7f46f-139">VERITABANıNDA SELECT:: myDatabase on The Public by</span><span class="sxs-lookup"><span data-stu-id="7f46f-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="7f46f-140">ŞEMAYı seçme:: mySchema-public ile</span><span class="sxs-lookup"><span data-stu-id="7f46f-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="7f46f-141">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="7f46f-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-142">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="7f46f-142">-AuditActionGroup</span></span>
<span data-ttu-id="7f46f-143">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="7f46f-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7f46f-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7f46f-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7f46f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7f46f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7f46f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7f46f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7f46f-147">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="7f46f-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7f46f-148">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="7f46f-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7f46f-149">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7f46f-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="7f46f-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="7f46f-151">Blob deposunun denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f46f-152">-DatabaseName</span></span>
<span data-ttu-id="7f46f-153">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="7f46f-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7f46f-154">-DatabaseObject</span></span>
<span data-ttu-id="7f46f-155">Denetim ilkesini yönetmek için veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f46f-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f46f-156">-DefaultProfile</span></span>
<span data-ttu-id="7f46f-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f46f-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f46f-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7f46f-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7f46f-159">Olay Merkezi yetkilendirme kuralı için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7f46f-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7f46f-160">-EventHubName</span></span>
<span data-ttu-id="7f46f-161">Olay Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="7f46f-161">The name of the event hub.</span></span> <span data-ttu-id="7f46f-162">EventHubAuthorizationRuleResourceId sağlama sırasında hiçbiri belirtilmemişse, varsayılan olay hub 'ı seçilir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="7f46f-163">-EventHubTargetState</span></span>
<span data-ttu-id="7f46f-164">Olay Hub 'ının denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-165">-Loganalyzer Ticstargetstate</span><span class="sxs-lookup"><span data-stu-id="7f46f-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="7f46f-166">Log Analytics 'in denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-167">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7f46f-167">-PassThru</span></span>
<span data-ttu-id="7f46f-168">Cmdlet 'in yürütülmesinin sonunda denetim ilkesinin çıktısının çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="7f46f-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7f46f-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7f46f-169">-PredicateExpression</span></span>
<span data-ttu-id="7f46f-170">Denetim günlüklerini filtrelemek için kullanılan T-SQL koşulu (WHERE yan tümcesi).</span><span class="sxs-lookup"><span data-stu-id="7f46f-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f46f-171">-ResourceGroupName</span></span>
<span data-ttu-id="7f46f-172">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7f46f-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7f46f-173">-RetentionInDays</span></span>
<span data-ttu-id="7f46f-174">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="7f46f-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f46f-175">-ServerName</span></span>
<span data-ttu-id="7f46f-176">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="7f46f-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-177">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="7f46f-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="7f46f-178">Depolama hesabı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7f46f-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7f46f-179">-StorageKeyType</span></span>
<span data-ttu-id="7f46f-180">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7f46f-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="7f46f-182">Denetim günlükleri göndermek istediğiniz bir Log Analytics çalışma alanı için çalışma alanı KIMLIĞI (Log Analytics çalışma alanının kaynak KIMLIĞI).</span><span class="sxs-lookup"><span data-stu-id="7f46f-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7f46f-183">Örnek:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7f46f-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f46f-184">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f46f-184">-Confirm</span></span>
<span data-ttu-id="7f46f-185">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f46f-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f46f-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f46f-186">-WhatIf</span></span>
<span data-ttu-id="7f46f-187">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f46f-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f46f-188">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f46f-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f46f-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f46f-189">CommonParameters</span></span>
<span data-ttu-id="7f46f-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f46f-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f46f-191">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f46f-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f46f-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f46f-192">INPUTS</span></span>

### <span data-ttu-id="7f46f-193">System. String</span><span class="sxs-lookup"><span data-stu-id="7f46f-193">System.String</span></span>

### <span data-ttu-id="7f46f-194">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="7f46f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="7f46f-195">Microsoft. Azure. Commands. Sql. Auditing. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="7f46f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7f46f-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f46f-196">System.String[]</span></span>

### <span data-ttu-id="7f46f-197">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7f46f-197">System.Guid</span></span>

### <span data-ttu-id="7f46f-198">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="7f46f-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7f46f-199">Microsoft. Azure. Commands. Sql. Auditing. model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="7f46f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="7f46f-200">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f46f-200">OUTPUTS</span></span>

### <span data-ttu-id="7f46f-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f46f-201">System.Boolean</span></span>

## <span data-ttu-id="7f46f-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f46f-202">NOTES</span></span>

## <span data-ttu-id="7f46f-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f46f-203">RELATED LINKS</span></span>
