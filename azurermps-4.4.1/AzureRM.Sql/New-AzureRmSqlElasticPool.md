---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765140"
---
# <span data-ttu-id="395b8-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="395b8-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="395b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="395b8-102">SYNOPSIS</span></span>
<span data-ttu-id="395b8-103">SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="395b8-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="395b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="395b8-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="395b8-105">DESCRIPTION</span></span>
<span data-ttu-id="395b8-106">**Yeni-Azurermsqlelak,** BIR Azure SQL veritabanı için elastik bir veritabanı havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="395b8-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="395b8-107">Birkaç parametre ( *-DTU,-Databasedtumın ve-DatabaseDtuMax* ), ayarlanmış değerin bu parametrenin geçerli değerleri listesinden olduğundan emin olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="395b8-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="395b8-108">Örneğin,-Databasevseçvet Standart 100 eDTU havuzu için yalnızca 10, 20, 50 veya 100 olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="395b8-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="395b8-109">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="395b8-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="395b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="395b8-110">EXAMPLES</span></span>

### <span data-ttu-id="395b8-111">Örnek 1: esnek havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="395b8-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="395b8-112">Bu komut, ElasticPool01 adındaki standart hizmet katmanında esnek bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="395b8-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="395b8-113">ResourceGroup01 adındaki bir Azure Kaynak grubuna atanan server01 adlı sunucu, ' da esnek havuzu barındırır.</span><span class="sxs-lookup"><span data-stu-id="395b8-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="395b8-114">Komut havuz için DTU özellik değerlerini ve havuzdaki veritabanları belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="395b8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="395b8-115">PARAMETERS</span></span>

### <span data-ttu-id="395b8-116">-Databasevseçtumax</span><span class="sxs-lookup"><span data-stu-id="395b8-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="395b8-117">Havuzdaki tek bir veritabanının tüketebileceği en fazla veritabanı üretimi birimi (Vseçma) sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="395b8-118">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="395b8-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="395b8-119">Ana.</span><span class="sxs-lookup"><span data-stu-id="395b8-119">Basic.</span></span> <span data-ttu-id="395b8-120">5 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-120">5 DTUs</span></span>
- <span data-ttu-id="395b8-121">Ardından.</span><span class="sxs-lookup"><span data-stu-id="395b8-121">Standard.</span></span> <span data-ttu-id="395b8-122">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-122">100 DTUs</span></span>
- <span data-ttu-id="395b8-123">Min.</span><span class="sxs-lookup"><span data-stu-id="395b8-123">Premium.</span></span> <span data-ttu-id="395b8-124">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-124">125 DTUs</span></span>

<span data-ttu-id="395b8-125">Hangi değerlerin geçerli olduğu hakkında daha fazla bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) belirli boyut havuzunuzun tablosuna bakın</span><span class="sxs-lookup"><span data-stu-id="395b8-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


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

### <span data-ttu-id="395b8-126">-Databasedtumın</span><span class="sxs-lookup"><span data-stu-id="395b8-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="395b8-127">, Elastik havuzun havuzdaki tüm veritabanlarına garanti edilen en az MTU sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="395b8-128">Varsayılan değer sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="395b8-128">The default value is zero (0).</span></span>

<span data-ttu-id="395b8-129">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="395b8-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="395b8-130">-DTU</span><span class="sxs-lookup"><span data-stu-id="395b8-130">-Dtu</span></span>
<span data-ttu-id="395b8-131">Esnek havuzda toplam paylaşılan Çifdin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="395b8-132">Farklı sürümlerin varsayılan değerleri aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="395b8-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="395b8-133">Ana.</span><span class="sxs-lookup"><span data-stu-id="395b8-133">Basic.</span></span>
<span data-ttu-id="395b8-134">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-134">100 DTUs</span></span>
- <span data-ttu-id="395b8-135">Ardından.</span><span class="sxs-lookup"><span data-stu-id="395b8-135">Standard.</span></span>
<span data-ttu-id="395b8-136">100 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-136">100 DTUs</span></span>
- <span data-ttu-id="395b8-137">Min.</span><span class="sxs-lookup"><span data-stu-id="395b8-137">Premium.</span></span>
<span data-ttu-id="395b8-138">125 Vseçma</span><span class="sxs-lookup"><span data-stu-id="395b8-138">125 DTUs</span></span>

