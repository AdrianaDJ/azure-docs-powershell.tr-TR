---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588817"
---
# <span data-ttu-id="74fc6-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74fc6-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="74fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="74fc6-103">Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74fc6-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74fc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74fc6-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="74fc6-106">**Yeni-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74fc6-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="74fc6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="74fc6-108">Örnek 1: Redis Cache oluşturma</span><span class="sxs-lookup"><span data-stu-id="74fc6-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="74fc6-109">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74fc6-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="74fc6-110">Örnek 2: Standart SKU ön belleğini oluşturma</span><span class="sxs-lookup"><span data-stu-id="74fc6-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="74fc6-111">Bu komut, Redbir önbellek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74fc6-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="74fc6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74fc6-112">PARAMETERS</span></span>

### <span data-ttu-id="74fc6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fc6-113">-DefaultProfile</span></span>
<span data-ttu-id="74fc6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74fc6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fc6-115">-Enablen, SslPort</span><span class="sxs-lookup"><span data-stu-id="74fc6-115">-EnableNonSslPort</span></span>
<span data-ttu-id="74fc6-116">SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="74fc6-117">Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).</span><span class="sxs-lookup"><span data-stu-id="74fc6-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="74fc6-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="74fc6-118">-Location</span></span>
<span data-ttu-id="74fc6-119">Redis önbelleğinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="74fc6-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="74fc6-120">Valid values are:</span></span> 

- <span data-ttu-id="74fc6-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="74fc6-121">North Central US</span></span>
- <span data-ttu-id="74fc6-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="74fc6-122">South Central US</span></span>
- <span data-ttu-id="74fc6-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="74fc6-123">Central US</span></span>
- <span data-ttu-id="74fc6-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="74fc6-124">West Europe</span></span>
- <span data-ttu-id="74fc6-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="74fc6-125">North Europe</span></span>
- <span data-ttu-id="74fc6-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="74fc6-126">West US</span></span>
- <span data-ttu-id="74fc6-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="74fc6-127">East US</span></span>
- <span data-ttu-id="74fc6-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="74fc6-128">East US 2</span></span>
- <span data-ttu-id="74fc6-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="74fc6-129">Japan East</span></span>
- <span data-ttu-id="74fc6-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="74fc6-130">Japan West</span></span>
- <span data-ttu-id="74fc6-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="74fc6-131">Brazil South</span></span>
- <span data-ttu-id="74fc6-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="74fc6-132">Southeast Asia</span></span>
- <span data-ttu-id="74fc6-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="74fc6-133">East Asia</span></span>
- <span data-ttu-id="74fc6-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="74fc6-134">Australia East</span></span>
- <span data-ttu-id="74fc6-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="74fc6-135">Australia Southeast</span></span>

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

### <span data-ttu-id="74fc6-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="74fc6-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="74fc6-137">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="74fc6-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="74fc6-138">MaxMemory-ilkesini ayarlamak için *Redisconfiguration* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="74fc6-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="74fc6-139">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="74fc6-139">For example:</span></span> 

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

