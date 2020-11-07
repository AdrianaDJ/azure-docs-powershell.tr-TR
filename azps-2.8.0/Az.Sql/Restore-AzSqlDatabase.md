---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: 262d4266a41cd9072ff9109819a2268999d26d7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933516"
---
# <span data-ttu-id="c1093-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1093-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="c1093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1093-102">SYNOPSIS</span></span>
<span data-ttu-id="c1093-103">SQL veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c1093-103">Restores a SQL database.</span></span>

## <span data-ttu-id="c1093-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1093-104">SYNTAX</span></span>

### <span data-ttu-id="c1093-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1093-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="c1093-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1093-107">Fromdatabasebackup</span><span class="sxs-lookup"><span data-stu-id="c1093-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1093-108">Fromdatabasebackupwithvcore</span><span class="sxs-lookup"><span data-stu-id="c1093-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1093-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1093-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="c1093-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1093-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1093-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="c1093-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1093-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1093-113">DESCRIPTION</span></span>
<span data-ttu-id="c1093-114">**Restore-AzSqlDatabase** cmdlet 'i, bir SQL veritabanını coğrafi olarak yedekli bir yedekten, silinmiş bir veritabanının yedeğini, uzun dönemli bir yedek yedeklemeyi veya Live veritabanında bir noktayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c1093-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="c1093-115">Geri yüklenen veritabanı yeni bir veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c1093-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="c1093-116">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, esnek bir SQL veritabanı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1093-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="c1093-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1093-117">EXAMPLES</span></span>

### <span data-ttu-id="c1093-118">Örnek 1: veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c1093-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="c1093-119">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c1093-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="c1093-120">İkinci komut, $Database belirtilen noktadan noktaya yedekten, Restoredveritabanı adlı veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c1093-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="c1093-121">Örnek 2: bir veritabanını esnek bir havuzun bir noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c1093-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c1093-122">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c1093-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="c1093-123">İkinci komut, elasticpool01 adlı elastik havuzda geri Restokveritabanı adlı SQL veritabanına belirtilen noktadan noktaya $Database yedekten geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c1093-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="c1093-124">Örnek 3: silinen veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c1093-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="c1093-125">İlk komut, [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="c1093-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="c1093-126">İkinci komut restore [-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet 'ini kullanarak geri yüklemeyi silinmiş veritabanı yedeklemesinden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c1093-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="c1093-127">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="c1093-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="c1093-128">Örnek 4: silinen veritabanını esnek bir havuza geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c1093-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="c1093-129">İlk komut, [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="c1093-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="c1093-130">İkinci komut restore [-AzSqlDatabase kullanarak restore-azsqldatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="c1093-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="c1093-131">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="c1093-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="c1093-132">Örnek 5: veritabanı Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="c1093-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="c1093-133">İlk komut, Database01 adlı veritabanının coğrafi yedekli yedeklemesini alır ve $GeoBackup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c1093-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="c1093-134">İkinci komut $GeoBackup, yedeği RestoredDatabase adlı SQL veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c1093-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="c1093-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1093-135">PARAMETERS</span></span>

### <span data-ttu-id="c1093-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="c1093-136">-AsJob</span></span>
<span data-ttu-id="c1093-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c1093-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1093-138">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c1093-138">-ComputeGeneration</span></span>
<span data-ttu-id="c1093-139">Geri yüklenen veritabanına atanacak işlem oluşturma</span><span class="sxs-lookup"><span data-stu-id="c1093-139">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="c1093-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1093-140">-DefaultProfile</span></span>
<span data-ttu-id="c1093-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c1093-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1093-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="c1093-142">-DeletionDate</span></span>
<span data-ttu-id="c1093-143">Silme tarihini **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="c1093-144">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1093-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="c1093-145">-Edition</span><span class="sxs-lookup"><span data-stu-id="c1093-145">-Edition</span></span>
<span data-ttu-id="c1093-146">SQL veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="c1093-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1093-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c1093-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1093-148">None</span></span>
- <span data-ttu-id="c1093-149">Ana</span><span class="sxs-lookup"><span data-stu-id="c1093-149">Basic</span></span>
- <span data-ttu-id="c1093-150">Ardından</span><span class="sxs-lookup"><span data-stu-id="c1093-150">Standard</span></span>
- <span data-ttu-id="c1093-151">Min</span><span class="sxs-lookup"><span data-stu-id="c1093-151">Premium</span></span>
- <span data-ttu-id="c1093-152">Ambarı</span><span class="sxs-lookup"><span data-stu-id="c1093-152">DataWarehouse</span></span>
- <span data-ttu-id="c1093-153">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="c1093-153">Free</span></span>
- <span data-ttu-id="c1093-154">:</span><span class="sxs-lookup"><span data-stu-id="c1093-154">Stretch</span></span>
- <span data-ttu-id="c1093-155">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="c1093-155">GeneralPurpose</span></span>
- <span data-ttu-id="c1093-156">Departmanla</span><span class="sxs-lookup"><span data-stu-id="c1093-156">BusinessCritical</span></span>

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

