---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fed3f32f5ff0a9920b87438b75cb25cee7c9217
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276673"
---
# <span data-ttu-id="99119-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="99119-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="99119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99119-102">SYNOPSIS</span></span>
<span data-ttu-id="99119-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99119-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="99119-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99119-104">SYNTAX</span></span>

### <span data-ttu-id="99119-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99119-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99119-106">Vcorebasevseçpool</span><span class="sxs-lookup"><span data-stu-id="99119-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99119-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99119-107">DESCRIPTION</span></span>
<span data-ttu-id="99119-108">**New-Azsqlelaunpool** cmdlet 'ı BIR Azure SQL veritabanı için elastik veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99119-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="99119-109">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="99119-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="99119-110">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="99119-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="99119-111">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="99119-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="99119-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99119-112">EXAMPLES</span></span>

### <span data-ttu-id="99119-113">Örnek 1: DTU elastik havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="99119-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
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

<span data-ttu-id="99119-114">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99119-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="99119-115">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="99119-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="99119-116">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="99119-117">Örnek 2: vCore esnek havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="99119-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
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

<span data-ttu-id="99119-118">Bu komut, ElasticPool01 adlı Gengeralamaç hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99119-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="99119-119">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="99119-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="99119-120">Komut havuz için vCore özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="99119-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="99119-121">Example 3</span></span>

<span data-ttu-id="99119-122">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99119-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="99119-123">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="99119-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="99119-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99119-124">PARAMETERS</span></span>

### <span data-ttu-id="99119-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="99119-125">-AsJob</span></span>
<span data-ttu-id="99119-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="99119-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99119-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="99119-127">-ComputeGeneration</span></span>
<span data-ttu-id="99119-128">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="99119-128">The compute generation to assign.</span></span>

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

### <span data-ttu-id="99119-129">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="99119-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="99119-130">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="99119-131">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="99119-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="99119-132">Ana.</span><span class="sxs-lookup"><span data-stu-id="99119-132">Basic.</span></span> <span data-ttu-id="99119-133">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="99119-133">5 DTUs</span></span>
- <span data-ttu-id="99119-134">Ardından.</span><span class="sxs-lookup"><span data-stu-id="99119-134">Standard.</span></span> <span data-ttu-id="99119-135">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="99119-135">100 DTUs</span></span>
- <span data-ttu-id="99119-136">Min.</span><span class="sxs-lookup"><span data-stu-id="99119-136">Premium.</span></span> <span data-ttu-id="99119-137">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılar Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="99119-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="99119-138">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="99119-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="99119-139">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="99119-140">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="99119-140">The default value is zero (0).</span></span>
<span data-ttu-id="99119-141">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="99119-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="99119-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="99119-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="99119-143">Havuzda en yüksek sayıda SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="99119-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="99119-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="99119-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="99119-145">Havuzda en az bir SqlAzure veritabanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="99119-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="99119-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99119-146">-DefaultProfile</span></span>
<span data-ttu-id="99119-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99119-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99119-148">-DTU</span><span class="sxs-lookup"><span data-stu-id="99119-148">-Dtu</span></span>
<span data-ttu-id="99119-149">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="99119-150">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="99119-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="99119-151">Ana.</span><span class="sxs-lookup"><span data-stu-id="99119-151">Basic.</span></span>
<span data-ttu-id="99119-152">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="99119-152">100 DTUs</span></span>
- <span data-ttu-id="99119-153">Ardından.</span><span class="sxs-lookup"><span data-stu-id="99119-153">Standard.</span></span>
<span data-ttu-id="99119-154">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="99119-154">100 DTUs</span></span>
- <span data-ttu-id="99119-155">Min.</span><span class="sxs-lookup"><span data-stu-id="99119-155">Premium.</span></span>
<span data-ttu-id="99119-156">125 değerleri hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi Için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)belirli boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="99119-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="99119-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="99119-157">-Edition</span></span>
<span data-ttu-id="99119-158">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="99119-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="99119-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99119-160">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99119-160">None</span></span>
- <span data-ttu-id="99119-161">Ana</span><span class="sxs-lookup"><span data-stu-id="99119-161">Basic</span></span>
- <span data-ttu-id="99119-162">Ardından</span><span class="sxs-lookup"><span data-stu-id="99119-162">Standard</span></span>
- <span data-ttu-id="99119-163">Min</span><span class="sxs-lookup"><span data-stu-id="99119-163">Premium</span></span>
- <span data-ttu-id="99119-164">Ambarı</span><span class="sxs-lookup"><span data-stu-id="99119-164">DataWarehouse</span></span>
- <span data-ttu-id="99119-165">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="99119-165">Free</span></span>
- <span data-ttu-id="99119-166">:</span><span class="sxs-lookup"><span data-stu-id="99119-166">Stretch</span></span>
- <span data-ttu-id="99119-167">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="99119-167">GeneralPurpose</span></span>
- <span data-ttu-id="99119-168">Departmanla</span><span class="sxs-lookup"><span data-stu-id="99119-168">BusinessCritical</span></span>

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

### <span data-ttu-id="99119-169">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="99119-169">-ElasticPoolName</span></span>
<span data-ttu-id="99119-170">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="99119-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="99119-171">-LicenseType</span></span>
<span data-ttu-id="99119-172">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="99119-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="99119-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99119-173">-ResourceGroupName</span></span>
<span data-ttu-id="99119-174">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-174">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="99119-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99119-175">-ServerName</span></span>
<span data-ttu-id="99119-176">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-176">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="99119-177">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="99119-177">-StorageMB</span></span>
<span data-ttu-id="99119-178">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-178">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="99119-179">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="99119-179">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="99119-180">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="99119-180">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="99119-181">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="99119-181">-Tags</span></span>
<span data-ttu-id="99119-182">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="99119-182">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="99119-183">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="99119-183">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99119-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="99119-184">-VCore</span></span>
<span data-ttu-id="99119-185">SQL Azure esnek havuzunun toplam paylaşılan sayısı.</span><span class="sxs-lookup"><span data-stu-id="99119-185">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="99119-186">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="99119-186">-ZoneRedundant</span></span>
<span data-ttu-id="99119-187">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="99119-187">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="99119-188">-Onay</span><span class="sxs-lookup"><span data-stu-id="99119-188">-Confirm</span></span>
<span data-ttu-id="99119-189">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99119-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99119-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99119-190">-WhatIf</span></span>
<span data-ttu-id="99119-191">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99119-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99119-192">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99119-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99119-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99119-193">CommonParameters</span></span>
<span data-ttu-id="99119-194">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99119-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99119-195">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99119-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99119-196">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99119-196">INPUTS</span></span>

### <span data-ttu-id="99119-197">System. String</span><span class="sxs-lookup"><span data-stu-id="99119-197">System.String</span></span>

## <span data-ttu-id="99119-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99119-198">OUTPUTS</span></span>

### <span data-ttu-id="99119-199">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="99119-199">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="99119-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99119-200">NOTES</span></span>

## <span data-ttu-id="99119-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99119-201">RELATED LINKS</span></span>

[<span data-ttu-id="99119-202">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99119-202">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="99119-203">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="99119-203">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="99119-204">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="99119-204">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="99119-205">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99119-205">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="99119-206">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="99119-206">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="99119-207">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="99119-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
