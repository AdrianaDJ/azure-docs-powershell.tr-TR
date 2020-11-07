---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933752"
---
# <span data-ttu-id="866cd-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="866cd-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="866cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="866cd-102">SYNOPSIS</span></span>
<span data-ttu-id="866cd-103">**Önemli: Bu cmdlet kullanım dışıdır, [set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) bunu değiştiriyor.**</span><span class="sxs-lookup"><span data-stu-id="866cd-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="866cd-104">Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="866cd-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="866cd-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="866cd-105">SYNTAX</span></span>

### <span data-ttu-id="866cd-106">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="866cd-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866cd-107">Storageaccountsubscriptionıdset</span><span class="sxs-lookup"><span data-stu-id="866cd-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="866cd-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="866cd-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866cd-109">Günlük çözümlemesi</span><span class="sxs-lookup"><span data-stu-id="866cd-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866cd-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="866cd-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866cd-111">Storageaccountsubscriptionıdbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="866cd-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="866cd-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="866cd-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866cd-113">Loganalyzer Ticsbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="866cd-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="866cd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="866cd-114">DESCRIPTION</span></span>
<span data-ttu-id="866cd-115">**Set-AzSqlServerAuditing** cmdlet 'ı BIR Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="866cd-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="866cd-116">Cmdlet 'i kullanmak için, sunucuyu belirlemek üzere *Resourcegroupname* ve *ServerName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="866cd-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="866cd-117">Denetim günlükleri hedefi, aşağıdaki Switch parametrelerinden biri belirtilerek belirlenir: BlobStorage, LogAnalytics veya EventHub (hiçbiri belirtilmemişse, varsayılan BlobStorage olur).</span><span class="sxs-lookup"><span data-stu-id="866cd-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="866cd-118">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="866cd-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="866cd-119">Denetim günlükleri hedefi BLOB depolama olduğunda, denetim günlüklerinin depolama hesabını belirlemek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="866cd-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="866cd-120">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="866cd-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="866cd-121">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , sunucu tanımlayıcılarına ek olarak geçerli denetleme ayarlarını açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="866cd-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="866cd-122">Sunucu tanımlayıcıları, **Resourcegroupname** ve **ServerName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="866cd-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="866cd-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="866cd-123">EXAMPLES</span></span>

### <span data-ttu-id="866cd-124">Örnek 1: Azure SQL Server 'ın BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="866cd-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="866cd-125">Örnek 2: Azure SQL Server 'ın BLOB depolama denetimi ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="866cd-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="866cd-126">Örnek 3: farklı bir abonelikten depolama hesabı kullanarak Azure SQL Server 'ın BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="866cd-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="866cd-127">Örnek 4: bir T-SQL koşulunu kullanarak, Gelişmiş filtreleme içeren bir Azure SQL Server 'ın BLOB depolama denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="866cd-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="866cd-128">Örnek 5: bir Azure SQL Server 'ın blob denetim depolama ilkesinden Gelişmiş filtreleme ayarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="866cd-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="866cd-129">Örnek 6: Azure SQL Server 'ın Olay Hub denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="866cd-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="866cd-130">Örnek 7: Azure SQL Server 'ın Olay Hub denetimini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="866cd-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="866cd-131">Örnek 8: Azure SQL Server 'ın Log Analytics denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="866cd-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="866cd-132">Örnek 9: Azure SQL Server 'ın Log Analytics denetimi ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="866cd-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="866cd-133">Örnek 10: Azure SQL Server 'ın Günlük Analizi denetim ilkesini ardışık düzen aracılığıyla devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="866cd-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="866cd-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="866cd-134">PARAMETERS</span></span>

