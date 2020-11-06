---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: ee4d5980743e5a78205c6e1f78cb55fa9b2f6496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593913"
---
# <span data-ttu-id="e00a3-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00a3-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="e00a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e00a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e00a3-103">Redis Cache alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e00a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e00a3-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e00a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e00a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e00a3-106">**Get-AzureRmRedisCache** cmdlet 'i, belirtilen Azure Redis önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="e00a3-107">Parametre belirtmezseniz, bu işlem geçerli aboneliğin tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="e00a3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e00a3-108">EXAMPLES</span></span>

### <span data-ttu-id="e00a3-109">Örnek 1: ad ile kırmızı bir önbellek alma</span><span class="sxs-lookup"><span data-stu-id="e00a3-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="e00a3-110">Bu komut myexists adındaki Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="e00a3-111">Örnek 2: kaynak grubundaki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="e00a3-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="e00a3-112">Bu komut, belirtilen kaynak grubundaki tüm kırmızı önbelleğe alma önbelleğini alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="e00a3-113">Örnek 3: geçerli abonelikteki her bir kırmızı önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="e00a3-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="e00a3-114">Bu komut geçerli abonelikteki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="e00a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e00a3-115">PARAMETERS</span></span>

### <span data-ttu-id="e00a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00a3-116">-DefaultProfile</span></span>
<span data-ttu-id="e00a3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e00a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e00a3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e00a3-118">-Name</span></span>
<span data-ttu-id="e00a3-119">Alınacak Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e00a3-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="e00a3-120">*Resourcegroupname* parametresiyle kullanın.</span><span class="sxs-lookup"><span data-stu-id="e00a3-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="e00a3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e00a3-121">-ResourceGroupName</span></span>
<span data-ttu-id="e00a3-122">Alınacak Redis Cache içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e00a3-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="e00a3-123">Yalnızca *Resourcegroupname* parametresini belirtirseniz, bu işlem belirtilen kaynak grubundaki tüm Redis Cache 'i alır.</span><span class="sxs-lookup"><span data-stu-id="e00a3-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="e00a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00a3-124">CommonParameters</span></span>
<span data-ttu-id="e00a3-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e00a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00a3-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e00a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00a3-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e00a3-127">INPUTS</span></span>

### <span data-ttu-id="e00a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e00a3-128">System.String</span></span>

## <span data-ttu-id="e00a3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e00a3-129">OUTPUTS</span></span>

### <span data-ttu-id="e00a3-130">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="e00a3-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="e00a3-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e00a3-131">NOTES</span></span>

## <span data-ttu-id="e00a3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e00a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="e00a3-133">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00a3-133">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e00a3-134">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00a3-134">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e00a3-135">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00a3-135">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


