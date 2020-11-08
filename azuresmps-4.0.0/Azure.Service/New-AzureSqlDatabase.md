---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105973"
---
# <span data-ttu-id="069bb-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="069bb-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="069bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="069bb-102">SYNOPSIS</span></span>
<span data-ttu-id="069bb-103">Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="069bb-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="069bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="069bb-104">SYNTAX</span></span>

### <span data-ttu-id="069bb-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="069bb-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="069bb-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="069bb-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="069bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="069bb-107">DESCRIPTION</span></span>
<span data-ttu-id="069bb-108">**New-Azurestabanı** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="069bb-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="069bb-109">**Yeni-Azuressqldatabaseservercontext** cmdlet 'ini kullanarak oluşturduğunuz BIR Azure SQL veritabanı sunucusu bağlantı bağlamını kullanarak sunucuyu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="069bb-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="069bb-110">Veya sunucu adını belirtirseniz, cmdlet, sunucuya erişim isteğinde kimlik doğrulaması yapmak için geçerli Azure aboneliği bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="069bb-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="069bb-111">Bir Azure SQL veritabanı sunucusu belirterek yeni bir veritabanı oluşturduğunuzda, **Yeni-Azuressqldatabase** cmdlet 'i, bu işlemi gerçekleştirmek için belirtilen sunucu adını ve geçerli Azure aboneliği bilgilerini kullanarak geçici bir bağlantı bağlamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="069bb-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="069bb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="069bb-112">EXAMPLES</span></span>

### <span data-ttu-id="069bb-113">Örnek 1: veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="069bb-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="069bb-114">Bu komut, Azure SQL veritabanı sunucusu $Context bağlantı bağlamı için Database1 adlı bir Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="069bb-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="069bb-115">Örnek 2: geçerli abonelikte veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="069bb-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="069bb-116">Bu örnek, lpqd0zbr8y adlı belirtilen Azure SQL veritabanı sunucusunda Database1 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="069bb-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="069bb-117">Cmdlet, sunucuya erişim isteğinin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="069bb-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="069bb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="069bb-118">PARAMETERS</span></span>

### <span data-ttu-id="069bb-119">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="069bb-119">-Collation</span></span>
<span data-ttu-id="069bb-120">Yeni veritabanı için harmanlamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="069bb-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="069bb-121">-ConnectionContext</span></span>
<span data-ttu-id="069bb-122">Bu cmdlet 'in veritabanı oluşturduğu sunucunun bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="069bb-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="069bb-123">-DatabaseName</span></span>
<span data-ttu-id="069bb-124">Yeni veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-124">Specifies the name of the new database.</span></span>

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

### <span data-ttu-id="069bb-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="069bb-125">-Edition</span></span>
<span data-ttu-id="069bb-126">Yeni Azure SQL veritabanı için sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="069bb-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="069bb-127">Valid values are:</span></span> 

- <span data-ttu-id="069bb-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="069bb-128">None</span></span>
- <span data-ttu-id="069bb-129">Web</span><span class="sxs-lookup"><span data-stu-id="069bb-129">Web</span></span>
- <span data-ttu-id="069bb-130">Karar</span><span class="sxs-lookup"><span data-stu-id="069bb-130">Business</span></span>
- <span data-ttu-id="069bb-131">Ana</span><span class="sxs-lookup"><span data-stu-id="069bb-131">Basic</span></span>
- <span data-ttu-id="069bb-132">Ardından</span><span class="sxs-lookup"><span data-stu-id="069bb-132">Standard</span></span>
-  <span data-ttu-id="069bb-133">Min</span><span class="sxs-lookup"><span data-stu-id="069bb-133">Premium</span></span>

<span data-ttu-id="069bb-134">Varsayılan değer Web.</span><span class="sxs-lookup"><span data-stu-id="069bb-134">The default value is Web.</span></span>

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