### <span data-ttu-id="74fc6-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="74fc6-140">-Name</span></span>
<span data-ttu-id="74fc6-141">Oluşturulacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="74fc6-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="74fc6-142">-RedisConfiguration</span></span>
<span data-ttu-id="74fc6-143">Redis yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="74fc6-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="74fc6-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74fc6-145">RDB-yedekleme etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="74fc6-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="74fc6-146">Veri kalıcılığını etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="74fc6-147">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="74fc6-147">Premium tier only.</span></span>
- <span data-ttu-id="74fc6-148">RDB-depolama-bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="74fc6-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="74fc6-149">Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="74fc6-150">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="74fc6-150">Premium tier only.</span></span>
- <span data-ttu-id="74fc6-151">RDB-yedekleme-frekans.</span><span class="sxs-lookup"><span data-stu-id="74fc6-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="74fc6-152">Redis veri kalıcılığı için yedekleme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="74fc6-153">Yalnızca Premium katman.</span><span class="sxs-lookup"><span data-stu-id="74fc6-153">Premium tier only.</span></span> 
- <span data-ttu-id="74fc6-154">MaxMemory-ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="74fc6-154">maxmemory-reserved.</span></span>
<span data-ttu-id="74fc6-155">Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="74fc6-156">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-157">MaxMemory-ilke.</span><span class="sxs-lookup"><span data-stu-id="74fc6-157">maxmemory-policy.</span></span>
<span data-ttu-id="74fc6-158">Önbellek için çıkarma ilkesini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="74fc6-159">Tüm fiyatlandırma katmanları.</span><span class="sxs-lookup"><span data-stu-id="74fc6-159">All pricing tiers.</span></span> 
- <span data-ttu-id="74fc6-160">Notify-anahtar uzayı-olaylar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-160">notify-keyspace-events.</span></span>
<span data-ttu-id="74fc6-161">Anahtar alanı bildirimlerini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="74fc6-162">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="74fc6-163">Hash-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="74fc6-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="74fc6-164">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="74fc6-165">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-166">Hash-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="74fc6-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="74fc6-167">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="74fc6-168">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-169">Set-Max-ıntset-Entries.</span><span class="sxs-lookup"><span data-stu-id="74fc6-169">set-max-intset-entries.</span></span>
<span data-ttu-id="74fc6-170">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="74fc6-171">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-172">zset-Max-ZipList-Entries.</span><span class="sxs-lookup"><span data-stu-id="74fc6-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="74fc6-173">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="74fc6-174">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-175">zset-Max-ZipList-değer.</span><span class="sxs-lookup"><span data-stu-id="74fc6-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="74fc6-176">Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="74fc6-177">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="74fc6-178">Databases.</span><span class="sxs-lookup"><span data-stu-id="74fc6-178">databases.</span></span>
<span data-ttu-id="74fc6-179">Veritabanlarının sayısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-179">Configures the number of databases.</span></span>
<span data-ttu-id="74fc6-180">Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="74fc6-181">Standart ve Premium katmanlar.</span><span class="sxs-lookup"><span data-stu-id="74fc6-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="74fc6-182">Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="74fc6-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="74fc6-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="74fc6-183">-RedisVersion</span></span>
<span data-ttu-id="74fc6-184">Bu parametre kullanım dışıdır ve ileriki sürümlerden kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="74fc6-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74fc6-185">-ResourceGroupName</span></span>
<span data-ttu-id="74fc6-186">Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="74fc6-187">-Shardsay</span><span class="sxs-lookup"><span data-stu-id="74fc6-187">-ShardCount</span></span>
<span data-ttu-id="74fc6-188">Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="74fc6-189">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="74fc6-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74fc6-190">2</span><span class="sxs-lookup"><span data-stu-id="74fc6-190">1</span></span>
- <span data-ttu-id="74fc6-191">2</span><span class="sxs-lookup"><span data-stu-id="74fc6-191">2</span></span>
- <span data-ttu-id="74fc6-192">@</span><span class="sxs-lookup"><span data-stu-id="74fc6-192">3</span></span>
- <span data-ttu-id="74fc6-193">1.921.024</span><span class="sxs-lookup"><span data-stu-id="74fc6-193">4</span></span>
- <span data-ttu-id="74fc6-194">tir</span><span class="sxs-lookup"><span data-stu-id="74fc6-194">5</span></span>
- <span data-ttu-id="74fc6-195">+</span><span class="sxs-lookup"><span data-stu-id="74fc6-195">6</span></span>
- <span data-ttu-id="74fc6-196">+</span><span class="sxs-lookup"><span data-stu-id="74fc6-196">7</span></span>
- <span data-ttu-id="74fc6-197">8@@</span><span class="sxs-lookup"><span data-stu-id="74fc6-197">8</span></span>
- <span data-ttu-id="74fc6-198">döndürdü</span><span class="sxs-lookup"><span data-stu-id="74fc6-198">9</span></span> 
- <span data-ttu-id="74fc6-199">on</span><span class="sxs-lookup"><span data-stu-id="74fc6-199">10</span></span>

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

### <span data-ttu-id="74fc6-200">-Boyut</span><span class="sxs-lookup"><span data-stu-id="74fc6-200">-Size</span></span>
<span data-ttu-id="74fc6-201">Redis önbelleğinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="74fc6-202">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="74fc6-202">Valid values are:</span></span> 

- <span data-ttu-id="74fc6-203">P1</span><span class="sxs-lookup"><span data-stu-id="74fc6-203">P1</span></span>
- <span data-ttu-id="74fc6-204">P2</span><span class="sxs-lookup"><span data-stu-id="74fc6-204">P2</span></span>
- <span data-ttu-id="74fc6-205">P3</span><span class="sxs-lookup"><span data-stu-id="74fc6-205">P3</span></span>
- <span data-ttu-id="74fc6-206">P4</span><span class="sxs-lookup"><span data-stu-id="74fc6-206">P4</span></span>
- <span data-ttu-id="74fc6-207">C0</span><span class="sxs-lookup"><span data-stu-id="74fc6-207">C0</span></span>
- <span data-ttu-id="74fc6-208">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="74fc6-208">C1</span></span>
- <span data-ttu-id="74fc6-209">İşlemcinin</span><span class="sxs-lookup"><span data-stu-id="74fc6-209">C2</span></span>
- <span data-ttu-id="74fc6-210">C3</span><span class="sxs-lookup"><span data-stu-id="74fc6-210">C3</span></span>
- <span data-ttu-id="74fc6-211">C4</span><span class="sxs-lookup"><span data-stu-id="74fc6-211">C4</span></span>
- <span data-ttu-id="74fc6-212">C5</span><span class="sxs-lookup"><span data-stu-id="74fc6-212">C5</span></span>
- <span data-ttu-id="74fc6-213">C6</span><span class="sxs-lookup"><span data-stu-id="74fc6-213">C6</span></span>
- <span data-ttu-id="74fc6-214">250MB</span><span class="sxs-lookup"><span data-stu-id="74fc6-214">250MB</span></span>
- <span data-ttu-id="74fc6-215">1GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-215">1GB</span></span>
- <span data-ttu-id="74fc6-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-216">2.5GB</span></span>
- <span data-ttu-id="74fc6-217">6GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-217">6GB</span></span>
- <span data-ttu-id="74fc6-218">13GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-218">13GB</span></span>
- <span data-ttu-id="74fc6-219">26GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-219">26GB</span></span>
- <span data-ttu-id="74fc6-220">53GB</span><span class="sxs-lookup"><span data-stu-id="74fc6-220">53GB</span></span>

