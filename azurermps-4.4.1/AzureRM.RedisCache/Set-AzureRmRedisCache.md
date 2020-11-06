---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589143"
---
# <span data-ttu-id="0b39a-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b39a-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="0b39a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b39a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b39a-103">Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b39a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b39a-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b39a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b39a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b39a-106">**Set-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="0b39a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b39a-107">EXAMPLES</span></span>

### <span data-ttu-id="0b39a-108">Örnek 1: Redis önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0b39a-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
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

<span data-ttu-id="0b39a-109">Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="0b39a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b39a-110">PARAMETERS</span></span>

### <span data-ttu-id="0b39a-111">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="0b39a-111">-EnableNonSslPort</span></span>
<span data-ttu-id="0b39a-112">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="0b39a-113">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="0b39a-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="0b39a-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="0b39a-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="0b39a-115">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0b39a-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="0b39a-116">MaxMemory-ilkesini ayarlamak için *Redisconfiguration* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0b39a-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="0b39a-117">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0b39a-117">For example:</span></span> 

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

### <span data-ttu-id="0b39a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b39a-118">-Name</span></span>
<span data-ttu-id="0b39a-119">Güncelleştirilecek Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="0b39a-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b39a-120">-RedisConfiguration</span></span>
<span data-ttu-id="0b39a-121">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="0b39a-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0b39a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b39a-123">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0b39a-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="0b39a-124">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="0b39a-125">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0b39a-125">Premium tier only.</span></span>
- <span data-ttu-id="0b39a-126">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="0b39a-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="0b39a-127">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="0b39a-128">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0b39a-128">Premium tier only.</span></span>
- <span data-ttu-id="0b39a-129">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="0b39a-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="0b39a-130">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="0b39a-131">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0b39a-131">Premium tier only.</span></span> 
- <span data-ttu-id="0b39a-132">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="0b39a-132">maxmemory-reserved.</span></span>
<span data-ttu-id="0b39a-133">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="0b39a-134">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-135">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="0b39a-135">maxmemory-policy.</span></span>
<span data-ttu-id="0b39a-136">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="0b39a-137">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="0b39a-137">All pricing tiers.</span></span> 
- <span data-ttu-id="0b39a-138">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-138">notify-keyspace-events.</span></span>
<span data-ttu-id="0b39a-139">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="0b39a-140">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="0b39a-141">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="0b39a-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="0b39a-142">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0b39a-143">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-144">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="0b39a-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="0b39a-145">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0b39a-146">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-147">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="0b39a-147">set-max-intset-entries.</span></span>
<span data-ttu-id="0b39a-148">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0b39a-149">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-150">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="0b39a-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="0b39a-151">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0b39a-152">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-153">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="0b39a-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="0b39a-154">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0b39a-155">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0b39a-156">Databases.</span><span class="sxs-lookup"><span data-stu-id="0b39a-156">databases.</span></span>
<span data-ttu-id="0b39a-157">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-157">Configures the number of databases.</span></span>
<span data-ttu-id="0b39a-158">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="0b39a-159">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0b39a-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="0b39a-160">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="0b39a-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="0b39a-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b39a-161">-ResourceGroupName</span></span>
<span data-ttu-id="0b39a-162">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="0b39a-163">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="0b39a-163">-ShardCount</span></span>
<span data-ttu-id="0b39a-164">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="0b39a-165">-Boyut</span><span class="sxs-lookup"><span data-stu-id="0b39a-165">-Size</span></span>
<span data-ttu-id="0b39a-166">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="0b39a-167">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0b39a-167">Valid values are:</span></span> 

- <span data-ttu-id="0b39a-168">P1</span><span class="sxs-lookup"><span data-stu-id="0b39a-168">P1</span></span>
- <span data-ttu-id="0b39a-169">P2</span><span class="sxs-lookup"><span data-stu-id="0b39a-169">P2</span></span>
- <span data-ttu-id="0b39a-170">P3</span><span class="sxs-lookup"><span data-stu-id="0b39a-170">P3</span></span>
- <span data-ttu-id="0b39a-171">P4</span><span class="sxs-lookup"><span data-stu-id="0b39a-171">P4</span></span>
- <span data-ttu-id="0b39a-172">C0</span><span class="sxs-lookup"><span data-stu-id="0b39a-172">C0</span></span>
- <span data-ttu-id="0b39a-173">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="0b39a-173">C1</span></span>
- <span data-ttu-id="0b39a-174">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="0b39a-174">C2</span></span>
- <span data-ttu-id="0b39a-175">C3</span><span class="sxs-lookup"><span data-stu-id="0b39a-175">C3</span></span>
- <span data-ttu-id="0b39a-176">C4</span><span class="sxs-lookup"><span data-stu-id="0b39a-176">C4</span></span>
- <span data-ttu-id="0b39a-177">C5</span><span class="sxs-lookup"><span data-stu-id="0b39a-177">C5</span></span>
- <span data-ttu-id="0b39a-178">C6</span><span class="sxs-lookup"><span data-stu-id="0b39a-178">C6</span></span>
- <span data-ttu-id="0b39a-179">250MB</span><span class="sxs-lookup"><span data-stu-id="0b39a-179">250MB</span></span>
- <span data-ttu-id="0b39a-180">1GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-180">1GB</span></span>
- <span data-ttu-id="0b39a-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-181">2.5GB</span></span>
- <span data-ttu-id="0b39a-182">6GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-182">6GB</span></span>
- <span data-ttu-id="0b39a-183">13GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-183">13GB</span></span>
- <span data-ttu-id="0b39a-184">26GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-184">26GB</span></span>
- <span data-ttu-id="0b39a-185">53GB</span><span class="sxs-lookup"><span data-stu-id="0b39a-185">53GB</span></span>

<span data-ttu-id="0b39a-186">Varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="0b39a-186">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="0b39a-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b39a-187">-Sku</span></span>
<span data-ttu-id="0b39a-188">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b39a-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="0b39a-189">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0b39a-189">Valid values are:</span></span> 

- <span data-ttu-id="0b39a-190">Ana</span><span class="sxs-lookup"><span data-stu-id="0b39a-190">Basic</span></span>
- <span data-ttu-id="0b39a-191">Ardından</span><span class="sxs-lookup"><span data-stu-id="0b39a-191">Standard</span></span>
- <span data-ttu-id="0b39a-192">Min</span><span class="sxs-lookup"><span data-stu-id="0b39a-192">Premium</span></span>

<span data-ttu-id="0b39a-193">Varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="0b39a-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="0b39a-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="0b39a-194">-TenantSettings</span></span>
<span data-ttu-id="0b39a-195">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0b39a-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="0b39a-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b39a-196">-DefaultProfile</span></span>
<span data-ttu-id="0b39a-197">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b39a-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b39a-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b39a-198">CommonParameters</span></span>
<span data-ttu-id="0b39a-199">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b39a-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b39a-200">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b39a-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b39a-201">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b39a-201">INPUTS</span></span>

### <span data-ttu-id="0b39a-202">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b39a-202">None</span></span>
<span data-ttu-id="0b39a-203">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b39a-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0b39a-204">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b39a-204">OUTPUTS</span></span>

### <span data-ttu-id="0b39a-205">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0b39a-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="0b39a-206">Birincil ve ikincil erişim tuşları dahil olmak üzere, kırmızı bir önbelleğin tüm özniteliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b39a-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="0b39a-207">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b39a-207">NOTES</span></span>

## <span data-ttu-id="0b39a-208">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b39a-208">RELATED LINKS</span></span>

[<span data-ttu-id="0b39a-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b39a-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0b39a-210">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b39a-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0b39a-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0b39a-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


