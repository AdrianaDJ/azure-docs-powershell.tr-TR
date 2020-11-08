---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278796"
---
# <span data-ttu-id="42a32-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="42a32-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="42a32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42a32-102">SYNOPSIS</span></span>
<span data-ttu-id="42a32-103">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="42a32-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="42a32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42a32-104">SYNTAX</span></span>

### <span data-ttu-id="42a32-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42a32-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a32-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="42a32-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a32-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42a32-107">DESCRIPTION</span></span>
<span data-ttu-id="42a32-108">**Set-Azsqlelaunpool** cmdlet 'ı, Azure SQL veritabanında esnek bir havuzun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="42a32-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="42a32-109">Bu cmdlet, havuz başına eDTU ( *DTU* ), havuz başına depolama sınırı ( *storagemb* ), veritabanı başına en fazla eDTU ( *databaseval* ) ve en az eDTU ( *databasedtumın* ).</span><span class="sxs-lookup"><span data-stu-id="42a32-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="42a32-110">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="42a32-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="42a32-111">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="42a32-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="42a32-112">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="42a32-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42a32-113">EXAMPLES</span></span>

### <span data-ttu-id="42a32-114">Örnek 1: esnek bir havuzun özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="42a32-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
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

<span data-ttu-id="42a32-115">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="42a32-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="42a32-116">Komut, elastik havuzun sayısını 1000 olarak ayarlar ve en az ve en fazla değer sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="42a32-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="42a32-117">Örnek 2: esnek bir havuzun en büyük depolama boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="42a32-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
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

<span data-ttu-id="42a32-118">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="42a32-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="42a32-119">Bu komut, elastik havuzun en büyük depolama alanını 2 TB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="42a32-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="42a32-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="42a32-120">Example 3</span></span>

<span data-ttu-id="42a32-121">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="42a32-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="42a32-122">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="42a32-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="42a32-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42a32-123">PARAMETERS</span></span>

### <span data-ttu-id="42a32-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="42a32-124">-AsJob</span></span>
<span data-ttu-id="42a32-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="42a32-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42a32-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="42a32-126">-ComputeGeneration</span></span>
<span data-ttu-id="42a32-127">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="42a32-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="42a32-128">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="42a32-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="42a32-129">Havuzdaki tek bir veritabanının tüketebileceği en fazla MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="42a32-130">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="42a32-131">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="42a32-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="42a32-132">Ana.</span><span class="sxs-lookup"><span data-stu-id="42a32-132">Basic.</span></span>  <span data-ttu-id="42a32-133">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-133">5 DTUs</span></span>
- <span data-ttu-id="42a32-134">Ardından.</span><span class="sxs-lookup"><span data-stu-id="42a32-134">Standard.</span></span> <span data-ttu-id="42a32-135">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-135">100 DTUs</span></span>
- <span data-ttu-id="42a32-136">Min.</span><span class="sxs-lookup"><span data-stu-id="42a32-136">Premium.</span></span> <span data-ttu-id="42a32-137">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-137">125 DTUs</span></span>

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

### <span data-ttu-id="42a32-138">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="42a32-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="42a32-139">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="42a32-140">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="42a32-141">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="42a32-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="42a32-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="42a32-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="42a32-143">Havuzda en yüksek sayıda SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42a32-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="42a32-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="42a32-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="42a32-145">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42a32-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="42a32-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a32-146">-DefaultProfile</span></span>
<span data-ttu-id="42a32-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42a32-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42a32-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="42a32-148">-Dtu</span></span>
<span data-ttu-id="42a32-149">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="42a32-150">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="42a32-151">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="42a32-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="42a32-152">Ana.</span><span class="sxs-lookup"><span data-stu-id="42a32-152">Basic.</span></span> <span data-ttu-id="42a32-153">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-153">100 DTUs</span></span>
- <span data-ttu-id="42a32-154">Ardından.</span><span class="sxs-lookup"><span data-stu-id="42a32-154">Standard.</span></span> <span data-ttu-id="42a32-155">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-155">100 DTUs</span></span>
- <span data-ttu-id="42a32-156">Min.</span><span class="sxs-lookup"><span data-stu-id="42a32-156">Premium.</span></span> <span data-ttu-id="42a32-157">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="42a32-157">125 DTUs</span></span>

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

