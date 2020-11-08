---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105845"
---
# <span data-ttu-id="29216-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="29216-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="29216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29216-102">SYNOPSIS</span></span>
<span data-ttu-id="29216-103">Azure SQL veritabanının kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="29216-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="29216-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29216-104">SYNTAX</span></span>

### <span data-ttu-id="29216-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29216-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29216-106">Byinputobjectdevamlı</span><span class="sxs-lookup"><span data-stu-id="29216-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29216-107">VeritabanıAdı</span><span class="sxs-lookup"><span data-stu-id="29216-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29216-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="29216-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29216-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="29216-109">DESCRIPTION</span></span>
<span data-ttu-id="29216-110">**Start-azures, Databasecopy** cmdlet 'i bir kerelik bir kopya işlemi başlatır veya belirli BIR Azure SQL veritabanının sürekli kopyalama işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="29216-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="29216-111">Bu cmdlet işlem değildir.</span><span class="sxs-lookup"><span data-stu-id="29216-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="29216-112">Özgün veritabanı kaynak veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="29216-112">The original database is the source database.</span></span>
<span data-ttu-id="29216-113">Kopya ikincil veya hedef veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="29216-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="29216-114">Sürekli bir kopyada, kaynak ve hedef veritabanları aynı sunucuda yer alamaz ve kaynak ve hedef veritabanlarını barındıran sunucular aynı aboneliğin bir parçası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="29216-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="29216-115">*ContinuousCopy* parametresini belirtmezseniz, bu cmdlet kaynak veritabanının tek seferlik bir kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="29216-116">Yanıt alındığında işlem hala devam ediyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="29216-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="29216-117">Get-AzureSqlDatabaseCopy veya Get-AzureSqlDatabaseOperation cmdlet 'ini kullanarak işlemi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29216-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="29216-118">*ContinuousCopy* belirtirseniz, bu cmdlet kaynak veritabanının sürekli bir kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="29216-119">Yanıt alındığında işlem devam eder.</span><span class="sxs-lookup"><span data-stu-id="29216-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="29216-120">**Get-azures, Databasecopy** veya **Get-azuressqldatabaseoperation** kullanarak işlemi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29216-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="29216-121">Çevrimiçi veya çevrimdışı veritabanı olarak sürekli bir kopya oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29216-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="29216-122">Çevrimiçi sürekli kopya, Azure SQL veritabanı için Active Geo-Replication Directory 'yi yapılandırmak için kullanılır https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="29216-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="29216-123">Çevrimdışı sürekli kopya, Azure SQL veritabanı için standart Geo-Replication yapılandırmak için kullanılır https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="29216-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="29216-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29216-124">EXAMPLES</span></span>

### <span data-ttu-id="29216-125">Örnek 1: sürekli bir veritabanı kopyası zamanlama</span><span class="sxs-lookup"><span data-stu-id="29216-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="29216-126">Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının sürekli bir kopyasını zamanlar.</span><span class="sxs-lookup"><span data-stu-id="29216-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="29216-127">Komut, bk0b8kf658 adlı sunucuda bir hedef veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="29216-128">Örnek 2: aynı sunucuda bir kerelik bir kopya oluşturma</span><span class="sxs-lookup"><span data-stu-id="29216-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="29216-129">Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının tek seferlik bir kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="29216-130">Bu komut aynı sunucuda OrdersCopy adlı bir kopya oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="29216-131">Örnek 3: sürekli bir çevrimdışı veritabanı kopyası zamanlama</span><span class="sxs-lookup"><span data-stu-id="29216-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="29216-132">Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının sürekli bir kopyasını zamanlar.</span><span class="sxs-lookup"><span data-stu-id="29216-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="29216-133">Bu komut, bk0b8kf658 adlı sunucuda bir çevrimdışı hedef veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29216-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="29216-134">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29216-134">PARAMETERS</span></span>

