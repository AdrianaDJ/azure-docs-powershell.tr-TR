---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: a27d8c91f7262e83b139b6662a1f5f401f964b56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937314"
---
# <span data-ttu-id="a79b0-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a79b0-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="a79b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a79b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a79b0-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a79b0-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="a79b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a79b0-104">SYNTAX</span></span>

### <span data-ttu-id="a79b0-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a79b0-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79b0-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="a79b0-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a79b0-107">DESCRIPTION</span></span>
<span data-ttu-id="a79b0-108">**New-Azsqlelaunpool** cmdlet 'ı BIR Azure SQL veritabanı için elastik veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a79b0-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="a79b0-109">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="a79b0-110">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="a79b0-111">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="a79b0-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="a79b0-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a79b0-112">EXAMPLES</span></span>

### <span data-ttu-id="a79b0-113">Örnek 1: DTU elastik havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="a79b0-113">Example 1: Create a DTU elastic pool</span></span>

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

<span data-ttu-id="a79b0-114">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a79b0-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="a79b0-115">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="a79b0-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a79b0-116">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="a79b0-117">Örnek 2: vCore esnek havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a79b0-117">Example 2: Create a vCore elastic pool</span></span>

```
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="a79b0-118">Bu komut, ElasticPool01 adlı Gengeralamaç hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a79b0-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="a79b0-119">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="a79b0-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a79b0-120">Komut havuz için vCore özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="a79b0-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a79b0-121">PARAMETERS</span></span>

### <span data-ttu-id="a79b0-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="a79b0-122">-AsJob</span></span>
<span data-ttu-id="a79b0-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a79b0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a79b0-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a79b0-124">-ComputeGeneration</span></span>
<span data-ttu-id="a79b0-125">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="a79b0-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="a79b0-126">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="a79b0-126">-DatabaseDtuMax</span></span>
<span data-ttu-id="a79b0-127">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-127">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="a79b0-128">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="a79b0-128">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a79b0-129">Ana.</span><span class="sxs-lookup"><span data-stu-id="a79b0-129">Basic.</span></span> <span data-ttu-id="a79b0-130">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="a79b0-130">5 DTUs</span></span>
- <span data-ttu-id="a79b0-131">Ardından.</span><span class="sxs-lookup"><span data-stu-id="a79b0-131">Standard.</span></span> <span data-ttu-id="a79b0-132">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="a79b0-132">100 DTUs</span></span>
- <span data-ttu-id="a79b0-133">Min.</span><span class="sxs-lookup"><span data-stu-id="a79b0-133">Premium.</span></span> <span data-ttu-id="a79b0-134">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılar Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="a79b0-134">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="a79b0-135">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="a79b0-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="a79b0-136">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="a79b0-137">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="a79b0-137">The default value is zero (0).</span></span>
<span data-ttu-id="a79b0-138">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="a79b0-138">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a79b0-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="a79b0-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="a79b0-140">Havuzda en yüksek sayıda SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a79b0-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="a79b0-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="a79b0-142">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="a79b0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79b0-143">-DefaultProfile</span></span>
<span data-ttu-id="a79b0-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a79b0-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a79b0-145">-DTU</span><span class="sxs-lookup"><span data-stu-id="a79b0-145">-Dtu</span></span>
<span data-ttu-id="a79b0-146">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="a79b0-147">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="a79b0-147">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="a79b0-148">Ana.</span><span class="sxs-lookup"><span data-stu-id="a79b0-148">Basic.</span></span>
<span data-ttu-id="a79b0-149">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="a79b0-149">100 DTUs</span></span>
- <span data-ttu-id="a79b0-150">Ardından.</span><span class="sxs-lookup"><span data-stu-id="a79b0-150">Standard.</span></span>
<span data-ttu-id="a79b0-151">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="a79b0-151">100 DTUs</span></span>
- <span data-ttu-id="a79b0-152">Min.</span><span class="sxs-lookup"><span data-stu-id="a79b0-152">Premium.</span></span>
<span data-ttu-id="a79b0-153">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)belirli boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="a79b0-153">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="a79b0-154">-Edition</span><span class="sxs-lookup"><span data-stu-id="a79b0-154">-Edition</span></span>
<span data-ttu-id="a79b0-155">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-155">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="a79b0-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a79b0-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a79b0-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a79b0-157">None</span></span>
- <span data-ttu-id="a79b0-158">Ana</span><span class="sxs-lookup"><span data-stu-id="a79b0-158">Basic</span></span>
- <span data-ttu-id="a79b0-159">Ardından</span><span class="sxs-lookup"><span data-stu-id="a79b0-159">Standard</span></span>
- <span data-ttu-id="a79b0-160">Min</span><span class="sxs-lookup"><span data-stu-id="a79b0-160">Premium</span></span>
- <span data-ttu-id="a79b0-161">Ambarı</span><span class="sxs-lookup"><span data-stu-id="a79b0-161">DataWarehouse</span></span>
- <span data-ttu-id="a79b0-162">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="a79b0-162">Free</span></span>
- <span data-ttu-id="a79b0-163">:</span><span class="sxs-lookup"><span data-stu-id="a79b0-163">Stretch</span></span>
- <span data-ttu-id="a79b0-164">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="a79b0-164">GeneralPurpose</span></span>
- <span data-ttu-id="a79b0-165">Departmanla</span><span class="sxs-lookup"><span data-stu-id="a79b0-165">BusinessCritical</span></span>

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

### <span data-ttu-id="a79b0-166">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="a79b0-166">-ElasticPoolName</span></span>
<span data-ttu-id="a79b0-167">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-167">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a79b0-168">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a79b0-168">-LicenseType</span></span>
<span data-ttu-id="a79b0-169">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="a79b0-169">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a79b0-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79b0-170">-ResourceGroupName</span></span>
<span data-ttu-id="a79b0-171">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-171">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="a79b0-172">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a79b0-172">-ServerName</span></span>
<span data-ttu-id="a79b0-173">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-173">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="a79b0-174">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="a79b0-174">-StorageMB</span></span>
<span data-ttu-id="a79b0-175">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-175">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="a79b0-176">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="a79b0-176">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="a79b0-177">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="a79b0-177">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="a79b0-178">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="a79b0-178">-Tags</span></span>
<span data-ttu-id="a79b0-179">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-179">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="a79b0-180">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a79b0-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a79b0-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="a79b0-181">-VCore</span></span>
<span data-ttu-id="a79b0-182">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="a79b0-182">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="a79b0-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a79b0-183">-ZoneRedundant</span></span>
<span data-ttu-id="a79b0-184">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="a79b0-184">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="a79b0-185">-Onay</span><span class="sxs-lookup"><span data-stu-id="a79b0-185">-Confirm</span></span>
<span data-ttu-id="a79b0-186">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a79b0-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a79b0-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79b0-187">-WhatIf</span></span>
<span data-ttu-id="a79b0-188">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a79b0-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79b0-189">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a79b0-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a79b0-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79b0-190">CommonParameters</span></span>
<span data-ttu-id="a79b0-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a79b0-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79b0-192">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a79b0-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79b0-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a79b0-193">INPUTS</span></span>

### <span data-ttu-id="a79b0-194">System. String</span><span class="sxs-lookup"><span data-stu-id="a79b0-194">System.String</span></span>

## <span data-ttu-id="a79b0-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a79b0-195">OUTPUTS</span></span>

### <span data-ttu-id="a79b0-196">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="a79b0-196">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a79b0-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a79b0-197">NOTES</span></span>

## <span data-ttu-id="a79b0-198">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a79b0-198">RELATED LINKS</span></span>

[<span data-ttu-id="a79b0-199">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a79b0-199">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="a79b0-200">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a79b0-200">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="a79b0-201">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="a79b0-201">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="a79b0-202">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a79b0-202">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a79b0-203">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a79b0-203">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="a79b0-204">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a79b0-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
