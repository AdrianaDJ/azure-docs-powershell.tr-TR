---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a40b5bd15681342975ddb080fa12fbaac9bcf60e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938097"
---
# <span data-ttu-id="5ab29-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5ab29-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="5ab29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab29-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab29-103">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="5ab29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ab29-104">SYNTAX</span></span>

### <span data-ttu-id="5ab29-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ab29-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab29-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="5ab29-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ab29-107">DESCRIPTION</span></span>
<span data-ttu-id="5ab29-108">**Set-Azsqlelaunpool** cmdlet 'ı, Azure SQL veritabanında esnek bir havuzun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ab29-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="5ab29-109">Bu cmdlet, havuz başına eDTU ( *DTU* ), havuz başına depolama sınırı ( *storagemb* ), veritabanı başına en fazla eDTU ( *databaseval* ) ve en az eDTU ( *databasedtumın* ).</span><span class="sxs-lookup"><span data-stu-id="5ab29-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="5ab29-110">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="5ab29-111">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="5ab29-112">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="5ab29-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ab29-113">EXAMPLES</span></span>

### <span data-ttu-id="5ab29-114">Örnek 1: esnek bir havuzun özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5ab29-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="5ab29-115">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5ab29-116">Komut, elastik havuzun sayısını 1000 olarak ayarlar ve en az ve en fazla değer sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ab29-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="5ab29-117">Örnek 2: esnek bir havuzun en büyük depolama boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="5ab29-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="5ab29-118">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="5ab29-119">Bu komut, elastik havuzun en büyük depolama alanını 2 TB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ab29-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="5ab29-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ab29-120">PARAMETERS</span></span>

### <span data-ttu-id="5ab29-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="5ab29-121">-AsJob</span></span>
<span data-ttu-id="5ab29-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5ab29-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ab29-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5ab29-123">-ComputeGeneration</span></span>
<span data-ttu-id="5ab29-124">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="5ab29-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab29-125">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="5ab29-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="5ab29-126">Havuzdaki tek bir veritabanının tüketebileceği en fazla MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="5ab29-127">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5ab29-128">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="5ab29-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="5ab29-129">Ana.</span><span class="sxs-lookup"><span data-stu-id="5ab29-129">Basic.</span></span>  <span data-ttu-id="5ab29-130">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-130">5 DTUs</span></span>
- <span data-ttu-id="5ab29-131">Ardından.</span><span class="sxs-lookup"><span data-stu-id="5ab29-131">Standard.</span></span> <span data-ttu-id="5ab29-132">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-132">100 DTUs</span></span>
- <span data-ttu-id="5ab29-133">Min.</span><span class="sxs-lookup"><span data-stu-id="5ab29-133">Premium.</span></span> <span data-ttu-id="5ab29-134">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-134">125 DTUs</span></span>

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

### <span data-ttu-id="5ab29-135">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="5ab29-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="5ab29-136">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="5ab29-137">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5ab29-138">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="5ab29-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="5ab29-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="5ab29-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="5ab29-140">Havuzda en yüksek sayıda SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5ab29-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="5ab29-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="5ab29-142">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="5ab29-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab29-143">-DefaultProfile</span></span>
<span data-ttu-id="5ab29-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5ab29-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ab29-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="5ab29-145">-Dtu</span></span>
<span data-ttu-id="5ab29-146">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="5ab29-147">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="5ab29-148">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="5ab29-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="5ab29-149">Ana.</span><span class="sxs-lookup"><span data-stu-id="5ab29-149">Basic.</span></span> <span data-ttu-id="5ab29-150">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-150">100 DTUs</span></span>
- <span data-ttu-id="5ab29-151">Ardından.</span><span class="sxs-lookup"><span data-stu-id="5ab29-151">Standard.</span></span> <span data-ttu-id="5ab29-152">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-152">100 DTUs</span></span>
- <span data-ttu-id="5ab29-153">Min.</span><span class="sxs-lookup"><span data-stu-id="5ab29-153">Premium.</span></span> <span data-ttu-id="5ab29-154">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="5ab29-154">125 DTUs</span></span>

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

