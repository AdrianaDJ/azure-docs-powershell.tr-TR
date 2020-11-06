---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588713"
---
# <span data-ttu-id="a5979-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="a5979-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="a5979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5979-102">SYNOPSIS</span></span>
<span data-ttu-id="a5979-103">Azure SQL veritabanı için denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5979-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5979-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5979-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5979-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5979-105">DESCRIPTION</span></span>
<span data-ttu-id="a5979-106">**Set-AzureRmSqlDatabaseAuditing** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a5979-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="a5979-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a5979-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a5979-108">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a5979-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="a5979-109">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5979-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="a5979-110">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5979-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="a5979-111">Cmdlet başarıyla çalıştıktan sonra, veritabanının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a5979-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="a5979-112">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , veritabanı tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5979-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="a5979-113">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="a5979-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="a5979-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5979-114">EXAMPLES</span></span>

### <span data-ttu-id="a5979-115">Örnek 1: Azure SQL veritabanının Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a5979-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="a5979-116">Örnek 2: Azure SQL veritabanının blob denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a5979-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="a5979-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5979-117">PARAMETERS</span></span>

### <span data-ttu-id="a5979-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="a5979-118">-AuditAction</span></span>
<span data-ttu-id="a5979-119">Denetim eylemleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="a5979-119">The set of audit actions.</span></span>  
<span data-ttu-id="a5979-120">Denetlenecek desteklenen eylemler:</span><span class="sxs-lookup"><span data-stu-id="a5979-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="a5979-121">SEÇMESINI</span><span class="sxs-lookup"><span data-stu-id="a5979-121">SELECT</span></span>  
<span data-ttu-id="a5979-122">GÜNCELLEŞTIREMEDI</span><span class="sxs-lookup"><span data-stu-id="a5979-122">UPDATE</span></span>  
<span data-ttu-id="a5979-123">EKLEMEYE</span><span class="sxs-lookup"><span data-stu-id="a5979-123">INSERT</span></span>  
<span data-ttu-id="a5979-124">SILME</span><span class="sxs-lookup"><span data-stu-id="a5979-124">DELETE</span></span>  
<span data-ttu-id="a5979-125">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="a5979-125">EXECUTE</span></span>  
<span data-ttu-id="a5979-126">ALıP</span><span class="sxs-lookup"><span data-stu-id="a5979-126">RECEIVE</span></span>  
<span data-ttu-id="a5979-127">BULUNUYOR</span><span class="sxs-lookup"><span data-stu-id="a5979-127">REFERENCES</span></span>  

<span data-ttu-id="a5979-128">Denetlenecek eylemi tanımlamaya yönelik genel form:</span><span class="sxs-lookup"><span data-stu-id="a5979-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="a5979-129">eylemle [Nesne] ON [Principal]</span><span class="sxs-lookup"><span data-stu-id="a5979-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="a5979-130">Yukarıdaki biçimdeki [Object] ' in, tablo, görünüm veya saklı yordam gibi bir nesneye veya tüm veritabanı veya şemaya başvuruda bulunduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a5979-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="a5979-131">Son durumlarda, sırasıyla formlar VERITABANı: [dbname] ve şema:: [SchemaName] kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a5979-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="a5979-132">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="a5979-132">For example:</span></span>  
<span data-ttu-id="a5979-133">Dbo. myTable ' de genel olarak seçme</span><span class="sxs-lookup"><span data-stu-id="a5979-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="a5979-134">VERITABANıNDA SELECT:: myDatabase on The Public by</span><span class="sxs-lookup"><span data-stu-id="a5979-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="a5979-135">ŞEMAYı seçme:: mySchema-public ile</span><span class="sxs-lookup"><span data-stu-id="a5979-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="a5979-136">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="a5979-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-137">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="a5979-137">-AuditActionGroup</span></span>
<span data-ttu-id="a5979-138">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="a5979-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="a5979-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a5979-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="a5979-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a5979-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="a5979-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a5979-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="a5979-142">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="a5979-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="a5979-143">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="a5979-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="a5979-144">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="a5979-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5979-145">-DatabaseName</span></span>
<span data-ttu-id="a5979-146">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="a5979-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5979-147">-DefaultProfile</span></span>
<span data-ttu-id="a5979-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5979-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-149">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a5979-149">-PassThru</span></span>
<span data-ttu-id="a5979-150">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="a5979-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5979-151">-ResourceGroupName</span></span>
<span data-ttu-id="a5979-152">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5979-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a5979-153">-RetentionInDays</span></span>
<span data-ttu-id="a5979-154">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="a5979-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5979-155">-ServerName</span></span>
<span data-ttu-id="a5979-156">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="a5979-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-157">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a5979-157">-State</span></span>
<span data-ttu-id="a5979-158">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="a5979-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5979-159">-StorageAccountName</span></span>
<span data-ttu-id="a5979-160">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a5979-160">The name of the storage account.</span></span> <span data-ttu-id="a5979-161">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="a5979-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="a5979-162">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="a5979-162">This parameter is not required.</span></span>  
<span data-ttu-id="a5979-163">Bu parametreyi belirtmezseniz cmdlet, daha önce denetim ilkesinin bir parçası olarak tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5979-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="a5979-164">Bu, denetim ilkesinin ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="a5979-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a5979-165">-StorageKeyType</span></span>
<span data-ttu-id="a5979-166">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5979-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5979-167">-Confirm</span></span>
<span data-ttu-id="a5979-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5979-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5979-169">-WhatIf</span></span>
<span data-ttu-id="a5979-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5979-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5979-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5979-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5979-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5979-172">CommonParameters</span></span>
<span data-ttu-id="a5979-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5979-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5979-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5979-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5979-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5979-175">INPUTS</span></span>

### <span data-ttu-id="a5979-176">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a5979-176">None</span></span>
<span data-ttu-id="a5979-177">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a5979-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5979-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5979-178">OUTPUTS</span></span>

### <span data-ttu-id="a5979-179">Microsoft. Azure. Commands. Sql. Security. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a5979-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="a5979-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5979-180">NOTES</span></span>

## <span data-ttu-id="a5979-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5979-181">RELATED LINKS</span></span>
