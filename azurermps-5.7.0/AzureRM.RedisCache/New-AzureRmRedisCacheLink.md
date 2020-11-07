---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: dd9e070a0228cf9bc492f8680917ae0f308e9019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763556"
---
# <span data-ttu-id="b3ec1-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b3ec1-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="b3ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ec1-103">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ec1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ec1-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3ec1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ec1-106">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="b3ec1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ec1-108">Örnek 1: iki önbellek arasında bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b3ec1-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="b3ec1-109">Bu komut, Redis Cache myCache1 ve mycache2 arasında coğrafi çoğaltma bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="b3ec1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="b3ec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ec1-111">-DefaultProfile</span></span>
<span data-ttu-id="b3ec1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ec1-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="b3ec1-113">-PrimaryServerName</span></span>
<span data-ttu-id="b3ec1-114">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="b3ec1-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="b3ec1-115">-SecondaryServerName</span></span>
<span data-ttu-id="b3ec1-116">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="b3ec1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3ec1-117">-Confirm</span></span>
<span data-ttu-id="b3ec1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ec1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ec1-119">-WhatIf</span></span>
<span data-ttu-id="b3ec1-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ec1-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ec1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ec1-122">CommonParameters</span></span>
<span data-ttu-id="b3ec1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ec1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ec1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ec1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ec1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ec1-125">INPUTS</span></span>

### <span data-ttu-id="b3ec1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ec1-126">System.String</span></span>

## <span data-ttu-id="b3ec1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ec1-127">OUTPUTS</span></span>

### <span data-ttu-id="b3ec1-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="b3ec1-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="b3ec1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ec1-129">NOTES</span></span>

## <span data-ttu-id="b3ec1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ec1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b3ec1-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b3ec1-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="b3ec1-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="b3ec1-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="b3ec1-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b3ec1-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b3ec1-134">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b3ec1-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b3ec1-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b3ec1-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b3ec1-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b3ec1-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
