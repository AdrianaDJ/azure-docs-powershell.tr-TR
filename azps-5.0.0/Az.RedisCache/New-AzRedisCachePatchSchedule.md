---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277678"
---
# <span data-ttu-id="a45d6-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a45d6-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a45d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a45d6-103">Düzeltme programı ekler.</span><span class="sxs-lookup"><span data-stu-id="a45d6-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="a45d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a45d6-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a45d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a45d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a45d6-106">**Yeni-Azrediscachepatchzamanlama** cmdlet 'ı, Azure Redis Cache 'de bir önbelleğe düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="a45d6-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a45d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a45d6-107">EXAMPLES</span></span>

### <span data-ttu-id="a45d6-108">Örnek 1: önbellekte düzeltme eki zamanlama oluşturma ve ekleme</span><span class="sxs-lookup"><span data-stu-id="a45d6-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="a45d6-109">Bu komut, RedisCache06 adlı önbelleğe bir düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="a45d6-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="a45d6-110">Entries parametresi, bir zamanlama oluşturmak için **New-Azredecachescheduleentry** kullanan bir komut değeridir.</span><span class="sxs-lookup"><span data-stu-id="a45d6-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="a45d6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a45d6-111">PARAMETERS</span></span>

### <span data-ttu-id="a45d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45d6-112">-DefaultProfile</span></span>
<span data-ttu-id="a45d6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a45d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a45d6-114">-Girişler</span><span class="sxs-lookup"><span data-stu-id="a45d6-114">-Entries</span></span>
<span data-ttu-id="a45d6-115">Bu cmdlet 'in bir önbellekte ayarladığı zamanlama dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45d6-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="a45d6-116">**Psscheduleentry** nesnesi almak için New-AzRedisCacheScheduleEntry cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a45d6-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a45d6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a45d6-117">-Name</span></span>
<span data-ttu-id="a45d6-118">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45d6-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="a45d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a45d6-120">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a45d6-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a45d6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a45d6-121">-Confirm</span></span>
<span data-ttu-id="a45d6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a45d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a45d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a45d6-123">-WhatIf</span></span>
<span data-ttu-id="a45d6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a45d6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a45d6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a45d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a45d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45d6-126">CommonParameters</span></span>
<span data-ttu-id="a45d6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a45d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45d6-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45d6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a45d6-129">INPUTS</span></span>

### <span data-ttu-id="a45d6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a45d6-130">System.String</span></span>

### <span data-ttu-id="a45d6-131">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="a45d6-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="a45d6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a45d6-132">OUTPUTS</span></span>

### <span data-ttu-id="a45d6-133">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a45d6-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a45d6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a45d6-134">NOTES</span></span>
* <span data-ttu-id="a45d6-135">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="a45d6-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a45d6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a45d6-136">RELATED LINKS</span></span>

[<span data-ttu-id="a45d6-137">Get-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="a45d6-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a45d6-138">Yeni-Azredecachescheduleentry</span><span class="sxs-lookup"><span data-stu-id="a45d6-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="a45d6-139">Remove-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="a45d6-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


