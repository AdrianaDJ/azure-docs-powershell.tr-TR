---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592707"
---
# <span data-ttu-id="af42c-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="af42c-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="af42c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af42c-102">SYNOPSIS</span></span>
<span data-ttu-id="af42c-103">Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af42c-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af42c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af42c-104">SYNTAX</span></span>

### <span data-ttu-id="af42c-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af42c-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af42c-106">Storageaccountsubscriptionıdset</span><span class="sxs-lookup"><span data-stu-id="af42c-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af42c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af42c-107">DESCRIPTION</span></span>
<span data-ttu-id="af42c-108">**Set-AzureRmSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af42c-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="af42c-109">Cmdlet 'i kullanmak için, sunucuyu belirlemek üzere *Resourcegroupname* ve *ServerName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="af42c-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="af42c-110">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="af42c-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="af42c-111">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="af42c-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="af42c-112">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af42c-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="af42c-113">Cmdlet başarıyla çalıştıktan sonra, belirtilen Azure SQL Server 'da tanımlanan Azure SQL veritabanlarının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="af42c-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="af42c-114">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , sunucu tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="af42c-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="af42c-115">Sunucu tanımlayıcıları, **Resourcegroupname** ve **ServerName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="af42c-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="af42c-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af42c-116">EXAMPLES</span></span>

### <span data-ttu-id="af42c-117">Örnek 1: Azure SQL Server 'ın denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="af42c-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="af42c-118">Örnek 2: Azure SQL Server 'ın denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="af42c-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="af42c-119">Örnek 3: farklı bir abonelikten depolama hesabı kullanarak Azure SQL Server 'ın Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="af42c-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="af42c-120">Örnek 4: bir Azure SQL veritabanının genişletilmiş denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="af42c-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="af42c-121">Örnek 5: bir Azure SQL veritabanının genişletilmiş denetim ilkesini kaldırın ve bunun yerine denetim ilkesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af42c-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="af42c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af42c-122">PARAMETERS</span></span>

### <span data-ttu-id="af42c-123">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="af42c-123">-AuditActionGroup</span></span>
<span data-ttu-id="af42c-124">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="af42c-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="af42c-125">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="af42c-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="af42c-126">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="af42c-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="af42c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af42c-127">-DefaultProfile</span></span>
<span data-ttu-id="af42c-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af42c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af42c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="af42c-129">-PassThru</span></span>
<span data-ttu-id="af42c-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="af42c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="af42c-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="af42c-131">-PredicateExpression</span></span>
<span data-ttu-id="af42c-132">Denetim günlüklerini filtrelemek için kullanılan where yan tümcesinin ifadesi.</span><span class="sxs-lookup"><span data-stu-id="af42c-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="af42c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af42c-133">-ResourceGroupName</span></span>
<span data-ttu-id="af42c-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="af42c-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="af42c-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="af42c-135">-RetentionInDays</span></span>
<span data-ttu-id="af42c-136">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="af42c-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="af42c-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af42c-137">-ServerName</span></span>
<span data-ttu-id="af42c-138">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="af42c-138">SQL server name.</span></span>

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

### <span data-ttu-id="af42c-139">Durumlu</span><span class="sxs-lookup"><span data-stu-id="af42c-139">-State</span></span>
<span data-ttu-id="af42c-140">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="af42c-140">The state of the policy.</span></span>

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

### <span data-ttu-id="af42c-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="af42c-141">-StorageAccountName</span></span>
<span data-ttu-id="af42c-142">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="af42c-142">The name of the storage account.</span></span> <span data-ttu-id="af42c-143">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="af42c-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="af42c-144">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="af42c-144">This parameter is not required.</span></span>
<span data-ttu-id="af42c-145">Bu parametreyi belirtmezseniz cmdlet, daha önce denetim ilkesinin bir parçası olarak tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="af42c-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="af42c-146">Bu, denetim ilkesinin ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="af42c-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="af42c-147">-Storageaccountsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="af42c-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="af42c-148">Depolama hesabı aboneliği kimliğini belirtir</span><span class="sxs-lookup"><span data-stu-id="af42c-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="af42c-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="af42c-149">-StorageKeyType</span></span>
<span data-ttu-id="af42c-150">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af42c-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="af42c-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="af42c-151">-Confirm</span></span>
<span data-ttu-id="af42c-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af42c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af42c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af42c-153">-WhatIf</span></span>
<span data-ttu-id="af42c-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af42c-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af42c-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af42c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af42c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af42c-156">CommonParameters</span></span>
<span data-ttu-id="af42c-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af42c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af42c-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af42c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af42c-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af42c-159">INPUTS</span></span>

## <span data-ttu-id="af42c-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af42c-160">OUTPUTS</span></span>

## <span data-ttu-id="af42c-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af42c-161">NOTES</span></span>

## <span data-ttu-id="af42c-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af42c-162">RELATED LINKS</span></span>
