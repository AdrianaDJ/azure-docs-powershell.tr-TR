---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278477"
---
# <span data-ttu-id="ea068-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea068-101">New-AzRedisCache</span></span>

## <span data-ttu-id="ea068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea068-102">SYNOPSIS</span></span>
<span data-ttu-id="ea068-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea068-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="ea068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea068-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea068-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea068-105">DESCRIPTION</span></span>
<span data-ttu-id="ea068-106">**Yeni-AzRedisCache** cmdlet 'ı Azure Redis önbelleği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea068-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="ea068-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea068-107">EXAMPLES</span></span>

### <span data-ttu-id="ea068-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea068-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="ea068-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea068-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="ea068-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea068-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="ea068-111">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea068-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="ea068-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea068-112">PARAMETERS</span></span>

### <span data-ttu-id="ea068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea068-113">-DefaultProfile</span></span>
<span data-ttu-id="ea068-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea068-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea068-115">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="ea068-115">-EnableNonSslPort</span></span>
<span data-ttu-id="ea068-116">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea068-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="ea068-117">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="ea068-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="ea068-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="ea068-118">-Location</span></span>
<span data-ttu-id="ea068-119">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="ea068-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ea068-120">Valid values are:</span></span> 
- <span data-ttu-id="ea068-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="ea068-121">North Central US</span></span>
- <span data-ttu-id="ea068-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="ea068-122">South Central US</span></span>
- <span data-ttu-id="ea068-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="ea068-123">Central US</span></span>
- <span data-ttu-id="ea068-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="ea068-124">West Europe</span></span>
- <span data-ttu-id="ea068-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="ea068-125">North Europe</span></span>
- <span data-ttu-id="ea068-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="ea068-126">West US</span></span>
- <span data-ttu-id="ea068-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="ea068-127">East US</span></span>
- <span data-ttu-id="ea068-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="ea068-128">East US 2</span></span>
- <span data-ttu-id="ea068-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="ea068-129">Japan East</span></span>
- <span data-ttu-id="ea068-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="ea068-130">Japan West</span></span>
- <span data-ttu-id="ea068-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="ea068-131">Brazil South</span></span>
- <span data-ttu-id="ea068-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="ea068-132">Southeast Asia</span></span>
- <span data-ttu-id="ea068-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="ea068-133">East Asia</span></span>
- <span data-ttu-id="ea068-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="ea068-134">Australia East</span></span>
- <span data-ttu-id="ea068-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="ea068-135">Australia Southeast</span></span>

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

### <span data-ttu-id="ea068-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ea068-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="ea068-137">İstemcilere bağlanacak istemcilerin gerektirdiği TLS sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="ea068-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="ea068-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea068-138">-Name</span></span>
<span data-ttu-id="ea068-139">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="ea068-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea068-140">-RedisConfiguration</span></span>
<span data-ttu-id="ea068-141">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="ea068-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ea068-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea068-143">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ea068-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="ea068-144">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="ea068-145">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="ea068-145">Premium tier only.</span></span>
- <span data-ttu-id="ea068-146">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="ea068-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="ea068-147">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="ea068-148">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="ea068-148">Premium tier only.</span></span>
- <span data-ttu-id="ea068-149">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="ea068-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="ea068-150">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="ea068-151">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="ea068-151">Premium tier only.</span></span> 
- <span data-ttu-id="ea068-152">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="ea068-152">maxmemory-reserved.</span></span>
<span data-ttu-id="ea068-153">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="ea068-154">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-155">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="ea068-155">maxmemory-policy.</span></span>
<span data-ttu-id="ea068-156">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="ea068-157">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="ea068-157">All pricing tiers.</span></span> 
- <span data-ttu-id="ea068-158">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="ea068-158">notify-keyspace-events.</span></span>
<span data-ttu-id="ea068-159">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="ea068-160">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="ea068-161">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="ea068-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="ea068-162">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ea068-163">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-164">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="ea068-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="ea068-165">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ea068-166">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-167">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="ea068-167">set-max-intset-entries.</span></span>
<span data-ttu-id="ea068-168">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ea068-169">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-170">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="ea068-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="ea068-171">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ea068-172">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-173">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="ea068-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="ea068-174">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ea068-175">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ea068-176">Databases.</span><span class="sxs-lookup"><span data-stu-id="ea068-176">databases.</span></span>
<span data-ttu-id="ea068-177">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ea068-177">Configures the number of databases.</span></span>
<span data-ttu-id="ea068-178">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ea068-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="ea068-179">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="ea068-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="ea068-180">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="ea068-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="ea068-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea068-181">-ResourceGroupName</span></span>
<span data-ttu-id="ea068-182">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="ea068-183">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="ea068-183">-ShardCount</span></span>
<span data-ttu-id="ea068-184">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="ea068-185">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ea068-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ea068-186">2</span><span class="sxs-lookup"><span data-stu-id="ea068-186">1</span></span>
- <span data-ttu-id="ea068-187">2</span><span class="sxs-lookup"><span data-stu-id="ea068-187">2</span></span>
- <span data-ttu-id="ea068-188">@</span><span class="sxs-lookup"><span data-stu-id="ea068-188">3</span></span>
- <span data-ttu-id="ea068-189">1.921.024</span><span class="sxs-lookup"><span data-stu-id="ea068-189">4</span></span>
- <span data-ttu-id="ea068-190">tir</span><span class="sxs-lookup"><span data-stu-id="ea068-190">5</span></span>
- <span data-ttu-id="ea068-191">+</span><span class="sxs-lookup"><span data-stu-id="ea068-191">6</span></span>
- <span data-ttu-id="ea068-192">+</span><span class="sxs-lookup"><span data-stu-id="ea068-192">7</span></span>
- <span data-ttu-id="ea068-193">8@@</span><span class="sxs-lookup"><span data-stu-id="ea068-193">8</span></span>
- <span data-ttu-id="ea068-194">döndürdü</span><span class="sxs-lookup"><span data-stu-id="ea068-194">9</span></span> 
- <span data-ttu-id="ea068-195">on</span><span class="sxs-lookup"><span data-stu-id="ea068-195">10</span></span>

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

