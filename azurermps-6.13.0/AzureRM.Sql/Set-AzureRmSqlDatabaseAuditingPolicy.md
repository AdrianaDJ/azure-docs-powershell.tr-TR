---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588031"
---
# <span data-ttu-id="146f7-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="146f7-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="146f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="146f7-102">SYNOPSIS</span></span>
<span data-ttu-id="146f7-103">Veritabanının denetim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="146f7-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="146f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="146f7-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="146f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="146f7-105">DESCRIPTION</span></span>
<span data-ttu-id="146f7-106">**Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet 'i, BIR Azure SQL veritabanının denetim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="146f7-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="146f7-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="146f7-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="146f7-108">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="146f7-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="146f7-109">Denetim günlükleri tablosu için bekletme 'yi, *RetentionInDays* ve *tableıdentifier* parametrelerinin değerini ayarlayarak, denetim günlüğü tablo adlarının dönemini ve çekirdek değerini ayarlayarak da tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="146f7-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="146f7-110">Hangi olay türlerinin denetleneceğini tanımlayan *EventType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="146f7-110">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="146f7-111">Cmdlet başarıyla çalıştıktan sonra, veritabanının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="146f7-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="146f7-112">Tablo denetimi için veritabanı, bu cmdlet 'i çalıştırmadan önce veritabanı Denetleme ilkesini kullandıysa, denetim bu ilkeyi kullanmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="146f7-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="146f7-113">Blob denetiminde, veritabanı, bu cmdlet 'i çalıştırmadan önce veritabanı denetleme ilkesi kullandıysa, her iki denetim ilkesi de yan yana olacaktır.</span><span class="sxs-lookup"><span data-stu-id="146f7-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="146f7-114">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , veritabanı tanımlayıcılarına ek olarak geçerli denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="146f7-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="146f7-115">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="146f7-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="146f7-116">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="146f7-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="146f7-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="146f7-117">EXAMPLES</span></span>

### <span data-ttu-id="146f7-118">Örnek 1: veritabanının denetim ilkesini tablo denetimini kullanacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="146f7-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="146f7-119">Bu komut, server01 'te bulunan Database01 adlı veritabanının denetim ilkesini Storage31 adlı depolama hesabını kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="146f7-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="146f7-120">Örnek 2: bir veritabanının varolan denetim ilkesinin depolama hesabı anahtarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="146f7-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="146f7-121">Bu komut, server01 'te bulunan Database01 adlı veritabanının denetim ilkesini aynı depolama hesabı adını kullanmaya devam etmek için, ancak şimdi ikincil anahtarı kullanmaya devam etmek için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="146f7-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="146f7-122">Örnek 3: veritabanının denetim ilkesini belirli bir olay türünü kullanacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="146f7-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="146f7-123">Örnek 4: bir veritabanının denetim ilkesini blob denetimini kullanacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="146f7-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="146f7-124">Bu komut, server01 'te bulunan Database01 adlı veritabanının denetim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="146f7-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="146f7-125">İlke Login_Failure olay türünü günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="146f7-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="146f7-126">Komut depolama ayarlarını değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="146f7-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="146f7-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="146f7-127">PARAMETERS</span></span>

