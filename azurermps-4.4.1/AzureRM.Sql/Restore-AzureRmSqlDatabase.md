---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589038"
---
# <span data-ttu-id="b36fc-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b36fc-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="b36fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b36fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b36fc-103">SQL veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b36fc-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b36fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b36fc-104">SYNTAX</span></span>

### <span data-ttu-id="b36fc-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b36fc-106">Fromdatabasebackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b36fc-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b36fc-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b36fc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b36fc-109">DESCRIPTION</span></span>
<span data-ttu-id="b36fc-110">**Restore-AzureRmSqlDatabase** cmdlet 'i, bir SQL veritabanını coğrafi olarak yedekli bir yedekten, silinmiş bir veritabanının yedeğini, uzun dönemli bir yedek yedeklemeyi veya Live veritabanında bir noktayı geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b36fc-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="b36fc-111">Geri yüklenen veritabanı yeni bir veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b36fc-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="b36fc-112">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, esnek bir SQL veritabanı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b36fc-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="b36fc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b36fc-113">EXAMPLES</span></span>

### <span data-ttu-id="b36fc-114">Örnek 1: veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b36fc-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="b36fc-115">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b36fc-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="b36fc-116">İkinci komut, $Database belirtilen noktadan noktaya yedekten, Restoredveritabanı adlı veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b36fc-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="b36fc-117">Örnek 2: bir veritabanını esnek bir havuzun bir noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b36fc-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="b36fc-118">İlk komut Database01 adındaki SQL veritabanını alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b36fc-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="b36fc-119">İkinci komut, elasticpool01 adlı elastik havuzda geri Restokveritabanı adlı SQL veritabanına belirtilen noktadan noktaya $Database yedekten geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b36fc-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="b36fc-120">Örnek 3: silinen veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b36fc-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="b36fc-121">İlk komut, [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b36fc-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b36fc-122">İkinci komut restore [-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet 'ini kullanarak silinen veritabanı yedeklemesinden geri yüklemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b36fc-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="b36fc-123">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b36fc-124">Örnek 4: silinen veritabanını esnek bir havuza geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b36fc-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="b36fc-125">İlk komut, [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)kullanarak geri yüklemek istediğiniz silinmiş veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="b36fc-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="b36fc-126">İkinci komut restore [-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)öğesini kullanarak silinen veritabanı yedeklemesinden geri yüklemeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="b36fc-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="b36fc-127">-PointInTime parametresi belirtilmemişse, veritabanı silme zamanına geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="b36fc-128">Örnek 5: veritabanı Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="b36fc-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="b36fc-129">İlk komut, Database01 adlı veritabanının coğrafi yedekli yedeklemesini alır ve $GeoBackup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b36fc-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="b36fc-130">İkinci komut $GeoBackup, yedeği RestoredDatabase adlı SQL veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="b36fc-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="b36fc-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b36fc-131">PARAMETERS</span></span>

### <span data-ttu-id="b36fc-132">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="b36fc-132">-DeletionDate</span></span>
<span data-ttu-id="b36fc-133">Silme tarihini **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-133">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="b36fc-134">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b36fc-134">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="b36fc-135">-Edition</span></span>
<span data-ttu-id="b36fc-136">SQL veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-136">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="b36fc-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b36fc-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b36fc-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b36fc-138">None</span></span>
- <span data-ttu-id="b36fc-139">Min</span><span class="sxs-lookup"><span data-stu-id="b36fc-139">Premium</span></span>
- <span data-ttu-id="b36fc-140">Ana</span><span class="sxs-lookup"><span data-stu-id="b36fc-140">Basic</span></span>
- <span data-ttu-id="b36fc-141">Ardından</span><span class="sxs-lookup"><span data-stu-id="b36fc-141">Standard</span></span>
- <span data-ttu-id="b36fc-142">Ambarı</span><span class="sxs-lookup"><span data-stu-id="b36fc-142">DataWarehouse</span></span>
- <span data-ttu-id="b36fc-143">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="b36fc-143">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-144">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="b36fc-144">-ElasticPoolName</span></span>
<span data-ttu-id="b36fc-145">SQL veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-145">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="b36fc-146">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-146">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="b36fc-147">Bu cmdlet 'in, silinmiş bir SQL veritabanının yedeklemesinden bir veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-147">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="b36fc-148">Silinmiş bir SQL veritabanının yedeklemesini almak için Get-AzureRMSqlDeletedDatabaseBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b36fc-148">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-149">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-149">-FromGeoBackup</span></span>
<span data-ttu-id="b36fc-150">Bu cmdlet 'in bir SQL veritabanını coğrafi olarak yedekli bir yedekten geri göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-150">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="b36fc-151">Coğrafi artıklık yedeği almak için Get-AzureRMSqlDatabaseGeoBackup cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b36fc-151">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-152">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-152">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="b36fc-153">Bu cmdlet 'in bir SQL veritabanını uzun süreli bekletme yedeklemesinden geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-153">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-154">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-154">-FromPointInTimeBackup</span></span>
<span data-ttu-id="b36fc-155">Bu cmdlet 'in bir gelen bir noktadan itibaren SQL veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-155">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-156">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="b36fc-156">-PointInTime</span></span>
<span data-ttu-id="b36fc-157">SQL veritabanınızı geri yüklemek istediğiniz zamanı bir **Tarih** saat içinde belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-157">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="b36fc-158">**DateTime** nesnesini almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b36fc-158">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="b36fc-159">Bu parametreyi *FromPointInTimeBackup* parametresiyle birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="b36fc-159">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b36fc-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b36fc-160">-ResourceGroupName</span></span>
<span data-ttu-id="b36fc-161">Bu cmdlet 'in SQL veritabanını atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-161">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="b36fc-162">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b36fc-162">-ResourceId</span></span>
<span data-ttu-id="b36fc-163">Geri yüklenecek kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-163">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="b36fc-164">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b36fc-164">-ServerName</span></span>
<span data-ttu-id="b36fc-165">SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-165">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="b36fc-166">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b36fc-166">-ServiceObjectiveName</span></span>
<span data-ttu-id="b36fc-167">Hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-167">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="b36fc-168">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b36fc-168">-TargetDatabaseName</span></span>
<span data-ttu-id="b36fc-169">Geri yüklenecek veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b36fc-169">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="b36fc-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36fc-170">-DefaultProfile</span></span>
<span data-ttu-id="b36fc-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b36fc-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36fc-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36fc-172">CommonParameters</span></span>
<span data-ttu-id="b36fc-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b36fc-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36fc-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b36fc-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36fc-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b36fc-175">INPUTS</span></span>

## <span data-ttu-id="b36fc-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b36fc-176">OUTPUTS</span></span>

### <span data-ttu-id="b36fc-177">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="b36fc-177">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b36fc-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b36fc-178">NOTES</span></span>

## <span data-ttu-id="b36fc-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b36fc-179">RELATED LINKS</span></span>

[<span data-ttu-id="b36fc-180">Azure SQL veritabanını kesinti 'den kurtarma</span><span class="sxs-lookup"><span data-stu-id="b36fc-180">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="b36fc-181">Kullanıcı hatasından Azure SQL veritabanını kurtarma</span><span class="sxs-lookup"><span data-stu-id="b36fc-181">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="b36fc-182">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b36fc-182">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="b36fc-183">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-183">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="b36fc-184">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="b36fc-184">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="b36fc-185">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b36fc-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

