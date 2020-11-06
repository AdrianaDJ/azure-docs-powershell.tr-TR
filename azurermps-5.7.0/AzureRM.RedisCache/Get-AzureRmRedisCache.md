---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589718"
---
# <span data-ttu-id="0310a-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0310a-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="0310a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0310a-102">SYNOPSIS</span></span>
<span data-ttu-id="0310a-103">Redis Cache alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0310a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0310a-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0310a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0310a-105">DESCRIPTION</span></span>
<span data-ttu-id="0310a-106">**Get-AzureRmRedisCache** cmdlet 'i, belirtilen Azure Redis önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="0310a-107">Parametre belirtmezseniz, bu işlem geçerli aboneliğin tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="0310a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0310a-108">EXAMPLES</span></span>

### <span data-ttu-id="0310a-109">Örnek 1: ad ile kırmızı bir önbellek alma</span><span class="sxs-lookup"><span data-stu-id="0310a-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

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
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="0310a-110">Bu komut myexists adındaki Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="0310a-111">Örnek 2: kaynak grubundaki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="0310a-111">Example 2: Get every Redis Cache in a resource group</span></span>
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
        Tag                : {}
        Zone               : []

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
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="0310a-112">Bu komut, belirtilen kaynak grubundaki tüm kırmızı önbelleğe alma önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="0310a-113">Örnek 3: geçerli abonelikteki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="0310a-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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
        Tag                : {}
        Zone               : []

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
        Tag                : {}
        Zone               : []

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
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="0310a-114">Bu komut geçerli abonelikteki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="0310a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0310a-115">PARAMETERS</span></span>

### <span data-ttu-id="0310a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0310a-116">-DefaultProfile</span></span>
<span data-ttu-id="0310a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0310a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0310a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0310a-118">-Name</span></span>
<span data-ttu-id="0310a-119">Alınacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0310a-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="0310a-120">*Resourcegroupname* parametresiyle kullanın.</span><span class="sxs-lookup"><span data-stu-id="0310a-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="0310a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0310a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0310a-122">Alınacak Redis Cache içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0310a-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="0310a-123">Yalnızca *Resourcegroupname* parametresini belirtirseniz, bu işlem belirtilen kaynak grubundaki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="0310a-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="0310a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0310a-124">CommonParameters</span></span>
<span data-ttu-id="0310a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0310a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0310a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0310a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0310a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0310a-127">INPUTS</span></span>

### <span data-ttu-id="0310a-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0310a-128">None</span></span>
<span data-ttu-id="0310a-129">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0310a-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="0310a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0310a-130">OUTPUTS</span></span>

### <span data-ttu-id="0310a-131">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="0310a-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="0310a-132">Bir **RedisCacheAttributes** nesneleri dizisi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0310a-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="0310a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0310a-133">NOTES</span></span>

## <span data-ttu-id="0310a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0310a-134">RELATED LINKS</span></span>

[<span data-ttu-id="0310a-135">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0310a-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="0310a-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0310a-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="0310a-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="0310a-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


