---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588819"
---
# <span data-ttu-id="e252c-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e252c-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="e252c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e252c-102">SYNOPSIS</span></span>
<span data-ttu-id="e252c-103">Redis Cache için coğrafi çoğaltma bağlantısı alın.</span><span class="sxs-lookup"><span data-stu-id="e252c-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e252c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e252c-104">SYNTAX</span></span>

### <span data-ttu-id="e252c-105">AllLinksForCache (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e252c-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e252c-106">Alllinkforprimarycache</span><span class="sxs-lookup"><span data-stu-id="e252c-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e252c-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="e252c-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e252c-108">Alllinkforsecondarycache</span><span class="sxs-lookup"><span data-stu-id="e252c-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e252c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e252c-109">DESCRIPTION</span></span>
<span data-ttu-id="e252c-110">Coğrafi çoğaltma bağlantı ayrıntısı almanın dört farklı yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="e252c-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="e252c-111">Parametre adı veya PrimaryServerName ve/veya SecondaryServerName sağlayın.</span><span class="sxs-lookup"><span data-stu-id="e252c-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="e252c-112">Ad verilirse, önbelleğin var olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="e252c-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="e252c-113">Yalnızca PrimaryServerName verilirse, önbelleğin birincili olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="e252c-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="e252c-114">Yalnızca SecondaryServerName etkinleştirilirse önbelleğin ikincil olduğu tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="e252c-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="e252c-115">PrimaryServerName ve SecondaryServerName her ikisi de verilirse, doğru role sahip belirli bir bağlantı döndürülür.</span><span class="sxs-lookup"><span data-stu-id="e252c-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="e252c-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e252c-116">EXAMPLES</span></span>

### <span data-ttu-id="e252c-117">Örnek 1: AllLinksForCache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="e252c-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="e252c-118">Bu komut, myCache1 adlı Red, Cache için tüm coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e252c-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="e252c-119">Örnek 2: Alllinkforprimarycache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="e252c-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="e252c-120">Bu komut, myCache1 adındaki Redis önbelleğinin birincili coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e252c-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="e252c-121">Örnek 3: Alllinkforsecondarycache parametresini kullanma</span><span class="sxs-lookup"><span data-stu-id="e252c-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="e252c-122">Bu komut, mycache2 adındaki Redis önbelleğinin ikincili coğrafi çoğaltma bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e252c-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="e252c-123">Örnek 4: parametre kümesi SingleLink kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="e252c-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="e252c-124">Bu komut, myCache1 adındaki Redis önbelleğinin birincil ve mycache2 adındaki Redis Cache olan tek bir coğrafi çoğaltma bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="e252c-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="e252c-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e252c-125">PARAMETERS</span></span>

### <span data-ttu-id="e252c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e252c-126">-DefaultProfile</span></span>
<span data-ttu-id="e252c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e252c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e252c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e252c-128">-Name</span></span>
<span data-ttu-id="e252c-129">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e252c-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e252c-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="e252c-130">-PrimaryServerName</span></span>
<span data-ttu-id="e252c-131">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e252c-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e252c-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="e252c-132">-SecondaryServerName</span></span>
<span data-ttu-id="e252c-133">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e252c-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e252c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e252c-134">CommonParameters</span></span>
<span data-ttu-id="e252c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e252c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e252c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e252c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e252c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e252c-137">INPUTS</span></span>

### <span data-ttu-id="e252c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e252c-138">System.String</span></span>
<span data-ttu-id="e252c-139">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e252c-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="e252c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e252c-140">OUTPUTS</span></span>

### <span data-ttu-id="e252c-141">System. koleksiyonları. Generic. LIST ' 1 [[Microsoft. Azure. Commands. RedisCache. modeller. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e252c-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e252c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e252c-142">NOTES</span></span>

## <span data-ttu-id="e252c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e252c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e252c-144">Yeni-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e252c-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="e252c-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e252c-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="e252c-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e252c-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="e252c-147">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e252c-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e252c-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e252c-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e252c-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e252c-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
