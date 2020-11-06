---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593911"
---
# <span data-ttu-id="a9f8e-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a9f8e-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="a9f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f8e-103">Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9f8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9f8e-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9f8e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9f8e-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f8e-106">**Set-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="a9f8e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9f8e-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f8e-108">Örnek 1: Redis önbelleğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a9f8e-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="a9f8e-109">Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="a9f8e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9f8e-110">PARAMETERS</span></span>

### <span data-ttu-id="a9f8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f8e-111">-DefaultProfile</span></span>
<span data-ttu-id="a9f8e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9f8e-113">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="a9f8e-113">-EnableNonSslPort</span></span>
<span data-ttu-id="a9f8e-114">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="a9f8e-115">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="a9f8e-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="a9f8e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9f8e-116">-Name</span></span>
<span data-ttu-id="a9f8e-117">Güncelleştirilecek Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="a9f8e-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9f8e-118">-RedisConfiguration</span></span>
<span data-ttu-id="a9f8e-119">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="a9f8e-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a9f8e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9f8e-121">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="a9f8e-122">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="a9f8e-123">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-123">Premium tier only.</span></span>
- <span data-ttu-id="a9f8e-124">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="a9f8e-125">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="a9f8e-126">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-126">Premium tier only.</span></span>
- <span data-ttu-id="a9f8e-127">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="a9f8e-128">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="a9f8e-129">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-129">Premium tier only.</span></span> 
- <span data-ttu-id="a9f8e-130">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-130">maxmemory-reserved.</span></span>
<span data-ttu-id="a9f8e-131">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="a9f8e-132">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-133">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-133">maxmemory-policy.</span></span>
<span data-ttu-id="a9f8e-134">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="a9f8e-135">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-135">All pricing tiers.</span></span> 
- <span data-ttu-id="a9f8e-136">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-136">notify-keyspace-events.</span></span>
<span data-ttu-id="a9f8e-137">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="a9f8e-138">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-139">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="a9f8e-140">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a9f8e-141">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-142">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="a9f8e-143">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a9f8e-144">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-145">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-145">set-max-intset-entries.</span></span>
<span data-ttu-id="a9f8e-146">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a9f8e-147">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-148">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="a9f8e-149">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a9f8e-150">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-151">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="a9f8e-152">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a9f8e-153">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a9f8e-154">Databases.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-154">databases.</span></span>
<span data-ttu-id="a9f8e-155">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-155">Configures the number of databases.</span></span>
<span data-ttu-id="a9f8e-156">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="a9f8e-157">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="a9f8e-158">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="a9f8e-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="a9f8e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f8e-159">-ResourceGroupName</span></span>
<span data-ttu-id="a9f8e-160">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="a9f8e-161">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="a9f8e-161">-ShardCount</span></span>
<span data-ttu-id="a9f8e-162">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="a9f8e-163">-Boyut</span><span class="sxs-lookup"><span data-stu-id="a9f8e-163">-Size</span></span>
<span data-ttu-id="a9f8e-164">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="a9f8e-165">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a9f8e-165">Valid values are:</span></span> 
- <span data-ttu-id="a9f8e-166">P1</span><span class="sxs-lookup"><span data-stu-id="a9f8e-166">P1</span></span>
- <span data-ttu-id="a9f8e-167">P2</span><span class="sxs-lookup"><span data-stu-id="a9f8e-167">P2</span></span>
- <span data-ttu-id="a9f8e-168">P3</span><span class="sxs-lookup"><span data-stu-id="a9f8e-168">P3</span></span>
- <span data-ttu-id="a9f8e-169">P4</span><span class="sxs-lookup"><span data-stu-id="a9f8e-169">P4</span></span>
- <span data-ttu-id="a9f8e-170">C0</span><span class="sxs-lookup"><span data-stu-id="a9f8e-170">C0</span></span>
- <span data-ttu-id="a9f8e-171">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="a9f8e-171">C1</span></span>
- <span data-ttu-id="a9f8e-172">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="a9f8e-172">C2</span></span>
- <span data-ttu-id="a9f8e-173">C3</span><span class="sxs-lookup"><span data-stu-id="a9f8e-173">C3</span></span>
- <span data-ttu-id="a9f8e-174">C4</span><span class="sxs-lookup"><span data-stu-id="a9f8e-174">C4</span></span>
- <span data-ttu-id="a9f8e-175">C5</span><span class="sxs-lookup"><span data-stu-id="a9f8e-175">C5</span></span>
- <span data-ttu-id="a9f8e-176">C6</span><span class="sxs-lookup"><span data-stu-id="a9f8e-176">C6</span></span>
- <span data-ttu-id="a9f8e-177">250MB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-177">250MB</span></span>
- <span data-ttu-id="a9f8e-178">1GB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-178">1GB</span></span>
- <span data-ttu-id="a9f8e-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-179">2.5GB</span></span>
- <span data-ttu-id="a9f8e-180">6GB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-180">6GB</span></span>
- <span data-ttu-id="a9f8e-181">13GB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-181">13GB</span></span>
- <span data-ttu-id="a9f8e-182">26GB</span><span class="sxs-lookup"><span data-stu-id="a9f8e-182">26GB</span></span>
- <span data-ttu-id="a9f8e-183">53GB varsayılan değer 1GB veya C1 'dır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="a9f8e-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9f8e-184">-Sku</span></span>
<span data-ttu-id="a9f8e-185">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="a9f8e-186">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a9f8e-186">Valid values are:</span></span> 
- <span data-ttu-id="a9f8e-187">Ana</span><span class="sxs-lookup"><span data-stu-id="a9f8e-187">Basic</span></span>
- <span data-ttu-id="a9f8e-188">Ardından</span><span class="sxs-lookup"><span data-stu-id="a9f8e-188">Standard</span></span>
- <span data-ttu-id="a9f8e-189">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="a9f8e-190">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a9f8e-190">-Tag</span></span>
<span data-ttu-id="a9f8e-191">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="a9f8e-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="a9f8e-192">-TenantSettings</span></span>
<span data-ttu-id="a9f8e-193">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="a9f8e-194">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9f8e-194">-Confirm</span></span>
<span data-ttu-id="a9f8e-195">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9f8e-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9f8e-196">-WhatIf</span></span>
<span data-ttu-id="a9f8e-197">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9f8e-198">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9f8e-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f8e-199">CommonParameters</span></span>
<span data-ttu-id="a9f8e-200">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9f8e-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f8e-201">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f8e-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f8e-202">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9f8e-202">INPUTS</span></span>

### <span data-ttu-id="a9f8e-203">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f8e-203">System.String</span></span>

### <span data-ttu-id="a9f8e-204">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9f8e-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9f8e-205">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9f8e-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a9f8e-206">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9f8e-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a9f8e-207">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9f8e-207">OUTPUTS</span></span>

### <span data-ttu-id="a9f8e-208">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a9f8e-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="a9f8e-209">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9f8e-209">NOTES</span></span>

## <span data-ttu-id="a9f8e-210">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9f8e-210">RELATED LINKS</span></span>

[<span data-ttu-id="a9f8e-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a9f8e-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a9f8e-212">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a9f8e-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a9f8e-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a9f8e-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


