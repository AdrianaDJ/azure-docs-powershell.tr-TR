---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 2f43cfa1e10fe115f8bf5fc94404f532f04f6573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762012"
---
# <span data-ttu-id="4f14d-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4f14d-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="4f14d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f14d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f14d-103">Zamanlama girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f14d-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f14d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f14d-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f14d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f14d-105">DESCRIPTION</span></span>
<span data-ttu-id="4f14d-106">**New-AzureRmRedisCacheScheduleEntry** cmdlet 'ı **psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f14d-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="4f14d-107">Azure Redis Cache düzeltme programı (New-AzureRmRedisCachePatchSchedule cmdlet 'i gibi) zamanlama girişi nesnelerini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4f14d-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="4f14d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f14d-108">EXAMPLES</span></span>

### <span data-ttu-id="4f14d-109">Örnek 1: hafta sonları için zamanlama girdisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f14d-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="4f14d-110">Bu komut, belirtilen başlangıç zamanına ve penceresine sahip bir hafta sonu zamanlamasını temsil eden bir **Psscheduleentry** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f14d-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="4f14d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f14d-111">PARAMETERS</span></span>

### <span data-ttu-id="4f14d-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="4f14d-112">-DayOfWeek</span></span>
<span data-ttu-id="4f14d-113">Zamanlama girişi için haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f14d-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="4f14d-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4f14d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f14d-115">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="4f14d-115">Everyday</span></span> 
- <span data-ttu-id="4f14d-116">Saatlerine</span><span class="sxs-lookup"><span data-stu-id="4f14d-116">Weekend</span></span> 
- <span data-ttu-id="4f14d-117">Den</span><span class="sxs-lookup"><span data-stu-id="4f14d-117">Monday</span></span> 
- <span data-ttu-id="4f14d-118">Salı</span><span class="sxs-lookup"><span data-stu-id="4f14d-118">Tuesday</span></span> 
- <span data-ttu-id="4f14d-119">Günü</span><span class="sxs-lookup"><span data-stu-id="4f14d-119">Wednesday</span></span> 
- <span data-ttu-id="4f14d-120">Per</span><span class="sxs-lookup"><span data-stu-id="4f14d-120">Thursday</span></span> 
- <span data-ttu-id="4f14d-121">Cuma</span><span class="sxs-lookup"><span data-stu-id="4f14d-121">Friday</span></span> 
- <span data-ttu-id="4f14d-122">Günü</span><span class="sxs-lookup"><span data-stu-id="4f14d-122">Saturday</span></span> 
- <span data-ttu-id="4f14d-123">Gününü</span><span class="sxs-lookup"><span data-stu-id="4f14d-123">Sunday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f14d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f14d-124">-DefaultProfile</span></span>
<span data-ttu-id="4f14d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f14d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f14d-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="4f14d-126">-MaintenanceWindow</span></span>
<span data-ttu-id="4f14d-127">Güncelleştirmelerde izin verilen zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f14d-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f14d-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="4f14d-128">-StartHourUtc</span></span>
<span data-ttu-id="4f14d-129">Zamanlamanın başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f14d-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f14d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f14d-130">CommonParameters</span></span>
<span data-ttu-id="4f14d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f14d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f14d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f14d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f14d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f14d-133">INPUTS</span></span>

### <span data-ttu-id="4f14d-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f14d-134">None</span></span>
<span data-ttu-id="4f14d-135">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f14d-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4f14d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f14d-136">OUTPUTS</span></span>

### <span data-ttu-id="4f14d-137">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4f14d-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="4f14d-138">Bu cmdlet bir zamanlama girişi nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="4f14d-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="4f14d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f14d-139">NOTES</span></span>
* <span data-ttu-id="4f14d-140">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="4f14d-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="4f14d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f14d-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f14d-142">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="4f14d-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4f14d-143">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="4f14d-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4f14d-144">Remove-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="4f14d-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


