---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106298"
---
# <span data-ttu-id="e7472-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="e7472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7472-102">SYNOPSIS</span></span>
<span data-ttu-id="e7472-103">Bir veya daha fazla veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="e7472-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7472-104">SYNTAX</span></span>

### <span data-ttu-id="e7472-105">ByConnectionContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7472-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e7472-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="e7472-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7472-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7472-107">DESCRIPTION</span></span>
<span data-ttu-id="e7472-108">**Get-Azurestabanı** cmdlet 'i BIR Azure SQL veritabanı sunucusundan bir veya birden çok Azure SQL veritabanının örneğini alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="e7472-109">Sunucuyu, **New-Azuressqldatabaseservercontext** cmdlet 'ini kullanarak oluşturduğunuz BIR Azure SQL veritabanı sunucusu bağlantı içeriğiyle belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7472-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="e7472-110">Veya Azure SQL veritabanı sunucusu adını belirtirseniz cmdlet, sunucuya erişim isteğinin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7472-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="e7472-111">Bir veritabanı belirtmezseniz, **Get-Azurestabanı** cmdlet 'i belirtilen sunucudaki tüm veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7472-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="e7472-112">Geri yüklenebilen veritabanları alınıyor:</span><span class="sxs-lookup"><span data-stu-id="e7472-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="e7472-113">*Restorabledroburparameter* 'ı kullanarak geri yüklenebilen veritabanlarını alın.</span><span class="sxs-lookup"><span data-stu-id="e7472-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="e7472-114">Geri yüklenebilen tüm veritabanlarını döndürmek için *DatabaseName* ve *Databasedeletiondate* olmadan *restorabledroburparameter* 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7472-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="e7472-115">Geri yüklenebilen belirli bir veritabanını geri yüklemek için, *DatabaseName* ve *Databasedeletiondate* parametreleriyle *restorabledroburparametresini* kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7472-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="e7472-116">*DatabaseName* parametresini kullanarak geri yüklenebilen belirli bir veritabanını alırken, *databasedeletiondate* parametresini de eklemeniz gerekir ve belirtilen *databasedeletiondate* değeri, istenen veritabanıyla eşleşen milisaniyeyi içermelidir.</span><span class="sxs-lookup"><span data-stu-id="e7472-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="e7472-117">**Get-Azurestabanı** cmdlet 'i, bir sunucuda bırakılmış tüm geri yüklenebilir veritabanları veya hem *DatabaseName* hem de *databasedeletiondate* ile eşleşen belirli bir veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="e7472-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="e7472-118">Belirli bir adın geri yüklenebilen tüm veritabanları gibi farklı ölçütlere uyan geri yüklenebilen bırakılmış veritabanlarını geri yüklemek için, geri yüklenebilen tüm veritabanlarını geri iade etmelisiniz ve ardından sonuçları istemcide filtrelemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e7472-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="e7472-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7472-119">EXAMPLES</span></span>

### <span data-ttu-id="e7472-120">Örnek 1: sunucudaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="e7472-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="e7472-121">Bu komut, lpqd0zbr8y adındaki sunucudaki tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="e7472-122">Örnek 2: sunucuda bırakılan tüm geri yüklenebilen veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="e7472-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="e7472-123">Bu komut, lpqd0zbr8y adlı sunucudaki tüm geri yüklenebilen veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="e7472-124">Örnek 3: bağlantı bağlamında belirtilen sunucudan veritabanı alma</span><span class="sxs-lookup"><span data-stu-id="e7472-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="e7472-125">Bu komut, Database01 adlı veritabanını bağlantı bağlamında belirtilen sunucudan alır $Context.</span><span class="sxs-lookup"><span data-stu-id="e7472-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="e7472-126">Örnek 4: bir değişkende veritabanı nesnesini depolama</span><span class="sxs-lookup"><span data-stu-id="e7472-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="e7472-127">Bu komut, Database01 adlı sunucudan gelen veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e7472-128">Komut, veritabanı nesnesini $Database 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e7472-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="e7472-129">Örnek 5: geri yüklenebilen bir veritabanını alma</span><span class="sxs-lookup"><span data-stu-id="e7472-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="e7472-130">Bu komut, 11/9/2012 tarihinde lpqd0zbr8y adındaki sunucudan silinen Database01 adlı geri yüklenebilen veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="e7472-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e7472-131">Bu komut sonuçları $DroppedDB değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e7472-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="e7472-132">Örnek 6: tüm geri yüklenebilen veritabanlarını bir sunucuda alma ve sonuçlara filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="e7472-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="e7472-133">Bu komut, lpqd0zbr8y adlı sunucudaki tüm geri yüklenebilen veritabanlarını alır ve sonuçları yalnızca ContactDB adlı veritabanlarına süzer.</span><span class="sxs-lookup"><span data-stu-id="e7472-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="e7472-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7472-134">PARAMETERS</span></span>

