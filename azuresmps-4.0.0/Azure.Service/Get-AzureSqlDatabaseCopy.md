---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106295"
---
# <span data-ttu-id="a45df-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a45df-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="a45df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45df-102">SYNOPSIS</span></span>
<span data-ttu-id="a45df-103">İlişki kopyalama durumunu denetler.</span><span class="sxs-lookup"><span data-stu-id="a45df-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="a45df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a45df-104">SYNTAX</span></span>

### <span data-ttu-id="a45df-105">ByServerNameOnly (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a45df-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a45df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a45df-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a45df-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="a45df-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a45df-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a45df-108">DESCRIPTION</span></span>
<span data-ttu-id="a45df-109">**Get-azures, Databasecopy** cmdlet 'i bir veya daha fazla etkin kopya ilişkisinin durumunu denetler.</span><span class="sxs-lookup"><span data-stu-id="a45df-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="a45df-110">Start-AzureSqlDatabaseCopy veya Stop-AzureSqlDatabaseCopy cmdlet 'ini çalıştırdıktan sonra bu cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a45df-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="a45df-111">Belirli bir kopya ilişkisini, tüm kopya ilişkilerini veya belirli bir hedef sunucudaki tüm kopyalar gibi kopyalama ilişkilerinin filtrelenmiş listesini denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a45df-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="a45df-112">Bu cmdlet 'i kaynak veya hedef veritabanını barındıran sunucuda çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a45df-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="a45df-113">Bu cmdlet zaman uyumludur.</span><span class="sxs-lookup"><span data-stu-id="a45df-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="a45df-114">Cmdlet, bir durum nesnesi döndürdüğünden Azure PowerShell konsolunu engeller.</span><span class="sxs-lookup"><span data-stu-id="a45df-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="a45df-115">*PartnerServer* ve *partnerdatabase* parametreleri isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a45df-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="a45df-116">Parametre belirtmezseniz, bu cmdlet bir sonuç tablosu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a45df-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="a45df-117">Yalnızca belirli bir veritabanının durumunu görmek için her iki parametreyi de belirtin.</span><span class="sxs-lookup"><span data-stu-id="a45df-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="a45df-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a45df-118">EXAMPLES</span></span>

### <span data-ttu-id="a45df-119">Örnek 1: veritabanının kopyalama durumunu alma</span><span class="sxs-lookup"><span data-stu-id="a45df-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="a45df-120">Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a45df-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="a45df-121">*PartnerServer* parametresi bu komutu bk0b8kf658 sunucusuyla sınırlar.</span><span class="sxs-lookup"><span data-stu-id="a45df-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="a45df-122">Örnek 2: sunucudaki tüm kopyaların durumunu alma sunucudaki tüm kopyaların durumunu alma</span><span class="sxs-lookup"><span data-stu-id="a45df-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="a45df-123">Bu komut, lpqd0zbr8y adındaki sunucudaki tüm etkin kopyaların durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a45df-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="a45df-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a45df-124">PARAMETERS</span></span>

### <span data-ttu-id="a45df-125">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="a45df-125">-Database</span></span>
<span data-ttu-id="a45df-126">Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="a45df-127">Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a45df-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a45df-128">-DatabaseCopy</span></span>
<span data-ttu-id="a45df-129">Veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="a45df-130">Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a45df-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="a45df-131">Bu parametre kanal girişini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="a45df-131">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a45df-132">-DatabaseName</span></span>
<span data-ttu-id="a45df-133">Kaynak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="a45df-134">Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a45df-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="a45df-135">-PartnerDatabase</span></span>
<span data-ttu-id="a45df-136">İkincil veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="a45df-137">Bu veritabanı sys.dm_database_copies dinamik yönetim görünümünde bulunmazsa, bu cmdlet boş bir durum nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a45df-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="a45df-138">-PartnerServer</span></span>
<span data-ttu-id="a45df-139">Hedef veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="a45df-140">Bu sunucu sys.dm_database_copies dinamik yönetim görünümünde bulunmazsa, bu cmdlet boş bir durum nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a45df-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="a45df-141">-Profile</span></span>
<span data-ttu-id="a45df-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a45df-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a45df-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a45df-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a45df-144">-ServerName</span></span>
<span data-ttu-id="a45df-145">Veritabanı kopyasının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45df-145">Specifies the name of the server on which the database copy resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a45df-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45df-146">CommonParameters</span></span>
<span data-ttu-id="a45df-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a45df-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45df-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45df-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45df-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a45df-149">INPUTS</span></span>

### <span data-ttu-id="a45df-150">Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a45df-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="a45df-151">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="a45df-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="a45df-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a45df-152">OUTPUTS</span></span>

### <span data-ttu-id="a45df-153">Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a45df-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="a45df-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a45df-154">NOTES</span></span>
* <span data-ttu-id="a45df-155">Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a45df-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="a45df-156">Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için New-AzureSqlDatabaseServerContext cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a45df-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="a45df-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a45df-157">RELATED LINKS</span></span>

[<span data-ttu-id="a45df-158">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="a45df-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a45df-159">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="a45df-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a45df-160">Azure SQL veritabanı cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a45df-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="a45df-161">Start-Azuressqldatabasecopy</span><span class="sxs-lookup"><span data-stu-id="a45df-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="a45df-162">Stop-Azuresurdatabasecopy</span><span class="sxs-lookup"><span data-stu-id="a45df-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


