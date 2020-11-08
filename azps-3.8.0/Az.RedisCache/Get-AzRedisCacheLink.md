---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103565"
---
# <span data-ttu-id="dca6c-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="dca6c-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="dca6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca6c-102">SYNOPSIS</span></span>
<span data-ttu-id="dca6c-103">Redis Cache için coğrafi çoğaltma bağlantısı alın.</span><span class="sxs-lookup"><span data-stu-id="dca6c-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="dca6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dca6c-104">SYNTAX</span></span>

### <span data-ttu-id="dca6c-105">AllLinksForCache (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dca6c-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dca6c-106">Alllinkforprimarycache</span><span class="sxs-lookup"><span data-stu-id="dca6c-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dca6c-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="dca6c-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dca6c-108">Alllinkforsecondarycache</span><span class="sxs-lookup"><span data-stu-id="dca6c-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dca6c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dca6c-109">DESCRIPTION</span></span>
<span data-ttu-id="dca6c-110">Coğrafi çoğaltma bağlantı ayrıntısı almanın dört farklı yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="dca6c-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="dca6c-111">Parametre adı veya PrimaryServerName ve/veya SecondaryServerName sağlayın.</span><span class="sxs-lookup"><span data-stu-id="dca6c-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="dca6c-112">Ad verilirse, önbelleğin var olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="dca6c-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="dca6c-113">Yalnızca PrimaryServerName verilirse, önbelleğin birincili olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="dca6c-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="dca6c-114">Yalnızca SecondaryServerName etkinleştirilirse önbelleğin ikincil olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="dca6c-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="dca6c-115">PrimaryServerName ve SecondaryServerName her ikisi de verilirse, doğru role sahip belirli bir bağlantı döndürülür.</span><span class="sxs-lookup"><span data-stu-id="dca6c-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="dca6c-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dca6c-116">EXAMPLES</span></span>

### <span data-ttu-id="dca6c-117">Örnek 1: AllLinksForCache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="dca6c-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="dca6c-118">Bu komut, myCache1 adlı Red, Cache için tüm coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dca6c-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="dca6c-119">Örnek 2: Alllinkforprimarycache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="dca6c-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="dca6c-120">Bu komut, myCache1 adındaki Redis önbelleğinin birincili coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dca6c-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="dca6c-121">Örnek 3: Alllinkforsecondarycache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="dca6c-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="dca6c-122">Bu komut, mycache2 adındaki Redis önbelleğinin ikincili coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dca6c-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="dca6c-123">Örnek 4: parametre kümesi SingleLink kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="dca6c-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="dca6c-124">Bu komut, myCache1 adındaki Redis önbelleğinin birincil ve mycache2 adındaki Redis Cache olan tek bir coğrafi çoğaltma bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="dca6c-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="dca6c-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dca6c-125">PARAMETERS</span></span>

### <span data-ttu-id="dca6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca6c-126">-DefaultProfile</span></span>
<span data-ttu-id="dca6c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dca6c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca6c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="dca6c-128">-Name</span></span>
<span data-ttu-id="dca6c-129">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dca6c-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca6c-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="dca6c-130">-PrimaryServerName</span></span>
<span data-ttu-id="dca6c-131">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dca6c-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca6c-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="dca6c-132">-SecondaryServerName</span></span>
<span data-ttu-id="dca6c-133">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="dca6c-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dca6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca6c-134">CommonParameters</span></span>
<span data-ttu-id="dca6c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dca6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca6c-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca6c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca6c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dca6c-137">INPUTS</span></span>

### <span data-ttu-id="dca6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dca6c-138">System.String</span></span>

## <span data-ttu-id="dca6c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dca6c-139">OUTPUTS</span></span>

### <span data-ttu-id="dca6c-140">Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="dca6c-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="dca6c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dca6c-141">NOTES</span></span>

## <span data-ttu-id="dca6c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dca6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="dca6c-143">Yeni-Azreercachelink</span><span class="sxs-lookup"><span data-stu-id="dca6c-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="dca6c-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="dca6c-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="dca6c-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca6c-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="dca6c-146">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca6c-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="dca6c-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca6c-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="dca6c-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="dca6c-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)