### <span data-ttu-id="e7472-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="e7472-135">-ConnectionContext</span></span>
<span data-ttu-id="e7472-136">Veritabanının alınacağı sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7472-137">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="e7472-137">-Database</span></span>
<span data-ttu-id="e7472-138">Bu cmdlet 'in aldığı veritabanını temsil eden nesneyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7472-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="e7472-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="e7472-140">Silme işleminin tarih ve saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="e7472-141">Geri yüklenebilen parametreyi belirtirseniz, silme tarih ve saatine göre geri yüklenebilen bir veritabanını almak için *Bu parametreyi belirtin* .</span><span class="sxs-lookup"><span data-stu-id="e7472-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="e7472-142">*Databasedeletiondate* parametresi, istenen veritabanının saatine uyması için milisaniye içermelidir.</span><span class="sxs-lookup"><span data-stu-id="e7472-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="e7472-143">Milisaniye olmadan bir değer belirttiğinizde veritabanı bulunamamıştır.</span><span class="sxs-lookup"><span data-stu-id="e7472-143">Specifying a value without milliseconds results in the database not being found.</span></span>

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

### <span data-ttu-id="e7472-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7472-144">-DatabaseName</span></span>
<span data-ttu-id="e7472-145">Bu cmdlet 'in aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="e7472-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7472-146">-Profile</span></span>
<span data-ttu-id="e7472-147">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7472-148">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e7472-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7472-149">-Geri yüklenebilen</span><span class="sxs-lookup"><span data-stu-id="e7472-149">-RestorableDropped</span></span>
<span data-ttu-id="e7472-150">Bu cmdlet 'in *veritabanı* nesneleri yerine *Restorabledroppeddatabase* nesnelerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="e7472-151">Belirli bir geri yüklenebilen veritabanını seçmek için *Databasedeletiondate* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7472-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

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

### <span data-ttu-id="e7472-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="e7472-153">Bu cmdlet 'in aldığı geri yüklenebilen veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7472-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7472-154">-ServerName</span></span>
<span data-ttu-id="e7472-155">Bu cmdlet 'in aldığı veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7472-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="e7472-156">Cmdlet sunucuya erişmek için geçerli Azure aboneliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7472-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7472-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7472-157">CommonParameters</span></span>
<span data-ttu-id="e7472-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7472-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7472-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7472-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7472-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7472-160">INPUTS</span></span>

### <span data-ttu-id="e7472-161">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="e7472-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="e7472-162">Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="e7472-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7472-163">OUTPUTS</span></span>

### <span data-ttu-id="e7472-164">'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="e7472-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="e7472-165">Geri *yüklenebilen* parametreyi belirtmezseniz, bu cmdlet *veritabanı* nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7472-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="e7472-166">'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="e7472-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="e7472-167">Bu cmdlet, *restorabledroburparameter* 'i belirttiğinizde bir *Restorabıledroppeddatabase* nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7472-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="e7472-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7472-168">NOTES</span></span>

## <span data-ttu-id="e7472-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7472-169">RELATED LINKS</span></span>

[<span data-ttu-id="e7472-170">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="e7472-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e7472-171">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="e7472-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e7472-172">Yeni-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="e7472-173">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="e7472-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="e7472-174">Remove-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="e7472-175">Set-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="e7472-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


