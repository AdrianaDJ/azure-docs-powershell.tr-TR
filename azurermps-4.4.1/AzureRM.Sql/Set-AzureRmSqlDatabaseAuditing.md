---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589946"
---
# <span data-ttu-id="20f0f-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="20f0f-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="20f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="20f0f-103">Azure SQL veritabanı için denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="20f0f-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20f0f-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="20f0f-106">**Set-AzureRmSqlDatabaseAuditing** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="20f0f-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="20f0f-107">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="20f0f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="20f0f-108">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="20f0f-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="20f0f-109">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="20f0f-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="20f0f-110">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20f0f-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="20f0f-111">Cmdlet başarıyla çalıştıktan sonra, veritabanının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="20f0f-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="20f0f-112">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , veritabanı tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="20f0f-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="20f0f-113">Veritabanı tanımlayıcıları, **Resourcegroupname** , **ServerName** ve **DatabaseName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="20f0f-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="20f0f-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20f0f-114">EXAMPLES</span></span>

### <span data-ttu-id="20f0f-115">Örnek 1: Azure SQL veritabanının Denetleme ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="20f0f-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="20f0f-116">Örnek 2: Azure SQL veritabanının blob denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="20f0f-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="20f0f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20f0f-117">PARAMETERS</span></span>

### <span data-ttu-id="20f0f-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="20f0f-118">-AuditAction</span></span>
<span data-ttu-id="20f0f-119">Denetim eylemleri kümesi</span><span class="sxs-lookup"><span data-stu-id="20f0f-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="20f0f-120">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="20f0f-120">-AuditActionGroup</span></span>
<span data-ttu-id="20f0f-121">Denetim eylemi grupları kümesi</span><span class="sxs-lookup"><span data-stu-id="20f0f-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="20f0f-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="20f0f-122">-DatabaseName</span></span>
<span data-ttu-id="20f0f-123">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="20f0f-123">SQL Database name.</span></span>

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

### <span data-ttu-id="20f0f-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20f0f-124">-PassThru</span></span>
<span data-ttu-id="20f0f-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="20f0f-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20f0f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f0f-126">-ResourceGroupName</span></span>
<span data-ttu-id="20f0f-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="20f0f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="20f0f-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="20f0f-128">-RetentionInDays</span></span>
<span data-ttu-id="20f0f-129">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="20f0f-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="20f0f-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20f0f-130">-ServerName</span></span>
<span data-ttu-id="20f0f-131">SQL veritabanı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="20f0f-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="20f0f-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="20f0f-132">-State</span></span>
<span data-ttu-id="20f0f-133">Denetim ilkesinin durumu</span><span class="sxs-lookup"><span data-stu-id="20f0f-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="20f0f-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20f0f-134">-StorageAccountName</span></span>
<span data-ttu-id="20f0f-135">Depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="20f0f-135">The name of the storage account</span></span>

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

### <span data-ttu-id="20f0f-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="20f0f-136">-StorageKeyType</span></span>
<span data-ttu-id="20f0f-137">Depolama anahtarının türü</span><span class="sxs-lookup"><span data-stu-id="20f0f-137">The type of the storage key</span></span>

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

### <span data-ttu-id="20f0f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="20f0f-138">-Confirm</span></span>
<span data-ttu-id="20f0f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20f0f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f0f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f0f-140">-WhatIf</span></span>
<span data-ttu-id="20f0f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20f0f-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20f0f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20f0f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f0f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f0f-143">-DefaultProfile</span></span>
<span data-ttu-id="20f0f-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20f0f-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f0f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f0f-145">CommonParameters</span></span>
<span data-ttu-id="20f0f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20f0f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f0f-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f0f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f0f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20f0f-148">INPUTS</span></span>

## <span data-ttu-id="20f0f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20f0f-149">OUTPUTS</span></span>

### <span data-ttu-id="20f0f-150">Microsoft. Azure. Commands. Sql. Security. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="20f0f-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="20f0f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20f0f-151">NOTES</span></span>

## <span data-ttu-id="20f0f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20f0f-152">RELATED LINKS</span></span>

