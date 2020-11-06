---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 6b059905cdc1e9474ce455f78fac88f282b5ce10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590812"
---
# <span data-ttu-id="af2bf-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="af2bf-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="af2bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="af2bf-103">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af2bf-104">SYNTAX</span></span>

### <span data-ttu-id="af2bf-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af2bf-105">DtuBasedPool (Default)</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af2bf-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="af2bf-106">VcoreBasedPool</span></span>
```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2bf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af2bf-107">DESCRIPTION</span></span>
<span data-ttu-id="af2bf-108">**Set-Azurermsqlelak,** Azure SQL veritabanındaki esnek bir havuzun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="af2bf-108">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="af2bf-109">Bu cmdlet, havuz başına eDTU ( *DTU* ), havuz başına depolama sınırı ( *storagemb* ), veritabanı başına en fazla eDTU ( *databaseval\*\*) ve* en az eDTU</span><span class="sxs-lookup"><span data-stu-id="af2bf-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>
<span data-ttu-id="af2bf-110">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="af2bf-111">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="af2bf-112">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="af2bf-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="af2bf-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af2bf-113">EXAMPLES</span></span>

### <span data-ttu-id="af2bf-114">Örnek 1: esnek bir havuzun özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="af2bf-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="af2bf-115">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="af2bf-116">Komut, elastik havuzun sayısını 1000 olarak ayarlar ve en az ve en fazla değer sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="af2bf-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="af2bf-117">Örnek 2: esnek bir havuzun en büyük depolama boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="af2bf-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="af2bf-118">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="af2bf-119">Bu komut, elastik havuzun en büyük depolama alanını 2 TB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="af2bf-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="af2bf-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af2bf-120">PARAMETERS</span></span>

### <span data-ttu-id="af2bf-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="af2bf-121">-AsJob</span></span>
<span data-ttu-id="af2bf-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="af2bf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af2bf-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="af2bf-123">-ComputeGeneration</span></span>
<span data-ttu-id="af2bf-124">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="af2bf-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="af2bf-125">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="af2bf-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="af2bf-126">Havuzdaki tek bir veritabanının tüketebileceği en fazla MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="af2bf-127">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="af2bf-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="af2bf-128">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="af2bf-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="af2bf-129">Ana.</span><span class="sxs-lookup"><span data-stu-id="af2bf-129">Basic.</span></span>  <span data-ttu-id="af2bf-130">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-130">5 DTUs</span></span>
- <span data-ttu-id="af2bf-131">Ardından.</span><span class="sxs-lookup"><span data-stu-id="af2bf-131">Standard.</span></span> <span data-ttu-id="af2bf-132">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-132">100 DTUs</span></span>
- <span data-ttu-id="af2bf-133">Min.</span><span class="sxs-lookup"><span data-stu-id="af2bf-133">Premium.</span></span> <span data-ttu-id="af2bf-134">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-134">125 DTUs</span></span>

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

### <span data-ttu-id="af2bf-135">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="af2bf-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="af2bf-136">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="af2bf-137">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="af2bf-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="af2bf-138">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="af2bf-138">The default value is zero (0).</span></span>

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

### <span data-ttu-id="af2bf-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="af2bf-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="af2bf-140">Tüm SqlAzure veritabanı, havuzda tüketebilir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-140">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="af2bf-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="af2bf-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="af2bf-142">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="af2bf-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2bf-143">-DefaultProfile</span></span>
<span data-ttu-id="af2bf-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="af2bf-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af2bf-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="af2bf-145">-Dtu</span></span>
<span data-ttu-id="af2bf-146">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="af2bf-147">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="af2bf-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="af2bf-148">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="af2bf-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="af2bf-149">Ana.</span><span class="sxs-lookup"><span data-stu-id="af2bf-149">Basic.</span></span> <span data-ttu-id="af2bf-150">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-150">100 DTUs</span></span>
- <span data-ttu-id="af2bf-151">Ardından.</span><span class="sxs-lookup"><span data-stu-id="af2bf-151">Standard.</span></span> <span data-ttu-id="af2bf-152">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-152">100 DTUs</span></span>
- <span data-ttu-id="af2bf-153">Min.</span><span class="sxs-lookup"><span data-stu-id="af2bf-153">Premium.</span></span> <span data-ttu-id="af2bf-154">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="af2bf-154">125 DTUs</span></span>

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

### <span data-ttu-id="af2bf-155">-Edition</span><span class="sxs-lookup"><span data-stu-id="af2bf-155">-Edition</span></span>
<span data-ttu-id="af2bf-156">Elastik havuz için Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="af2bf-157">Sürümü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="af2bf-157">You cannot change the edition.</span></span> <span data-ttu-id="af2bf-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af2bf-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af2bf-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af2bf-159">None</span></span>
- <span data-ttu-id="af2bf-160">Ana</span><span class="sxs-lookup"><span data-stu-id="af2bf-160">Basic</span></span>
- <span data-ttu-id="af2bf-161">Ardından</span><span class="sxs-lookup"><span data-stu-id="af2bf-161">Standard</span></span>
- <span data-ttu-id="af2bf-162">Min</span><span class="sxs-lookup"><span data-stu-id="af2bf-162">Premium</span></span>
- <span data-ttu-id="af2bf-163">Ambarı</span><span class="sxs-lookup"><span data-stu-id="af2bf-163">DataWarehouse</span></span>
- <span data-ttu-id="af2bf-164">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="af2bf-164">Free</span></span>
- <span data-ttu-id="af2bf-165">:</span><span class="sxs-lookup"><span data-stu-id="af2bf-165">Stretch</span></span>
- <span data-ttu-id="af2bf-166">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="af2bf-166">GeneralPurpose</span></span>
- <span data-ttu-id="af2bf-167">Departmanla</span><span class="sxs-lookup"><span data-stu-id="af2bf-167">BusinessCritical</span></span>

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

### <span data-ttu-id="af2bf-168">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="af2bf-168">-ElasticPoolName</span></span>
<span data-ttu-id="af2bf-169">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-169">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="af2bf-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="af2bf-170">-LicenseType</span></span>
<span data-ttu-id="af2bf-171">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="af2bf-171">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="af2bf-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2bf-172">-ResourceGroupName</span></span>
<span data-ttu-id="af2bf-173">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="af2bf-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af2bf-174">-ServerName</span></span>
<span data-ttu-id="af2bf-175">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="af2bf-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="af2bf-176">-StorageMB</span></span>
<span data-ttu-id="af2bf-177">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="af2bf-178">Daha fazla bilgi için New-AzureRmSqlElasticPool cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="af2bf-178">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="af2bf-179">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="af2bf-179">-Tags</span></span>
<span data-ttu-id="af2bf-180">Bu cmdlet 'in karma tablo biçimindeki esnek havuz ile ilişki kurduğu anahtar değer çiftlerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="af2bf-181">Örneğin: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="af2bf-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="af2bf-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="af2bf-182">-VCore</span></span>
<span data-ttu-id="af2bf-183">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="af2bf-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="af2bf-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="af2bf-184">-ZoneRedundant</span></span>
<span data-ttu-id="af2bf-185">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="af2bf-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="af2bf-186">-Onay</span><span class="sxs-lookup"><span data-stu-id="af2bf-186">-Confirm</span></span>
<span data-ttu-id="af2bf-187">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af2bf-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af2bf-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2bf-188">-WhatIf</span></span>
<span data-ttu-id="af2bf-189">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af2bf-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2bf-190">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af2bf-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af2bf-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2bf-191">CommonParameters</span></span>
<span data-ttu-id="af2bf-192">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af2bf-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2bf-193">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2bf-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2bf-194">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af2bf-194">INPUTS</span></span>

### <span data-ttu-id="af2bf-195">System. String</span><span class="sxs-lookup"><span data-stu-id="af2bf-195">System.String</span></span>

## <span data-ttu-id="af2bf-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af2bf-196">OUTPUTS</span></span>

### <span data-ttu-id="af2bf-197">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="af2bf-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="af2bf-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af2bf-198">NOTES</span></span>

## <span data-ttu-id="af2bf-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af2bf-199">RELATED LINKS</span></span>

[<span data-ttu-id="af2bf-200">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="af2bf-200">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="af2bf-201">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="af2bf-201">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="af2bf-202">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="af2bf-202">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="af2bf-203">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="af2bf-203">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="af2bf-204">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="af2bf-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
