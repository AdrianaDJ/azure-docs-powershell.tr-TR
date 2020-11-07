---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759547"
---
# <span data-ttu-id="defd6-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="defd6-101">New-AzRedisCache</span></span>

## <span data-ttu-id="defd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="defd6-102">SYNOPSIS</span></span>
<span data-ttu-id="defd6-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="defd6-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="defd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="defd6-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="defd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="defd6-105">DESCRIPTION</span></span>
<span data-ttu-id="defd6-106">**Yeni-AzRedisCache** cmdlet 'ı Azure Redis önbelleği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="defd6-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="defd6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="defd6-107">EXAMPLES</span></span>

### <span data-ttu-id="defd6-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="defd6-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="defd6-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="defd6-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="defd6-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="defd6-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="defd6-111">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="defd6-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="defd6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="defd6-112">PARAMETERS</span></span>

### <span data-ttu-id="defd6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defd6-113">-DefaultProfile</span></span>
<span data-ttu-id="defd6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="defd6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="defd6-115">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="defd6-115">-EnableNonSslPort</span></span>
<span data-ttu-id="defd6-116">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="defd6-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="defd6-117">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="defd6-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="defd6-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="defd6-118">-Location</span></span>
<span data-ttu-id="defd6-119">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="defd6-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="defd6-120">Valid values are:</span></span> 
- <span data-ttu-id="defd6-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="defd6-121">North Central US</span></span>
- <span data-ttu-id="defd6-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="defd6-122">South Central US</span></span>
- <span data-ttu-id="defd6-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="defd6-123">Central US</span></span>
- <span data-ttu-id="defd6-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="defd6-124">West Europe</span></span>
- <span data-ttu-id="defd6-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="defd6-125">North Europe</span></span>
- <span data-ttu-id="defd6-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="defd6-126">West US</span></span>
- <span data-ttu-id="defd6-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="defd6-127">East US</span></span>
- <span data-ttu-id="defd6-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="defd6-128">East US 2</span></span>
- <span data-ttu-id="defd6-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="defd6-129">Japan East</span></span>
- <span data-ttu-id="defd6-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="defd6-130">Japan West</span></span>
- <span data-ttu-id="defd6-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="defd6-131">Brazil South</span></span>
- <span data-ttu-id="defd6-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="defd6-132">Southeast Asia</span></span>
- <span data-ttu-id="defd6-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="defd6-133">East Asia</span></span>
- <span data-ttu-id="defd6-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="defd6-134">Australia East</span></span>
- <span data-ttu-id="defd6-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="defd6-135">Australia Southeast</span></span>

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

### <span data-ttu-id="defd6-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="defd6-136">-Name</span></span>
<span data-ttu-id="defd6-137">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="defd6-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="defd6-138">-RedisConfiguration</span></span>
<span data-ttu-id="defd6-139">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="defd6-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="defd6-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="defd6-141">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="defd6-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="defd6-142">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="defd6-143">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="defd6-143">Premium tier only.</span></span>
- <span data-ttu-id="defd6-144">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="defd6-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="defd6-145">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="defd6-146">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="defd6-146">Premium tier only.</span></span>
- <span data-ttu-id="defd6-147">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="defd6-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="defd6-148">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="defd6-149">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="defd6-149">Premium tier only.</span></span> 
- <span data-ttu-id="defd6-150">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="defd6-150">maxmemory-reserved.</span></span>
<span data-ttu-id="defd6-151">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="defd6-152">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-153">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="defd6-153">maxmemory-policy.</span></span>
<span data-ttu-id="defd6-154">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="defd6-155">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="defd6-155">All pricing tiers.</span></span> 
- <span data-ttu-id="defd6-156">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="defd6-156">notify-keyspace-events.</span></span>
<span data-ttu-id="defd6-157">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="defd6-158">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="defd6-159">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="defd6-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="defd6-160">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="defd6-161">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-162">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="defd6-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="defd6-163">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="defd6-164">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-165">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="defd6-165">set-max-intset-entries.</span></span>
<span data-ttu-id="defd6-166">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="defd6-167">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-168">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="defd6-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="defd6-169">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="defd6-170">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-171">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="defd6-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="defd6-172">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="defd6-173">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="defd6-174">Databases.</span><span class="sxs-lookup"><span data-stu-id="defd6-174">databases.</span></span>
<span data-ttu-id="defd6-175">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="defd6-175">Configures the number of databases.</span></span>
<span data-ttu-id="defd6-176">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="defd6-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="defd6-177">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="defd6-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="defd6-178">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="defd6-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="defd6-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="defd6-179">-ResourceGroupName</span></span>
<span data-ttu-id="defd6-180">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="defd6-181">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="defd6-181">-ShardCount</span></span>
<span data-ttu-id="defd6-182">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="defd6-183">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="defd6-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="defd6-184">2</span><span class="sxs-lookup"><span data-stu-id="defd6-184">1</span></span>
- <span data-ttu-id="defd6-185">2</span><span class="sxs-lookup"><span data-stu-id="defd6-185">2</span></span>
- <span data-ttu-id="defd6-186">@</span><span class="sxs-lookup"><span data-stu-id="defd6-186">3</span></span>
- <span data-ttu-id="defd6-187">1.921.024</span><span class="sxs-lookup"><span data-stu-id="defd6-187">4</span></span>
- <span data-ttu-id="defd6-188">tir</span><span class="sxs-lookup"><span data-stu-id="defd6-188">5</span></span>
- <span data-ttu-id="defd6-189">+</span><span class="sxs-lookup"><span data-stu-id="defd6-189">6</span></span>
- <span data-ttu-id="defd6-190">+</span><span class="sxs-lookup"><span data-stu-id="defd6-190">7</span></span>
- <span data-ttu-id="defd6-191">8@@</span><span class="sxs-lookup"><span data-stu-id="defd6-191">8</span></span>
- <span data-ttu-id="defd6-192">döndürdü</span><span class="sxs-lookup"><span data-stu-id="defd6-192">9</span></span> 
- <span data-ttu-id="defd6-193">on</span><span class="sxs-lookup"><span data-stu-id="defd6-193">10</span></span>

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

