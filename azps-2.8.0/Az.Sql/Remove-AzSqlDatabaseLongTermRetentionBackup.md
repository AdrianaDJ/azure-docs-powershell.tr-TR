---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e83845002e090afb962272bcf9c73e158a27e374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933547"
---
# <span data-ttu-id="0b58c-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0b58c-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="0b58c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b58c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b58c-103">Uzun süreli bekletme yedeklemesi siler.</span><span class="sxs-lookup"><span data-stu-id="0b58c-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="0b58c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b58c-104">SYNTAX</span></span>

### <span data-ttu-id="0b58c-105">RemoveBackupDefault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b58c-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b58c-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b58c-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b58c-107">Removebackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b58c-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b58c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b58c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b58c-109">**Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet 'i belirtilen yedeği siler.</span><span class="sxs-lookup"><span data-stu-id="0b58c-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="0b58c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b58c-110">EXAMPLES</span></span>

### <span data-ttu-id="0b58c-111">Örnek 1: kaynak grubuyla tek bir yedeklemeyi silme</span><span class="sxs-lookup"><span data-stu-id="0b58c-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="0b58c-112">Adı 601061b7-vseç10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="0b58c-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="0b58c-113">Örnek 2: kaynak grubu olmadan tek bir yedeklemeyi silme</span><span class="sxs-lookup"><span data-stu-id="0b58c-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="0b58c-114">Adı 601061b7-vseç10b-46e0-bf77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="0b58c-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="0b58c-115">Örnek 3: konumun tüm yedeklerini silme</span><span class="sxs-lookup"><span data-stu-id="0b58c-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="0b58c-116">Bu komut northeurope konumunun tüm uzun süreli bekletme yedeklemelerini siler.</span><span class="sxs-lookup"><span data-stu-id="0b58c-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="0b58c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b58c-117">PARAMETERS</span></span>

### <span data-ttu-id="0b58c-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="0b58c-118">-BackupName</span></span>
<span data-ttu-id="0b58c-119">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="0b58c-119">The name of the backup.</span></span>

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

### <span data-ttu-id="0b58c-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b58c-120">-DatabaseName</span></span>
<span data-ttu-id="0b58c-121">Yedeklemenin kimden olduğu Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="0b58c-121">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="0b58c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b58c-122">-DefaultProfile</span></span>
<span data-ttu-id="0b58c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b58c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b58c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0b58c-124">-Force</span></span>
<span data-ttu-id="0b58c-125">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="0b58c-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0b58c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b58c-126">-InputObject</span></span>
<span data-ttu-id="0b58c-127">Kaldırılacak veritabanı uzun süreli bekletme yedekleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0b58c-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b58c-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="0b58c-128">-Location</span></span>
<span data-ttu-id="0b58c-129">Yedeklemelerin kaynak sunucusunun konumu.</span><span class="sxs-lookup"><span data-stu-id="0b58c-129">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="0b58c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b58c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0b58c-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b58c-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b58c-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b58c-132">-ResourceId</span></span>
<span data-ttu-id="0b58c-133">Kaldırılacak veritabanı uzun süreli bekletme yedeklemesinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b58c-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="0b58c-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b58c-134">-ServerName</span></span>
<span data-ttu-id="0b58c-135">Yedeklemenin altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="0b58c-135">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="0b58c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b58c-136">-Confirm</span></span>
<span data-ttu-id="0b58c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b58c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b58c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b58c-138">-WhatIf</span></span>
<span data-ttu-id="0b58c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b58c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b58c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b58c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b58c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b58c-141">CommonParameters</span></span>
<span data-ttu-id="0b58c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b58c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b58c-143">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b58c-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b58c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b58c-144">INPUTS</span></span>

### <span data-ttu-id="0b58c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0b58c-145">System.String</span></span>

## <span data-ttu-id="0b58c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b58c-146">OUTPUTS</span></span>

### <span data-ttu-id="0b58c-147">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="0b58c-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="0b58c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b58c-148">NOTES</span></span>

## <span data-ttu-id="0b58c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b58c-149">RELATED LINKS</span></span>

[<span data-ttu-id="0b58c-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0b58c-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="0b58c-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b58c-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0b58c-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b58c-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="0b58c-153">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0b58c-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)