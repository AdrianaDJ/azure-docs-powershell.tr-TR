---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938191"
---
# <span data-ttu-id="9ab17-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9ab17-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="9ab17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab17-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab17-103">Zamanlama girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ab17-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="9ab17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ab17-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ab17-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ab17-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab17-106">**New-AzRedisCacheScheduleEntry** cmdlet 'ı **psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ab17-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="9ab17-107">Azure Redis Cache düzeltme programı (New-AzRedisCachePatchSchedule cmdlet 'i gibi) zamanlama girişi nesnelerini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="9ab17-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="9ab17-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ab17-108">EXAMPLES</span></span>

### <span data-ttu-id="9ab17-109">Örnek 1: hafta sonları için zamanlama girdisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ab17-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="9ab17-110">Bu komut, belirtilen başlangıç zamanına ve penceresine sahip bir hafta sonu zamanlamasını temsil eden bir **Psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ab17-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="9ab17-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ab17-111">PARAMETERS</span></span>

### <span data-ttu-id="9ab17-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9ab17-112">-DayOfWeek</span></span>
<span data-ttu-id="9ab17-113">Zamanlama girişi için haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab17-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="9ab17-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9ab17-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ab17-115">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="9ab17-115">Everyday</span></span> 
- <span data-ttu-id="9ab17-116">Saatlerine</span><span class="sxs-lookup"><span data-stu-id="9ab17-116">Weekend</span></span> 
- <span data-ttu-id="9ab17-117">Den</span><span class="sxs-lookup"><span data-stu-id="9ab17-117">Monday</span></span> 
- <span data-ttu-id="9ab17-118">Salı</span><span class="sxs-lookup"><span data-stu-id="9ab17-118">Tuesday</span></span> 
- <span data-ttu-id="9ab17-119">Günü</span><span class="sxs-lookup"><span data-stu-id="9ab17-119">Wednesday</span></span> 
- <span data-ttu-id="9ab17-120">Per</span><span class="sxs-lookup"><span data-stu-id="9ab17-120">Thursday</span></span> 
- <span data-ttu-id="9ab17-121">Cuma</span><span class="sxs-lookup"><span data-stu-id="9ab17-121">Friday</span></span> 
- <span data-ttu-id="9ab17-122">Günü</span><span class="sxs-lookup"><span data-stu-id="9ab17-122">Saturday</span></span> 
- <span data-ttu-id="9ab17-123">Gününü</span><span class="sxs-lookup"><span data-stu-id="9ab17-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab17-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab17-124">-DefaultProfile</span></span>
<span data-ttu-id="9ab17-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ab17-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ab17-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="9ab17-126">-MaintenanceWindow</span></span>
<span data-ttu-id="9ab17-127">Güncelleştirmelerde izin verilen zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab17-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab17-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="9ab17-128">-StartHourUtc</span></span>
<span data-ttu-id="9ab17-129">Zamanlamanın başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ab17-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab17-130">CommonParameters</span></span>
<span data-ttu-id="9ab17-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ab17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab17-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab17-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab17-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ab17-133">INPUTS</span></span>

### <span data-ttu-id="9ab17-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab17-134">System.String</span></span>

### <span data-ttu-id="9ab17-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9ab17-135">System.Int32</span></span>

### <span data-ttu-id="9ab17-136">System. Nullable ' 1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="9ab17-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9ab17-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ab17-137">OUTPUTS</span></span>

### <span data-ttu-id="9ab17-138">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="9ab17-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="9ab17-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ab17-139">NOTES</span></span>
* <span data-ttu-id="9ab17-140">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="9ab17-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9ab17-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ab17-141">RELATED LINKS</span></span>

[<span data-ttu-id="9ab17-142">Get-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="9ab17-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9ab17-143">Yeni-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="9ab17-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9ab17-144">Remove-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="9ab17-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


