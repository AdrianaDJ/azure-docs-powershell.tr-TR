---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938184"
---
# <span data-ttu-id="da6ec-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="da6ec-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="da6ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="da6ec-103">Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="da6ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da6ec-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da6ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="da6ec-106">**Set-AzRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="da6ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da6ec-107">EXAMPLES</span></span>

### <span data-ttu-id="da6ec-108">Örnek 1: Redis önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="da6ec-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="da6ec-109">Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="da6ec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da6ec-110">PARAMETERS</span></span>

### <span data-ttu-id="da6ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6ec-111">-DefaultProfile</span></span>
<span data-ttu-id="da6ec-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da6ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da6ec-113">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="da6ec-113">-EnableNonSslPort</span></span>
<span data-ttu-id="da6ec-114">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="da6ec-115">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="da6ec-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="da6ec-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="da6ec-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="da6ec-117">İstemcilere bağlanacak istemcilerin gerektirdiği TLS sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="da6ec-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="da6ec-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="da6ec-118">-Name</span></span>
<span data-ttu-id="da6ec-119">Güncelleştirilecek Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="da6ec-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="da6ec-120">-RedisConfiguration</span></span>
<span data-ttu-id="da6ec-121">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="da6ec-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="da6ec-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da6ec-123">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="da6ec-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="da6ec-124">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="da6ec-125">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="da6ec-125">Premium tier only.</span></span>
- <span data-ttu-id="da6ec-126">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="da6ec-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="da6ec-127">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="da6ec-128">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="da6ec-128">Premium tier only.</span></span>
- <span data-ttu-id="da6ec-129">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="da6ec-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="da6ec-130">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="da6ec-131">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="da6ec-131">Premium tier only.</span></span> 
- <span data-ttu-id="da6ec-132">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="da6ec-132">maxmemory-reserved.</span></span>
<span data-ttu-id="da6ec-133">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="da6ec-134">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-135">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="da6ec-135">maxmemory-policy.</span></span>
<span data-ttu-id="da6ec-136">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="da6ec-137">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="da6ec-137">All pricing tiers.</span></span> 
- <span data-ttu-id="da6ec-138">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-138">notify-keyspace-events.</span></span>
<span data-ttu-id="da6ec-139">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="da6ec-140">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="da6ec-141">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="da6ec-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="da6ec-142">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="da6ec-143">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-144">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="da6ec-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="da6ec-145">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="da6ec-146">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-147">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="da6ec-147">set-max-intset-entries.</span></span>
<span data-ttu-id="da6ec-148">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="da6ec-149">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-150">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="da6ec-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="da6ec-151">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="da6ec-152">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-153">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="da6ec-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="da6ec-154">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="da6ec-155">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="da6ec-156">Databases.</span><span class="sxs-lookup"><span data-stu-id="da6ec-156">databases.</span></span>
<span data-ttu-id="da6ec-157">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-157">Configures the number of databases.</span></span>
<span data-ttu-id="da6ec-158">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="da6ec-159">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="da6ec-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="da6ec-160">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="da6ec-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="da6ec-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da6ec-161">-ResourceGroupName</span></span>
<span data-ttu-id="da6ec-162">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="da6ec-163">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="da6ec-163">-ShardCount</span></span>
<span data-ttu-id="da6ec-164">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="da6ec-165">-Boyut</span><span class="sxs-lookup"><span data-stu-id="da6ec-165">-Size</span></span>
<span data-ttu-id="da6ec-166">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="da6ec-167">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="da6ec-167">Valid values are:</span></span> 
- <span data-ttu-id="da6ec-168">P1</span><span class="sxs-lookup"><span data-stu-id="da6ec-168">P1</span></span>
- <span data-ttu-id="da6ec-169">P2</span><span class="sxs-lookup"><span data-stu-id="da6ec-169">P2</span></span>
- <span data-ttu-id="da6ec-170">P3</span><span class="sxs-lookup"><span data-stu-id="da6ec-170">P3</span></span>
- <span data-ttu-id="da6ec-171">P4</span><span class="sxs-lookup"><span data-stu-id="da6ec-171">P4</span></span>
- <span data-ttu-id="da6ec-172">P5</span><span class="sxs-lookup"><span data-stu-id="da6ec-172">P5</span></span>
- <span data-ttu-id="da6ec-173">C0</span><span class="sxs-lookup"><span data-stu-id="da6ec-173">C0</span></span>
- <span data-ttu-id="da6ec-174">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="da6ec-174">C1</span></span>
- <span data-ttu-id="da6ec-175">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="da6ec-175">C2</span></span>
- <span data-ttu-id="da6ec-176">C3</span><span class="sxs-lookup"><span data-stu-id="da6ec-176">C3</span></span>
- <span data-ttu-id="da6ec-177">C4</span><span class="sxs-lookup"><span data-stu-id="da6ec-177">C4</span></span>
- <span data-ttu-id="da6ec-178">C5</span><span class="sxs-lookup"><span data-stu-id="da6ec-178">C5</span></span>
- <span data-ttu-id="da6ec-179">C6</span><span class="sxs-lookup"><span data-stu-id="da6ec-179">C6</span></span>
- <span data-ttu-id="da6ec-180">250MB</span><span class="sxs-lookup"><span data-stu-id="da6ec-180">250MB</span></span>
- <span data-ttu-id="da6ec-181">1GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-181">1GB</span></span>
- <span data-ttu-id="da6ec-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-182">2.5GB</span></span>
- <span data-ttu-id="da6ec-183">6GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-183">6GB</span></span>
- <span data-ttu-id="da6ec-184">13GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-184">13GB</span></span>
- <span data-ttu-id="da6ec-185">26GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-185">26GB</span></span>
- <span data-ttu-id="da6ec-186">53GB</span><span class="sxs-lookup"><span data-stu-id="da6ec-186">53GB</span></span>
- <span data-ttu-id="da6ec-187">120 GB varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="da6ec-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="da6ec-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="da6ec-188">-Sku</span></span>
<span data-ttu-id="da6ec-189">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="da6ec-190">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="da6ec-190">Valid values are:</span></span> 
- <span data-ttu-id="da6ec-191">Ana</span><span class="sxs-lookup"><span data-stu-id="da6ec-191">Basic</span></span>
- <span data-ttu-id="da6ec-192">Ardından</span><span class="sxs-lookup"><span data-stu-id="da6ec-192">Standard</span></span>
- <span data-ttu-id="da6ec-193">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="da6ec-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="da6ec-194">Etiketli</span><span class="sxs-lookup"><span data-stu-id="da6ec-194">-Tag</span></span>
<span data-ttu-id="da6ec-195">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="da6ec-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="da6ec-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="da6ec-196">-TenantSettings</span></span>
<span data-ttu-id="da6ec-197">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="da6ec-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="da6ec-198">-Onay</span><span class="sxs-lookup"><span data-stu-id="da6ec-198">-Confirm</span></span>
<span data-ttu-id="da6ec-199">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da6ec-199">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ec-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da6ec-200">-WhatIf</span></span>
<span data-ttu-id="da6ec-201">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da6ec-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da6ec-202">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da6ec-202">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da6ec-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6ec-203">CommonParameters</span></span>
<span data-ttu-id="da6ec-204">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da6ec-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6ec-205">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da6ec-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6ec-206">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da6ec-206">INPUTS</span></span>

### <span data-ttu-id="da6ec-207">System. String</span><span class="sxs-lookup"><span data-stu-id="da6ec-207">System.String</span></span>

### <span data-ttu-id="da6ec-208">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da6ec-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="da6ec-209">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="da6ec-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da6ec-210">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="da6ec-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="da6ec-211">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da6ec-211">OUTPUTS</span></span>

### <span data-ttu-id="da6ec-212">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="da6ec-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="da6ec-213">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da6ec-213">NOTES</span></span>

## <span data-ttu-id="da6ec-214">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da6ec-214">RELATED LINKS</span></span>

[<span data-ttu-id="da6ec-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="da6ec-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="da6ec-216">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="da6ec-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="da6ec-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="da6ec-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

