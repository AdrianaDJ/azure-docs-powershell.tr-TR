---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275694"
---
# <span data-ttu-id="a9731-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a9731-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="a9731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9731-102">SYNOPSIS</span></span>
<span data-ttu-id="a9731-103">Zamanlama girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9731-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="a9731-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9731-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9731-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9731-105">DESCRIPTION</span></span>
<span data-ttu-id="a9731-106">**New-AzRedisCacheScheduleEntry** cmdlet 'ı **psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9731-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="a9731-107">Azure Redis Cache düzeltme programı (New-AzRedisCachePatchSchedule cmdlet 'i gibi) zamanlama girişi nesnelerini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a9731-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="a9731-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9731-108">EXAMPLES</span></span>

### <span data-ttu-id="a9731-109">Örnek 1: hafta sonları için zamanlama girdisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9731-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="a9731-110">Bu komut, belirtilen başlangıç zamanına ve penceresine sahip bir hafta sonu zamanlamasını temsil eden bir **Psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9731-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="a9731-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9731-111">PARAMETERS</span></span>

### <span data-ttu-id="a9731-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="a9731-112">-DayOfWeek</span></span>
<span data-ttu-id="a9731-113">Zamanlama girişi için haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9731-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="a9731-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a9731-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9731-115">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="a9731-115">Everyday</span></span> 
- <span data-ttu-id="a9731-116">Saatlerine</span><span class="sxs-lookup"><span data-stu-id="a9731-116">Weekend</span></span> 
- <span data-ttu-id="a9731-117">Den</span><span class="sxs-lookup"><span data-stu-id="a9731-117">Monday</span></span> 
- <span data-ttu-id="a9731-118">Salı</span><span class="sxs-lookup"><span data-stu-id="a9731-118">Tuesday</span></span> 
- <span data-ttu-id="a9731-119">Günü</span><span class="sxs-lookup"><span data-stu-id="a9731-119">Wednesday</span></span> 
- <span data-ttu-id="a9731-120">Per</span><span class="sxs-lookup"><span data-stu-id="a9731-120">Thursday</span></span> 
- <span data-ttu-id="a9731-121">Cuma</span><span class="sxs-lookup"><span data-stu-id="a9731-121">Friday</span></span> 
- <span data-ttu-id="a9731-122">Günü</span><span class="sxs-lookup"><span data-stu-id="a9731-122">Saturday</span></span> 
- <span data-ttu-id="a9731-123">Gününü</span><span class="sxs-lookup"><span data-stu-id="a9731-123">Sunday</span></span>

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

### <span data-ttu-id="a9731-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9731-124">-DefaultProfile</span></span>
<span data-ttu-id="a9731-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9731-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9731-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="a9731-126">-MaintenanceWindow</span></span>
<span data-ttu-id="a9731-127">Güncelleştirmelerde izin verilen zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9731-127">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="a9731-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="a9731-128">-StartHourUtc</span></span>
<span data-ttu-id="a9731-129">Zamanlamanın başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9731-129">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="a9731-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9731-130">CommonParameters</span></span>
<span data-ttu-id="a9731-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9731-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9731-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9731-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9731-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9731-133">INPUTS</span></span>

### <span data-ttu-id="a9731-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9731-134">System.String</span></span>

### <span data-ttu-id="a9731-135">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a9731-135">System.Int32</span></span>

### <span data-ttu-id="a9731-136">System. Nullable ' 1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9731-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9731-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9731-137">OUTPUTS</span></span>

### <span data-ttu-id="a9731-138">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a9731-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a9731-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9731-139">NOTES</span></span>
* <span data-ttu-id="a9731-140">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="a9731-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a9731-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9731-141">RELATED LINKS</span></span>

[<span data-ttu-id="a9731-142">Get-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="a9731-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a9731-143">Yeni-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="a9731-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a9731-144">Remove-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="a9731-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