### <span data-ttu-id="5ab29-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="5ab29-155">-Edition</span></span>
<span data-ttu-id="5ab29-156">Elastik havuz için Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="5ab29-157">Sürümü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ab29-157">You cannot change the edition.</span></span> <span data-ttu-id="5ab29-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5ab29-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5ab29-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5ab29-159">None</span></span>
- <span data-ttu-id="5ab29-160">Ana</span><span class="sxs-lookup"><span data-stu-id="5ab29-160">Basic</span></span>
- <span data-ttu-id="5ab29-161">Ardından</span><span class="sxs-lookup"><span data-stu-id="5ab29-161">Standard</span></span>
- <span data-ttu-id="5ab29-162">Min</span><span class="sxs-lookup"><span data-stu-id="5ab29-162">Premium</span></span>
- <span data-ttu-id="5ab29-163">Ambarı</span><span class="sxs-lookup"><span data-stu-id="5ab29-163">DataWarehouse</span></span>
- <span data-ttu-id="5ab29-164">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="5ab29-164">Free</span></span>
- <span data-ttu-id="5ab29-165">:</span><span class="sxs-lookup"><span data-stu-id="5ab29-165">Stretch</span></span>
- <span data-ttu-id="5ab29-166">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="5ab29-166">GeneralPurpose</span></span>
- <span data-ttu-id="5ab29-167">Departmanla</span><span class="sxs-lookup"><span data-stu-id="5ab29-167">BusinessCritical</span></span>

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

### <span data-ttu-id="5ab29-168">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="5ab29-168">-ElasticPoolName</span></span>
<span data-ttu-id="5ab29-169">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-169">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab29-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5ab29-170">-LicenseType</span></span>
<span data-ttu-id="5ab29-171">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="5ab29-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5ab29-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab29-172">-ResourceGroupName</span></span>
<span data-ttu-id="5ab29-173">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5ab29-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ab29-174">-ServerName</span></span>
<span data-ttu-id="5ab29-175">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5ab29-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="5ab29-176">-StorageMB</span></span>
<span data-ttu-id="5ab29-177">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="5ab29-178">Daha fazla bilgi için New-AzSqlElasticPool cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="5ab29-179">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="5ab29-179">-Tags</span></span>
<span data-ttu-id="5ab29-180">Bu cmdlet 'in karma tablo biçimindeki esnek havuz ile ilişki kurduğu anahtar değer çiftlerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="5ab29-181">Örneğin: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="5ab29-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="5ab29-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="5ab29-182">-VCore</span></span>
<span data-ttu-id="5ab29-183">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="5ab29-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab29-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5ab29-184">-ZoneRedundant</span></span>
<span data-ttu-id="5ab29-185">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="5ab29-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="5ab29-186">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ab29-186">-Confirm</span></span>
<span data-ttu-id="5ab29-187">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ab29-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab29-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab29-188">-WhatIf</span></span>
<span data-ttu-id="5ab29-189">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ab29-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab29-190">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ab29-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab29-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab29-191">CommonParameters</span></span>
<span data-ttu-id="5ab29-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ab29-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab29-193">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ab29-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab29-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ab29-194">INPUTS</span></span>

### <span data-ttu-id="5ab29-195">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab29-195">System.String</span></span>

## <span data-ttu-id="5ab29-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ab29-196">OUTPUTS</span></span>

### <span data-ttu-id="5ab29-197">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="5ab29-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5ab29-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ab29-198">NOTES</span></span>

## <span data-ttu-id="5ab29-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ab29-199">RELATED LINKS</span></span>

[<span data-ttu-id="5ab29-200">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="5ab29-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="5ab29-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5ab29-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="5ab29-202">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="5ab29-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="5ab29-203">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="5ab29-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="5ab29-204">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5ab29-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
