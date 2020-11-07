---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758892"
---
# <span data-ttu-id="186df-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="186df-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="186df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186df-102">SYNOPSIS</span></span>
<span data-ttu-id="186df-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="186df-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="186df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="186df-104">SYNTAX</span></span>

### <span data-ttu-id="186df-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="186df-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="186df-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="186df-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="186df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="186df-107">DESCRIPTION</span></span>
<span data-ttu-id="186df-108">**New-Azsqlelaunpool** cmdlet 'ı BIR Azure SQL veritabanı için elastik veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="186df-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="186df-109">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="186df-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="186df-110">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="186df-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="186df-111">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="186df-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="186df-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="186df-112">EXAMPLES</span></span>

### <span data-ttu-id="186df-113">Örnek 1: esnek havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="186df-113">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="186df-114">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="186df-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="186df-115">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="186df-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="186df-116">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="186df-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="186df-117">PARAMETERS</span></span>

### <span data-ttu-id="186df-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="186df-118">-AsJob</span></span>
<span data-ttu-id="186df-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="186df-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="186df-120">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="186df-120">-ComputeGeneration</span></span>
<span data-ttu-id="186df-121">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="186df-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="186df-122">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="186df-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="186df-123">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="186df-124">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="186df-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="186df-125">Ana.</span><span class="sxs-lookup"><span data-stu-id="186df-125">Basic.</span></span> <span data-ttu-id="186df-126">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="186df-126">5 DTUs</span></span>
- <span data-ttu-id="186df-127">Ardından.</span><span class="sxs-lookup"><span data-stu-id="186df-127">Standard.</span></span> <span data-ttu-id="186df-128">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="186df-128">100 DTUs</span></span>
- <span data-ttu-id="186df-129">Min.</span><span class="sxs-lookup"><span data-stu-id="186df-129">Premium.</span></span> <span data-ttu-id="186df-130">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılar Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="186df-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="186df-131">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="186df-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="186df-132">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="186df-133">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="186df-133">The default value is zero (0).</span></span>
<span data-ttu-id="186df-134">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="186df-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="186df-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="186df-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="186df-136">Tüm SqlAzure veritabanı, havuzda tüketebilir.</span><span class="sxs-lookup"><span data-stu-id="186df-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="186df-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="186df-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="186df-138">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="186df-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="186df-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186df-139">-DefaultProfile</span></span>
<span data-ttu-id="186df-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="186df-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="186df-141">-DTU</span><span class="sxs-lookup"><span data-stu-id="186df-141">-Dtu</span></span>
<span data-ttu-id="186df-142">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="186df-143">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="186df-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="186df-144">Ana.</span><span class="sxs-lookup"><span data-stu-id="186df-144">Basic.</span></span>
<span data-ttu-id="186df-145">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="186df-145">100 DTUs</span></span>
- <span data-ttu-id="186df-146">Ardından.</span><span class="sxs-lookup"><span data-stu-id="186df-146">Standard.</span></span>
<span data-ttu-id="186df-147">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="186df-147">100 DTUs</span></span>
- <span data-ttu-id="186df-148">Min.</span><span class="sxs-lookup"><span data-stu-id="186df-148">Premium.</span></span>
<span data-ttu-id="186df-149">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)belirli boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="186df-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="186df-150">-Edition</span><span class="sxs-lookup"><span data-stu-id="186df-150">-Edition</span></span>
<span data-ttu-id="186df-151">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="186df-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="186df-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="186df-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="186df-153">None</span></span>
- <span data-ttu-id="186df-154">Ana</span><span class="sxs-lookup"><span data-stu-id="186df-154">Basic</span></span>
- <span data-ttu-id="186df-155">Ardından</span><span class="sxs-lookup"><span data-stu-id="186df-155">Standard</span></span>
- <span data-ttu-id="186df-156">Min</span><span class="sxs-lookup"><span data-stu-id="186df-156">Premium</span></span>
- <span data-ttu-id="186df-157">Ambarı</span><span class="sxs-lookup"><span data-stu-id="186df-157">DataWarehouse</span></span>
- <span data-ttu-id="186df-158">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="186df-158">Free</span></span>
- <span data-ttu-id="186df-159">:</span><span class="sxs-lookup"><span data-stu-id="186df-159">Stretch</span></span>
- <span data-ttu-id="186df-160">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="186df-160">GeneralPurpose</span></span>
- <span data-ttu-id="186df-161">Departmanla</span><span class="sxs-lookup"><span data-stu-id="186df-161">BusinessCritical</span></span>

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

### <span data-ttu-id="186df-162">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="186df-162">-ElasticPoolName</span></span>
<span data-ttu-id="186df-163">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="186df-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="186df-164">-LicenseType</span></span>
<span data-ttu-id="186df-165">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="186df-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="186df-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="186df-166">-ResourceGroupName</span></span>
<span data-ttu-id="186df-167">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="186df-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="186df-168">-ServerName</span></span>
<span data-ttu-id="186df-169">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="186df-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="186df-170">-StorageMB</span></span>
<span data-ttu-id="186df-171">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="186df-172">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="186df-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="186df-173">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="186df-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="186df-174">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="186df-174">-Tags</span></span>
<span data-ttu-id="186df-175">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="186df-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="186df-176">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="186df-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="186df-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="186df-177">-VCore</span></span>
<span data-ttu-id="186df-178">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="186df-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="186df-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="186df-179">-ZoneRedundant</span></span>
<span data-ttu-id="186df-180">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="186df-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="186df-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="186df-181">-Confirm</span></span>
<span data-ttu-id="186df-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="186df-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="186df-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="186df-183">-WhatIf</span></span>
<span data-ttu-id="186df-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="186df-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="186df-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="186df-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="186df-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186df-186">CommonParameters</span></span>
<span data-ttu-id="186df-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="186df-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186df-188">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="186df-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186df-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="186df-189">INPUTS</span></span>

### <span data-ttu-id="186df-190">System. String</span><span class="sxs-lookup"><span data-stu-id="186df-190">System.String</span></span>

## <span data-ttu-id="186df-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="186df-191">OUTPUTS</span></span>

### <span data-ttu-id="186df-192">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="186df-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="186df-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="186df-193">NOTES</span></span>

## <span data-ttu-id="186df-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="186df-194">RELATED LINKS</span></span>

[<span data-ttu-id="186df-195">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="186df-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="186df-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="186df-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="186df-197">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="186df-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="186df-198">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="186df-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="186df-199">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="186df-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="186df-200">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="186df-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
