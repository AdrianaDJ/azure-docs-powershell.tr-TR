---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: da3b47923f39e6910566a210ddbd325d9da76ca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573197"
---
# <span data-ttu-id="97e0a-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="97e0a-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="97e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="97e0a-103">Bir veya daha fazla uzun süreli bekletme yedeğini alır.</span><span class="sxs-lookup"><span data-stu-id="97e0a-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97e0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97e0a-104">SYNTAX</span></span>

### <span data-ttu-id="97e0a-105">Konum (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97e0a-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97e0a-106">Uzaktaki</span><span class="sxs-lookup"><span data-stu-id="97e0a-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e0a-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="97e0a-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e0a-108">Getbackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="97e0a-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e0a-109">Getbackupsbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="97e0a-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e0a-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="97e0a-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e0a-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="97e0a-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97e0a-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="97e0a-112">DESCRIPTION</span></span>
<span data-ttu-id="97e0a-113">**Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet 'i bir konum, sunucu veya veritabanı için tüm uzun süreli bekletme yedeklemelerini alır veya belirli bir uzun süreli bekletme yedeğini alır.</span><span class="sxs-lookup"><span data-stu-id="97e0a-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="97e0a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97e0a-114">EXAMPLES</span></span>

### <span data-ttu-id="97e0a-115">Örnek 1: bir konumun tüm yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="97e0a-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="97e0a-116">Bu komut, northeurope 'de tüm veritabanları (canlı veya silinmiş olabilir) için tüm uzun süreli bekletme yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="97e0a-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="97e0a-117">Örnek 2: belirli bir uzun süreli bekletme yedeği alma</span><span class="sxs-lookup"><span data-stu-id="97e0a-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="97e0a-118">Bu komut, adı 601061b7-vseç10b-46e0-bf77-a2bfb16a6add; 131655666550000000 ile yedeklemeyi alıyor</span><span class="sxs-lookup"><span data-stu-id="97e0a-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="97e0a-119">Örnek 3: veritabanı için tüm uzun süreli bekletme yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="97e0a-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="97e0a-120">Bu komut, database01 için tüm uzun süreli bekletme yedeklemelerini alır</span><span class="sxs-lookup"><span data-stu-id="97e0a-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="97e0a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97e0a-121">PARAMETERS</span></span>

### <span data-ttu-id="97e0a-122">-BackupName</span><span class="sxs-lookup"><span data-stu-id="97e0a-122">-BackupName</span></span>
<span data-ttu-id="97e0a-123">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="97e0a-123">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97e0a-124">-DatabaseName</span></span>
<span data-ttu-id="97e0a-125">Yedeklemenin kimden olduğu Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="97e0a-125">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: ServerName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="97e0a-126">-DatabaseState</span></span>
<span data-ttu-id="97e0a-127">Yedekleri bulmak, canlı, silinmesini veya tamamını bulmak istediğiniz veritabanının durumu.</span><span class="sxs-lookup"><span data-stu-id="97e0a-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="97e0a-128">Varsayılan olarak tüm</span><span class="sxs-lookup"><span data-stu-id="97e0a-128">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e0a-129">-DefaultProfile</span></span>
<span data-ttu-id="97e0a-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97e0a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e0a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97e0a-131">-InputObject</span></span>
<span data-ttu-id="97e0a-132">Yedeklemelerin alınacağı veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="97e0a-132">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="97e0a-133">-Location</span></span>
<span data-ttu-id="97e0a-134">Yedeklemelerin kaynak sunucusunun konumu.</span><span class="sxs-lookup"><span data-stu-id="97e0a-134">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="97e0a-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="97e0a-136">Her veritabanı için yalnızca en son yedeklemeyi alma.</span><span class="sxs-lookup"><span data-stu-id="97e0a-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="97e0a-137">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="97e0a-137">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97e0a-138">-ResourceId</span></span>
<span data-ttu-id="97e0a-139">Yedeklemelerin alınacağı veritabanı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="97e0a-139">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="97e0a-140">-ServerName</span></span>
<span data-ttu-id="97e0a-141">Yedeklemelerin altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="97e0a-141">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e0a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="97e0a-142">-Confirm</span></span>
<span data-ttu-id="97e0a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97e0a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e0a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e0a-144">-WhatIf</span></span>
<span data-ttu-id="97e0a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97e0a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e0a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97e0a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e0a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e0a-147">CommonParameters</span></span>
<span data-ttu-id="97e0a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97e0a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="97e0a-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e0a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e0a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97e0a-150">INPUTS</span></span>

### <span data-ttu-id="97e0a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="97e0a-151">System.String</span></span>
<span data-ttu-id="97e0a-152">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="97e0a-152">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="97e0a-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97e0a-153">OUTPUTS</span></span>

### <span data-ttu-id="97e0a-154">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="97e0a-154">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="97e0a-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97e0a-155">NOTES</span></span>

## <span data-ttu-id="97e0a-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97e0a-156">RELATED LINKS</span></span>

[<span data-ttu-id="97e0a-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="97e0a-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="97e0a-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="97e0a-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="97e0a-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="97e0a-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="97e0a-160">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="97e0a-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
