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
ms.locfileid: "93932941"
---
# <span data-ttu-id="30e79-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="30e79-101">New-AzRedisCache</span></span>

## <span data-ttu-id="30e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e79-102">SYNOPSIS</span></span>
<span data-ttu-id="30e79-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30e79-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="30e79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30e79-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30e79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30e79-105">DESCRIPTION</span></span>
<span data-ttu-id="30e79-106">**Yeni-AzRedisCache** cmdlet 'ı Azure Redis önbelleği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30e79-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="30e79-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30e79-107">EXAMPLES</span></span>

### <span data-ttu-id="30e79-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="30e79-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="30e79-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30e79-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="30e79-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="30e79-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="30e79-111">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30e79-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="30e79-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30e79-112">PARAMETERS</span></span>

### <span data-ttu-id="30e79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e79-113">-DefaultProfile</span></span>
<span data-ttu-id="30e79-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30e79-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e79-115">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="30e79-115">-EnableNonSslPort</span></span>
<span data-ttu-id="30e79-116">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="30e79-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="30e79-117">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="30e79-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="30e79-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="30e79-118">-Location</span></span>
<span data-ttu-id="30e79-119">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="30e79-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="30e79-120">Valid values are:</span></span> 
- <span data-ttu-id="30e79-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="30e79-121">North Central US</span></span>
- <span data-ttu-id="30e79-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="30e79-122">South Central US</span></span>
- <span data-ttu-id="30e79-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="30e79-123">Central US</span></span>
- <span data-ttu-id="30e79-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="30e79-124">West Europe</span></span>
- <span data-ttu-id="30e79-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="30e79-125">North Europe</span></span>
- <span data-ttu-id="30e79-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="30e79-126">West US</span></span>
- <span data-ttu-id="30e79-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="30e79-127">East US</span></span>
- <span data-ttu-id="30e79-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="30e79-128">East US 2</span></span>
- <span data-ttu-id="30e79-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="30e79-129">Japan East</span></span>
- <span data-ttu-id="30e79-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="30e79-130">Japan West</span></span>
- <span data-ttu-id="30e79-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="30e79-131">Brazil South</span></span>
- <span data-ttu-id="30e79-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="30e79-132">Southeast Asia</span></span>
- <span data-ttu-id="30e79-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="30e79-133">East Asia</span></span>
- <span data-ttu-id="30e79-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="30e79-134">Australia East</span></span>
- <span data-ttu-id="30e79-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="30e79-135">Australia Southeast</span></span>

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

### <span data-ttu-id="30e79-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="30e79-136">-Name</span></span>
<span data-ttu-id="30e79-137">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="30e79-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="30e79-138">-RedisConfiguration</span></span>
<span data-ttu-id="30e79-139">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="30e79-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="30e79-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30e79-141">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="30e79-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="30e79-142">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="30e79-143">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="30e79-143">Premium tier only.</span></span>
- <span data-ttu-id="30e79-144">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="30e79-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="30e79-145">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="30e79-146">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="30e79-146">Premium tier only.</span></span>
- <span data-ttu-id="30e79-147">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="30e79-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="30e79-148">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="30e79-149">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="30e79-149">Premium tier only.</span></span> 
- <span data-ttu-id="30e79-150">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="30e79-150">maxmemory-reserved.</span></span>
<span data-ttu-id="30e79-151">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="30e79-152">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-153">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="30e79-153">maxmemory-policy.</span></span>
<span data-ttu-id="30e79-154">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="30e79-155">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="30e79-155">All pricing tiers.</span></span> 
- <span data-ttu-id="30e79-156">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="30e79-156">notify-keyspace-events.</span></span>
<span data-ttu-id="30e79-157">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="30e79-158">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="30e79-159">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="30e79-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="30e79-160">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="30e79-161">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-162">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="30e79-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="30e79-163">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="30e79-164">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-165">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="30e79-165">set-max-intset-entries.</span></span>
<span data-ttu-id="30e79-166">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="30e79-167">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-168">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="30e79-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="30e79-169">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="30e79-170">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-171">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="30e79-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="30e79-172">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="30e79-173">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="30e79-174">Databases.</span><span class="sxs-lookup"><span data-stu-id="30e79-174">databases.</span></span>
<span data-ttu-id="30e79-175">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="30e79-175">Configures the number of databases.</span></span>
<span data-ttu-id="30e79-176">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="30e79-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="30e79-177">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="30e79-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="30e79-178">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="30e79-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="30e79-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e79-179">-ResourceGroupName</span></span>
<span data-ttu-id="30e79-180">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="30e79-181">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="30e79-181">-ShardCount</span></span>
<span data-ttu-id="30e79-182">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="30e79-183">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="30e79-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30e79-184">2</span><span class="sxs-lookup"><span data-stu-id="30e79-184">1</span></span>
- <span data-ttu-id="30e79-185">2</span><span class="sxs-lookup"><span data-stu-id="30e79-185">2</span></span>
- <span data-ttu-id="30e79-186">@</span><span class="sxs-lookup"><span data-stu-id="30e79-186">3</span></span>
- <span data-ttu-id="30e79-187">1.921.024</span><span class="sxs-lookup"><span data-stu-id="30e79-187">4</span></span>
- <span data-ttu-id="30e79-188">tir</span><span class="sxs-lookup"><span data-stu-id="30e79-188">5</span></span>
- <span data-ttu-id="30e79-189">+</span><span class="sxs-lookup"><span data-stu-id="30e79-189">6</span></span>
- <span data-ttu-id="30e79-190">+</span><span class="sxs-lookup"><span data-stu-id="30e79-190">7</span></span>
- <span data-ttu-id="30e79-191">8@@</span><span class="sxs-lookup"><span data-stu-id="30e79-191">8</span></span>
- <span data-ttu-id="30e79-192">döndürdü</span><span class="sxs-lookup"><span data-stu-id="30e79-192">9</span></span> 
- <span data-ttu-id="30e79-193">on</span><span class="sxs-lookup"><span data-stu-id="30e79-193">10</span></span>

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

