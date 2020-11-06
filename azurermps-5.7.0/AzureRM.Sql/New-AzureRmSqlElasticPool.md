---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591571"
---
# <span data-ttu-id="c4a51-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c4a51-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="c4a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a51-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a51-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4a51-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4a51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4a51-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4a51-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a51-106">**Yeni-Azurermsqlelak,** BIR Azure SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4a51-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="c4a51-107">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="c4a51-108">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="c4a51-109">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c4a51-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="c4a51-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4a51-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a51-111">Örnek 1: esnek havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="c4a51-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="c4a51-112">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4a51-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="c4a51-113">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="c4a51-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="c4a51-114">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="c4a51-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4a51-115">PARAMETERS</span></span>

### <span data-ttu-id="c4a51-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="c4a51-116">-AsJob</span></span>
<span data-ttu-id="c4a51-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c4a51-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="c4a51-118">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="c4a51-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="c4a51-119">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="c4a51-120">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="c4a51-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c4a51-121">Ana.</span><span class="sxs-lookup"><span data-stu-id="c4a51-121">Basic.</span></span> <span data-ttu-id="c4a51-122">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-122">5 DTUs</span></span>
- <span data-ttu-id="c4a51-123">Ardından.</span><span class="sxs-lookup"><span data-stu-id="c4a51-123">Standard.</span></span> <span data-ttu-id="c4a51-124">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-124">100 DTUs</span></span>
- <span data-ttu-id="c4a51-125">Min.</span><span class="sxs-lookup"><span data-stu-id="c4a51-125">Premium.</span></span> <span data-ttu-id="c4a51-126">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-126">125 DTUs</span></span>

<span data-ttu-id="c4a51-127">Hangi değerlerin geçerli olduğu hakkında daha fazla bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="c4a51-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="c4a51-128">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="c4a51-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="c4a51-129">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="c4a51-130">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="c4a51-130">The default value is zero (0).</span></span>

<span data-ttu-id="c4a51-131">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c4a51-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="c4a51-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a51-132">-DefaultProfile</span></span>
<span data-ttu-id="c4a51-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4a51-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4a51-134">-DTU</span><span class="sxs-lookup"><span data-stu-id="c4a51-134">-Dtu</span></span>
<span data-ttu-id="c4a51-135">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="c4a51-136">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="c4a51-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="c4a51-137">Ana.</span><span class="sxs-lookup"><span data-stu-id="c4a51-137">Basic.</span></span>
<span data-ttu-id="c4a51-138">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-138">100 DTUs</span></span>
- <span data-ttu-id="c4a51-139">Ardından.</span><span class="sxs-lookup"><span data-stu-id="c4a51-139">Standard.</span></span>
<span data-ttu-id="c4a51-140">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-140">100 DTUs</span></span>
- <span data-ttu-id="c4a51-141">Min.</span><span class="sxs-lookup"><span data-stu-id="c4a51-141">Premium.</span></span>
<span data-ttu-id="c4a51-142">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="c4a51-142">125 DTUs</span></span>

<span data-ttu-id="c4a51-143">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c4a51-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="c4a51-144">-Edition</span><span class="sxs-lookup"><span data-stu-id="c4a51-144">-Edition</span></span>
<span data-ttu-id="c4a51-145">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="c4a51-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c4a51-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4a51-147">Min</span><span class="sxs-lookup"><span data-stu-id="c4a51-147">Premium</span></span>
- <span data-ttu-id="c4a51-148">Ana</span><span class="sxs-lookup"><span data-stu-id="c4a51-148">Basic</span></span>
- <span data-ttu-id="c4a51-149">Ardından</span><span class="sxs-lookup"><span data-stu-id="c4a51-149">Standard</span></span>
- <span data-ttu-id="c4a51-150">Ambarı</span><span class="sxs-lookup"><span data-stu-id="c4a51-150">DataWarehouse</span></span>
- <span data-ttu-id="c4a51-151">:</span><span class="sxs-lookup"><span data-stu-id="c4a51-151">Stretch</span></span>

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

### <span data-ttu-id="c4a51-152">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="c4a51-152">-ElasticPoolName</span></span>
<span data-ttu-id="c4a51-153">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a51-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a51-154">-ResourceGroupName</span></span>
<span data-ttu-id="c4a51-155">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="c4a51-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4a51-156">-ServerName</span></span>
<span data-ttu-id="c4a51-157">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-157">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="c4a51-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="c4a51-158">-StorageMB</span></span>
<span data-ttu-id="c4a51-159">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="c4a51-160">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="c4a51-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="c4a51-161">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="c4a51-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="c4a51-162">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="c4a51-162">-Tags</span></span>
<span data-ttu-id="c4a51-163">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="c4a51-164">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="c4a51-164">For example:</span></span>

<span data-ttu-id="c4a51-165">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c4a51-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c4a51-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c4a51-166">-ZoneRedundant</span></span>
<span data-ttu-id="c4a51-167">Azure SQL esnek havuzuyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="c4a51-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="c4a51-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4a51-168">-Confirm</span></span>
<span data-ttu-id="c4a51-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4a51-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a51-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a51-170">-WhatIf</span></span>
<span data-ttu-id="c4a51-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4a51-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a51-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4a51-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a51-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a51-173">CommonParameters</span></span>
<span data-ttu-id="c4a51-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4a51-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a51-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a51-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a51-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4a51-176">INPUTS</span></span>

### <span data-ttu-id="c4a51-177">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c4a51-177">None</span></span>
<span data-ttu-id="c4a51-178">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c4a51-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4a51-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4a51-179">OUTPUTS</span></span>

### <span data-ttu-id="c4a51-180">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="c4a51-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="c4a51-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4a51-181">NOTES</span></span>

## <span data-ttu-id="c4a51-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4a51-182">RELATED LINKS</span></span>

[<span data-ttu-id="c4a51-183">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c4a51-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c4a51-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c4a51-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="c4a51-185">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="c4a51-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="c4a51-186">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="c4a51-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c4a51-187">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c4a51-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c4a51-188">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c4a51-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
