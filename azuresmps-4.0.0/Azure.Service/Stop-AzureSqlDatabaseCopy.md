---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106403"
---
# <span data-ttu-id="d3e0c-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d3e0c-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="d3e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e0c-103">Sürekli bir kopya ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="d3e0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3e0c-104">SYNTAX</span></span>

### <span data-ttu-id="d3e0c-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3e0c-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e0c-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="d3e0c-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e0c-107">VeritabanıAdı</span><span class="sxs-lookup"><span data-stu-id="d3e0c-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3e0c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3e0c-108">DESCRIPTION</span></span>
<span data-ttu-id="d3e0c-109">**Stop-Azuresurdatabasecopy** cmdlet 'i sürekli bir kopyalama ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="d3e0c-110">Bu cmdlet, kaynak veritabanı ile ikincil veya hedef veritabanı arasındaki veri hareketini durdurur ve ikincil veritabanının durumunu tek başına bir çevrimiçi veritabanı olacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="d3e0c-111">Sürekli bir kopya ilişkisini, sonlandırmasını veya planlı sonlandırmayı ve olası veri kaybına karşı zorla sonlandırmanın iki yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="d3e0c-112">Kaynak veritabanını barındıran sunucuda bu cmdlet 'i sonlandırma veya zorunlu sonlandırma modunda çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="d3e0c-113">İkincil veritabanını barındıran sunucuda Zorlanmış sonlandırma modunu kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="d3e0c-114">Bir planlı sonlandırma, kaynak veritabanındaki tüm teslim edilen işlemlerin, cmdlet 'i çalıştırdığınız sırada ikincil veritabanına çoğaltıldığını belirten şekilde bekler.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="d3e0c-115">Zorunlu sonlandırma, bekleyen kaydedilmiş işlemlerin çoğaltılmasını beklemez ve ikincil veritabanında olası veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="d3e0c-116">Çoğaltma durumu beklemede olduğunda, sürekli bir kopya ilişkisini başarıyla sonlandırabilir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="d3e0c-117">Çoğaltma durumu beklemede olduğunda, zorunlu olmayan sonlandırma desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="d3e0c-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3e0c-118">EXAMPLES</span></span>

### <span data-ttu-id="d3e0c-119">Örnek 1: sürekli bir kopya ilişkisini sonlandırma</span><span class="sxs-lookup"><span data-stu-id="d3e0c-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="d3e0c-120">Bu komut, lpqd0zbr8y adlı sunucudaki veritabanı adlı siparişlerin sürekli kopyalama ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="d3e0c-121">Bk0b8kf658 adındaki sunucu ikincil veritabanını barındırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="d3e0c-122">Örnek 2: sürekli bir kopya ilişkisini zorla sonlandırma</span><span class="sxs-lookup"><span data-stu-id="d3e0c-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="d3e0c-123">İlk komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanı için veritabanı kopyalama ilişkisini alır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="d3e0c-124">İkinci komut, ikincil veritabanını barındıran sunucudan sürekli bir kopya ilişkisini zorla sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="d3e0c-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3e0c-125">PARAMETERS</span></span>