### <span data-ttu-id="866cd-135">-Iş</span><span class="sxs-lookup"><span data-stu-id="866cd-135">-AsJob</span></span>
<span data-ttu-id="866cd-136">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="866cd-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="866cd-137">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="866cd-137">-AuditActionGroup</span></span>
<span data-ttu-id="866cd-138">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="866cd-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="866cd-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="866cd-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="866cd-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="866cd-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="866cd-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="866cd-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="866cd-142">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="866cd-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="866cd-143">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="866cd-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="866cd-144">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="866cd-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="866cd-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="866cd-145">-BlobStorage</span></span>
<span data-ttu-id="866cd-146">Denetim günlükleri hedefinin blob depolaması olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="866cd-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="866cd-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866cd-147">-DefaultProfile</span></span>
<span data-ttu-id="866cd-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="866cd-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866cd-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="866cd-149">-EventHub</span></span>
<span data-ttu-id="866cd-150">Denetim günlükleri hedefinin Olay Hub olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="866cd-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="866cd-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="866cd-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="866cd-152">Olay Merkezi yetkilendirme kuralı için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="866cd-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="866cd-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="866cd-153">-EventHubName</span></span>
<span data-ttu-id="866cd-154">Olay Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="866cd-154">The name of the event hub.</span></span> <span data-ttu-id="866cd-155">EventHubAuthorizationRuleResourceId sağlama sırasında hiçbiri belirtilmemişse, varsayılan olay hub 'ı seçilir.</span><span class="sxs-lookup"><span data-stu-id="866cd-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="866cd-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="866cd-156">-InputObject</span></span>
<span data-ttu-id="866cd-157">Denetim ilkesini yönetmek için sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="866cd-157">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866cd-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="866cd-158">-LogAnalytics</span></span>
<span data-ttu-id="866cd-159">Denetim günlükleri hedefinin Günlük Analizi olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="866cd-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="866cd-160">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="866cd-160">-PassThru</span></span>
<span data-ttu-id="866cd-161">Cmdlet 'in yürütülmesinin sonunda denetim ilkesinin çıktısının çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="866cd-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="866cd-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="866cd-162">-PredicateExpression</span></span>
<span data-ttu-id="866cd-163">Denetim günlüklerini filtrelemek için kullanılan T-SQL koşulu (WHERE yan tümcesi).</span><span class="sxs-lookup"><span data-stu-id="866cd-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="866cd-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866cd-164">-ResourceGroupName</span></span>
<span data-ttu-id="866cd-165">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="866cd-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="866cd-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="866cd-166">-RetentionInDays</span></span>
<span data-ttu-id="866cd-167">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="866cd-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="866cd-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="866cd-168">-ServerName</span></span>
<span data-ttu-id="866cd-169">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="866cd-169">SQL server name.</span></span>

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

### <span data-ttu-id="866cd-170">Durumlu</span><span class="sxs-lookup"><span data-stu-id="866cd-170">-State</span></span>
<span data-ttu-id="866cd-171">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="866cd-171">The state of the policy.</span></span>

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

### <span data-ttu-id="866cd-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="866cd-172">-StorageAccountName</span></span>
<span data-ttu-id="866cd-173">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="866cd-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="866cd-174">-Storageaccountsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="866cd-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="866cd-175">Depolama hesabı abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="866cd-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="866cd-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="866cd-176">-StorageKeyType</span></span>
<span data-ttu-id="866cd-177">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="866cd-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="866cd-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="866cd-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="866cd-179">Denetim günlükleri göndermek istediğiniz bir Log Analytics çalışma alanı için çalışma alanı KIMLIĞI (Log Analytics çalışma alanının kaynak KIMLIĞI).</span><span class="sxs-lookup"><span data-stu-id="866cd-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="866cd-180">Örnek:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="866cd-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="866cd-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="866cd-181">-Confirm</span></span>
<span data-ttu-id="866cd-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="866cd-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866cd-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866cd-183">-WhatIf</span></span>
<span data-ttu-id="866cd-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="866cd-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="866cd-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="866cd-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866cd-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866cd-186">CommonParameters</span></span>
<span data-ttu-id="866cd-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="866cd-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866cd-188">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="866cd-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866cd-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="866cd-189">INPUTS</span></span>

### <span data-ttu-id="866cd-190">System. String</span><span class="sxs-lookup"><span data-stu-id="866cd-190">System.String</span></span>

### <span data-ttu-id="866cd-191">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="866cd-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="866cd-192">Microsoft. Azure. Commands. Sql. Auditing. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="866cd-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="866cd-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="866cd-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="866cd-194">System. Guid</span><span class="sxs-lookup"><span data-stu-id="866cd-194">System.Guid</span></span>

### <span data-ttu-id="866cd-195">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="866cd-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="866cd-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="866cd-196">OUTPUTS</span></span>

### <span data-ttu-id="866cd-197">Microsoft. Azure. Commands. Sql. Auditing. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="866cd-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="866cd-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="866cd-198">NOTES</span></span>

## <span data-ttu-id="866cd-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="866cd-199">RELATED LINKS</span></span>
