---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 68481d49fb37fb5246021fb8daa2d53a64b5c6b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591868"
---
# <span data-ttu-id="bc02e-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bc02e-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="bc02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc02e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc02e-103">Uzun süreli bekletme yedeklemesi siler.</span><span class="sxs-lookup"><span data-stu-id="bc02e-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc02e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc02e-104">SYNTAX</span></span>

### <span data-ttu-id="bc02e-105">RemoveBackupDefault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bc02e-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc02e-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc02e-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc02e-107">Removebackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="bc02e-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc02e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc02e-108">DESCRIPTION</span></span>
<span data-ttu-id="bc02e-109">**Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet 'i belirtilen yedeği siler.</span><span class="sxs-lookup"><span data-stu-id="bc02e-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="bc02e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc02e-110">EXAMPLES</span></span>

### <span data-ttu-id="bc02e-111">Örnek 1: tek bir yedeği silme</span><span class="sxs-lookup"><span data-stu-id="bc02e-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="bc02e-112">Adı 601061b7-vseç10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="bc02e-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="bc02e-113">Örnek 2: bir konumun tüm yedeklerini silme</span><span class="sxs-lookup"><span data-stu-id="bc02e-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="bc02e-114">Bu komut northeurope konumunun tüm uzun süreli bekletme yedeklemelerini siler.</span><span class="sxs-lookup"><span data-stu-id="bc02e-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="bc02e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc02e-115">PARAMETERS</span></span>

### <span data-ttu-id="bc02e-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="bc02e-116">-BackupName</span></span>
<span data-ttu-id="bc02e-117">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="bc02e-117">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc02e-118">-DatabaseName</span></span>
<span data-ttu-id="bc02e-119">Yedeklemenin kimden olduğu Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="bc02e-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc02e-120">-DefaultProfile</span></span>
<span data-ttu-id="bc02e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc02e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc02e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bc02e-122">-Force</span></span>
<span data-ttu-id="bc02e-123">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="bc02e-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bc02e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc02e-124">-InputObject</span></span>
<span data-ttu-id="bc02e-125">Kaldırılacak veritabanı uzun süreli bekletme yedekleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bc02e-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="bc02e-126">-Location</span></span>
<span data-ttu-id="bc02e-127">Yedeklemelerin kaynak sunucusunun konumu.</span><span class="sxs-lookup"><span data-stu-id="bc02e-127">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bc02e-128">-ResourceId</span></span>
<span data-ttu-id="bc02e-129">Kaldırılacak veritabanı uzun süreli bekletme yedeklemesinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bc02e-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc02e-130">-ServerName</span></span>
<span data-ttu-id="bc02e-131">Yedeklemenin altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="bc02e-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc02e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc02e-132">-Confirm</span></span>
<span data-ttu-id="bc02e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc02e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc02e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc02e-134">-WhatIf</span></span>
<span data-ttu-id="bc02e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc02e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc02e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc02e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc02e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc02e-137">CommonParameters</span></span>
<span data-ttu-id="bc02e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc02e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc02e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc02e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc02e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc02e-140">INPUTS</span></span>

### <span data-ttu-id="bc02e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bc02e-141">System.String</span></span>

## <span data-ttu-id="bc02e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc02e-142">OUTPUTS</span></span>

### <span data-ttu-id="bc02e-143">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="bc02e-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="bc02e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc02e-144">NOTES</span></span>

## <span data-ttu-id="bc02e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc02e-145">RELATED LINKS</span></span>

[<span data-ttu-id="bc02e-146">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="bc02e-146">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="bc02e-147">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bc02e-147">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="bc02e-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bc02e-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="bc02e-149">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="bc02e-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