### <span data-ttu-id="ea068-196">-Boyut</span><span class="sxs-lookup"><span data-stu-id="ea068-196">-Size</span></span>
<span data-ttu-id="ea068-197">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="ea068-198">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ea068-198">Valid values are:</span></span> 
- <span data-ttu-id="ea068-199">P1</span><span class="sxs-lookup"><span data-stu-id="ea068-199">P1</span></span>
- <span data-ttu-id="ea068-200">P2</span><span class="sxs-lookup"><span data-stu-id="ea068-200">P2</span></span>
- <span data-ttu-id="ea068-201">P3</span><span class="sxs-lookup"><span data-stu-id="ea068-201">P3</span></span>
- <span data-ttu-id="ea068-202">P4</span><span class="sxs-lookup"><span data-stu-id="ea068-202">P4</span></span>
- <span data-ttu-id="ea068-203">P5</span><span class="sxs-lookup"><span data-stu-id="ea068-203">P5</span></span>
- <span data-ttu-id="ea068-204">C0</span><span class="sxs-lookup"><span data-stu-id="ea068-204">C0</span></span>
- <span data-ttu-id="ea068-205">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="ea068-205">C1</span></span>
- <span data-ttu-id="ea068-206">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="ea068-206">C2</span></span>
- <span data-ttu-id="ea068-207">C3</span><span class="sxs-lookup"><span data-stu-id="ea068-207">C3</span></span>
- <span data-ttu-id="ea068-208">C4</span><span class="sxs-lookup"><span data-stu-id="ea068-208">C4</span></span>
- <span data-ttu-id="ea068-209">C5</span><span class="sxs-lookup"><span data-stu-id="ea068-209">C5</span></span>
- <span data-ttu-id="ea068-210">C6</span><span class="sxs-lookup"><span data-stu-id="ea068-210">C6</span></span>
- <span data-ttu-id="ea068-211">250MB</span><span class="sxs-lookup"><span data-stu-id="ea068-211">250MB</span></span>
- <span data-ttu-id="ea068-212">1GB</span><span class="sxs-lookup"><span data-stu-id="ea068-212">1GB</span></span>
- <span data-ttu-id="ea068-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="ea068-213">2.5GB</span></span>
- <span data-ttu-id="ea068-214">6GB</span><span class="sxs-lookup"><span data-stu-id="ea068-214">6GB</span></span>
- <span data-ttu-id="ea068-215">13GB</span><span class="sxs-lookup"><span data-stu-id="ea068-215">13GB</span></span>
- <span data-ttu-id="ea068-216">26GB</span><span class="sxs-lookup"><span data-stu-id="ea068-216">26GB</span></span>
- <span data-ttu-id="ea068-217">53GB varsayılan değer 1GB veya C1 'dır.</span><span class="sxs-lookup"><span data-stu-id="ea068-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="ea068-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="ea068-218">-Sku</span></span>
<span data-ttu-id="ea068-219">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="ea068-220">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ea068-220">Valid values are:</span></span> 
- <span data-ttu-id="ea068-221">Ana</span><span class="sxs-lookup"><span data-stu-id="ea068-221">Basic</span></span>
- <span data-ttu-id="ea068-222">Ardından</span><span class="sxs-lookup"><span data-stu-id="ea068-222">Standard</span></span>
- <span data-ttu-id="ea068-223">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="ea068-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="ea068-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="ea068-224">-StaticIP</span></span>
<span data-ttu-id="ea068-225">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea068-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="ea068-226">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="ea068-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="ea068-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ea068-227">-SubnetId</span></span>
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

### <span data-ttu-id="ea068-228">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ea068-228">-Tag</span></span>
<span data-ttu-id="ea068-229">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="ea068-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="ea068-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="ea068-230">-TenantSettings</span></span>
<span data-ttu-id="ea068-231">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="ea068-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="ea068-232">-Bölge</span><span class="sxs-lookup"><span data-stu-id="ea068-232">-Zone</span></span>
<span data-ttu-id="ea068-233">Bölgeler listesi.</span><span class="sxs-lookup"><span data-stu-id="ea068-233">List of zones.</span></span>

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

### <span data-ttu-id="ea068-234">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea068-234">-Confirm</span></span>
<span data-ttu-id="ea068-235">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea068-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea068-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea068-236">-WhatIf</span></span>
<span data-ttu-id="ea068-237">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea068-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea068-238">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea068-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea068-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea068-239">CommonParameters</span></span>
<span data-ttu-id="ea068-240">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea068-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea068-241">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ea068-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea068-242">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea068-242">INPUTS</span></span>

### <span data-ttu-id="ea068-243">System. String</span><span class="sxs-lookup"><span data-stu-id="ea068-243">System.String</span></span>

### <span data-ttu-id="ea068-244">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea068-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ea068-245">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea068-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ea068-246">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea068-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ea068-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="ea068-247">System.String[]</span></span>

## <span data-ttu-id="ea068-248">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea068-248">OUTPUTS</span></span>

### <span data-ttu-id="ea068-249">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ea068-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="ea068-250">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea068-250">NOTES</span></span>

## <span data-ttu-id="ea068-251">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea068-251">RELATED LINKS</span></span>

[<span data-ttu-id="ea068-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea068-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ea068-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea068-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ea068-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ea068-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


