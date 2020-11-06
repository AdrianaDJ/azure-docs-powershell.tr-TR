---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589652"
---
# <span data-ttu-id="55018-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="55018-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="55018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55018-102">SYNOPSIS</span></span>
<span data-ttu-id="55018-103">SQL veritabanı sunucusunun denetim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="55018-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55018-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55018-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55018-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55018-105">DESCRIPTION</span></span>
<span data-ttu-id="55018-106">**Set-AzureRmSqlServerAuditingPolicy** cmdlet 'i, BIR Azure SQL veritabanı sunucusunun denetim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="55018-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="55018-107">Sunucuyu tanımlayan *Resourcegroupname* ve *ServerName* parametrelerini, denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve kullanılacak depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="55018-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="55018-108">Denetim günlükleri tablosu için bekletme 'yi, *RetentionInDays* ve *tableıdentifier* parametrelerinin değerini ayarlayarak, denetim günlüğü tablo adlarının dönemini ve çekirdek değerini ayarlayarak da tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55018-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="55018-109">Hangi olay türlerinin denetleneceğini tanımlayan *EventType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="55018-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="55018-110">Bu cmdlet 'i çalıştırdıktan sonra, bu sunucunun ilkesini kullanan veritabanlarının denetlenmesi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="55018-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="55018-111">Cmdlet başarılı olur ve *geçiş parametresini belirtirseniz* cmdlet, geçerli denetim ilkesini ve sunucu tanımlayıcılarını tanımlayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="55018-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="55018-112">Sunucu tanımlayıcıları **Resourcegroupname** ve **ServerName** içerir.</span><span class="sxs-lookup"><span data-stu-id="55018-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="55018-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55018-113">EXAMPLES</span></span>

### <span data-ttu-id="55018-114">Örnek 1: Azure SQL Server 'ın denetim ilkesini ayarlama tablo denetimini kullanma</span><span class="sxs-lookup"><span data-stu-id="55018-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="55018-115">Bu komut, server01 adındaki sunucunun Storage22 adlı bir depolama hesabını kullanması için denetim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55018-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="55018-116">Örnek 2: bir Azure SQL Server 'ın var olan denetim ilkesinin depolama hesabı anahtarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="55018-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="55018-117">Bu komut, server01 adındaki sunucunun ikincil anahtarı kullanması için denetim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55018-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="55018-118">Komut, depolama hesabı adını değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="55018-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="55018-119">Örnek 3: Azure SQL Server 'ın denetim ilkesini belirli bir olay türü kullanacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="55018-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="55018-120">Örnek 4: bir veritabanının denetim ilkesini blob denetimini kullanacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="55018-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="55018-121">Bu komut, server01 adındaki sunucunun Denetim ilkesini Login_Failure olay türünü kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55018-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="55018-122">Bu komut, başka hiçbir ayarı değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="55018-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="55018-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55018-123">PARAMETERS</span></span>

### <span data-ttu-id="55018-124">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="55018-124">-AuditActionGroup</span></span>
<span data-ttu-id="55018-125">Bir veya daha fazla denetim eylem grubu belirtin.</span><span class="sxs-lookup"><span data-stu-id="55018-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="55018-126">Bu parametre yalnızca blob denetimine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="55018-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="55018-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="55018-127">-AuditType</span></span>
<span data-ttu-id="55018-128">Denetim türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="55018-128">Specify the audit type.</span></span> <span data-ttu-id="55018-129">Denetim günlükleri, tablo depolama veya blob depolama birimine yazılabilir.</span><span class="sxs-lookup"><span data-stu-id="55018-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="55018-130">Blob denetimi daha yüksek performans sağlar ve nesne düzeyinde denetimi destekler.</span><span class="sxs-lookup"><span data-stu-id="55018-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55018-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55018-131">-DefaultProfile</span></span>
<span data-ttu-id="55018-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="55018-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55018-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="55018-133">-EventType</span></span>
<span data-ttu-id="55018-134">Denetlenecek olay türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="55018-135">Bu parametre yalnızca tablo denetimine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="55018-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="55018-136">Birçok olay türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55018-136">You can specify several event types.</span></span>
<span data-ttu-id="55018-137">Tüm olay türlerini denetlemeye ve hiçbir olayın denetleneceğini belirtmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="55018-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="55018-138">Tümünü veya hiçbirini aynı anda belirtirseniz, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="55018-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55018-139">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="55018-139">-PassThru</span></span>
<span data-ttu-id="55018-140">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="55018-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55018-141">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="55018-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55018-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55018-142">-ResourceGroupName</span></span>
<span data-ttu-id="55018-143">Veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="55018-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="55018-144">-RetentionInDays</span></span>
<span data-ttu-id="55018-145">Denetim günlükleri tablosu için bekletme günü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="55018-146">Sıfır (0) değeri tablonun saklanmadığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="55018-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="55018-147">Bu varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="55018-147">this is the default.</span></span>
<span data-ttu-id="55018-148">Sıfırdan büyük bir değer belirtirseniz, *Tableıdenkeer* parametresi için de bir değer belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="55018-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="55018-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55018-149">-ServerName</span></span>
<span data-ttu-id="55018-150">Veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55018-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="55018-151">-StorageAccountName</span></span>
<span data-ttu-id="55018-152">Veritabanını denetlemek için depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="55018-153">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="55018-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="55018-154">Bu parametreyi belirtmezseniz cmdlet, önceden tanımlanmış depolama hesabını veritabanı denetim ilkesinin parçası olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="55018-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="55018-155">Veritabanı denetleme ilkesi ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="55018-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="55018-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="55018-156">-StorageKeyType</span></span>
<span data-ttu-id="55018-157">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="55018-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55018-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55018-159">Yararı</span><span class="sxs-lookup"><span data-stu-id="55018-159">Primary</span></span>
- <span data-ttu-id="55018-160">İK</span><span class="sxs-lookup"><span data-stu-id="55018-160">Secondary</span></span>

<span data-ttu-id="55018-161">Varsayılan değer birincili değeridir.</span><span class="sxs-lookup"><span data-stu-id="55018-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="55018-162">-Tableıdentifier</span><span class="sxs-lookup"><span data-stu-id="55018-162">-TableIdentifier</span></span>
<span data-ttu-id="55018-163">Denetim günlükleri tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55018-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="55018-164">*RetentionInDays* parametresi için sıfırdan büyük bir değer belirtirseniz bu değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="55018-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="55018-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="55018-165">-Confirm</span></span>
<span data-ttu-id="55018-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55018-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55018-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55018-167">-WhatIf</span></span>
<span data-ttu-id="55018-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55018-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55018-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55018-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55018-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55018-170">CommonParameters</span></span>
<span data-ttu-id="55018-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55018-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55018-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55018-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55018-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55018-173">INPUTS</span></span>

### <span data-ttu-id="55018-174">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55018-174">None</span></span>
<span data-ttu-id="55018-175">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55018-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55018-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55018-176">OUTPUTS</span></span>

### <span data-ttu-id="55018-177">Microsoft. Azure. Commands. Sql. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="55018-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="55018-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55018-178">NOTES</span></span>

## <span data-ttu-id="55018-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55018-179">RELATED LINKS</span></span>

[<span data-ttu-id="55018-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="55018-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="55018-181">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="55018-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="55018-182">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="55018-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


