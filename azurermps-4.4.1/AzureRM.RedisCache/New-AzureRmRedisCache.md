---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762420"
---
# <span data-ttu-id="c6fc6-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6fc6-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="c6fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fc6-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6fc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6fc6-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6fc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="c6fc6-106">**Yeni-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="c6fc6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="c6fc6-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6fc6-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="c6fc6-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="c6fc6-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6fc6-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

<span data-ttu-id="c6fc6-111">Bu komut, zaten varsa Redis önbelleğini oluşturur</span><span class="sxs-lookup"><span data-stu-id="c6fc6-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="c6fc6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6fc6-112">PARAMETERS</span></span>

### <span data-ttu-id="c6fc6-113">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="c6fc6-113">-EnableNonSslPort</span></span>
<span data-ttu-id="c6fc6-114">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="c6fc6-115">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="c6fc6-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="c6fc6-116">-Location</span></span>
<span data-ttu-id="c6fc6-117">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="c6fc6-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-118">Valid values are:</span></span> 

- <span data-ttu-id="c6fc6-119">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="c6fc6-119">North Central US</span></span>
- <span data-ttu-id="c6fc6-120">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="c6fc6-120">South Central US</span></span>
- <span data-ttu-id="c6fc6-121">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="c6fc6-121">Central US</span></span>
- <span data-ttu-id="c6fc6-122">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="c6fc6-122">West Europe</span></span>
- <span data-ttu-id="c6fc6-123">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="c6fc6-123">North Europe</span></span>
- <span data-ttu-id="c6fc6-124">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="c6fc6-124">West US</span></span>
- <span data-ttu-id="c6fc6-125">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="c6fc6-125">East US</span></span>
- <span data-ttu-id="c6fc6-126">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="c6fc6-126">East US 2</span></span>
- <span data-ttu-id="c6fc6-127">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="c6fc6-127">Japan East</span></span>
- <span data-ttu-id="c6fc6-128">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="c6fc6-128">Japan West</span></span>
- <span data-ttu-id="c6fc6-129">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="c6fc6-129">Brazil South</span></span>
- <span data-ttu-id="c6fc6-130">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="c6fc6-130">Southeast Asia</span></span>
- <span data-ttu-id="c6fc6-131">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="c6fc6-131">East Asia</span></span>
- <span data-ttu-id="c6fc6-132">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="c6fc6-132">Australia East</span></span>
- <span data-ttu-id="c6fc6-133">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="c6fc6-133">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="c6fc6-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="c6fc6-135">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="c6fc6-136">MaxMemory-ilkesini ayarlamak için *Redisconfiguration* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="c6fc6-137">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-137">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6fc6-138">-Name</span></span>
<span data-ttu-id="c6fc6-139">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-139">Specifies the name of the Redis Cache to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6fc6-140">-RedisConfiguration</span></span>
<span data-ttu-id="c6fc6-141">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="c6fc6-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6fc6-143">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="c6fc6-144">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="c6fc6-145">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-145">Premium tier only.</span></span>
- <span data-ttu-id="c6fc6-146">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="c6fc6-147">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="c6fc6-148">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-148">Premium tier only.</span></span>
- <span data-ttu-id="c6fc6-149">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="c6fc6-150">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="c6fc6-151">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-151">Premium tier only.</span></span> 
- <span data-ttu-id="c6fc6-152">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-152">maxmemory-reserved.</span></span>
<span data-ttu-id="c6fc6-153">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="c6fc6-154">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-155">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-155">maxmemory-policy.</span></span>
<span data-ttu-id="c6fc6-156">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="c6fc6-157">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-157">All pricing tiers.</span></span> 
- <span data-ttu-id="c6fc6-158">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-158">notify-keyspace-events.</span></span>
<span data-ttu-id="c6fc6-159">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="c6fc6-160">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-161">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="c6fc6-162">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c6fc6-163">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-164">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="c6fc6-165">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c6fc6-166">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-167">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-167">set-max-intset-entries.</span></span>
<span data-ttu-id="c6fc6-168">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c6fc6-169">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-170">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="c6fc6-171">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c6fc6-172">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-173">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="c6fc6-174">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="c6fc6-175">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="c6fc6-176">Databases.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-176">databases.</span></span>
<span data-ttu-id="c6fc6-177">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-177">Configures the number of databases.</span></span>
<span data-ttu-id="c6fc6-178">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="c6fc6-179">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="c6fc6-180">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="c6fc6-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="c6fc6-181">-RedisVersion</span></span>
<span data-ttu-id="c6fc6-182">Bu parametre kullanım dışıdır ve ileriki sürümlerden kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-182">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6fc6-183">-ResourceGroupName</span></span>
<span data-ttu-id="c6fc6-184">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-185">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="c6fc6-185">-ShardCount</span></span>
<span data-ttu-id="c6fc6-186">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="c6fc6-187">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c6fc6-188">2</span><span class="sxs-lookup"><span data-stu-id="c6fc6-188">1</span></span>
- <span data-ttu-id="c6fc6-189">2</span><span class="sxs-lookup"><span data-stu-id="c6fc6-189">2</span></span>
- <span data-ttu-id="c6fc6-190">@</span><span class="sxs-lookup"><span data-stu-id="c6fc6-190">3</span></span>
- <span data-ttu-id="c6fc6-191">1.921.024</span><span class="sxs-lookup"><span data-stu-id="c6fc6-191">4</span></span>
- <span data-ttu-id="c6fc6-192">tir</span><span class="sxs-lookup"><span data-stu-id="c6fc6-192">5</span></span>
- <span data-ttu-id="c6fc6-193">+</span><span class="sxs-lookup"><span data-stu-id="c6fc6-193">6</span></span>
- <span data-ttu-id="c6fc6-194">+</span><span class="sxs-lookup"><span data-stu-id="c6fc6-194">7</span></span>
- <span data-ttu-id="c6fc6-195">8@@</span><span class="sxs-lookup"><span data-stu-id="c6fc6-195">8</span></span>
- <span data-ttu-id="c6fc6-196">döndürdü</span><span class="sxs-lookup"><span data-stu-id="c6fc6-196">9</span></span> 
- <span data-ttu-id="c6fc6-197">on</span><span class="sxs-lookup"><span data-stu-id="c6fc6-197">10</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-198">-Boyut</span><span class="sxs-lookup"><span data-stu-id="c6fc6-198">-Size</span></span>
<span data-ttu-id="c6fc6-199">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="c6fc6-200">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-200">Valid values are:</span></span> 