### <span data-ttu-id="30e79-194">-Boyut</span><span class="sxs-lookup"><span data-stu-id="30e79-194">-Size</span></span>
<span data-ttu-id="30e79-195">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="30e79-196">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="30e79-196">Valid values are:</span></span> 
- <span data-ttu-id="30e79-197">P1</span><span class="sxs-lookup"><span data-stu-id="30e79-197">P1</span></span>
- <span data-ttu-id="30e79-198">P2</span><span class="sxs-lookup"><span data-stu-id="30e79-198">P2</span></span>
- <span data-ttu-id="30e79-199">P3</span><span class="sxs-lookup"><span data-stu-id="30e79-199">P3</span></span>
- <span data-ttu-id="30e79-200">P4</span><span class="sxs-lookup"><span data-stu-id="30e79-200">P4</span></span>
- <span data-ttu-id="30e79-201">C0</span><span class="sxs-lookup"><span data-stu-id="30e79-201">C0</span></span>
- <span data-ttu-id="30e79-202">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="30e79-202">C1</span></span>
- <span data-ttu-id="30e79-203">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="30e79-203">C2</span></span>
- <span data-ttu-id="30e79-204">C3</span><span class="sxs-lookup"><span data-stu-id="30e79-204">C3</span></span>
- <span data-ttu-id="30e79-205">C4</span><span class="sxs-lookup"><span data-stu-id="30e79-205">C4</span></span>
- <span data-ttu-id="30e79-206">C5</span><span class="sxs-lookup"><span data-stu-id="30e79-206">C5</span></span>
- <span data-ttu-id="30e79-207">C6</span><span class="sxs-lookup"><span data-stu-id="30e79-207">C6</span></span>
- <span data-ttu-id="30e79-208">250MB</span><span class="sxs-lookup"><span data-stu-id="30e79-208">250MB</span></span>
- <span data-ttu-id="30e79-209">1GB</span><span class="sxs-lookup"><span data-stu-id="30e79-209">1GB</span></span>
- <span data-ttu-id="30e79-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="30e79-210">2.5GB</span></span>
- <span data-ttu-id="30e79-211">6GB</span><span class="sxs-lookup"><span data-stu-id="30e79-211">6GB</span></span>
- <span data-ttu-id="30e79-212">13GB</span><span class="sxs-lookup"><span data-stu-id="30e79-212">13GB</span></span>
- <span data-ttu-id="30e79-213">26GB</span><span class="sxs-lookup"><span data-stu-id="30e79-213">26GB</span></span>
- <span data-ttu-id="30e79-214">53GB varsayılan değer 1GB veya C1 'dır.</span><span class="sxs-lookup"><span data-stu-id="30e79-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="30e79-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="30e79-215">-Sku</span></span>
<span data-ttu-id="30e79-216">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="30e79-217">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="30e79-217">Valid values are:</span></span> 
- <span data-ttu-id="30e79-218">Ana</span><span class="sxs-lookup"><span data-stu-id="30e79-218">Basic</span></span>
- <span data-ttu-id="30e79-219">Ardından</span><span class="sxs-lookup"><span data-stu-id="30e79-219">Standard</span></span>
- <span data-ttu-id="30e79-220">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="30e79-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="30e79-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="30e79-221">-StaticIP</span></span>
<span data-ttu-id="30e79-222">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e79-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="30e79-223">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="30e79-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="30e79-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="30e79-224">-SubnetId</span></span>
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

### <span data-ttu-id="30e79-225">Etiketli</span><span class="sxs-lookup"><span data-stu-id="30e79-225">-Tag</span></span>
<span data-ttu-id="30e79-226">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="30e79-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="30e79-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="30e79-227">-TenantSettings</span></span>
<span data-ttu-id="30e79-228">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="30e79-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="30e79-229">-Bölge</span><span class="sxs-lookup"><span data-stu-id="30e79-229">-Zone</span></span>
<span data-ttu-id="30e79-230">Bölgeler listesi.</span><span class="sxs-lookup"><span data-stu-id="30e79-230">List of zones.</span></span>

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

### <span data-ttu-id="30e79-231">-Onay</span><span class="sxs-lookup"><span data-stu-id="30e79-231">-Confirm</span></span>
<span data-ttu-id="30e79-232">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30e79-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e79-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e79-233">-WhatIf</span></span>
<span data-ttu-id="30e79-234">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30e79-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30e79-235">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30e79-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e79-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e79-236">CommonParameters</span></span>
<span data-ttu-id="30e79-237">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30e79-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e79-238">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e79-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e79-239">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30e79-239">INPUTS</span></span>

### <span data-ttu-id="30e79-240">System. String</span><span class="sxs-lookup"><span data-stu-id="30e79-240">System.String</span></span>

### <span data-ttu-id="30e79-241">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="30e79-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="30e79-242">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="30e79-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30e79-243">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="30e79-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30e79-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="30e79-244">System.String[]</span></span>

## <span data-ttu-id="30e79-245">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30e79-245">OUTPUTS</span></span>

### <span data-ttu-id="30e79-246">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="30e79-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="30e79-247">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30e79-247">NOTES</span></span>

## <span data-ttu-id="30e79-248">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30e79-248">RELATED LINKS</span></span>

[<span data-ttu-id="30e79-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="30e79-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="30e79-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="30e79-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="30e79-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="30e79-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


