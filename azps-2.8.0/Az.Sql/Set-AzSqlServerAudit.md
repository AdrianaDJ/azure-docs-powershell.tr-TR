---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8601be969ce08c86a723af51e82be89125367d4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933699"
---
# <span data-ttu-id="7ca3e-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7ca3e-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="7ca3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca3e-103">Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="7ca3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ca3e-104">SYNTAX</span></span>

### <span data-ttu-id="7ca3e-105">Sunucuparametrekümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ca3e-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca3e-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca3e-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ca3e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ca3e-107">DESCRIPTION</span></span>
<span data-ttu-id="7ca3e-108">**Set-AzSqlServerAudit** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="7ca3e-109">Cmdlet 'i kullanmak için, sunucuyu belirlemek üzere *Resourcegroupname* ve *ServerName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="7ca3e-110">BLOB depolama alanı denetim günlükleri için bir hedef olduğunda, denetim günlüklerinin depolama hesabını belirlemek için *Storageaccountresourceıd* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7ca3e-111">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="7ca3e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ca3e-112">EXAMPLES</span></span>

### <span data-ttu-id="7ca3e-113">Örnek 1: Azure SQL Server 'ın BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7ca3e-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="7ca3e-114">Örnek 2: Azure SQL Server 'ın BLOB depolama denetimi ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ca3e-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7ca3e-115">Örnek 3,1: bir T-SQL koşulunu kullanarak, Gelişmiş filtreleme içeren bir Azure SQL Server 'ın BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7ca3e-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="7ca3e-116">Örnek 3,2: bir Azure SQL Server 'ın denetim ilkesinden Gelişmiş filtreleme ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7ca3e-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="7ca3e-117">Örnek 4: Azure SQL Server 'ın Olay Hub denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7ca3e-117">Example 4: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7ca3e-118">Örnek 5: Azure SQL Server 'ın Olay Hub denetimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ca3e-118">Example 5: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="7ca3e-119">Örnek 6: Azure SQL Server 'ın Log Analytics denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7ca3e-119">Example 6: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7ca3e-120">Örnek 7: Azure SQL Server 'ın Log Analytics denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ca3e-120">Example 7: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7ca3e-121">Örnek 8: Azure SQL Server 'ın Günlük Analizi denetim ilkesini ardışık düzen ile devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7ca3e-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="7ca3e-122">Örnek 9: Azure SQL Server 'ın kayıtlarını BLOB depolama alanına göndermeyi devre dışı bırakın ve bunları Log Analytics 'e göndermeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-122">Example 9: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="7ca3e-123">Örnek 10: Azure SQL Server 'ın denetim kayıtlarını BLOB depolama, Olay Hub 'ı ve Log Analytics 'e göndermeyi etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-123">Example 10: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="7ca3e-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ca3e-124">PARAMETERS</span></span>

### <span data-ttu-id="7ca3e-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ca3e-125">-AsJob</span></span>
<span data-ttu-id="7ca3e-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ca3e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ca3e-127">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="7ca3e-127">-AuditActionGroup</span></span>
<span data-ttu-id="7ca3e-128">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="7ca3e-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7ca3e-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7ca3e-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7ca3e-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7ca3e-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7ca3e-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7ca3e-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7ca3e-132">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7ca3e-133">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7ca3e-134">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7ca3e-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="7ca3e-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="7ca3e-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="7ca3e-136">Blob deposunun denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="7ca3e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca3e-137">-DefaultProfile</span></span>
<span data-ttu-id="7ca3e-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca3e-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca3e-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7ca3e-140">Olay Merkezi yetkilendirme kuralı için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7ca3e-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="7ca3e-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7ca3e-141">-EventHubName</span></span>
<span data-ttu-id="7ca3e-142">Olay Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-142">The name of the event hub.</span></span> <span data-ttu-id="7ca3e-143">EventHubAuthorizationRuleResourceId sağlama sırasında hiçbiri belirtilmemişse, varsayılan olay hub 'ı seçilir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="7ca3e-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="7ca3e-144">-EventHubTargetState</span></span>
<span data-ttu-id="7ca3e-145">Olay Hub 'ının denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="7ca3e-146">-Loganalyzer Ticstargetstate</span><span class="sxs-lookup"><span data-stu-id="7ca3e-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="7ca3e-147">Log Analytics 'in denetim kayıtları için bir hedef olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="7ca3e-148">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7ca3e-148">-PassThru</span></span>
<span data-ttu-id="7ca3e-149">Cmdlet 'in yürütülmesinin sonunda denetim ilkesinin çıktısının çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="7ca3e-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7ca3e-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7ca3e-150">-PredicateExpression</span></span>
<span data-ttu-id="7ca3e-151">Denetim günlüklerini filtrelemek için kullanılan T-SQL koşulu (WHERE yan tümcesi).</span><span class="sxs-lookup"><span data-stu-id="7ca3e-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="7ca3e-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca3e-152">-ResourceGroupName</span></span>
<span data-ttu-id="7ca3e-153">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca3e-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7ca3e-154">-RetentionInDays</span></span>
<span data-ttu-id="7ca3e-155">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="7ca3e-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ca3e-156">-ServerName</span></span>
<span data-ttu-id="7ca3e-157">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca3e-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="7ca3e-158">-ServerObject</span></span>
<span data-ttu-id="7ca3e-159">Denetim ilkesini yönetmek için sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca3e-160">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="7ca3e-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="7ca3e-161">Depolama hesabı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7ca3e-161">The storage account resource id</span></span>

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

### <span data-ttu-id="7ca3e-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7ca3e-162">-StorageKeyType</span></span>
<span data-ttu-id="7ca3e-163">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="7ca3e-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca3e-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="7ca3e-165">Denetim günlükleri göndermek istediğiniz bir Log Analytics çalışma alanı için çalışma alanı KIMLIĞI (Log Analytics çalışma alanının kaynak KIMLIĞI).</span><span class="sxs-lookup"><span data-stu-id="7ca3e-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7ca3e-166">Örnek:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7ca3e-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="7ca3e-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ca3e-167">-Confirm</span></span>
<span data-ttu-id="7ca3e-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca3e-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca3e-169">-WhatIf</span></span>
<span data-ttu-id="7ca3e-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ca3e-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca3e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca3e-172">CommonParameters</span></span>
<span data-ttu-id="7ca3e-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca3e-174">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7ca3e-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca3e-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ca3e-175">INPUTS</span></span>

### <span data-ttu-id="7ca3e-176">System. String</span><span class="sxs-lookup"><span data-stu-id="7ca3e-176">System.String</span></span>

### <span data-ttu-id="7ca3e-177">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="7ca3e-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="7ca3e-178">Microsoft. Azure. Commands. Sql. Auditing. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="7ca3e-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7ca3e-179">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7ca3e-179">System.Guid</span></span>

### <span data-ttu-id="7ca3e-180">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ca3e-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7ca3e-181">Microsoft. Azure. Commands. Sql. Auditing. model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="7ca3e-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="7ca3e-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ca3e-182">OUTPUTS</span></span>

### <span data-ttu-id="7ca3e-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ca3e-183">System.Boolean</span></span>

## <span data-ttu-id="7ca3e-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ca3e-184">NOTES</span></span>

## <span data-ttu-id="7ca3e-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ca3e-185">RELATED LINKS</span></span>
