---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591759"
---
# <span data-ttu-id="cb2e6-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="cb2e6-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="cb2e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2e6-103">Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb2e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb2e6-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb2e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="cb2e6-106">**Set-AzureRmSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="cb2e6-107">Cmdlet 'i kullanmak için, sunucuyu belirlemek üzere *Resourcegroupname* ve *ServerName* parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="cb2e6-108">Denetim günlüklerinin depolama hesabını belirtmek için *storageAccountName* parametresini ve depolama tuşlarının tanımlanması için *StorageKeyType* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="cb2e6-109">İlkeyi etkinleştirmek/devre dışı bırakmak için *State* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="cb2e6-110">Denetim günlükleri için, denetim günlüklerinin süresini tanımlamak üzere *RetentionInDays* parametresinin değerini ayarlayarak da bekletme tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="cb2e6-111">Cmdlet başarıyla çalıştıktan sonra, belirtilen Azure SQL Server 'da tanımlanan Azure SQL veritabanlarının denetimi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="cb2e6-112">Cmdlet başarılı olur ve *geçiş parametresini kullanıyorsanız* , sunucu tanımlayıcılarına ek olarak geçerli blob denetim ilkesini açıklayan bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="cb2e6-113">Sunucu tanımlayıcıları, **Resourcegroupname** ve **ServerName** ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="cb2e6-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb2e6-114">EXAMPLES</span></span>

### <span data-ttu-id="cb2e6-115">Örnek 1: Azure SQL Server 'ın denetim ilkesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="cb2e6-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="cb2e6-116">Örnek 2: Azure SQL Server 'ın denetim ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="cb2e6-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="cb2e6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb2e6-117">PARAMETERS</span></span>

### <span data-ttu-id="cb2e6-118">-Sestactiongroup</span><span class="sxs-lookup"><span data-stu-id="cb2e6-118">-AuditActionGroup</span></span>
<span data-ttu-id="cb2e6-119">Denetim eylemi grupları kümesi</span><span class="sxs-lookup"><span data-stu-id="cb2e6-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="cb2e6-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb2e6-120">-PassThru</span></span>
<span data-ttu-id="cb2e6-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="cb2e6-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cb2e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb2e6-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb2e6-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cb2e6-124">-RetentionInDays</span></span>
<span data-ttu-id="cb2e6-125">Denetim günlükleri için bekletme günü sayısı</span><span class="sxs-lookup"><span data-stu-id="cb2e6-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="cb2e6-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb2e6-126">-ServerName</span></span>
<span data-ttu-id="cb2e6-127">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-127">SQL server name.</span></span>

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

### <span data-ttu-id="cb2e6-128">Durumlu</span><span class="sxs-lookup"><span data-stu-id="cb2e6-128">-State</span></span>
<span data-ttu-id="cb2e6-129">Denetim ilkesinin durumu</span><span class="sxs-lookup"><span data-stu-id="cb2e6-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="cb2e6-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cb2e6-130">-StorageAccountName</span></span>
<span data-ttu-id="cb2e6-131">Depolama hesabının adı</span><span class="sxs-lookup"><span data-stu-id="cb2e6-131">The name of the storage account</span></span>

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

### <span data-ttu-id="cb2e6-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="cb2e6-132">-StorageKeyType</span></span>
<span data-ttu-id="cb2e6-133">Depolama anahtarının türü</span><span class="sxs-lookup"><span data-stu-id="cb2e6-133">The type of the storage key</span></span>

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

### <span data-ttu-id="cb2e6-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb2e6-134">-Confirm</span></span>
<span data-ttu-id="cb2e6-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2e6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2e6-136">-WhatIf</span></span>
<span data-ttu-id="cb2e6-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb2e6-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2e6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2e6-139">-DefaultProfile</span></span>
<span data-ttu-id="cb2e6-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2e6-141">CommonParameters</span></span>
<span data-ttu-id="cb2e6-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb2e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2e6-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb2e6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2e6-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb2e6-144">INPUTS</span></span>

## <span data-ttu-id="cb2e6-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb2e6-145">OUTPUTS</span></span>

### <span data-ttu-id="cb2e6-146">Microsoft. Azure. Commands. Sql. Security. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="cb2e6-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="cb2e6-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb2e6-147">NOTES</span></span>

## <span data-ttu-id="cb2e6-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb2e6-148">RELATED LINKS</span></span>