### <span data-ttu-id="146f7-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="146f7-128">-AuditAction</span></span>
<span data-ttu-id="146f7-129">Bir veya daha fazla denetim eylemi belirtin.</span><span class="sxs-lookup"><span data-stu-id="146f7-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="146f7-130">Bu parametre yalnızca blob denetimine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="146f7-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="146f7-131">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="146f7-131">-AuditActionGroup</span></span>
<span data-ttu-id="146f7-132">Bir veya daha fazla denetim eylem grubu belirtin.</span><span class="sxs-lookup"><span data-stu-id="146f7-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="146f7-133">Bu parametre yalnızca blob denetimine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="146f7-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="146f7-134">-AuditType</span><span class="sxs-lookup"><span data-stu-id="146f7-134">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="146f7-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="146f7-135">-DatabaseName</span></span>
<span data-ttu-id="146f7-136">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="146f7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146f7-137">-DefaultProfile</span></span>
<span data-ttu-id="146f7-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="146f7-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="146f7-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="146f7-139">-EventType</span></span>
<span data-ttu-id="146f7-140">Denetlenecek olay türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="146f7-141">Bu parametre yalnızca tablo denetimine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="146f7-141">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="146f7-142">Birçok olay türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="146f7-142">You can specify several event types.</span></span>
<span data-ttu-id="146f7-143">Tüm olay türlerini denetlemeye ve hiçbir olayın denetleneceğini belirtmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="146f7-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="146f7-144">Tümünü veya hiçbirini aynı anda belirtirseniz cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="146f7-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="146f7-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="146f7-145">-PassThru</span></span>
<span data-ttu-id="146f7-146">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="146f7-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="146f7-147">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="146f7-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="146f7-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="146f7-148">-ResourceGroupName</span></span>
<span data-ttu-id="146f7-149">Veritabanının atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="146f7-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="146f7-150">-RetentionInDays</span></span>
<span data-ttu-id="146f7-151">Denetim günlükleri tablosu için bekletme günü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="146f7-152">Sıfır (0) değeri tablonun saklanmadığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="146f7-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="146f7-153">Varsayılan değer sıfırdır.</span><span class="sxs-lookup"><span data-stu-id="146f7-153">The default value is zero.</span></span>
<span data-ttu-id="146f7-154">Sıfırdan büyük bir değer belirtirseniz, *Tableıdenkeer* parametresi için bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="146f7-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="146f7-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="146f7-155">-ServerName</span></span>
<span data-ttu-id="146f7-156">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="146f7-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="146f7-157">-StorageAccountName</span></span>
<span data-ttu-id="146f7-158">Veritabanını denetlemek için depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="146f7-159">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="146f7-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="146f7-160">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="146f7-160">This parameter is not required.</span></span>
<span data-ttu-id="146f7-161">Bu parametreyi belirtmezseniz cmdlet, önceden tanımlanmış depolama hesabını veritabanı denetim ilkesinin parçası olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="146f7-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="146f7-162">Veritabanı denetleme ilkesi ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="146f7-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="146f7-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="146f7-163">-StorageKeyType</span></span>
<span data-ttu-id="146f7-164">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="146f7-165">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="146f7-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="146f7-166">Yararı</span><span class="sxs-lookup"><span data-stu-id="146f7-166">Primary</span></span>
- <span data-ttu-id="146f7-167">İkincil varsayılan değer birincili.</span><span class="sxs-lookup"><span data-stu-id="146f7-167">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="146f7-168">-Tableıdentifier</span><span class="sxs-lookup"><span data-stu-id="146f7-168">-TableIdentifier</span></span>
<span data-ttu-id="146f7-169">Denetim günlükleri tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="146f7-169">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="146f7-170">*RetentionInDays* parametresi için sıfırdan büyük bir değer belirtirseniz bu değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="146f7-170">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="146f7-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="146f7-171">-Confirm</span></span>
<span data-ttu-id="146f7-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="146f7-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="146f7-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="146f7-173">-WhatIf</span></span>
<span data-ttu-id="146f7-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="146f7-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="146f7-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="146f7-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="146f7-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146f7-176">CommonParameters</span></span>
<span data-ttu-id="146f7-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="146f7-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146f7-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="146f7-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146f7-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="146f7-179">INPUTS</span></span>

### <span data-ttu-id="146f7-180">Microsoft. Azure. Commands. Sql. Auditing. model. AuditType</span><span class="sxs-lookup"><span data-stu-id="146f7-180">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="146f7-181">Microsoft. Azure. Commands. Sql. Auditing. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="146f7-181">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="146f7-182">System. String []</span><span class="sxs-lookup"><span data-stu-id="146f7-182">System.String[]</span></span>

### <span data-ttu-id="146f7-183">System. String</span><span class="sxs-lookup"><span data-stu-id="146f7-183">System.String</span></span>

### <span data-ttu-id="146f7-184">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="146f7-184">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="146f7-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="146f7-185">OUTPUTS</span></span>

### <span data-ttu-id="146f7-186">Microsoft. Azure. Commands. Sql. Auditing. model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="146f7-186">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="146f7-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="146f7-187">NOTES</span></span>

## <span data-ttu-id="146f7-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="146f7-188">RELATED LINKS</span></span>

[<span data-ttu-id="146f7-189">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="146f7-189">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="146f7-190">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="146f7-190">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="146f7-191">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="146f7-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


