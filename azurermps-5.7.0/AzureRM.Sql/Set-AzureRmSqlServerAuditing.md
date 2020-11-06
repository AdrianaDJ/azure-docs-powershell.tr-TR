---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589653"
---
# <span data-ttu-id="4e414-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="4e414-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="4e414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e414-102">SYNOPSIS</span></span>
<span data-ttu-id="4e414-103">Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4e414-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e414-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e414-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e414-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e414-105">DESCRIPTION</span></span>
<span data-ttu-id="4e414-106">**Set-AzureRmSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4e414-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="4e414-107">Cmdlet 'i kullanmak için, sunucuyu belirlemek üzere *Resourcegroupname* ve *ServerName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e414-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="4e414-108">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e414-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="4e414-109">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e414-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="4e414-110">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e414-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="4e414-111">Cmdlet başarıyla çalıştıktan sonra, belirtilen Azure SQL Server 'da tanımlanan Azure SQL veritabanlarının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4e414-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="4e414-112">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , sunucu tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4e414-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="4e414-113">Sunucu tanımlayıcıları, **Resourcegroupname** ve **ServerName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="4e414-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="4e414-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e414-114">EXAMPLES</span></span>

### <span data-ttu-id="4e414-115">Örnek 1: Azure SQL Server 'ın denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4e414-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="4e414-116">Örnek 2: Azure SQL Server 'ın denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4e414-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="4e414-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e414-117">PARAMETERS</span></span>

### <span data-ttu-id="4e414-118">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="4e414-118">-AuditActionGroup</span></span>
<span data-ttu-id="4e414-119">Kullanılacak önerilen eylem grupları kümesi aşağıdaki bileşimdir-bu, veritabanında yürütülen tüm sorguların ve depolanan yordamların yanı sıra başarılı ve başarısız oturum açma işlemleri için denetim sağlayacaktır:</span><span class="sxs-lookup"><span data-stu-id="4e414-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="4e414-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4e414-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="4e414-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4e414-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="4e414-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="4e414-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="4e414-123">Yukarıdaki birleşim, varsayılan olarak yapılandırılan bir küme.</span><span class="sxs-lookup"><span data-stu-id="4e414-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="4e414-124">Bu gruplar, veritabanında yürütülen tüm SQL deyimlerini ve saklı yordamları kapsar ve aynı zamanda diğer gruplarla birlikte kullanılmamalıdır çünkü bu, yinelenen denetim günlüklerine yol açar.</span><span class="sxs-lookup"><span data-stu-id="4e414-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="4e414-125">Daha fazla bilgi için bkz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="4e414-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="4e414-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e414-126">-DefaultProfile</span></span>
<span data-ttu-id="4e414-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e414-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e414-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4e414-128">-PassThru</span></span>
<span data-ttu-id="4e414-129">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4e414-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4e414-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e414-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e414-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4e414-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e414-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4e414-132">-RetentionInDays</span></span>
<span data-ttu-id="4e414-133">Denetim günlüklerinin bekletme günü sayısı.</span><span class="sxs-lookup"><span data-stu-id="4e414-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="4e414-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e414-134">-ServerName</span></span>
<span data-ttu-id="4e414-135">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="4e414-135">SQL server name.</span></span>

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

### <span data-ttu-id="4e414-136">Durumlu</span><span class="sxs-lookup"><span data-stu-id="4e414-136">-State</span></span>
<span data-ttu-id="4e414-137">İlkenin durumu.</span><span class="sxs-lookup"><span data-stu-id="4e414-137">The state of the policy.</span></span>

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

### <span data-ttu-id="4e414-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4e414-138">-StorageAccountName</span></span>
<span data-ttu-id="4e414-139">Depolama hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4e414-139">The name of the storage account.</span></span> <span data-ttu-id="4e414-140">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4e414-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="4e414-141">Bu parametre gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="4e414-141">This parameter is not required.</span></span>  
<span data-ttu-id="4e414-142">Bu parametreyi belirtmezseniz cmdlet, daha önce denetim ilkesinin bir parçası olarak tanımlanan depolama hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e414-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="4e414-143">Bu, denetim ilkesinin ilk kez tanımlandıysa ve bu parametreyi belirtmezseniz, cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="4e414-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="4e414-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="4e414-144">-StorageKeyType</span></span>
<span data-ttu-id="4e414-145">Depolama erişim anahtarlarının hangi şekilde kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e414-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="4e414-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e414-146">-Confirm</span></span>
<span data-ttu-id="4e414-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e414-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e414-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e414-148">-WhatIf</span></span>
<span data-ttu-id="4e414-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e414-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e414-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e414-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e414-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e414-151">CommonParameters</span></span>
<span data-ttu-id="4e414-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e414-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e414-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e414-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e414-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e414-154">INPUTS</span></span>

### <span data-ttu-id="4e414-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e414-155">None</span></span>
<span data-ttu-id="4e414-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4e414-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e414-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e414-157">OUTPUTS</span></span>

### <span data-ttu-id="4e414-158">Microsoft. Azure. Commands. Sql. Security. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="4e414-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="4e414-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e414-159">NOTES</span></span>

## <span data-ttu-id="4e414-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e414-160">RELATED LINKS</span></span>
