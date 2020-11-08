---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266938"
---
# <span data-ttu-id="5bd31-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5bd31-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="5bd31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd31-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd31-103">İki kırmızı bir önbellek arasındaki coğrafi çoğaltma bağlantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5bd31-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="5bd31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bd31-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bd31-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd31-106">İki kırmızı bir önbellek arasındaki coğrafi çoğaltma bağlantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5bd31-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="5bd31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bd31-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd31-108">Örnek 1: coğrafi çoğaltma bağlantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5bd31-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="5bd31-109">Bu komut, myCache1 adındaki Redis Cache 'in birincil ve mycache2 adındaki Redis Cache olan coğrafi çoğaltma bağlantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5bd31-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="5bd31-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bd31-110">PARAMETERS</span></span>

### <span data-ttu-id="5bd31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd31-111">-DefaultProfile</span></span>
<span data-ttu-id="5bd31-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bd31-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bd31-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5bd31-113">-PassThru</span></span>
<span data-ttu-id="5bd31-114">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5bd31-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bd31-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="5bd31-115">-PrimaryServerName</span></span>
<span data-ttu-id="5bd31-116">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="5bd31-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="5bd31-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="5bd31-117">-SecondaryServerName</span></span>
<span data-ttu-id="5bd31-118">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="5bd31-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="5bd31-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5bd31-119">-Confirm</span></span>
<span data-ttu-id="5bd31-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5bd31-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd31-121">-WhatIf</span></span>
<span data-ttu-id="5bd31-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bd31-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd31-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5bd31-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd31-124">CommonParameters</span></span>
<span data-ttu-id="5bd31-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bd31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd31-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd31-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd31-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bd31-127">INPUTS</span></span>

### <span data-ttu-id="5bd31-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5bd31-128">System.String</span></span>

## <span data-ttu-id="5bd31-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bd31-129">OUTPUTS</span></span>

### <span data-ttu-id="5bd31-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bd31-130">System.Boolean</span></span>

## <span data-ttu-id="5bd31-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bd31-131">NOTES</span></span>

## <span data-ttu-id="5bd31-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bd31-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bd31-133">Yeni-Azreercachelink</span><span class="sxs-lookup"><span data-stu-id="5bd31-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="5bd31-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5bd31-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="5bd31-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5bd31-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="5bd31-136">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5bd31-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5bd31-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5bd31-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5bd31-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5bd31-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)