### <span data-ttu-id="42a32-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="42a32-158">-Edition</span></span>
<span data-ttu-id="42a32-159">Elastik havuz için Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="42a32-160">Sürümü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="42a32-160">You cannot change the edition.</span></span> <span data-ttu-id="42a32-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="42a32-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42a32-162">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42a32-162">None</span></span>
- <span data-ttu-id="42a32-163">Ana</span><span class="sxs-lookup"><span data-stu-id="42a32-163">Basic</span></span>
- <span data-ttu-id="42a32-164">Ardından</span><span class="sxs-lookup"><span data-stu-id="42a32-164">Standard</span></span>
- <span data-ttu-id="42a32-165">Min</span><span class="sxs-lookup"><span data-stu-id="42a32-165">Premium</span></span>
- <span data-ttu-id="42a32-166">Ambarı</span><span class="sxs-lookup"><span data-stu-id="42a32-166">DataWarehouse</span></span>
- <span data-ttu-id="42a32-167">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="42a32-167">Free</span></span>
- <span data-ttu-id="42a32-168">:</span><span class="sxs-lookup"><span data-stu-id="42a32-168">Stretch</span></span>
- <span data-ttu-id="42a32-169">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="42a32-169">GeneralPurpose</span></span>
- <span data-ttu-id="42a32-170">Departmanla</span><span class="sxs-lookup"><span data-stu-id="42a32-170">BusinessCritical</span></span>

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

### <span data-ttu-id="42a32-171">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="42a32-171">-ElasticPoolName</span></span>
<span data-ttu-id="42a32-172">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="42a32-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="42a32-173">-LicenseType</span></span>
<span data-ttu-id="42a32-174">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="42a32-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="42a32-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a32-175">-ResourceGroupName</span></span>
<span data-ttu-id="42a32-176">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="42a32-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42a32-177">-ServerName</span></span>
<span data-ttu-id="42a32-178">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="42a32-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="42a32-179">-StorageMB</span></span>
<span data-ttu-id="42a32-180">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="42a32-181">Daha fazla bilgi için New-AzSqlElasticPool cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="42a32-182">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="42a32-182">-Tags</span></span>
<span data-ttu-id="42a32-183">Bu cmdlet 'in karma tablo biçimindeki esnek havuz ile ilişki kurduğu anahtar değer çiftlerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="42a32-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="42a32-184">Örneğin: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="42a32-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="42a32-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="42a32-185">-VCore</span></span>
<span data-ttu-id="42a32-186">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="42a32-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="42a32-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="42a32-187">-ZoneRedundant</span></span>
<span data-ttu-id="42a32-188">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="42a32-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="42a32-189">-Onay</span><span class="sxs-lookup"><span data-stu-id="42a32-189">-Confirm</span></span>
<span data-ttu-id="42a32-190">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42a32-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a32-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a32-191">-WhatIf</span></span>
<span data-ttu-id="42a32-192">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42a32-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a32-193">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42a32-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a32-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a32-194">CommonParameters</span></span>
<span data-ttu-id="42a32-195">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42a32-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a32-196">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42a32-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a32-197">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42a32-197">INPUTS</span></span>

### <span data-ttu-id="42a32-198">System. String</span><span class="sxs-lookup"><span data-stu-id="42a32-198">System.String</span></span>

## <span data-ttu-id="42a32-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42a32-199">OUTPUTS</span></span>

### <span data-ttu-id="42a32-200">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="42a32-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="42a32-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42a32-201">NOTES</span></span>

## <span data-ttu-id="42a32-202">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42a32-202">RELATED LINKS</span></span>

[<span data-ttu-id="42a32-203">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="42a32-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="42a32-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="42a32-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="42a32-205">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="42a32-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="42a32-206">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="42a32-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="42a32-207">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="42a32-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
