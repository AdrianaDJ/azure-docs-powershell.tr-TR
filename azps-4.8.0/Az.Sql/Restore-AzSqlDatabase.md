---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110230"
---
# <span data-ttu-id="2ab54-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2ab54-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="2ab54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab54-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab54-103">SQL veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2ab54-103">Restores a SQL database.</span></span>

## <span data-ttu-id="2ab54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ab54-104">SYNTAX</span></span>

### <span data-ttu-id="2ab54-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab54-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="2ab54-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab54-107">Fromdatabasebackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab54-108">Fromdatabasebackupwithvcore</span><span class="sxs-lookup"><span data-stu-id="2ab54-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ab54-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab54-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="2ab54-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab54-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ab54-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="2ab54-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ab54-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ab54-113">DESCRIPTION</span></span>
<span data-ttu-id="2ab54-114">**Restore-AzSqlDatabase** cmdlet 'i, bir SQL veritabanını coğrafi olarak yedekli bir yedekten, silinmiş bir veritabanının yedeğini, uzun dönemli bir yedek yedeklemeyi veya Live veritabanında bir noktayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2ab54-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="2ab54-115">Geri yüklenen veritabanı yeni bir veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2ab54-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="2ab54-116">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, esnek bir SQL veritabanı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ab54-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="2ab54-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ab54-117">EXAMPLES</span></span>

### <span data-ttu-id="2ab54-118">Örnek 1: veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2ab54-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="2ab54-119">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ab54-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="2ab54-120">İkinci komut, $Database belirtilen noktadan noktaya yedekten, Restoredveritabanı adlı veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2ab54-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="2ab54-121">Örnek 2: bir veritabanını esnek bir havuzun bir noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2ab54-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2ab54-122">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ab54-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="2ab54-123">İkinci komut, elasticpool01 adlı elastik havuzda geri Restokveritabanı adlı SQL veritabanına belirtilen noktadan noktaya $Database yedekten geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2ab54-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="2ab54-124">Örnek 3: silinen veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2ab54-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="2ab54-125">İlk komut, [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="2ab54-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="2ab54-126">İkinci komut restore [-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet 'ini kullanarak geri yüklemeyi silinmiş veritabanı yedeklemesinden başlatır.</span><span class="sxs-lookup"><span data-stu-id="2ab54-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="2ab54-127">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="2ab54-128">Örnek 4: silinen veritabanını esnek bir havuza geri yükleme</span><span class="sxs-lookup"><span data-stu-id="2ab54-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="2ab54-129">İlk komut, [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="2ab54-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="2ab54-130">İkinci komut restore [-AzSqlDatabase kullanarak restore-azsqldatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="2ab54-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="2ab54-131">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="2ab54-132">Örnek 5: veritabanı Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="2ab54-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="2ab54-133">İlk komut, Database01 adlı veritabanının coğrafi yedekli yedeklemesini alır ve $GeoBackup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="2ab54-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="2ab54-134">İkinci komut $GeoBackup, yedeği RestoredDatabase adlı SQL veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="2ab54-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="2ab54-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ab54-135">PARAMETERS</span></span>

