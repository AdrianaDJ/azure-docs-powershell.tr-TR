---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591551"
---
# <span data-ttu-id="7ad34-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7ad34-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="7ad34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad34-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad34-103">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ad34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ad34-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ad34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ad34-105">DESCRIPTION</span></span>
<span data-ttu-id="7ad34-106">**Set-Azurermsqlelak,** Azure SQL veritabanındaki esnek bir havuzun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7ad34-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="7ad34-107">Bu cmdlet, havuz başına eDTU ( *DTU* ), havuz başına depolama sınırı ( *storagemb* ), veritabanı başına en fazla eDTU ( *databaseval\*\*) ve* en az eDTU</span><span class="sxs-lookup"><span data-stu-id="7ad34-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="7ad34-108">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="7ad34-109">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="7ad34-110">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7ad34-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="7ad34-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ad34-111">EXAMPLES</span></span>

### <span data-ttu-id="7ad34-112">Örnek 1: esnek bir havuzun özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="7ad34-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="7ad34-113">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="7ad34-114">Komut, elastik havuzun sayısını 1000 olarak ayarlar ve en az ve en fazla değer sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7ad34-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="7ad34-115">Örnek 2: esnek bir havuzun en büyük depolama boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="7ad34-115">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="7ad34-116">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="7ad34-117">Bu komut, elastik havuzun en büyük depolama alanını 2 TB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7ad34-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="7ad34-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ad34-118">PARAMETERS</span></span>

### <span data-ttu-id="7ad34-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ad34-119">-AsJob</span></span>
<span data-ttu-id="7ad34-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ad34-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="7ad34-121">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="7ad34-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="7ad34-122">Havuzdaki tek bir veritabanının tüketebileceği en fazla MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="7ad34-123">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7ad34-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="7ad34-124">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7ad34-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="7ad34-125">Ana.</span><span class="sxs-lookup"><span data-stu-id="7ad34-125">Basic.</span></span>  <span data-ttu-id="7ad34-126">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-126">5 DTUs</span></span>
- <span data-ttu-id="7ad34-127">Ardından.</span><span class="sxs-lookup"><span data-stu-id="7ad34-127">Standard.</span></span> <span data-ttu-id="7ad34-128">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-128">100 DTUs</span></span>
- <span data-ttu-id="7ad34-129">Min.</span><span class="sxs-lookup"><span data-stu-id="7ad34-129">Premium.</span></span> <span data-ttu-id="7ad34-130">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-130">125 DTUs</span></span>


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

### <span data-ttu-id="7ad34-131">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="7ad34-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="7ad34-132">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="7ad34-133">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7ad34-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="7ad34-134">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="7ad34-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="7ad34-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad34-135">-DefaultProfile</span></span>
<span data-ttu-id="7ad34-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7ad34-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-137">-DTU</span><span class="sxs-lookup"><span data-stu-id="7ad34-137">-Dtu</span></span>
<span data-ttu-id="7ad34-138">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="7ad34-139">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7ad34-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="7ad34-140">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7ad34-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="7ad34-141">Ana.</span><span class="sxs-lookup"><span data-stu-id="7ad34-141">Basic.</span></span> <span data-ttu-id="7ad34-142">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-142">100 DTUs</span></span>
- <span data-ttu-id="7ad34-143">Ardından.</span><span class="sxs-lookup"><span data-stu-id="7ad34-143">Standard.</span></span> <span data-ttu-id="7ad34-144">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-144">100 DTUs</span></span>
- <span data-ttu-id="7ad34-145">Min.</span><span class="sxs-lookup"><span data-stu-id="7ad34-145">Premium.</span></span> <span data-ttu-id="7ad34-146">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="7ad34-146">125 DTUs</span></span>

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

### <span data-ttu-id="7ad34-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="7ad34-147">-Edition</span></span>
<span data-ttu-id="7ad34-148">Elastik havuz için Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="7ad34-149">Sürümü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="7ad34-149">You cannot change the edition.</span></span> <span data-ttu-id="7ad34-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7ad34-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ad34-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7ad34-151">None</span></span>
- <span data-ttu-id="7ad34-152">Ana</span><span class="sxs-lookup"><span data-stu-id="7ad34-152">Basic</span></span>
- <span data-ttu-id="7ad34-153">Ardından</span><span class="sxs-lookup"><span data-stu-id="7ad34-153">Standard</span></span>
- <span data-ttu-id="7ad34-154">Min</span><span class="sxs-lookup"><span data-stu-id="7ad34-154">Premium</span></span>
- <span data-ttu-id="7ad34-155">Ambarı</span><span class="sxs-lookup"><span data-stu-id="7ad34-155">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-156">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="7ad34-156">-ElasticPoolName</span></span>
<span data-ttu-id="7ad34-157">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad34-158">-ResourceGroupName</span></span>
<span data-ttu-id="7ad34-159">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ad34-160">-ServerName</span></span>
<span data-ttu-id="7ad34-161">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-161">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="7ad34-162">-StorageMB</span></span>
<span data-ttu-id="7ad34-163">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="7ad34-164">Daha fazla bilgi için New-AzureRmSqlElasticPool cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="7ad34-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="7ad34-165">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="7ad34-165">-Tags</span></span>
<span data-ttu-id="7ad34-166">Bu cmdlet 'in karma tablo biçimindeki esnek havuz ile ilişki kurduğu anahtar değer çiftlerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="7ad34-167">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7ad34-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ad34-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7ad34-168">-ZoneRedundant</span></span>
<span data-ttu-id="7ad34-169">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="7ad34-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="7ad34-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ad34-170">-Confirm</span></span>
<span data-ttu-id="7ad34-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ad34-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ad34-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ad34-172">-WhatIf</span></span>
<span data-ttu-id="7ad34-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ad34-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ad34-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ad34-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ad34-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad34-175">CommonParameters</span></span>
<span data-ttu-id="7ad34-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ad34-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad34-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad34-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad34-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ad34-178">INPUTS</span></span>

### <span data-ttu-id="7ad34-179">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7ad34-179">None</span></span>
<span data-ttu-id="7ad34-180">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7ad34-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ad34-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ad34-181">OUTPUTS</span></span>

### <span data-ttu-id="7ad34-182">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="7ad34-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7ad34-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ad34-183">NOTES</span></span>

## <span data-ttu-id="7ad34-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ad34-184">RELATED LINKS</span></span>

[<span data-ttu-id="7ad34-185">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="7ad34-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7ad34-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7ad34-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="7ad34-187">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="7ad34-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="7ad34-188">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="7ad34-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7ad34-189">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7ad34-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
