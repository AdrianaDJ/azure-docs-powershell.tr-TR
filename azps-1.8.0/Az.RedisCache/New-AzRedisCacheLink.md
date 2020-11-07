---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 157490da6abeae7e947c22e88301d29043722a86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759544"
---
# <span data-ttu-id="e3e34-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e3e34-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="e3e34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e34-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e34-103">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e3e34-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="e3e34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3e34-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3e34-105">DESCRIPTION</span></span>
<span data-ttu-id="e3e34-106">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e3e34-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="e3e34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3e34-107">EXAMPLES</span></span>

### <span data-ttu-id="e3e34-108">Örnek 1: iki önbellek arasında bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3e34-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="e3e34-109">Bu komut, Redis Cache myCache1 ve mycache2 arasında coğrafi çoğaltma bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3e34-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="e3e34-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3e34-110">PARAMETERS</span></span>

### <span data-ttu-id="e3e34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e34-111">-DefaultProfile</span></span>
<span data-ttu-id="e3e34-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3e34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e34-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="e3e34-113">-PrimaryServerName</span></span>
<span data-ttu-id="e3e34-114">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3e34-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="e3e34-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="e3e34-115">-SecondaryServerName</span></span>
<span data-ttu-id="e3e34-116">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="e3e34-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="e3e34-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3e34-117">-Confirm</span></span>
<span data-ttu-id="e3e34-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3e34-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e34-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e34-119">-WhatIf</span></span>
<span data-ttu-id="e3e34-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3e34-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e34-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3e34-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e34-122">CommonParameters</span></span>
<span data-ttu-id="e3e34-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3e34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e34-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e34-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e34-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3e34-125">INPUTS</span></span>

### <span data-ttu-id="e3e34-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3e34-126">System.String</span></span>

## <span data-ttu-id="e3e34-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3e34-127">OUTPUTS</span></span>

### <span data-ttu-id="e3e34-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="e3e34-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="e3e34-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3e34-129">NOTES</span></span>

## <span data-ttu-id="e3e34-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3e34-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3e34-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e3e34-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="e3e34-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="e3e34-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="e3e34-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3e34-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="e3e34-134">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3e34-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e3e34-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3e34-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="e3e34-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3e34-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)