### <span data-ttu-id="defd6-194">-Boyut</span><span class="sxs-lookup"><span data-stu-id="defd6-194">-Size</span></span>
<span data-ttu-id="defd6-195">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="defd6-196">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="defd6-196">Valid values are:</span></span> 
- <span data-ttu-id="defd6-197">P1</span><span class="sxs-lookup"><span data-stu-id="defd6-197">P1</span></span>
- <span data-ttu-id="defd6-198">P2</span><span class="sxs-lookup"><span data-stu-id="defd6-198">P2</span></span>
- <span data-ttu-id="defd6-199">P3</span><span class="sxs-lookup"><span data-stu-id="defd6-199">P3</span></span>
- <span data-ttu-id="defd6-200">P4</span><span class="sxs-lookup"><span data-stu-id="defd6-200">P4</span></span>
- <span data-ttu-id="defd6-201">C0</span><span class="sxs-lookup"><span data-stu-id="defd6-201">C0</span></span>
- <span data-ttu-id="defd6-202">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="defd6-202">C1</span></span>
- <span data-ttu-id="defd6-203">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="defd6-203">C2</span></span>
- <span data-ttu-id="defd6-204">C3</span><span class="sxs-lookup"><span data-stu-id="defd6-204">C3</span></span>
- <span data-ttu-id="defd6-205">C4</span><span class="sxs-lookup"><span data-stu-id="defd6-205">C4</span></span>
- <span data-ttu-id="defd6-206">C5</span><span class="sxs-lookup"><span data-stu-id="defd6-206">C5</span></span>
- <span data-ttu-id="defd6-207">C6</span><span class="sxs-lookup"><span data-stu-id="defd6-207">C6</span></span>
- <span data-ttu-id="defd6-208">250MB</span><span class="sxs-lookup"><span data-stu-id="defd6-208">250MB</span></span>
- <span data-ttu-id="defd6-209">1GB</span><span class="sxs-lookup"><span data-stu-id="defd6-209">1GB</span></span>
- <span data-ttu-id="defd6-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="defd6-210">2.5GB</span></span>
- <span data-ttu-id="defd6-211">6GB</span><span class="sxs-lookup"><span data-stu-id="defd6-211">6GB</span></span>
- <span data-ttu-id="defd6-212">13GB</span><span class="sxs-lookup"><span data-stu-id="defd6-212">13GB</span></span>
- <span data-ttu-id="defd6-213">26GB</span><span class="sxs-lookup"><span data-stu-id="defd6-213">26GB</span></span>
- <span data-ttu-id="defd6-214">53GB varsayılan değer 1GB veya C1 'dır.</span><span class="sxs-lookup"><span data-stu-id="defd6-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="defd6-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="defd6-215">-Sku</span></span>
<span data-ttu-id="defd6-216">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="defd6-217">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="defd6-217">Valid values are:</span></span> 
- <span data-ttu-id="defd6-218">Ana</span><span class="sxs-lookup"><span data-stu-id="defd6-218">Basic</span></span>
- <span data-ttu-id="defd6-219">Ardından</span><span class="sxs-lookup"><span data-stu-id="defd6-219">Standard</span></span>
- <span data-ttu-id="defd6-220">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="defd6-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="defd6-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="defd6-221">-StaticIP</span></span>
<span data-ttu-id="defd6-222">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="defd6-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="defd6-223">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="defd6-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="defd6-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="defd6-224">-SubnetId</span></span>
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

### <span data-ttu-id="defd6-225">Etiketli</span><span class="sxs-lookup"><span data-stu-id="defd6-225">-Tag</span></span>
<span data-ttu-id="defd6-226">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="defd6-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="defd6-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="defd6-227">-TenantSettings</span></span>
<span data-ttu-id="defd6-228">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="defd6-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="defd6-229">-Bölge</span><span class="sxs-lookup"><span data-stu-id="defd6-229">-Zone</span></span>
<span data-ttu-id="defd6-230">Bölgeler listesi.</span><span class="sxs-lookup"><span data-stu-id="defd6-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="defd6-231">-Onay</span><span class="sxs-lookup"><span data-stu-id="defd6-231">-Confirm</span></span>
<span data-ttu-id="defd6-232">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="defd6-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="defd6-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="defd6-233">-WhatIf</span></span>
<span data-ttu-id="defd6-234">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="defd6-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="defd6-235">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="defd6-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="defd6-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defd6-236">CommonParameters</span></span>
<span data-ttu-id="defd6-237">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="defd6-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defd6-238">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="defd6-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defd6-239">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="defd6-239">INPUTS</span></span>

### <span data-ttu-id="defd6-240">System. String</span><span class="sxs-lookup"><span data-stu-id="defd6-240">System.String</span></span>

### <span data-ttu-id="defd6-241">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="defd6-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="defd6-242">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="defd6-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="defd6-243">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="defd6-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="defd6-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="defd6-244">System.String[]</span></span>

## <span data-ttu-id="defd6-245">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="defd6-245">OUTPUTS</span></span>

### <span data-ttu-id="defd6-246">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="defd6-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="defd6-247">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="defd6-247">NOTES</span></span>

## <span data-ttu-id="defd6-248">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="defd6-248">RELATED LINKS</span></span>

[<span data-ttu-id="defd6-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="defd6-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="defd6-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="defd6-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="defd6-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="defd6-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


