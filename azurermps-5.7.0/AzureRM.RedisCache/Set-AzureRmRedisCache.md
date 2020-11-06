---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589705"
---
# <span data-ttu-id="0e705-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0e705-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="0e705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e705-102">SYNOPSIS</span></span>
<span data-ttu-id="0e705-103">Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0e705-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e705-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e705-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e705-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e705-105">DESCRIPTION</span></span>
<span data-ttu-id="0e705-106">**Set-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0e705-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="0e705-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e705-107">EXAMPLES</span></span>

### <span data-ttu-id="0e705-108">Örnek 1: Redis önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0e705-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="0e705-109">Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e705-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="0e705-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e705-110">PARAMETERS</span></span>

### <span data-ttu-id="0e705-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e705-111">-DefaultProfile</span></span>
<span data-ttu-id="0e705-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e705-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e705-113">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="0e705-113">-EnableNonSslPort</span></span>
<span data-ttu-id="0e705-114">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e705-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="0e705-115">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="0e705-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="0e705-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="0e705-117">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0e705-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="0e705-118">MaxMemory-ilkesini ayarlamak için *Redisconfiguration* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0e705-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="0e705-119">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="0e705-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e705-120">-Name</span></span>
<span data-ttu-id="0e705-121">Güncelleştirilecek Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e705-122">-RedisConfiguration</span></span>
<span data-ttu-id="0e705-123">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="0e705-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0e705-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e705-125">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0e705-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="0e705-126">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="0e705-127">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0e705-127">Premium tier only.</span></span>
- <span data-ttu-id="0e705-128">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="0e705-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="0e705-129">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="0e705-130">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0e705-130">Premium tier only.</span></span>
- <span data-ttu-id="0e705-131">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="0e705-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="0e705-132">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="0e705-133">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="0e705-133">Premium tier only.</span></span> 
- <span data-ttu-id="0e705-134">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="0e705-134">maxmemory-reserved.</span></span>
<span data-ttu-id="0e705-135">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="0e705-136">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-137">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="0e705-137">maxmemory-policy.</span></span>
<span data-ttu-id="0e705-138">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="0e705-139">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="0e705-139">All pricing tiers.</span></span> 
- <span data-ttu-id="0e705-140">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="0e705-140">notify-keyspace-events.</span></span>
<span data-ttu-id="0e705-141">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="0e705-142">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="0e705-143">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="0e705-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="0e705-144">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0e705-145">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-146">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="0e705-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="0e705-147">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0e705-148">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-149">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="0e705-149">set-max-intset-entries.</span></span>
<span data-ttu-id="0e705-150">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0e705-151">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-152">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="0e705-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="0e705-153">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0e705-154">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-155">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="0e705-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="0e705-156">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="0e705-157">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="0e705-158">Databases.</span><span class="sxs-lookup"><span data-stu-id="0e705-158">databases.</span></span>
<span data-ttu-id="0e705-159">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0e705-159">Configures the number of databases.</span></span>
<span data-ttu-id="0e705-160">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0e705-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="0e705-161">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="0e705-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="0e705-162">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="0e705-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e705-163">-ResourceGroupName</span></span>
<span data-ttu-id="0e705-164">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-165">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="0e705-165">-ShardCount</span></span>
<span data-ttu-id="0e705-166">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-167">-Boyut</span><span class="sxs-lookup"><span data-stu-id="0e705-167">-Size</span></span>
<span data-ttu-id="0e705-168">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="0e705-169">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0e705-169">Valid values are:</span></span> 

