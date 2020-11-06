---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 5b1901ef5d06d24e6561861dca3c8e1d89185d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589994"
---
# <span data-ttu-id="fd5d2-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fd5d2-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="fd5d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5d2-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd5d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd5d2-104">SYNTAX</span></span>

### <span data-ttu-id="fd5d2-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd5d2-105">DtuBasedPool (Default)</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd5d2-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="fd5d2-106">VcoreBasedPool</span></span>
```
New-AzureRmSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd5d2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd5d2-107">DESCRIPTION</span></span>
<span data-ttu-id="fd5d2-108">**Yeni-Azurermsqlelak,** BIR Azure SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-108">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="fd5d2-109">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="fd5d2-110">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="fd5d2-111">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="fd5d2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd5d2-112">EXAMPLES</span></span>

### <span data-ttu-id="fd5d2-113">Örnek 1: esnek havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="fd5d2-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="fd5d2-114">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="fd5d2-115">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="fd5d2-116">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="fd5d2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd5d2-117">PARAMETERS</span></span>

### <span data-ttu-id="fd5d2-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="fd5d2-118">-AsJob</span></span>
<span data-ttu-id="fd5d2-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fd5d2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd5d2-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fd5d2-120">-ComputeGeneration</span></span>
<span data-ttu-id="fd5d2-121">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-121">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-122">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="fd5d2-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="fd5d2-123">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="fd5d2-124">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="fd5d2-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="fd5d2-125">Ana.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-125">Basic.</span></span> <span data-ttu-id="fd5d2-126">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="fd5d2-126">5 DTUs</span></span>
- <span data-ttu-id="fd5d2-127">Ardından.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-127">Standard.</span></span> <span data-ttu-id="fd5d2-128">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="fd5d2-128">100 DTUs</span></span>
- <span data-ttu-id="fd5d2-129">Min.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-129">Premium.</span></span> <span data-ttu-id="fd5d2-130">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılar Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="fd5d2-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-131">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="fd5d2-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="fd5d2-132">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="fd5d2-133">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="fd5d2-133">The default value is zero (0).</span></span>
<span data-ttu-id="fd5d2-134">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="fd5d2-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="fd5d2-136">Tüm SqlAzure veritabanı, havuzda tüketebilir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="fd5d2-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="fd5d2-138">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5d2-139">-DefaultProfile</span></span>
<span data-ttu-id="fd5d2-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd5d2-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd5d2-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="fd5d2-141">-Dtu</span></span>
<span data-ttu-id="fd5d2-142">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="fd5d2-143">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="fd5d2-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="fd5d2-144">Ana.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-144">Basic.</span></span>
<span data-ttu-id="fd5d2-145">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="fd5d2-145">100 DTUs</span></span>
- <span data-ttu-id="fd5d2-146">Ardından.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-146">Standard.</span></span>
<span data-ttu-id="fd5d2-147">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="fd5d2-147">100 DTUs</span></span>
- <span data-ttu-id="fd5d2-148">Min.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-148">Premium.</span></span>
<span data-ttu-id="fd5d2-149">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)belirli boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="fd5d2-150">-Edition</span></span>
<span data-ttu-id="fd5d2-151">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="fd5d2-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fd5d2-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd5d2-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fd5d2-153">None</span></span>
- <span data-ttu-id="fd5d2-154">Ana</span><span class="sxs-lookup"><span data-stu-id="fd5d2-154">Basic</span></span>
- <span data-ttu-id="fd5d2-155">Ardından</span><span class="sxs-lookup"><span data-stu-id="fd5d2-155">Standard</span></span>
- <span data-ttu-id="fd5d2-156">Min</span><span class="sxs-lookup"><span data-stu-id="fd5d2-156">Premium</span></span>
- <span data-ttu-id="fd5d2-157">Ambarı</span><span class="sxs-lookup"><span data-stu-id="fd5d2-157">DataWarehouse</span></span>
- <span data-ttu-id="fd5d2-158">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="fd5d2-158">Free</span></span>
- <span data-ttu-id="fd5d2-159">:</span><span class="sxs-lookup"><span data-stu-id="fd5d2-159">Stretch</span></span>
- <span data-ttu-id="fd5d2-160">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="fd5d2-160">GeneralPurpose</span></span>
- <span data-ttu-id="fd5d2-161">Departmanla</span><span class="sxs-lookup"><span data-stu-id="fd5d2-161">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-162">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="fd5d2-162">-ElasticPoolName</span></span>
<span data-ttu-id="fd5d2-163">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fd5d2-164">-LicenseType</span></span>
<span data-ttu-id="fd5d2-165">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="fd5d2-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5d2-166">-ResourceGroupName</span></span>
<span data-ttu-id="fd5d2-167">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="fd5d2-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd5d2-168">-ServerName</span></span>
<span data-ttu-id="fd5d2-169">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-169">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="fd5d2-170">-StorageMB</span></span>
<span data-ttu-id="fd5d2-171">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="fd5d2-172">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="fd5d2-173">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-174">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="fd5d2-174">-Tags</span></span>
<span data-ttu-id="fd5d2-175">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="fd5d2-176">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fd5d2-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="fd5d2-177">-VCore</span></span>
<span data-ttu-id="fd5d2-178">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fd5d2-179">-ZoneRedundant</span></span>
<span data-ttu-id="fd5d2-180">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="fd5d2-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="fd5d2-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd5d2-181">-Confirm</span></span>
<span data-ttu-id="fd5d2-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd5d2-183">-WhatIf</span></span>
<span data-ttu-id="fd5d2-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd5d2-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd5d2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5d2-186">CommonParameters</span></span>
<span data-ttu-id="fd5d2-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd5d2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5d2-188">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd5d2-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5d2-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd5d2-189">INPUTS</span></span>

### <span data-ttu-id="fd5d2-190">System. String</span><span class="sxs-lookup"><span data-stu-id="fd5d2-190">System.String</span></span>

## <span data-ttu-id="fd5d2-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd5d2-191">OUTPUTS</span></span>

### <span data-ttu-id="fd5d2-192">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="fd5d2-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="fd5d2-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd5d2-193">NOTES</span></span>

## <span data-ttu-id="fd5d2-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd5d2-194">RELATED LINKS</span></span>

[<span data-ttu-id="fd5d2-195">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="fd5d2-195">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fd5d2-196">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="fd5d2-196">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="fd5d2-197">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="fd5d2-197">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="fd5d2-198">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="fd5d2-198">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fd5d2-199">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="fd5d2-199">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="fd5d2-200">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="fd5d2-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
