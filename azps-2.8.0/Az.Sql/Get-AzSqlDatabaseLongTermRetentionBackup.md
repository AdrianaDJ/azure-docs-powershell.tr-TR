---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: fc6c6c2756ecb1c4174fc1255c175a49f66360cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933667"
---
# <span data-ttu-id="712df-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="712df-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="712df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712df-102">SYNOPSIS</span></span>
<span data-ttu-id="712df-103">Bir veya daha fazla uzun süreli bekletme yedeğini alır.</span><span class="sxs-lookup"><span data-stu-id="712df-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="712df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="712df-104">SYNTAX</span></span>

### <span data-ttu-id="712df-105">Konum (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="712df-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [[-ResourceGroupName] <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-106">Uzaktaki</span><span class="sxs-lookup"><span data-stu-id="712df-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [[-ResourceGroupName] <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="712df-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-108">Getbackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="712df-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-109">Getbackupsbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="712df-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="712df-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="712df-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="712df-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="712df-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="712df-112">DESCRIPTION</span></span>
<span data-ttu-id="712df-113">**Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet 'i bir konum, sunucu veya veritabanı için tüm uzun süreli bekletme yedeklemelerini alır veya belirli bir uzun süreli bekletme yedeğini alır.</span><span class="sxs-lookup"><span data-stu-id="712df-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="712df-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="712df-114">EXAMPLES</span></span>

### <span data-ttu-id="712df-115">Örnek 1: bir konumun tüm yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="712df-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="712df-116">Bu komut northeurope 'de tüm veritabanları (canlı veya silinmiş olabilir) için tüm uzun süreli bekletme yedeklemelerini alır, yalnızca sunucu canlı olduğunda ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="712df-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="712df-117">Örnek 2: kaynak grubu altındaki bir konum için tüm yedekleri alma</span><span class="sxs-lookup"><span data-stu-id="712df-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


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

<span data-ttu-id="712df-118">Bu komut, northeurope 'deki kaynak grubu altında tüm veritabanları (canlı veya silinmiş olabilir) için tüm uzun süreli bekletme yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="712df-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="712df-119">Örnek 3: belirli bir uzun süreli bekletme yedeği alma</span><span class="sxs-lookup"><span data-stu-id="712df-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="712df-120">Bu komut, adı 601061b7-vseç10b-46e0-bf77-a2bfb16a6add; 131655666550000000 ile yedeklemeyi alıyor</span><span class="sxs-lookup"><span data-stu-id="712df-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="712df-121">Örnek 4: bir veritabanının uzun süreli bekletme yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="712df-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="712df-122">Bu komut, database01 için tüm uzun süreli bekletme yedeklemelerini alır</span><span class="sxs-lookup"><span data-stu-id="712df-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="712df-123">Örnek 5: filtreleme kullanarak uzun süreli bekletme yedeklemelerini alın</span><span class="sxs-lookup"><span data-stu-id="712df-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

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

<span data-ttu-id="712df-124">Bu komut, adı "601061b7" ile başlayan tüm yedekleri alır</span><span class="sxs-lookup"><span data-stu-id="712df-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="712df-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="712df-125">PARAMETERS</span></span>

### <span data-ttu-id="712df-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="712df-126">-BackupName</span></span>
<span data-ttu-id="712df-127">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="712df-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="712df-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="712df-128">-DatabaseName</span></span>
<span data-ttu-id="712df-129">Yedeklemenin kimden olduğu Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="712df-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712df-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="712df-130">-DatabaseState</span></span>
<span data-ttu-id="712df-131">Yedekleri bulmak, canlı, silinmesini veya tamamını bulmak istediğiniz veritabanının durumu.</span><span class="sxs-lookup"><span data-stu-id="712df-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="712df-132">Varsayılan olarak tüm</span><span class="sxs-lookup"><span data-stu-id="712df-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="712df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712df-133">-DefaultProfile</span></span>
<span data-ttu-id="712df-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="712df-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712df-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="712df-135">-InputObject</span></span>
<span data-ttu-id="712df-136">Yedeklemelerin alınacağı veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="712df-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="712df-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="712df-137">-Location</span></span>
<span data-ttu-id="712df-138">Yedeklemelerin kaynak sunucusunun konumu.</span><span class="sxs-lookup"><span data-stu-id="712df-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712df-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="712df-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="712df-140">Her veritabanı için yalnızca en son yedeklemeyi alma.</span><span class="sxs-lookup"><span data-stu-id="712df-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="712df-141">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="712df-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712df-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="712df-142">-ResourceGroupName</span></span>
<span data-ttu-id="712df-143">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="712df-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712df-144">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="712df-144">-ResourceId</span></span>
<span data-ttu-id="712df-145">Yedeklemelerin alınacağı veritabanı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="712df-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="712df-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="712df-146">-ServerName</span></span>
<span data-ttu-id="712df-147">Yedeklemelerin altında olduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="712df-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712df-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="712df-148">-Confirm</span></span>
<span data-ttu-id="712df-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="712df-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="712df-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="712df-150">-WhatIf</span></span>
<span data-ttu-id="712df-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="712df-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="712df-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="712df-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="712df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712df-153">CommonParameters</span></span>
<span data-ttu-id="712df-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="712df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712df-155">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="712df-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712df-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="712df-156">INPUTS</span></span>

### <span data-ttu-id="712df-157">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="712df-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="712df-158">System. String</span><span class="sxs-lookup"><span data-stu-id="712df-158">System.String</span></span>

## <span data-ttu-id="712df-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="712df-159">OUTPUTS</span></span>

### <span data-ttu-id="712df-160">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="712df-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="712df-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="712df-161">NOTES</span></span>

## <span data-ttu-id="712df-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="712df-162">RELATED LINKS</span></span>

[<span data-ttu-id="712df-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="712df-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="712df-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="712df-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="712df-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="712df-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="712df-166">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="712df-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)