### <span data-ttu-id="29216-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="29216-135">-ContinuousCopy</span></span>
<span data-ttu-id="29216-136">Veritabanı kopyasının sürekli kopya olacağını (yineleme veritabanı) gösterir.</span><span class="sxs-lookup"><span data-stu-id="29216-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="29216-137">Aynı sunucuda sürekli kopyalama desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="29216-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="29216-138">Bu parametre belirtilmezse, bir kerelik kopya gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="29216-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="29216-139">Bir kerelik bir kopyada, kaynak ve iş ortağı veritabanları aynı sunucuda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="29216-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29216-140">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="29216-140">-Database</span></span>
<span data-ttu-id="29216-141">Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="29216-142">Bu parametre kanal girişini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="29216-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29216-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29216-143">-DatabaseName</span></span>
<span data-ttu-id="29216-144">Kaynak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29216-145">-Force</span><span class="sxs-lookup"><span data-stu-id="29216-145">-Force</span></span>
<span data-ttu-id="29216-146">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="29216-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29216-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="29216-147">-OfflineSecondary</span></span>
<span data-ttu-id="29216-148">Etkin bir kopya yerine sürekli bir kopyanın pasif kopya olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="29216-149">Kaynak veritabanı Standard Edition veritabanıdır, bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="29216-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="29216-150">Bu parametre belirtilirse, *ContinuousCopy* de belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="29216-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29216-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="29216-151">-PartnerDatabase</span></span>
<span data-ttu-id="29216-152">Hedef veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-152">Specifies name of the target database.</span></span>
<span data-ttu-id="29216-153">*ContinuousCopy* parametresini belirtirseniz, *partnerdatabase* değeri kaynak veritabanının adıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="29216-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="29216-154">*ContinuousCopy* belirtmezseniz, hedef veritabanı için kaynak veritabanı adından farklı olabilecek bir ad belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="29216-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29216-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="29216-155">-PartnerServer</span></span>
<span data-ttu-id="29216-156">Hedef veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="29216-157">Bu sunucunun kaynak veritabanı sunucusuyla aynı Azure aboneliği içinde olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="29216-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29216-158">-Profil</span><span class="sxs-lookup"><span data-stu-id="29216-158">-Profile</span></span>
<span data-ttu-id="29216-159">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29216-160">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="29216-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29216-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29216-161">-ServerName</span></span>
<span data-ttu-id="29216-162">Kaynak veritabanının bulunduğu sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29216-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="29216-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="29216-163">-Confirm</span></span>
<span data-ttu-id="29216-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29216-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29216-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29216-165">-WhatIf</span></span>
<span data-ttu-id="29216-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29216-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29216-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29216-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29216-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29216-168">CommonParameters</span></span>
<span data-ttu-id="29216-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29216-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29216-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29216-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29216-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29216-171">INPUTS</span></span>

### <span data-ttu-id="29216-172">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="29216-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="29216-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29216-173">OUTPUTS</span></span>

### <span data-ttu-id="29216-174">Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="29216-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="29216-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29216-175">NOTES</span></span>
* <span data-ttu-id="29216-176">Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir.</span><span class="sxs-lookup"><span data-stu-id="29216-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="29216-177">Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için New-AzureSqlDatabaseServerContext cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="29216-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="29216-178">İzleme: sunucuda etkin bir veya daha fazla sürekli kopya ilişkisinin durumunu denetlemek Için **Get-Azuressqldatabasecopy** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="29216-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="29216-179">Sürekli kopyalama ilişkisinin hem kaynağı hem de hedefinin her ikisinde de işlemlerin durumunu doğrulamak için **Get-Azuressqldatabaseoperation** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="29216-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="29216-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29216-180">RELATED LINKS</span></span>

[<span data-ttu-id="29216-181">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="29216-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="29216-182">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="29216-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="29216-183">Veritabanı kopyasını başlatma</span><span class="sxs-lookup"><span data-stu-id="29216-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="29216-184">Azure SQL veritabanı cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="29216-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="29216-185">Get-Azuressqldatabasecopy</span><span class="sxs-lookup"><span data-stu-id="29216-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="29216-186">Stop-Azuresurdatabasecopy</span><span class="sxs-lookup"><span data-stu-id="29216-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


