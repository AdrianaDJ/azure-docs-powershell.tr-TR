---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763441"
---
# <span data-ttu-id="14719-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="14719-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="14719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14719-102">SYNOPSIS</span></span>
<span data-ttu-id="14719-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14719-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14719-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14719-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14719-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14719-105">DESCRIPTION</span></span>
<span data-ttu-id="14719-106">**Yeni-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14719-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="14719-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14719-107">EXAMPLES</span></span>

### <span data-ttu-id="14719-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="14719-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="14719-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14719-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="14719-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="14719-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="14719-111">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14719-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="14719-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14719-112">PARAMETERS</span></span>

### <span data-ttu-id="14719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14719-113">-DefaultProfile</span></span>
<span data-ttu-id="14719-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14719-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14719-115">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="14719-115">-EnableNonSslPort</span></span>
<span data-ttu-id="14719-116">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="14719-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="14719-117">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="14719-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="14719-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="14719-118">-Location</span></span>
<span data-ttu-id="14719-119">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="14719-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="14719-120">Valid values are:</span></span> 
- <span data-ttu-id="14719-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="14719-121">North Central US</span></span>
- <span data-ttu-id="14719-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="14719-122">South Central US</span></span>
- <span data-ttu-id="14719-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="14719-123">Central US</span></span>
- <span data-ttu-id="14719-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="14719-124">West Europe</span></span>
- <span data-ttu-id="14719-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="14719-125">North Europe</span></span>
- <span data-ttu-id="14719-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="14719-126">West US</span></span>
- <span data-ttu-id="14719-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="14719-127">East US</span></span>
- <span data-ttu-id="14719-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="14719-128">East US 2</span></span>
- <span data-ttu-id="14719-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="14719-129">Japan East</span></span>
- <span data-ttu-id="14719-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="14719-130">Japan West</span></span>
- <span data-ttu-id="14719-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="14719-131">Brazil South</span></span>
- <span data-ttu-id="14719-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="14719-132">Southeast Asia</span></span>
- <span data-ttu-id="14719-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="14719-133">East Asia</span></span>
- <span data-ttu-id="14719-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="14719-134">Australia East</span></span>
- <span data-ttu-id="14719-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="14719-135">Australia Southeast</span></span>

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

### <span data-ttu-id="14719-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="14719-136">-Name</span></span>
<span data-ttu-id="14719-137">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="14719-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="14719-138">-RedisConfiguration</span></span>
<span data-ttu-id="14719-139">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="14719-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14719-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14719-141">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="14719-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="14719-142">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="14719-143">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="14719-143">Premium tier only.</span></span>
- <span data-ttu-id="14719-144">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="14719-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="14719-145">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="14719-146">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="14719-146">Premium tier only.</span></span>
- <span data-ttu-id="14719-147">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="14719-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="14719-148">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="14719-149">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="14719-149">Premium tier only.</span></span> 
- <span data-ttu-id="14719-150">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="14719-150">maxmemory-reserved.</span></span>
<span data-ttu-id="14719-151">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="14719-152">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-153">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="14719-153">maxmemory-policy.</span></span>
<span data-ttu-id="14719-154">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="14719-155">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="14719-155">All pricing tiers.</span></span> 
- <span data-ttu-id="14719-156">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="14719-156">notify-keyspace-events.</span></span>
<span data-ttu-id="14719-157">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="14719-158">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="14719-159">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="14719-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="14719-160">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="14719-161">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-162">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="14719-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="14719-163">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="14719-164">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-165">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="14719-165">set-max-intset-entries.</span></span>
<span data-ttu-id="14719-166">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="14719-167">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-168">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="14719-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="14719-169">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="14719-170">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-171">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="14719-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="14719-172">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="14719-173">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="14719-174">Databases.</span><span class="sxs-lookup"><span data-stu-id="14719-174">databases.</span></span>
<span data-ttu-id="14719-175">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="14719-175">Configures the number of databases.</span></span>
<span data-ttu-id="14719-176">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="14719-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="14719-177">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="14719-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="14719-178">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="14719-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="14719-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14719-179">-ResourceGroupName</span></span>
<span data-ttu-id="14719-180">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="14719-181">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="14719-181">-ShardCount</span></span>
<span data-ttu-id="14719-182">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="14719-183">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="14719-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="14719-184">2</span><span class="sxs-lookup"><span data-stu-id="14719-184">1</span></span>
- <span data-ttu-id="14719-185">2</span><span class="sxs-lookup"><span data-stu-id="14719-185">2</span></span>
- <span data-ttu-id="14719-186">@</span><span class="sxs-lookup"><span data-stu-id="14719-186">3</span></span>
- <span data-ttu-id="14719-187">1.921.024</span><span class="sxs-lookup"><span data-stu-id="14719-187">4</span></span>
- <span data-ttu-id="14719-188">tir</span><span class="sxs-lookup"><span data-stu-id="14719-188">5</span></span>
- <span data-ttu-id="14719-189">+</span><span class="sxs-lookup"><span data-stu-id="14719-189">6</span></span>
- <span data-ttu-id="14719-190">+</span><span class="sxs-lookup"><span data-stu-id="14719-190">7</span></span>
- <span data-ttu-id="14719-191">8@@</span><span class="sxs-lookup"><span data-stu-id="14719-191">8</span></span>
- <span data-ttu-id="14719-192">döndürdü</span><span class="sxs-lookup"><span data-stu-id="14719-192">9</span></span> 
- <span data-ttu-id="14719-193">on</span><span class="sxs-lookup"><span data-stu-id="14719-193">10</span></span>

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

