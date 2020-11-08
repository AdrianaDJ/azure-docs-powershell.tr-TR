---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105865"
---
# <span data-ttu-id="a773d-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a773d-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="a773d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a773d-102">SYNOPSIS</span></span>
<span data-ttu-id="a773d-103">Azure SQL veritabanı için özellikleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a773d-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="a773d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a773d-104">SYNTAX</span></span>

### <span data-ttu-id="a773d-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a773d-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a773d-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a773d-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a773d-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="a773d-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a773d-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="a773d-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a773d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a773d-109">DESCRIPTION</span></span>
<span data-ttu-id="a773d-110">**Set-Azurestabanı** cmdlet 'ı BIR Azure SQL veritabanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a773d-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="a773d-111">Veritabanını adla belirtebilirsiniz veya ardışık düzen aracılığıyla Azure SQL veritabanı nesnesini geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a773d-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="a773d-112">Sunucuyu ada göre belirtebilir veya Azure SQL veritabanı sunucusu bağlantı bağlamını geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a773d-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="a773d-113">**New-azures, Databaseservercontext** cmdlet 'ini çalıştırarak bir bağlantı bağlamı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a773d-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="a773d-114">Sunucuyu adıyla belirtirseniz cmdlet, isteğin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a773d-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="a773d-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a773d-115">EXAMPLES</span></span>

### <span data-ttu-id="a773d-116">Örnek 1: bağlantı bağlamı kullanarak veritabanının boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="a773d-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="a773d-117">Bu örnekte, Database01 adlı veritabanının boyutu, Azure SQL veritabanı sunucusu bağlantı bağlamında, $Context.</span><span class="sxs-lookup"><span data-stu-id="a773d-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="a773d-118">Örnek 2: sunucu adı kullanarak veritabanının boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="a773d-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="a773d-119">Bu örnekte, lpqd0zbr8y adlı sunucuda Database01 adlı veritabanının boyutu 20 GB ile değişir.</span><span class="sxs-lookup"><span data-stu-id="a773d-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="a773d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a773d-120">PARAMETERS</span></span>

### <span data-ttu-id="a773d-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a773d-121">-ConnectionContext</span></span>
<span data-ttu-id="a773d-122">Sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-123">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="a773d-123">-Database</span></span>
<span data-ttu-id="a773d-124">Bu cmdlet 'in değiştirdiği Azure SQL veritabanını temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a773d-125">-DatabaseName</span></span>
<span data-ttu-id="a773d-126">Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="a773d-127">-Edition</span></span>
<span data-ttu-id="a773d-128">Azure SQL veritabanı için yeni sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="a773d-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a773d-129">Valid values are:</span></span> 