### <span data-ttu-id="069bb-135">-Force</span><span class="sxs-lookup"><span data-stu-id="069bb-135">-Force</span></span>
<span data-ttu-id="069bb-136">Eylemin kullanıcıya onay istemeden yapılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="069bb-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="069bb-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="069bb-137">-MaxSizeBytes</span></span>
<span data-ttu-id="069bb-138">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="069bb-139">Bu parametreyi veya *Maxsizegb* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="069bb-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="069bb-140">Sürüm tabanlı kabul edilebilir değerler için *Maxsizegb* parametre açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="069bb-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="069bb-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="069bb-141">-MaxSizeGB</span></span>
<span data-ttu-id="069bb-142">En yüksek veritabanı boyutunu gigabayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="069bb-143">Bu parametreyi veya *Maxsizebytes* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="069bb-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="069bb-144">Kabul edilebilir değerler sürüme göre farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="069bb-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="069bb-145">Temel sürüm değerleri: 1 veya 2</span><span class="sxs-lookup"><span data-stu-id="069bb-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="069bb-146">Standart sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 veya 250</span><span class="sxs-lookup"><span data-stu-id="069bb-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="069bb-147">Premium sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 veya 500</span><span class="sxs-lookup"><span data-stu-id="069bb-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="069bb-148">Web Edition değerleri: 1 veya 5</span><span class="sxs-lookup"><span data-stu-id="069bb-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="069bb-149">İş sürümü değerleri: 10, 20, 30, 40, 50, 100 veya 150</span><span class="sxs-lookup"><span data-stu-id="069bb-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="069bb-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="069bb-150">-Profile</span></span>
<span data-ttu-id="069bb-151">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="069bb-152">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="069bb-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="069bb-153">-ServerName</span><span class="sxs-lookup"><span data-stu-id="069bb-153">-ServerName</span></span>
<span data-ttu-id="069bb-154">Yeni veritabanını içerecek Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

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

### <span data-ttu-id="069bb-155">-Serviceamacın</span><span class="sxs-lookup"><span data-stu-id="069bb-155">-ServiceObjective</span></span>
<span data-ttu-id="069bb-156">Bu veritabanının yeni hizmet amacını (performans düzeyi) temsil eden bir nesne belirtir.</span><span class="sxs-lookup"><span data-stu-id="069bb-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="069bb-157">Bu değer, bu veritabanına atanan kaynakların düzeyini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="069bb-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="069bb-158">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="069bb-158">Valid values are:</span></span> 

<span data-ttu-id="069bb-159">Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standart (S1): 1b1ebd4d/cr903-4baa-97f9-4ea675f5e928 standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 720348,-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="069bb-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="069bb-160">\* Standart (S3) en son SQL veritabanı güncelleştirme V12 (Önizleme) parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="069bb-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="069bb-161">Daha fazla bilgi için, Azure SQL Veritabanı V12 Preview 'daki yeniliklere göz atın https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="069bb-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="069bb-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="069bb-162">-Confirm</span></span>
<span data-ttu-id="069bb-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="069bb-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="069bb-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="069bb-164">-WhatIf</span></span>
<span data-ttu-id="069bb-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="069bb-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="069bb-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="069bb-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="069bb-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069bb-167">CommonParameters</span></span>
<span data-ttu-id="069bb-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="069bb-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069bb-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="069bb-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069bb-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="069bb-170">INPUTS</span></span>

## <span data-ttu-id="069bb-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="069bb-171">OUTPUTS</span></span>

### <span data-ttu-id="069bb-172">Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="069bb-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="069bb-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="069bb-173">NOTES</span></span>
* <span data-ttu-id="069bb-174">**Yeni-azures, veritabanı** tarafından oluşturulan veritabanını silmek için Remove-AzureSqlDatabase cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="069bb-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="069bb-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="069bb-175">RELATED LINKS</span></span>

[<span data-ttu-id="069bb-176">Azure SQL veritabanı</span><span class="sxs-lookup"><span data-stu-id="069bb-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="069bb-177">Veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="069bb-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="069bb-178">Azure SQL veritabanları için işlemler</span><span class="sxs-lookup"><span data-stu-id="069bb-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="069bb-179">Get-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="069bb-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="069bb-180">New-Azuressqldatabaseservercontext</span><span class="sxs-lookup"><span data-stu-id="069bb-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="069bb-181">Remove-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="069bb-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="069bb-182">Set-Azuressqldatabase</span><span class="sxs-lookup"><span data-stu-id="069bb-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