- <span data-ttu-id="c6fc6-201">P1</span><span class="sxs-lookup"><span data-stu-id="c6fc6-201">P1</span></span>
- <span data-ttu-id="c6fc6-202">P2</span><span class="sxs-lookup"><span data-stu-id="c6fc6-202">P2</span></span>
- <span data-ttu-id="c6fc6-203">P3</span><span class="sxs-lookup"><span data-stu-id="c6fc6-203">P3</span></span>
- <span data-ttu-id="c6fc6-204">P4</span><span class="sxs-lookup"><span data-stu-id="c6fc6-204">P4</span></span>
- <span data-ttu-id="c6fc6-205">C0</span><span class="sxs-lookup"><span data-stu-id="c6fc6-205">C0</span></span>
- <span data-ttu-id="c6fc6-206">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="c6fc6-206">C1</span></span>
- <span data-ttu-id="c6fc6-207">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="c6fc6-207">C2</span></span>
- <span data-ttu-id="c6fc6-208">C3</span><span class="sxs-lookup"><span data-stu-id="c6fc6-208">C3</span></span>
- <span data-ttu-id="c6fc6-209">C4</span><span class="sxs-lookup"><span data-stu-id="c6fc6-209">C4</span></span>
- <span data-ttu-id="c6fc6-210">C5</span><span class="sxs-lookup"><span data-stu-id="c6fc6-210">C5</span></span>
- <span data-ttu-id="c6fc6-211">C6</span><span class="sxs-lookup"><span data-stu-id="c6fc6-211">C6</span></span>
- <span data-ttu-id="c6fc6-212">250MB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-212">250MB</span></span>
- <span data-ttu-id="c6fc6-213">1GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-213">1GB</span></span>
- <span data-ttu-id="c6fc6-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-214">2.5GB</span></span>
- <span data-ttu-id="c6fc6-215">6GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-215">6GB</span></span>
- <span data-ttu-id="c6fc6-216">13GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-216">13GB</span></span>
- <span data-ttu-id="c6fc6-217">26GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-217">26GB</span></span>
- <span data-ttu-id="c6fc6-218">53GB</span><span class="sxs-lookup"><span data-stu-id="c6fc6-218">53GB</span></span>

<span data-ttu-id="c6fc6-219">Varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-219">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6fc6-220">-Sku</span></span>
<span data-ttu-id="c6fc6-221">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="c6fc6-222">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c6fc6-222">Valid values are:</span></span> 

- <span data-ttu-id="c6fc6-223">Ana</span><span class="sxs-lookup"><span data-stu-id="c6fc6-223">Basic</span></span>
- <span data-ttu-id="c6fc6-224">Ardından</span><span class="sxs-lookup"><span data-stu-id="c6fc6-224">Standard</span></span>
- <span data-ttu-id="c6fc6-225">Min</span><span class="sxs-lookup"><span data-stu-id="c6fc6-225">Premium</span></span>

<span data-ttu-id="c6fc6-226">Varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-226">The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="c6fc6-227">-StaticIP</span></span>
<span data-ttu-id="c6fc6-228">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="c6fc6-229">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-230">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c6fc6-230">-Subnet</span></span>
<span data-ttu-id="c6fc6-231">Redis önbelleğinin dağıtılacağı alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c6fc6-232">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="c6fc6-233">-TenantSettings</span></span>
<span data-ttu-id="c6fc6-234">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-234">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c6fc6-235">-VirtualNetwork</span></span>
<span data-ttu-id="c6fc6-236">Redis önbelleğinin dağıtılacağı sanal ağın kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fc6-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fc6-237">-DefaultProfile</span></span>
<span data-ttu-id="c6fc6-238">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6fc6-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fc6-239">CommonParameters</span></span>
<span data-ttu-id="c6fc6-240">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fc6-241">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6fc6-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fc6-242">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6fc6-242">INPUTS</span></span>

### <span data-ttu-id="c6fc6-243">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c6fc6-243">None</span></span>
<span data-ttu-id="c6fc6-244">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="c6fc6-245">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6fc6-245">OUTPUTS</span></span>

### <span data-ttu-id="c6fc6-246">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c6fc6-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="c6fc6-247">Bu cmdlet, birincil ve ikincil erişim tuşları gibi bir kırmızı tür önbelleğinin tüm özniteliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6fc6-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="c6fc6-248">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6fc6-248">NOTES</span></span>

## <span data-ttu-id="c6fc6-249">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6fc6-249">RELATED LINKS</span></span>

[<span data-ttu-id="c6fc6-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6fc6-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="c6fc6-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6fc6-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c6fc6-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6fc6-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


