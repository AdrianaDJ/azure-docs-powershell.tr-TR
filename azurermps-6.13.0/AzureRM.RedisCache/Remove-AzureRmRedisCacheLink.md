---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764124"
---
# <span data-ttu-id="6bbed-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6bbed-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="6bbed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bbed-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbed-103">İki kırmızı bir önbellek arasındaki coğrafi çoğaltma bağlantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6bbed-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bbed-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bbed-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbed-106">İki kırmızı bir önbellek arasındaki coğrafi çoğaltma bağlantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6bbed-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="6bbed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bbed-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbed-108">Örnek 1: coğrafi çoğaltma bağlantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6bbed-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="6bbed-109">Bu komut, myCache1 adındaki Redis Cache 'in birincil ve mycache2 adındaki Redis Cache olan coğrafi çoğaltma bağlantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6bbed-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="6bbed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bbed-110">PARAMETERS</span></span>

### <span data-ttu-id="6bbed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbed-111">-DefaultProfile</span></span>
<span data-ttu-id="6bbed-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bbed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bbed-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6bbed-113">-PassThru</span></span>
<span data-ttu-id="6bbed-114">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6bbed-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6bbed-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="6bbed-115">-PrimaryServerName</span></span>
<span data-ttu-id="6bbed-116">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6bbed-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="6bbed-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="6bbed-117">-SecondaryServerName</span></span>
<span data-ttu-id="6bbed-118">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6bbed-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="6bbed-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bbed-119">-Confirm</span></span>
<span data-ttu-id="6bbed-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bbed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbed-121">-WhatIf</span></span>
<span data-ttu-id="6bbed-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bbed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bbed-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bbed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbed-124">CommonParameters</span></span>
<span data-ttu-id="6bbed-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bbed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbed-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbed-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bbed-127">INPUTS</span></span>

### <span data-ttu-id="6bbed-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6bbed-128">System.String</span></span>

## <span data-ttu-id="6bbed-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bbed-129">OUTPUTS</span></span>

### <span data-ttu-id="6bbed-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6bbed-130">System.Boolean</span></span>

## <span data-ttu-id="6bbed-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bbed-131">NOTES</span></span>

## <span data-ttu-id="6bbed-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bbed-132">RELATED LINKS</span></span>

[<span data-ttu-id="6bbed-133">Yeni-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6bbed-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="6bbed-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="6bbed-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="6bbed-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6bbed-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="6bbed-136">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6bbed-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6bbed-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6bbed-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6bbed-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6bbed-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