- <span data-ttu-id="a773d-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a773d-130">None</span></span>
- <span data-ttu-id="a773d-131">Web</span><span class="sxs-lookup"><span data-stu-id="a773d-131">Web</span></span>
- <span data-ttu-id="a773d-132">Karar</span><span class="sxs-lookup"><span data-stu-id="a773d-132">Business</span></span>
- <span data-ttu-id="a773d-133">Ana</span><span class="sxs-lookup"><span data-stu-id="a773d-133">Basic</span></span>
- <span data-ttu-id="a773d-134">Ardından</span><span class="sxs-lookup"><span data-stu-id="a773d-134">Standard</span></span>
-  <span data-ttu-id="a773d-135">Min</span><span class="sxs-lookup"><span data-stu-id="a773d-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-136">-Force</span><span class="sxs-lookup"><span data-stu-id="a773d-136">-Force</span></span>
<span data-ttu-id="a773d-137">Eylemin onay istemeden yapılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="a773d-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a773d-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a773d-138">-MaxSizeBytes</span></span>
<span data-ttu-id="a773d-139">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="a773d-140">Bu parametreyi veya *Maxsizegb* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a773d-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="a773d-141">Sürüm tabanlı kabul edilebilir değerler için *Maxsizegb* parametresine bakın.</span><span class="sxs-lookup"><span data-stu-id="a773d-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="a773d-142">-MaxSizeGB</span></span>
<span data-ttu-id="a773d-143">Veritabanı için yeni en yüksek boyutu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="a773d-144">Bu parametreyi veya *Maxsizebytes* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a773d-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="a773d-145">Kabul edilebilir değerler sürüme göre farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="a773d-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="a773d-146">Temel sürüm değerleri: 1 veya 2</span><span class="sxs-lookup"><span data-stu-id="a773d-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="a773d-147">Standart sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 veya 250</span><span class="sxs-lookup"><span data-stu-id="a773d-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="a773d-148">Premium sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 veya 500</span><span class="sxs-lookup"><span data-stu-id="a773d-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="a773d-149">Web Edition değerleri: 1 veya 5</span><span class="sxs-lookup"><span data-stu-id="a773d-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="a773d-150">İş sürümü değerleri: 10, 20, 30, 40, 50, 100 veya 150</span><span class="sxs-lookup"><span data-stu-id="a773d-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a773d-151">-NewDatabaseName</span></span>
<span data-ttu-id="a773d-152">Veritabanının yeni adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-153">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a773d-153">-PassThru</span></span>
<span data-ttu-id="a773d-154">Güncelleştirilmiş Azure SQL veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a773d-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="a773d-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="a773d-155">-Profile</span></span>
<span data-ttu-id="a773d-156">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a773d-157">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a773d-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a773d-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a773d-158">-ServerName</span></span>
<span data-ttu-id="a773d-159">Bu cmdlet 'in değiştirdiği veritabanını içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-160">-Serviceamacın</span><span class="sxs-lookup"><span data-stu-id="a773d-160">-ServiceObjective</span></span>
<span data-ttu-id="a773d-161">Bu veritabanının yeni hizmet amacını (performans düzeyi) temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="a773d-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="a773d-162">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a773d-162">Valid values are:</span></span> 

- <span data-ttu-id="a773d-163">Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="a773d-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="a773d-164">Standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="a773d-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="a773d-165">Standart (S1): 1b1ebd4d-vseç903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="a773d-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="a773d-166">Standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="a773d-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="a773d-167">\* Standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="a773d-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="a773d-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="a773d-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="a773d-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="a773d-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="a773d-170">Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="a773d-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="a773d-171">\* Standart (S3) en son SQL veritabanı güncelleştirme V12 (Önizleme) parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="a773d-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="a773d-172">Daha fazla bilgi için, Azure SQL Veritabanı V12 Preview 'daki yeniliklere göz atın https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="a773d-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a773d-173">-Eşitleme</span><span class="sxs-lookup"><span data-stu-id="a773d-173">-Sync</span></span>
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

### <span data-ttu-id="a773d-174">-Onay</span><span class="sxs-lookup"><span data-stu-id="a773d-174">-Confirm</span></span>
<span data-ttu-id="a773d-175">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a773d-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a773d-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a773d-176">-WhatIf</span></span>
<span data-ttu-id="a773d-177">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a773d-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a773d-178">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a773d-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a773d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a773d-179">CommonParameters</span></span>
<span data-ttu-id="a773d-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a773d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a773d-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a773d-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a773d-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a773d-182">INPUTS</span></span>

### <span data-ttu-id="a773d-183">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="a773d-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="a773d-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a773d-184">OUTPUTS</span></span>

### <span data-ttu-id="a773d-185">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="a773d-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="a773d-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a773d-186">NOTES</span></span>

## <span data-ttu-id="a773d-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a773d-187">RELATED LINKS</span></span>

[<span data-ttu-id="a773d-188">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="a773d-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a773d-189">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="a773d-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a773d-190">Veritabanını güncelleştir</span><span class="sxs-lookup"><span data-stu-id="a773d-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="a773d-191">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="a773d-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="a773d-192">Yeni-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="a773d-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="a773d-193">Remove-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="a773d-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="a773d-194">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="a773d-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