### <span data-ttu-id="c1093-157">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="c1093-157">-ElasticPoolName</span></span>
<span data-ttu-id="c1093-158">SQL veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="c1093-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="c1093-160">Bu cmdlet 'in, silinmiş bir SQL veritabanının yedeklemesinden bir veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1093-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="c1093-161">Silinmiş bir SQL veritabanının yedeklemesini almak için Get-AzSqlDeletedDatabaseBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1093-161">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="c1093-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-162">-FromGeoBackup</span></span>
<span data-ttu-id="c1093-163">Bu cmdlet 'in bir SQL veritabanını coğrafi olarak yedekli bir yedekten geri göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1093-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="c1093-164">Coğrafi artıklık yedeği almak için Get-AzSqlDatabaseGeoBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1093-164">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="c1093-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="c1093-166">Bu cmdlet 'in bir SQL veritabanını uzun süreli bekletme yedeklemesinden geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1093-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="c1093-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="c1093-168">Bu cmdlet 'in bir gelen bir noktadan itibaren SQL veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1093-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="c1093-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c1093-169">-LicenseType</span></span>
<span data-ttu-id="c1093-170">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="c1093-170">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c1093-171">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="c1093-171">-PointInTime</span></span>
<span data-ttu-id="c1093-172">SQL veritabanınızı geri yüklemek istediğiniz zamanı bir **Tarih** saat içinde belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="c1093-173">**DateTime** nesnesini almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1093-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="c1093-174">Bu parametreyi *FromPointInTimeBackup* parametresiyle birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1093-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="c1093-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1093-175">-ResourceGroupName</span></span>
<span data-ttu-id="c1093-176">Bu cmdlet 'in SQL veritabanını atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="c1093-177">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c1093-177">-ResourceId</span></span>
<span data-ttu-id="c1093-178">Geri yüklenecek kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-178">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="c1093-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1093-179">-ServerName</span></span>
<span data-ttu-id="c1093-180">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-180">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="c1093-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c1093-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="c1093-182">Hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-182">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="c1093-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1093-183">-TargetDatabaseName</span></span>
<span data-ttu-id="c1093-184">Geri yüklenecek veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1093-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="c1093-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="c1093-185">-VCore</span></span>
<span data-ttu-id="c1093-186">Geri yüklenen Azure SQL veritabanının Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="c1093-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="c1093-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1093-187">CommonParameters</span></span>
<span data-ttu-id="c1093-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1093-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1093-189">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1093-189">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1093-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1093-190">INPUTS</span></span>

### <span data-ttu-id="c1093-191">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c1093-191">System.DateTime</span></span>

### <span data-ttu-id="c1093-192">System. String</span><span class="sxs-lookup"><span data-stu-id="c1093-192">System.String</span></span>

## <span data-ttu-id="c1093-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1093-193">OUTPUTS</span></span>

### <span data-ttu-id="c1093-194">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="c1093-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c1093-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1093-195">NOTES</span></span>

## <span data-ttu-id="c1093-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1093-196">RELATED LINKS</span></span>

[<span data-ttu-id="c1093-197">Azure SQL veritabanını kesinti 'den kurtarma</span><span class="sxs-lookup"><span data-stu-id="c1093-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="c1093-198">Kullanıcı hatasından Azure SQL veritabanını kurtarma</span><span class="sxs-lookup"><span data-stu-id="c1093-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="c1093-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c1093-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="c1093-200">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-200">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="c1093-201">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="c1093-201">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="c1093-202">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c1093-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

