---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572653"
---
# <span data-ttu-id="d2e48-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d2e48-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="d2e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e48-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e48-103">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d2e48-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2e48-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2e48-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e48-106">İki Redis önbellekler arasında coğrafi çoğaltma bağlantısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d2e48-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="d2e48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2e48-107">EXAMPLES</span></span>

### <span data-ttu-id="d2e48-108">Örnek 1: iki önbellek arasında bağlantı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d2e48-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="d2e48-109">Bu komut, Redis Cache myCache1 ve mycache2 arasında coğrafi çoğaltma bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2e48-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="d2e48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2e48-110">PARAMETERS</span></span>

### <span data-ttu-id="d2e48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e48-111">-DefaultProfile</span></span>
<span data-ttu-id="d2e48-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2e48-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e48-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="d2e48-113">-PrimaryServerName</span></span>
<span data-ttu-id="d2e48-114">Bağlantıdaki birincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d2e48-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="d2e48-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="d2e48-115">-SecondaryServerName</span></span>
<span data-ttu-id="d2e48-116">Bağlantıdaki ikincil Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="d2e48-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="d2e48-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2e48-117">-Confirm</span></span>
<span data-ttu-id="d2e48-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2e48-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e48-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e48-119">-WhatIf</span></span>
<span data-ttu-id="d2e48-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2e48-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e48-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2e48-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e48-122">CommonParameters</span></span>
<span data-ttu-id="d2e48-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2e48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e48-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e48-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e48-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2e48-125">INPUTS</span></span>

### <span data-ttu-id="d2e48-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e48-126">System.String</span></span>

## <span data-ttu-id="d2e48-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2e48-127">OUTPUTS</span></span>

### <span data-ttu-id="d2e48-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="d2e48-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="d2e48-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2e48-129">NOTES</span></span>

## <span data-ttu-id="d2e48-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2e48-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2e48-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d2e48-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="d2e48-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d2e48-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="d2e48-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2e48-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d2e48-134">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2e48-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="d2e48-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2e48-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="d2e48-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d2e48-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