<span data-ttu-id="395b8-139">Hangi değerlerin geçerli olduğu hakkında ayrıntılı bilgi için, [Esnek havuzlardaki](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)özel boyut havuzunuzun tablosuna bakın.</span><span class="sxs-lookup"><span data-stu-id="395b8-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

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

### <span data-ttu-id="395b8-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="395b8-140">-Edition</span></span>
<span data-ttu-id="395b8-141">Esnek havuz için kullanılan Azure SQL veritabanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="395b8-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="395b8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="395b8-143">Min</span><span class="sxs-lookup"><span data-stu-id="395b8-143">Premium</span></span>
- <span data-ttu-id="395b8-144">Ana</span><span class="sxs-lookup"><span data-stu-id="395b8-144">Basic</span></span>
- <span data-ttu-id="395b8-145">Ardından</span><span class="sxs-lookup"><span data-stu-id="395b8-145">Standard</span></span>
- <span data-ttu-id="395b8-146">Ambarı</span><span class="sxs-lookup"><span data-stu-id="395b8-146">DataWarehouse</span></span>
- <span data-ttu-id="395b8-147">:</span><span class="sxs-lookup"><span data-stu-id="395b8-147">Stretch</span></span>
- <span data-ttu-id="395b8-148">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="395b8-148">Free</span></span>
- <span data-ttu-id="395b8-149">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="395b8-149">PremiumRS</span></span>

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

### <span data-ttu-id="395b8-150">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="395b8-150">-ElasticPoolName</span></span>
<span data-ttu-id="395b8-151">Bu cmdlet 'in oluşturduğu esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395b8-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395b8-152">-ResourceGroupName</span></span>
<span data-ttu-id="395b8-153">Bu cmdlet 'in esnek havuzuna atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="395b8-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="395b8-154">-ServerName</span></span>
<span data-ttu-id="395b8-155">Esnek havuzu barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-155">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="395b8-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="395b8-156">-StorageMB</span></span>
<span data-ttu-id="395b8-157">Esnek havuz için, megabayt cinsinden depolama sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="395b8-158">Bu parametreyi belirtmezseniz, bu cmdlet *DTU* parametresinin değerine bağlı olarak bir değer hesaplar.</span><span class="sxs-lookup"><span data-stu-id="395b8-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="395b8-159">Olası değerler için [eDTU ve depolama limitlerini](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) görün.</span><span class="sxs-lookup"><span data-stu-id="395b8-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="395b8-160">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="395b8-160">-Tags</span></span>
<span data-ttu-id="395b8-161">Bu cmdlet 'in esnek havuzuyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="395b8-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="395b8-162">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="395b8-162">For example:</span></span>

<span data-ttu-id="395b8-163">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="395b8-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="395b8-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="395b8-164">-Confirm</span></span>
<span data-ttu-id="395b8-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="395b8-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395b8-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395b8-166">-WhatIf</span></span>
<span data-ttu-id="395b8-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="395b8-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395b8-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="395b8-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395b8-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395b8-169">-DefaultProfile</span></span>
<span data-ttu-id="395b8-170">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="395b8-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="395b8-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395b8-171">CommonParameters</span></span>
<span data-ttu-id="395b8-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="395b8-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395b8-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395b8-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395b8-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="395b8-174">INPUTS</span></span>

## <span data-ttu-id="395b8-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="395b8-175">OUTPUTS</span></span>

### <span data-ttu-id="395b8-176">Microsoft. Azure. Commands. Sql. Elaunpool. model. Azuresqlelakpoolmodel</span><span class="sxs-lookup"><span data-stu-id="395b8-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="395b8-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="395b8-177">NOTES</span></span>

## <span data-ttu-id="395b8-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="395b8-178">RELATED LINKS</span></span>

[<span data-ttu-id="395b8-179">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="395b8-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="395b8-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="395b8-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="395b8-181">Get-Azurermsqlelakpooldatabase</span><span class="sxs-lookup"><span data-stu-id="395b8-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="395b8-182">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="395b8-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="395b8-183">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="395b8-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="395b8-184">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="395b8-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
