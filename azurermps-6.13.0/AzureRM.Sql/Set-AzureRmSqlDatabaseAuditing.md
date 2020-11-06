---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588033"
---
# <span data-ttu-id="f83cf-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="f83cf-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="f83cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f83cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f83cf-103">Azure SQL veritabanı için denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f83cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f83cf-104">SYNTAX</span></span>

### <span data-ttu-id="f83cf-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f83cf-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f83cf-106">Storageaccountsubscriptionıdset</span><span class="sxs-lookup"><span data-stu-id="f83cf-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f83cf-107">DESCRIPTION</span></span>
<span data-ttu-id="f83cf-108">**Set-AzureRmSqlDatabaseAuditing** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f83cf-109">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f83cf-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f83cf-110">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f83cf-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="f83cf-111">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f83cf-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="f83cf-112">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f83cf-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="f83cf-113">Cmdlet başarıyla çalıştıktan sonra, veritabanının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="f83cf-114">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , veritabanı tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f83cf-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="f83cf-115">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="f83cf-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f83cf-116">EXAMPLES</span></span>

### <span data-ttu-id="f83cf-117">Örnek 1: Azure SQL veritabanının Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f83cf-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="f83cf-118">Örnek 2: Azure SQL veritabanının blob denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f83cf-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="f83cf-119">Örnek 3: farklı bir abonelikten depolama hesabı kullanarak Azure SQL veritabanının Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f83cf-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="f83cf-120">Örnek 4: bir Azure SQL veritabanının genişletilmiş denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f83cf-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="f83cf-121">Örnek 5: bir Azure SQL veritabanının genişletilmiş denetim ilkesini kaldırın ve bunun yerine denetim ilkesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f83cf-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="f83cf-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f83cf-122">PARAMETERS</span></span>

### <span data-ttu-id="f83cf-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="f83cf-123">-AuditAction</span></span>
<span data-ttu-id="f83cf-124">Denetim eylemleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="f83cf-124">The set of audit actions.</span></span>
<span data-ttu-id="f83cf-125">Denetlenecek desteklenen eylemler: SELECT Ekle SIL 'i SEÇIN yürütme alma BAŞVURULARı, [nesne] ÜZERINDEKI [eylem], yukarıdaki biçimde, bir tablo, görünüm veya saklı yordam gibi bir nesneye ya da tüm veritabanı veya şemaya başvuruda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="f83cf-126">Son durumlarda, sırasıyla formlar VERITABANı: [dbname] ve şema:: [SchemaName] kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f83cf-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="f83cf-127">Örneğin: dbo. myTable ' de genel olarak Select VERITABANıNDA Select:: myDatabase: myDatabase https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions</span><span class="sxs-lookup"><span data-stu-id="f83cf-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="f83cf-128">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="f83cf-128">-AuditActionGroup</span></span>
<span data-ttu-id="f83cf-129">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="f83cf-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="f83cf-130">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="f83cf-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="f83cf-131">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="f83cf-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f83cf-132">-DatabaseName</span></span>
<span data-ttu-id="f83cf-133">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="f83cf-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83cf-134">-DefaultProfile</span></span>
<span data-ttu-id="f83cf-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f83cf-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f83cf-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f83cf-136">-PassThru</span></span>
<span data-ttu-id="f83cf-137">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f83cf-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="f83cf-138">-PredicateExpression</span></span>
<span data-ttu-id="f83cf-139">Denetim günlüklerini filtrelemek için kullanılan where yan tümcesinin ifadesi.</span><span class="sxs-lookup"><span data-stu-id="f83cf-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="f83cf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83cf-140">-ResourceGroupName</span></span>
<span data-ttu-id="f83cf-141">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f83cf-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="f83cf-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f83cf-142">-RetentionInDays</span></span>
<span data-ttu-id="f83cf-143">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="f83cf-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f83cf-144">-ServerName</span></span>
<span data-ttu-id="f83cf-145">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="f83cf-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-146">Durumlu</span><span class="sxs-lookup"><span data-stu-id="f83cf-146">-State</span></span>
<span data-ttu-id="f83cf-147">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="f83cf-147">The state of the policy.</span></span>

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

### <span data-ttu-id="f83cf-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f83cf-148">-StorageAccountName</span></span>
<span data-ttu-id="f83cf-149">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="f83cf-149">The name of the storage account.</span></span> <span data-ttu-id="f83cf-150">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="f83cf-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="f83cf-151">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-151">This parameter is not required.</span></span>
<span data-ttu-id="f83cf-152">Bu parametreyi belirtmezseniz cmdlet, daha önce denetim ilkesinin bir parçası olarak tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="f83cf-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="f83cf-153">Bu, denetim ilkesinin ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="f83cf-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-154">-Storageaccountsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="f83cf-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="f83cf-155">Depolama hesabı aboneliği kimliğini belirtir</span><span class="sxs-lookup"><span data-stu-id="f83cf-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f83cf-156">-StorageKeyType</span></span>
<span data-ttu-id="f83cf-157">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="f83cf-158">-Confirm</span></span>
<span data-ttu-id="f83cf-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f83cf-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83cf-160">-WhatIf</span></span>
<span data-ttu-id="f83cf-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f83cf-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f83cf-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f83cf-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83cf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83cf-163">CommonParameters</span></span>
<span data-ttu-id="f83cf-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f83cf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83cf-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83cf-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83cf-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f83cf-166">INPUTS</span></span>

## <span data-ttu-id="f83cf-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f83cf-167">OUTPUTS</span></span>

## <span data-ttu-id="f83cf-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f83cf-168">NOTES</span></span>

## <span data-ttu-id="f83cf-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f83cf-169">RELATED LINKS</span></span>
