---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276559"
---
# <span data-ttu-id="127d8-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="127d8-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="127d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="127d8-102">SYNOPSIS</span></span>
<span data-ttu-id="127d8-103">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="127d8-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="127d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="127d8-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="127d8-105">DESCRIPTION</span></span>
<span data-ttu-id="127d8-106">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="127d8-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="127d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="127d8-107">EXAMPLES</span></span>

### <span data-ttu-id="127d8-108">Örnek 1: iki önbellek arasında bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="127d8-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="127d8-109">Bu komut, Redis Cache myCache1 ve mycache2 arasında coğrafi çoğaltma bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="127d8-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="127d8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="127d8-110">PARAMETERS</span></span>

### <span data-ttu-id="127d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127d8-111">-DefaultProfile</span></span>
<span data-ttu-id="127d8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="127d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="127d8-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="127d8-113">-PrimaryServerName</span></span>
<span data-ttu-id="127d8-114">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="127d8-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="127d8-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="127d8-115">-SecondaryServerName</span></span>
<span data-ttu-id="127d8-116">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="127d8-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="127d8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="127d8-117">-Confirm</span></span>
<span data-ttu-id="127d8-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="127d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127d8-119">-WhatIf</span></span>
<span data-ttu-id="127d8-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="127d8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127d8-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="127d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127d8-122">CommonParameters</span></span>
<span data-ttu-id="127d8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="127d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127d8-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127d8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127d8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="127d8-125">INPUTS</span></span>

### <span data-ttu-id="127d8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="127d8-126">System.String</span></span>

## <span data-ttu-id="127d8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="127d8-127">OUTPUTS</span></span>

### <span data-ttu-id="127d8-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="127d8-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="127d8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="127d8-129">NOTES</span></span>

## <span data-ttu-id="127d8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="127d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="127d8-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="127d8-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="127d8-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="127d8-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="127d8-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="127d8-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="127d8-134">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="127d8-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="127d8-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="127d8-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="127d8-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="127d8-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)