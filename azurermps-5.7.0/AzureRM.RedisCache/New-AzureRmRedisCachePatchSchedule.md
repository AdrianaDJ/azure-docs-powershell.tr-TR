---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573322"
---
# <span data-ttu-id="f0fc4-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f0fc4-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f0fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fc4-103">Düzeltme programı ekler.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0fc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0fc4-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0fc4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="f0fc4-106">**New-Azurermrediscachepatchzamanlama** cmdlet 'ı Azure Redis Cache 'de bir önbelleğe düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f0fc4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="f0fc4-108">Örnek 1: önbellekte düzeltme eki zamanlama oluşturma ve ekleme</span><span class="sxs-lookup"><span data-stu-id="f0fc4-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="f0fc4-109">Bu komut, RedisCache06 adlı önbelleğe bir düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="f0fc4-110">Entries parametresi, bir zamanlama oluşturmak için **New-AzureRmRedisCacheScheduleEntry** kullanan bir komut değeridir.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="f0fc4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0fc4-111">PARAMETERS</span></span>

### <span data-ttu-id="f0fc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fc4-112">-DefaultProfile</span></span>
<span data-ttu-id="f0fc4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0fc4-114">-Girişler</span><span class="sxs-lookup"><span data-stu-id="f0fc4-114">-Entries</span></span>
<span data-ttu-id="f0fc4-115">Bu cmdlet 'in bir önbellekte ayarladığı zamanlama dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="f0fc4-116">**Psscheduleentry** nesnesi almak için New-AzureRmRedisCacheScheduleEntry cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0fc4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0fc4-117">-Name</span></span>
<span data-ttu-id="f0fc4-118">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f0fc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0fc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0fc4-120">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="f0fc4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0fc4-121">-Confirm</span></span>
<span data-ttu-id="f0fc4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0fc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0fc4-123">-WhatIf</span></span>
<span data-ttu-id="f0fc4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0fc4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0fc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fc4-126">CommonParameters</span></span>
<span data-ttu-id="f0fc4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fc4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0fc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fc4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0fc4-129">INPUTS</span></span>

### <span data-ttu-id="f0fc4-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f0fc4-130">None</span></span>
<span data-ttu-id="f0fc4-131">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f0fc4-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0fc4-132">OUTPUTS</span></span>

### <span data-ttu-id="f0fc4-133">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f0fc4-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="f0fc4-134">Bu cmdlet, önbellekte ayarlanan düzeltme eki zamanlama girdilerinin döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="f0fc4-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0fc4-135">NOTES</span></span>
* <span data-ttu-id="f0fc4-136">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="f0fc4-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f0fc4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0fc4-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0fc4-138">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="f0fc4-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="f0fc4-139">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f0fc4-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="f0fc4-140">Remove-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="f0fc4-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