### <span data-ttu-id="d3e0c-126">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="d3e0c-126">-Database</span></span>
<span data-ttu-id="d3e0c-127">Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="d3e0c-128">Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3e0c-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d3e0c-129">-DatabaseCopy</span></span>
<span data-ttu-id="d3e0c-130">Veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="d3e0c-131">Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="d3e0c-132">Bu parametre kanal girişini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="d3e0c-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3e0c-133">-DatabaseName</span></span>
<span data-ttu-id="d3e0c-134">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-134">Specifies the name of a database.</span></span>
<span data-ttu-id="d3e0c-135">Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e0c-136">-Force</span><span class="sxs-lookup"><span data-stu-id="d3e0c-136">-Force</span></span>
<span data-ttu-id="d3e0c-137">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3e0c-138">-Forcevseçişten çıkarma</span><span class="sxs-lookup"><span data-stu-id="d3e0c-138">-ForcedTermination</span></span>
<span data-ttu-id="d3e0c-139">Bu cmdlet 'in sürekli kopyalama ilişkisinin zorunlu olarak sonlandırılmasına neden olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="d3e0c-140">Zorunlu sonlandırma veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="d3e0c-141">Bu cmdlet 'i hedef veritabanını barındıran bir sunucuda çalıştırmak için bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="d3e0c-142">Bu cmdlet 'i kaynak veritabanını barındıran bir sunucuda çalıştırmak için, ikincil veritabanı kullanılamıyorsa bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="d3e0c-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="d3e0c-143">-PartnerDatabase</span></span>
<span data-ttu-id="d3e0c-144">İkincil veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="d3e0c-145">Bir ad belirtirseniz, kaynak veritabanının adıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e0c-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="d3e0c-146">-PartnerServer</span></span>
<span data-ttu-id="d3e0c-147">Hedef veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e0c-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3e0c-148">-Profile</span></span>
<span data-ttu-id="d3e0c-149">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3e0c-150">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3e0c-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3e0c-151">-ServerName</span></span>
<span data-ttu-id="d3e0c-152">Kaynak veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="d3e0c-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3e0c-153">-Confirm</span></span>
<span data-ttu-id="d3e0c-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e0c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e0c-155">-WhatIf</span></span>
<span data-ttu-id="d3e0c-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e0c-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e0c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e0c-158">CommonParameters</span></span>
<span data-ttu-id="d3e0c-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e0c-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e0c-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e0c-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3e0c-161">INPUTS</span></span>

### <span data-ttu-id="d3e0c-162">Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d3e0c-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="d3e0c-163">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="d3e0c-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="d3e0c-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3e0c-164">OUTPUTS</span></span>

### <span data-ttu-id="d3e0c-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3e0c-165">None</span></span>

## <span data-ttu-id="d3e0c-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3e0c-166">NOTES</span></span>
* <span data-ttu-id="d3e0c-167">Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="d3e0c-168">Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için, **New-Azuressqldatabaseservercontext** cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="d3e0c-169">Kısıtlamalar: ikincil veritabanını barındıran sunucuda, yalnızca zorunlu sonlandırma desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="d3e0c-170">Eski ikincil veritabanında sonlandırma etkisi: sonlandırıldıktan sonra, ikincil veritabanı bağımsız bir veritabanı olur.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="d3e0c-171">İkinci veritabanında dengeli dağıtım işlemi tamamlandıktan sonra, bu veritabanı tam erişim için açılır.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="d3e0c-172">Kaynak veritabanı bir okuma-yazma veritabanıdır, eski ikincil veritabanı da okuma-yazma veritabanı olur.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="d3e0c-173">Dengeli dağıtım devam ediyorsa, dengeli dağıtım durdurulur ve eski ikincil veritabanı ikincil veritabanını barındıran sunucuda hiçbir zaman görünmez duruma geçmez.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="d3e0c-174">Kaynak veritabanını salt okunur moduna getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="d3e0c-175">Bu, kaynak ve ikincil veritabanlarının işten çıkarıldıktan sonra eşitlenmesini ve sonlandırma sırasında hiçbir hareketin tutulmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="d3e0c-176">Sonlandırma işlemi tamamlandıktan sonra, kaynağı tekrar okuma moduna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="d3e0c-177">İsteğe bağlı olarak, eski ikincil veritabanını okuma yazma moduna da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="d3e0c-178">İzleme: işlemlerin durumunu sürekli kopyalama ilişkisinin hem kaynağına hem de hedeften doğrulamak Için **Get-Azuressqldatabaseoperation** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="d3e0c-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3e0c-179">RELATED LINKS</span></span>

[<span data-ttu-id="d3e0c-180">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="d3e0c-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d3e0c-181">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="d3e0c-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d3e0c-182">Veritabanını Kopyalamayı durdur</span><span class="sxs-lookup"><span data-stu-id="d3e0c-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="d3e0c-183">Azure SQL veritabanı cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d3e0c-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="d3e0c-184">Get-Azuressqldatabasecopy</span><span class="sxs-lookup"><span data-stu-id="d3e0c-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="d3e0c-185">Start-Azuressqldatabasecopy</span><span class="sxs-lookup"><span data-stu-id="d3e0c-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