### <span data-ttu-id="14719-194">-Boyut</span><span class="sxs-lookup"><span data-stu-id="14719-194">-Size</span></span>
<span data-ttu-id="14719-195">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="14719-196">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="14719-196">Valid values are:</span></span> 
- <span data-ttu-id="14719-197">P1</span><span class="sxs-lookup"><span data-stu-id="14719-197">P1</span></span>
- <span data-ttu-id="14719-198">P2</span><span class="sxs-lookup"><span data-stu-id="14719-198">P2</span></span>
- <span data-ttu-id="14719-199">P3</span><span class="sxs-lookup"><span data-stu-id="14719-199">P3</span></span>
- <span data-ttu-id="14719-200">P4</span><span class="sxs-lookup"><span data-stu-id="14719-200">P4</span></span>
- <span data-ttu-id="14719-201">C0</span><span class="sxs-lookup"><span data-stu-id="14719-201">C0</span></span>
- <span data-ttu-id="14719-202">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="14719-202">C1</span></span>
- <span data-ttu-id="14719-203">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="14719-203">C2</span></span>
- <span data-ttu-id="14719-204">C3</span><span class="sxs-lookup"><span data-stu-id="14719-204">C3</span></span>
- <span data-ttu-id="14719-205">C4</span><span class="sxs-lookup"><span data-stu-id="14719-205">C4</span></span>
- <span data-ttu-id="14719-206">C5</span><span class="sxs-lookup"><span data-stu-id="14719-206">C5</span></span>
- <span data-ttu-id="14719-207">C6</span><span class="sxs-lookup"><span data-stu-id="14719-207">C6</span></span>
- <span data-ttu-id="14719-208">250MB</span><span class="sxs-lookup"><span data-stu-id="14719-208">250MB</span></span>
- <span data-ttu-id="14719-209">1GB</span><span class="sxs-lookup"><span data-stu-id="14719-209">1GB</span></span>
- <span data-ttu-id="14719-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="14719-210">2.5GB</span></span>
- <span data-ttu-id="14719-211">6GB</span><span class="sxs-lookup"><span data-stu-id="14719-211">6GB</span></span>
- <span data-ttu-id="14719-212">13GB</span><span class="sxs-lookup"><span data-stu-id="14719-212">13GB</span></span>
- <span data-ttu-id="14719-213">26GB</span><span class="sxs-lookup"><span data-stu-id="14719-213">26GB</span></span>
- <span data-ttu-id="14719-214">53GB varsayılan değer 1GB veya C1 'dır.</span><span class="sxs-lookup"><span data-stu-id="14719-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="14719-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="14719-215">-Sku</span></span>
<span data-ttu-id="14719-216">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="14719-217">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="14719-217">Valid values are:</span></span> 
- <span data-ttu-id="14719-218">Ana</span><span class="sxs-lookup"><span data-stu-id="14719-218">Basic</span></span>
- <span data-ttu-id="14719-219">Ardından</span><span class="sxs-lookup"><span data-stu-id="14719-219">Standard</span></span>
- <span data-ttu-id="14719-220">Premium varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="14719-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="14719-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="14719-221">-StaticIP</span></span>
<span data-ttu-id="14719-222">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="14719-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="14719-223">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="14719-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="14719-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="14719-224">-SubnetId</span></span>
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

### <span data-ttu-id="14719-225">Etiketli</span><span class="sxs-lookup"><span data-stu-id="14719-225">-Tag</span></span>
<span data-ttu-id="14719-226">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="14719-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="14719-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="14719-227">-TenantSettings</span></span>
<span data-ttu-id="14719-228">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="14719-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="14719-229">-Bölge</span><span class="sxs-lookup"><span data-stu-id="14719-229">-Zone</span></span>
<span data-ttu-id="14719-230">Bölgeler listesi.</span><span class="sxs-lookup"><span data-stu-id="14719-230">List of zones.</span></span>

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

### <span data-ttu-id="14719-231">-Onay</span><span class="sxs-lookup"><span data-stu-id="14719-231">-Confirm</span></span>
<span data-ttu-id="14719-232">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14719-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14719-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14719-233">-WhatIf</span></span>
<span data-ttu-id="14719-234">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14719-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14719-235">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14719-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14719-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14719-236">CommonParameters</span></span>
<span data-ttu-id="14719-237">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14719-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14719-238">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14719-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14719-239">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14719-239">INPUTS</span></span>

### <span data-ttu-id="14719-240">System. String</span><span class="sxs-lookup"><span data-stu-id="14719-240">System.String</span></span>

### <span data-ttu-id="14719-241">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="14719-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="14719-242">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14719-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="14719-243">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14719-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="14719-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="14719-244">System.String[]</span></span>

## <span data-ttu-id="14719-245">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14719-245">OUTPUTS</span></span>

### <span data-ttu-id="14719-246">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="14719-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="14719-247">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14719-247">NOTES</span></span>

## <span data-ttu-id="14719-248">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14719-248">RELATED LINKS</span></span>

[<span data-ttu-id="14719-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="14719-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="14719-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="14719-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="14719-251">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="14719-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