### <span data-ttu-id="2ab54-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ab54-136">-AsJob</span></span>
<span data-ttu-id="2ab54-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ab54-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ab54-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2ab54-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="2ab54-139">Yedekleme depolama yedeği, SQL veritabanının yedeklerini depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ab54-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="2ab54-140">Seçenekler şunlardır: yerel, bölge ve coğrafi.</span><span class="sxs-lookup"><span data-stu-id="2ab54-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2ab54-141">-ComputeGeneration</span></span>
<span data-ttu-id="2ab54-142">Geri yüklenen veritabanına atanacak işlem oluşturma</span><span class="sxs-lookup"><span data-stu-id="2ab54-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab54-143">-DefaultProfile</span></span>
<span data-ttu-id="2ab54-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2ab54-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ab54-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="2ab54-145">-DeletionDate</span></span>
<span data-ttu-id="2ab54-146">Silme tarihini **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="2ab54-147">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ab54-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="2ab54-148">-Edition</span></span>
<span data-ttu-id="2ab54-149">SQL veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="2ab54-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2ab54-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ab54-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2ab54-151">None</span></span>
- <span data-ttu-id="2ab54-152">Ana</span><span class="sxs-lookup"><span data-stu-id="2ab54-152">Basic</span></span>
- <span data-ttu-id="2ab54-153">Ardından</span><span class="sxs-lookup"><span data-stu-id="2ab54-153">Standard</span></span>
- <span data-ttu-id="2ab54-154">Min</span><span class="sxs-lookup"><span data-stu-id="2ab54-154">Premium</span></span>
- <span data-ttu-id="2ab54-155">Ambarı</span><span class="sxs-lookup"><span data-stu-id="2ab54-155">DataWarehouse</span></span>
- <span data-ttu-id="2ab54-156">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="2ab54-156">Free</span></span>
- <span data-ttu-id="2ab54-157">:</span><span class="sxs-lookup"><span data-stu-id="2ab54-157">Stretch</span></span>
- <span data-ttu-id="2ab54-158">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="2ab54-158">GeneralPurpose</span></span>
- <span data-ttu-id="2ab54-159">Departmanla</span><span class="sxs-lookup"><span data-stu-id="2ab54-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-160">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="2ab54-160">-ElasticPoolName</span></span>
<span data-ttu-id="2ab54-161">SQL veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="2ab54-163">Bu cmdlet 'in, silinmiş bir SQL veritabanının yedeklemesinden bir veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="2ab54-164">Silinmiş bir SQL veritabanının yedeklemesini almak için Get-AzSqlDeletedDatabaseBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ab54-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-165">-FromGeoBackup</span></span>
<span data-ttu-id="2ab54-166">Bu cmdlet 'in bir SQL veritabanını coğrafi olarak yedekli bir yedekten geri göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="2ab54-167">Coğrafi artıklık yedeği almak için Get-AzSqlDatabaseGeoBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ab54-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="2ab54-169">Bu cmdlet 'in bir SQL veritabanını uzun süreli bekletme yedeklemesinden geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="2ab54-171">Bu cmdlet 'in bir gelen bir noktadan itibaren SQL veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2ab54-172">-LicenseType</span></span>
<span data-ttu-id="2ab54-173">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="2ab54-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-174">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="2ab54-174">-PointInTime</span></span>
<span data-ttu-id="2ab54-175">SQL veritabanınızı geri yüklemek istediğiniz zamanı bir **Tarih** saat içinde belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="2ab54-176">**DateTime** nesnesini almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ab54-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="2ab54-177">Bu parametreyi *FromPointInTimeBackup* parametresiyle birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ab54-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab54-178">-ResourceGroupName</span></span>
<span data-ttu-id="2ab54-179">Bu cmdlet 'in SQL veritabanını atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="2ab54-180">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ab54-180">-ResourceId</span></span>
<span data-ttu-id="2ab54-181">Geri yüklenecek kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ab54-182">-ServerName</span></span>
<span data-ttu-id="2ab54-183">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2ab54-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="2ab54-185">Hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ab54-186">-TargetDatabaseName</span></span>
<span data-ttu-id="2ab54-187">Geri yüklenecek veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-187">Specifies the name of the database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="2ab54-188">-VCore</span></span>
<span data-ttu-id="2ab54-189">Geri yüklenen Azure SQL veritabanının Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="2ab54-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ab54-190">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ab54-190">-Confirm</span></span>
<span data-ttu-id="2ab54-191">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ab54-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ab54-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ab54-192">-WhatIf</span></span>
<span data-ttu-id="2ab54-193">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ab54-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ab54-194">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ab54-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ab54-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab54-195">CommonParameters</span></span>
<span data-ttu-id="2ab54-196">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ab54-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab54-197">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ab54-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab54-198">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ab54-198">INPUTS</span></span>

### <span data-ttu-id="2ab54-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="2ab54-199">System.DateTime</span></span>

### <span data-ttu-id="2ab54-200">System. String</span><span class="sxs-lookup"><span data-stu-id="2ab54-200">System.String</span></span>

## <span data-ttu-id="2ab54-201">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ab54-201">OUTPUTS</span></span>

### <span data-ttu-id="2ab54-202">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="2ab54-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2ab54-203">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ab54-203">NOTES</span></span>

## <span data-ttu-id="2ab54-204">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ab54-204">RELATED LINKS</span></span>

[<span data-ttu-id="2ab54-205">Azure SQL veritabanını kesinti 'den kurtarma</span><span class="sxs-lookup"><span data-stu-id="2ab54-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="2ab54-206">Kullanıcı hatasından Azure SQL veritabanını kurtarma</span><span class="sxs-lookup"><span data-stu-id="2ab54-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="2ab54-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2ab54-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="2ab54-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="2ab54-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="2ab54-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="2ab54-210">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="2ab54-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

