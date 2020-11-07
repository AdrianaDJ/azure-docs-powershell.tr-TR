---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932646"
---
# <span data-ttu-id="9f33c-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9f33c-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="9f33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f33c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f33c-103">Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="9f33c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f33c-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f33c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f33c-105">DESCRIPTION</span></span>
<span data-ttu-id="9f33c-106">**Set-AzRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="9f33c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f33c-107">EXAMPLES</span></span>

### <span data-ttu-id="9f33c-108">Örnek 1: Redis önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="9f33c-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="9f33c-109">Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="9f33c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f33c-110">PARAMETERS</span></span>

### <span data-ttu-id="9f33c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f33c-111">-DefaultProfile</span></span>
<span data-ttu-id="9f33c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f33c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f33c-113">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="9f33c-113">-EnableNonSslPort</span></span>
<span data-ttu-id="9f33c-114">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="9f33c-115">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="9f33c-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="9f33c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f33c-116">-Name</span></span>
<span data-ttu-id="9f33c-117">Güncelleştirilecek Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="9f33c-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f33c-118">-RedisConfiguration</span></span>
<span data-ttu-id="9f33c-119">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="9f33c-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9f33c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9f33c-121">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="9f33c-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="9f33c-122">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="9f33c-123">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="9f33c-123">Premium tier only.</span></span>
- <span data-ttu-id="9f33c-124">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9f33c-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="9f33c-125">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="9f33c-126">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="9f33c-126">Premium tier only.</span></span>
- <span data-ttu-id="9f33c-127">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="9f33c-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="9f33c-128">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="9f33c-129">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="9f33c-129">Premium tier only.</span></span> 
- <span data-ttu-id="9f33c-130">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="9f33c-130">maxmemory-reserved.</span></span>
<span data-ttu-id="9f33c-131">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="9f33c-132">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-133">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="9f33c-133">maxmemory-policy.</span></span>
<span data-ttu-id="9f33c-134">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="9f33c-135">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="9f33c-135">All pricing tiers.</span></span> 
- <span data-ttu-id="9f33c-136">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-136">notify-keyspace-events.</span></span>
<span data-ttu-id="9f33c-137">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="9f33c-138">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="9f33c-139">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="9f33c-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="9f33c-140">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9f33c-141">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-142">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="9f33c-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="9f33c-143">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9f33c-144">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-145">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="9f33c-145">set-max-intset-entries.</span></span>
<span data-ttu-id="9f33c-146">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9f33c-147">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-148">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="9f33c-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="9f33c-149">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9f33c-150">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-151">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="9f33c-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="9f33c-152">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="9f33c-153">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="9f33c-154">Databases.</span><span class="sxs-lookup"><span data-stu-id="9f33c-154">databases.</span></span>
<span data-ttu-id="9f33c-155">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-155">Configures the number of databases.</span></span>
<span data-ttu-id="9f33c-156">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="9f33c-157">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="9f33c-158">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="9f33c-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="9f33c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f33c-159">-ResourceGroupName</span></span>
<span data-ttu-id="9f33c-160">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="9f33c-161">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="9f33c-161">-ShardCount</span></span>
<span data-ttu-id="9f33c-162">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="9f33c-163">-Boyut</span><span class="sxs-lookup"><span data-stu-id="9f33c-163">-Size</span></span>
<span data-ttu-id="9f33c-164">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="9f33c-165">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f33c-165">Valid values are:</span></span> 
- <span data-ttu-id="9f33c-166">P1</span><span class="sxs-lookup"><span data-stu-id="9f33c-166">P1</span></span>
- <span data-ttu-id="9f33c-167">P2</span><span class="sxs-lookup"><span data-stu-id="9f33c-167">P2</span></span>
- <span data-ttu-id="9f33c-168">P3</span><span class="sxs-lookup"><span data-stu-id="9f33c-168">P3</span></span>
- <span data-ttu-id="9f33c-169">P4</span><span class="sxs-lookup"><span data-stu-id="9f33c-169">P4</span></span>
- <span data-ttu-id="9f33c-170">P5</span><span class="sxs-lookup"><span data-stu-id="9f33c-170">P5</span></span>
- <span data-ttu-id="9f33c-171">C0</span><span class="sxs-lookup"><span data-stu-id="9f33c-171">C0</span></span>
- <span data-ttu-id="9f33c-172">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="9f33c-172">C1</span></span>
- <span data-ttu-id="9f33c-173">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="9f33c-173">C2</span></span>
- <span data-ttu-id="9f33c-174">C3</span><span class="sxs-lookup"><span data-stu-id="9f33c-174">C3</span></span>
- <span data-ttu-id="9f33c-175">C4</span><span class="sxs-lookup"><span data-stu-id="9f33c-175">C4</span></span>
- <span data-ttu-id="9f33c-176">C5</span><span class="sxs-lookup"><span data-stu-id="9f33c-176">C5</span></span>
- <span data-ttu-id="9f33c-177">C6</span><span class="sxs-lookup"><span data-stu-id="9f33c-177">C6</span></span>
- <span data-ttu-id="9f33c-178">250MB</span><span class="sxs-lookup"><span data-stu-id="9f33c-178">250MB</span></span>
- <span data-ttu-id="9f33c-179">1GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-179">1GB</span></span>
- <span data-ttu-id="9f33c-180">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-180">2.5GB</span></span>
- <span data-ttu-id="9f33c-181">6GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-181">6GB</span></span>
- <span data-ttu-id="9f33c-182">13GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-182">13GB</span></span>
- <span data-ttu-id="9f33c-183">26GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-183">26GB</span></span>
- <span data-ttu-id="9f33c-184">53GB</span><span class="sxs-lookup"><span data-stu-id="9f33c-184">53GB</span></span>
- <span data-ttu-id="9f33c-185">120 GB varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="9f33c-185">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="9f33c-186">-SKU</span><span class="sxs-lookup"><span data-stu-id="9f33c-186">-Sku</span></span>
<span data-ttu-id="9f33c-187">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="9f33c-188">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9f33c-188">Valid values are:</span></span> 
- <span data-ttu-id="9f33c-189">Ana</span><span class="sxs-lookup"><span data-stu-id="9f33c-189">Basic</span></span>
- <span data-ttu-id="9f33c-190">Ardından</span><span class="sxs-lookup"><span data-stu-id="9f33c-190">Standard</span></span>
- <span data-ttu-id="9f33c-191">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-191">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="9f33c-192">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9f33c-192">-Tag</span></span>
<span data-ttu-id="9f33c-193">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="9f33c-193">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="9f33c-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="9f33c-194">-TenantSettings</span></span>
<span data-ttu-id="9f33c-195">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="9f33c-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="9f33c-196">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f33c-196">-Confirm</span></span>
<span data-ttu-id="9f33c-197">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f33c-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f33c-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f33c-198">-WhatIf</span></span>
<span data-ttu-id="9f33c-199">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f33c-200">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9f33c-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f33c-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f33c-201">CommonParameters</span></span>
<span data-ttu-id="9f33c-202">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f33c-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f33c-203">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f33c-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f33c-204">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f33c-204">INPUTS</span></span>

### <span data-ttu-id="9f33c-205">System. String</span><span class="sxs-lookup"><span data-stu-id="9f33c-205">System.String</span></span>

### <span data-ttu-id="9f33c-206">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9f33c-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9f33c-207">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f33c-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9f33c-208">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="9f33c-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9f33c-209">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f33c-209">OUTPUTS</span></span>

### <span data-ttu-id="9f33c-210">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9f33c-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="9f33c-211">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f33c-211">NOTES</span></span>

## <span data-ttu-id="9f33c-212">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f33c-212">RELATED LINKS</span></span>

[<span data-ttu-id="9f33c-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9f33c-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9f33c-214">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9f33c-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9f33c-215">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9f33c-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


