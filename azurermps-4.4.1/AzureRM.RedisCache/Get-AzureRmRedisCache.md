---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594184"
---
# <span data-ttu-id="c374f-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c374f-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="c374f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c374f-102">SYNOPSIS</span></span>
<span data-ttu-id="c374f-103">Redis Cache alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c374f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c374f-104">SYNTAX</span></span>

### <span data-ttu-id="c374f-105">Tüm abonelikte (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c374f-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c374f-106">Tümü kaynak grubunda</span><span class="sxs-lookup"><span data-stu-id="c374f-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c374f-107">Belirli bir Redis Cache</span><span class="sxs-lookup"><span data-stu-id="c374f-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c374f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c374f-108">DESCRIPTION</span></span>
<span data-ttu-id="c374f-109">**Get-AzureRmRedisCache** cmdlet 'i, belirtilen Azure Redis önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="c374f-110">Parametre belirtmezseniz, bu işlem geçerli aboneliğin tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="c374f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c374f-111">EXAMPLES</span></span>

### <span data-ttu-id="c374f-112">Örnek 1: ad ile kırmızı bir önbellek alma</span><span class="sxs-lookup"><span data-stu-id="c374f-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

          ResourceGroupName  : myGroup


          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}

          EnableNonSslPort   : False

          RedisVersion       : 2.8

          Size               : 1GB

          Sku                : Basic
```

<span data-ttu-id="c374f-113">Bu komut myexists adındaki Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="c374f-114">Örnek 2: kaynak grubundaki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="c374f-114">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

<span data-ttu-id="c374f-115">Bu komut, belirtilen kaynak grubundaki tüm kırmızı önbelleğe alma önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="c374f-116">Örnek 3: geçerli abonelikteki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="c374f-116">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard


          ResourceGroupName  : myGroup2
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
          Location           : North Central US
          Name               : myearlier2
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier2.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Basic
```

<span data-ttu-id="c374f-117">Bu komut geçerli abonelikteki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="c374f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c374f-118">PARAMETERS</span></span>

### <span data-ttu-id="c374f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c374f-119">-Name</span></span>
<span data-ttu-id="c374f-120">Alınacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c374f-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="c374f-121">*Resourcegroupname* parametresiyle kullanın.</span><span class="sxs-lookup"><span data-stu-id="c374f-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c374f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c374f-122">-ResourceGroupName</span></span>
<span data-ttu-id="c374f-123">Alınacak Redis Cache içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c374f-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="c374f-124">Yalnızca *Resourcegroupname* parametresini belirtirseniz, bu işlem belirtilen kaynak grubundaki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c374f-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c374f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c374f-125">-DefaultProfile</span></span>
<span data-ttu-id="c374f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c374f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c374f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c374f-127">CommonParameters</span></span>
<span data-ttu-id="c374f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c374f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c374f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c374f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c374f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c374f-130">INPUTS</span></span>

### <span data-ttu-id="c374f-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c374f-131">None</span></span>
<span data-ttu-id="c374f-132">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c374f-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="c374f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c374f-133">OUTPUTS</span></span>

### <span data-ttu-id="c374f-134">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="c374f-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="c374f-135">Bir **RedisCacheAttributes** nesneleri dizisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c374f-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="c374f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c374f-136">NOTES</span></span>

## <span data-ttu-id="c374f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c374f-137">RELATED LINKS</span></span>

[<span data-ttu-id="c374f-138">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c374f-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="c374f-139">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c374f-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="c374f-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="c374f-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