<span data-ttu-id="74fc6-221">Varsayılan değer 1GB veya C1.</span><span class="sxs-lookup"><span data-stu-id="74fc6-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="74fc6-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="74fc6-222">-Sku</span></span>
<span data-ttu-id="74fc6-223">Oluşturulacak Redis önbelleğinin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="74fc6-224">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="74fc6-224">Valid values are:</span></span> 

- <span data-ttu-id="74fc6-225">Ana</span><span class="sxs-lookup"><span data-stu-id="74fc6-225">Basic</span></span>
- <span data-ttu-id="74fc6-226">Ardından</span><span class="sxs-lookup"><span data-stu-id="74fc6-226">Standard</span></span>
- <span data-ttu-id="74fc6-227">Min</span><span class="sxs-lookup"><span data-stu-id="74fc6-227">Premium</span></span>

<span data-ttu-id="74fc6-228">Varsayılan değer standarttır.</span><span class="sxs-lookup"><span data-stu-id="74fc6-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="74fc6-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="74fc6-229">-StaticIP</span></span>
<span data-ttu-id="74fc6-230">Redis Cache için alt ağda benzersiz bir IP adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="74fc6-231">Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.</span><span class="sxs-lookup"><span data-stu-id="74fc6-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="74fc6-232">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="74fc6-232">-Subnet</span></span>
<span data-ttu-id="74fc6-233">Redis önbelleğinin dağıtılacağı alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="74fc6-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="74fc6-234">-SubnetId</span></span>
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

### <span data-ttu-id="74fc6-235">Etiketli</span><span class="sxs-lookup"><span data-stu-id="74fc6-235">-Tag</span></span>
<span data-ttu-id="74fc6-236">Etiketleri temsil eden karma tablo.</span><span class="sxs-lookup"><span data-stu-id="74fc6-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="74fc6-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="74fc6-237">-TenantSettings</span></span>
<span data-ttu-id="74fc6-238">Bu parametre kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="74fc6-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="74fc6-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="74fc6-239">-VirtualNetwork</span></span>
<span data-ttu-id="74fc6-240">Redis önbelleğinin dağıtılacağı sanal ağın kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="74fc6-241">-Bölge</span><span class="sxs-lookup"><span data-stu-id="74fc6-241">-Zone</span></span>
<span data-ttu-id="74fc6-242">Bölgeler listesi.</span><span class="sxs-lookup"><span data-stu-id="74fc6-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74fc6-243">-Onay</span><span class="sxs-lookup"><span data-stu-id="74fc6-243">-Confirm</span></span>
<span data-ttu-id="74fc6-244">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74fc6-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74fc6-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fc6-245">-WhatIf</span></span>
<span data-ttu-id="74fc6-246">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74fc6-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74fc6-247">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74fc6-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74fc6-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fc6-248">CommonParameters</span></span>
<span data-ttu-id="74fc6-249">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74fc6-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fc6-250">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fc6-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fc6-251">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74fc6-251">INPUTS</span></span>

### <span data-ttu-id="74fc6-252">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="74fc6-252">None</span></span>
<span data-ttu-id="74fc6-253">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74fc6-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="74fc6-254">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74fc6-254">OUTPUTS</span></span>

### <span data-ttu-id="74fc6-255">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="74fc6-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="74fc6-256">Bu cmdlet, birincil ve ikincil erişim tuşları gibi bir kırmızı tür önbelleğinin tüm özniteliklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="74fc6-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="74fc6-257">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74fc6-257">NOTES</span></span>

## <span data-ttu-id="74fc6-258">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74fc6-258">RELATED LINKS</span></span>

[<span data-ttu-id="74fc6-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74fc6-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="74fc6-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74fc6-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="74fc6-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74fc6-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