- <span data-ttu-id="0e705-170">P1</span><span class="sxs-lookup"><span data-stu-id="0e705-170">P1</span></span>
- <span data-ttu-id="0e705-171">P2</span><span class="sxs-lookup"><span data-stu-id="0e705-171">P2</span></span>
- <span data-ttu-id="0e705-172">P3</span><span class="sxs-lookup"><span data-stu-id="0e705-172">P3</span></span>
- <span data-ttu-id="0e705-173">P4</span><span class="sxs-lookup"><span data-stu-id="0e705-173">P4</span></span>
- <span data-ttu-id="0e705-174">C0</span><span class="sxs-lookup"><span data-stu-id="0e705-174">C0</span></span>
- <span data-ttu-id="0e705-175">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="0e705-175">C1</span></span>
- <span data-ttu-id="0e705-176">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="0e705-176">C2</span></span>
- <span data-ttu-id="0e705-177">C3</span><span class="sxs-lookup"><span data-stu-id="0e705-177">C3</span></span>
- <span data-ttu-id="0e705-178">C4</span><span class="sxs-lookup"><span data-stu-id="0e705-178">C4</span></span>
- <span data-ttu-id="0e705-179">C5</span><span class="sxs-lookup"><span data-stu-id="0e705-179">C5</span></span>
- <span data-ttu-id="0e705-180">C6</span><span class="sxs-lookup"><span data-stu-id="0e705-180">C6</span></span>
- <span data-ttu-id="0e705-181">250MB</span><span class="sxs-lookup"><span data-stu-id="0e705-181">250MB</span></span>
- <span data-ttu-id="0e705-182">1GB</span><span class="sxs-lookup"><span data-stu-id="0e705-182">1GB</span></span>
- <span data-ttu-id="0e705-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="0e705-183">2.5GB</span></span>
- <span data-ttu-id="0e705-184">6GB</span><span class="sxs-lookup"><span data-stu-id="0e705-184">6GB</span></span>
- <span data-ttu-id="0e705-185">13GB</span><span class="sxs-lookup"><span data-stu-id="0e705-185">13GB</span></span>
- <span data-ttu-id="0e705-186">26GB</span><span class="sxs-lookup"><span data-stu-id="0e705-186">26GB</span></span>
- <span data-ttu-id="0e705-187">53GB</span><span class="sxs-lookup"><span data-stu-id="0e705-187">53GB</span></span>

<span data-ttu-id="0e705-188">Varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="0e705-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="0e705-189">-Sku</span></span>
<span data-ttu-id="0e705-190">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e705-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="0e705-191">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0e705-191">Valid values are:</span></span> 

- <span data-ttu-id="0e705-192">Ana</span><span class="sxs-lookup"><span data-stu-id="0e705-192">Basic</span></span>
- <span data-ttu-id="0e705-193">Ardından</span><span class="sxs-lookup"><span data-stu-id="0e705-193">Standard</span></span>
- <span data-ttu-id="0e705-194">Min</span><span class="sxs-lookup"><span data-stu-id="0e705-194">Premium</span></span>

<span data-ttu-id="0e705-195">Varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="0e705-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-196">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0e705-196">-Tag</span></span>
<span data-ttu-id="0e705-197">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="0e705-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="0e705-198">-TenantSettings</span></span>
<span data-ttu-id="0e705-199">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0e705-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-200">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e705-200">-Confirm</span></span>
<span data-ttu-id="0e705-201">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e705-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e705-202">-WhatIf</span></span>
<span data-ttu-id="0e705-203">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e705-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e705-204">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e705-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e705-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e705-205">CommonParameters</span></span>
<span data-ttu-id="0e705-206">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e705-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e705-207">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e705-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e705-208">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e705-208">INPUTS</span></span>

### <span data-ttu-id="0e705-209">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0e705-209">None</span></span>
<span data-ttu-id="0e705-210">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e705-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0e705-211">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e705-211">OUTPUTS</span></span>

### <span data-ttu-id="0e705-212">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="0e705-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="0e705-213">Birincil ve ikincil erişim tuşları dahil olmak üzere, kırmızı bir önbelleğin tüm özniteliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0e705-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="0e705-214">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e705-214">NOTES</span></span>

## <span data-ttu-id="0e705-215">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e705-215">RELATED LINKS</span></span>

[<span data-ttu-id="0e705-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0e705-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="0e705-217">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0e705-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0e705-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0e705-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


