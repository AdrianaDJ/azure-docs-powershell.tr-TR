---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 512c77862c44af68b26eb300eb9a692c115b0750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589026"
---
# <span data-ttu-id="768fc-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="768fc-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="768fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="768fc-102">SYNOPSIS</span></span>
<span data-ttu-id="768fc-103">Azure SQL veritabanında elastik bir veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="768fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="768fc-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="768fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="768fc-105">DESCRIPTION</span></span>
<span data-ttu-id="768fc-106">**Set-Azurermsqlelak,** BIR Azure SQL veritabanındaki elastik veritabanı havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-106">The **Set-AzureRmSqlElasticPool** cmdlet modifies properties for an elastic database pool in an Azure SQL Database.</span></span> <span data-ttu-id="768fc-107">Bu cmdlet, veritabanı başına en fazla saniyedeki en az veritabanı üretimi birimleri (Vseçval), havuzun en yüksek sayısının yanı sıra havuzun depolama sınırını da değiştirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-107">This cmdlet can modify the minimum Database Throughput Units (DTUs) per database in addition to the maximum DTUs per database, the number of DTUs for the pool, and the storage limit for the pool.</span></span>

<span data-ttu-id="768fc-108">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="768fc-109">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="768fc-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="768fc-110">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="768fc-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="768fc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="768fc-111">EXAMPLES</span></span>

### <span data-ttu-id="768fc-112">Örnek 1: esnek bir havuzun özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="768fc-112">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="768fc-113">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="768fc-114">Komut, elastik havuzun sayısını 1000 olarak ayarlar ve en az ve en fazla değer sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="768fc-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="768fc-115">Örnek 2: esnek bir havuzun maksimum depolamasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="768fc-115">Example 2: Modify the max storage of an elastic pool</span></span>
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

<span data-ttu-id="768fc-116">Bu komut, elasticpool01 adlı esnek bir havuzun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="768fc-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="768fc-117">Bu komut, elastik havuzun en büyük depolama alanını 2 TB olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="768fc-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="768fc-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="768fc-118">PARAMETERS</span></span>

### <span data-ttu-id="768fc-119">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="768fc-119">-DatabaseDtuMax</span></span>
<span data-ttu-id="768fc-120">Havuzdaki tek bir veritabanının tüketebileceği en fazla MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-120">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="768fc-121">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="768fc-121">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="768fc-122">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="768fc-122">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="768fc-123">Ana.</span><span class="sxs-lookup"><span data-stu-id="768fc-123">Basic.</span></span>  <span data-ttu-id="768fc-124">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-124">5 DTUs</span></span>
- <span data-ttu-id="768fc-125">Ardından.</span><span class="sxs-lookup"><span data-stu-id="768fc-125">Standard.</span></span> <span data-ttu-id="768fc-126">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-126">100 DTUs</span></span>
- <span data-ttu-id="768fc-127">Min.</span><span class="sxs-lookup"><span data-stu-id="768fc-127">Premium.</span></span> <span data-ttu-id="768fc-128">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-128">125 DTUs</span></span>


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

### <span data-ttu-id="768fc-129">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="768fc-129">-DatabaseDtuMin</span></span>
<span data-ttu-id="768fc-130">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-130">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="768fc-131">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="768fc-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="768fc-132">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="768fc-132">The default value is zero (0).</span></span>

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

### <span data-ttu-id="768fc-133">-DTU</span><span class="sxs-lookup"><span data-stu-id="768fc-133">-Dtu</span></span>
<span data-ttu-id="768fc-134">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-134">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="768fc-135">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="768fc-135">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="768fc-136">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="768fc-136">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="768fc-137">Ana.</span><span class="sxs-lookup"><span data-stu-id="768fc-137">Basic.</span></span> <span data-ttu-id="768fc-138">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-138">100 DTUs</span></span>
- <span data-ttu-id="768fc-139">Ardından.</span><span class="sxs-lookup"><span data-stu-id="768fc-139">Standard.</span></span> <span data-ttu-id="768fc-140">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-140">100 DTUs</span></span>
- <span data-ttu-id="768fc-141">Min.</span><span class="sxs-lookup"><span data-stu-id="768fc-141">Premium.</span></span> <span data-ttu-id="768fc-142">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="768fc-142">125 DTUs</span></span>

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

### <span data-ttu-id="768fc-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="768fc-143">-Edition</span></span>
<span data-ttu-id="768fc-144">Elastik havuz için Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-144">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="768fc-145">Sürümü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="768fc-145">You cannot change the edition.</span></span> <span data-ttu-id="768fc-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="768fc-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="768fc-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="768fc-147">None</span></span>
- <span data-ttu-id="768fc-148">Ana</span><span class="sxs-lookup"><span data-stu-id="768fc-148">Basic</span></span>
- <span data-ttu-id="768fc-149">Ardından</span><span class="sxs-lookup"><span data-stu-id="768fc-149">Standard</span></span>
- <span data-ttu-id="768fc-150">Min</span><span class="sxs-lookup"><span data-stu-id="768fc-150">Premium</span></span>
- <span data-ttu-id="768fc-151">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="768fc-151">PremiumRS</span></span>
- <span data-ttu-id="768fc-152">Ambarı</span><span class="sxs-lookup"><span data-stu-id="768fc-152">DataWarehouse</span></span>
- <span data-ttu-id="768fc-153">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="768fc-153">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="768fc-154">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="768fc-154">-ElasticPoolName</span></span>
<span data-ttu-id="768fc-155">Esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-155">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="768fc-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="768fc-156">-ResourceGroupName</span></span>
<span data-ttu-id="768fc-157">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-157">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="768fc-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="768fc-158">-ServerName</span></span>
<span data-ttu-id="768fc-159">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-159">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="768fc-160">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="768fc-160">-StorageMB</span></span>
<span data-ttu-id="768fc-161">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-161">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="768fc-162">Daha fazla bilgi için New-AzureRmSqlElasticPool cmdlet 'ine bakın.</span><span class="sxs-lookup"><span data-stu-id="768fc-162">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="768fc-163">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="768fc-163">-Tags</span></span>
<span data-ttu-id="768fc-164">Bu cmdlet 'in karma tablo biçimindeki esnek havuz ile ilişki kurduğu anahtar değer çiftlerinin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="768fc-164">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="768fc-165">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="768fc-165">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="768fc-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="768fc-166">-Confirm</span></span>
<span data-ttu-id="768fc-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="768fc-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="768fc-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="768fc-168">-WhatIf</span></span>
<span data-ttu-id="768fc-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="768fc-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="768fc-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="768fc-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="768fc-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768fc-171">-DefaultProfile</span></span>
<span data-ttu-id="768fc-172">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="768fc-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="768fc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768fc-173">CommonParameters</span></span>
<span data-ttu-id="768fc-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="768fc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768fc-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="768fc-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768fc-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="768fc-176">INPUTS</span></span>

## <span data-ttu-id="768fc-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="768fc-177">OUTPUTS</span></span>

### <span data-ttu-id="768fc-178">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="768fc-178">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="768fc-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="768fc-179">NOTES</span></span>

## <span data-ttu-id="768fc-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="768fc-180">RELATED LINKS</span></span>

[<span data-ttu-id="768fc-181">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="768fc-181">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="768fc-182">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="768fc-182">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="768fc-183">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="768fc-183">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="768fc-184">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="768fc-184">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="768fc-185">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="768fc-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
