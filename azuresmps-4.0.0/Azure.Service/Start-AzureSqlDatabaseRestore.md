---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105426"
---
# <span data-ttu-id="fc833-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="fc833-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="fc833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc833-102">SYNOPSIS</span></span>
<span data-ttu-id="fc833-103">Bir veritabanının zaman içinde geri yüklenmesini gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc833-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="fc833-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc833-104">SYNTAX</span></span>

### <span data-ttu-id="fc833-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc833-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fc833-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc833-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fc833-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc833-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fc833-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc833-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fc833-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc833-109">DESCRIPTION</span></span>
<span data-ttu-id="fc833-110">**Start-AzureSqlDatabaseRestore** cmdlet 'i temel, standart veya Premium veritabanının zaman içinde geri yüklemesini gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc833-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="fc833-111">Azure SQL veritabanı, temel veritabanı yedeklemelerini 7 gün, 14 gün için standart ve 35 gündür Premium korur.</span><span class="sxs-lookup"><span data-stu-id="fc833-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="fc833-112">Geri yükleme işlemi yeni bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc833-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="fc833-113">Kaynak veritabanı silinmişse, *SourceDatabaseName* ve *TargetDatabaseName* parametresinde farklı değerler olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc833-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="fc833-114">Azure SQL veritabanı şu anda çapraz sunucu geri yüklemeyi desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="fc833-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="fc833-115">Kaynak ve hedef sunucu adları aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc833-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="fc833-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc833-116">EXAMPLES</span></span>

### <span data-ttu-id="fc833-117">Örnek 1: nesne olarak belirtilen veritabanını zaman bir noktaya geri yükleme</span><span class="sxs-lookup"><span data-stu-id="fc833-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="fc833-118">İlk komut, server01 adındaki sunucuda Database17 adlı veritabanı için bir veritabanı nesnesi alır ve $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fc833-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="fc833-119">İkinci komut, veritabanını belirli bir zaman noktasına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fc833-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="fc833-120">Bu komut yeni veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="fc833-121">Örnek 2: adla belirtilen bir veritabanını zaman bir noktaya geri yükleme</span><span class="sxs-lookup"><span data-stu-id="fc833-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="fc833-122">Bu komut, Database17 adlı veritabanını belirli bir zaman içinde geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fc833-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="fc833-123">Bu komut yeni veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="fc833-124">Örnek 3: nesne olarak belirtilen bırakılmış veritabanını zaman bir noktaya geri yükleme</span><span class="sxs-lookup"><span data-stu-id="fc833-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="fc833-125">İlk komut, server01 adındaki sunucuda Database01 adlı veritabanı için bir veritabanı nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="fc833-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="fc833-126">Komut geri *yüklenebilen* parametreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="fc833-127">Bu nedenle, cmdlet geri yüklenebilen bir veritabanını belirtilen geri yükleme noktasına alır.</span><span class="sxs-lookup"><span data-stu-id="fc833-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="fc833-128">Komut, veritabanı nesnesini $Database değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fc833-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="fc833-129">İkinci komut $Database tarafından belirtilen bırakılmış veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="fc833-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="fc833-130">Bu komut yeni veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="fc833-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc833-131">PARAMETERS</span></span>

### <span data-ttu-id="fc833-132">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="fc833-132">-PointInTime</span></span>
<span data-ttu-id="fc833-133">Veritabanının geri yükleneceği geri yükleme noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="fc833-134">Geri yükleme işlemi bittiğinde veritabanı, bu parametrenin belirttiği tarih ve saat olan durumuna geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="fc833-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="fc833-135">Varsayılan olarak, bu geçerli saate ayarlanan canlı bir veritabanı için ve bırakılan bir veritabanı için, bu cmdlet veritabanının bırakılmadığı zamanı kullanır.</span><span class="sxs-lookup"><span data-stu-id="fc833-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc833-136">-Profile</span></span>
<span data-ttu-id="fc833-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc833-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fc833-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-139">-Geri yüklenebilen</span><span class="sxs-lookup"><span data-stu-id="fc833-139">-RestorableDropped</span></span>
<span data-ttu-id="fc833-140">Bu cmdlet 'in geri yüklenebilen bir veritabanını geri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc833-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="fc833-141">-SourceDatabase</span></span>
<span data-ttu-id="fc833-142">Bu cmdlet 'in geri belirttiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="fc833-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="fc833-144">Veritabanının silindiği tarih ve saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="fc833-145">Gerçek veritabanı silme zamanına uygun zamanı belirttiğinizde milisaniyeyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc833-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc833-146">-SourceDatabaseName</span></span>
<span data-ttu-id="fc833-147">Bu cmdlet 'in geri belirttiği canlı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="fc833-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="fc833-149">Bu cmdlet 'in geri bildirdiği geri yüklenebilen veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="fc833-150">**Restorabledroppeddatabase** nesnesi almak için Get-AzureSqlDatabase cmdlet 'ini kullanın ve yeniden *stoklama* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="fc833-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="fc833-151">-SourceServerName</span></span>
<span data-ttu-id="fc833-152">Kaynak veritabanının canlı ve çalışıyor olduğu veya kaynak veritabanının silinmeden önce çalıştığı sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc833-153">-TargetDatabaseName</span></span>
<span data-ttu-id="fc833-154">Geri yükleme işleminin oluşturduğu yeni veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="fc833-155">-TargetServerName</span></span>
<span data-ttu-id="fc833-156">Bu cmdlet 'in veritabanını geri yüklediğinde sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc833-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="fc833-157">Azure SQL veritabanı şu anda çapraz sunucu geri yüklemeyi desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="fc833-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="fc833-158">Kaynak ve hedef sunucu adları aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc833-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc833-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc833-159">CommonParameters</span></span>
<span data-ttu-id="fc833-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc833-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc833-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc833-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc833-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc833-162">INPUTS</span></span>

### <span data-ttu-id="fc833-163">Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="fc833-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="fc833-164">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="fc833-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="fc833-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc833-165">OUTPUTS</span></span>

### <span data-ttu-id="fc833-166">Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. Restoredatabaseişlemi</span><span class="sxs-lookup"><span data-stu-id="fc833-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="fc833-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc833-167">NOTES</span></span>
* <span data-ttu-id="fc833-168">Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="fc833-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="fc833-169">Bu cmdlet 'i çalıştıran bilgisayarda aşağıdaki komutları çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="fc833-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="fc833-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc833-170">RELATED LINKS</span></span>

[<span data-ttu-id="fc833-171">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="fc833-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fc833-172">Veritabanı geri yükleme Isteği oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc833-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="fc833-173">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="fc833-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fc833-174">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="fc833-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


