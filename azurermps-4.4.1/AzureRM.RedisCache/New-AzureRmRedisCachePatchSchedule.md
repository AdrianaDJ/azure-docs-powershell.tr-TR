---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762418"
---
# <span data-ttu-id="460d2-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="460d2-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="460d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="460d2-102">SYNOPSIS</span></span>
<span data-ttu-id="460d2-103">Düzeltme programı ekler.</span><span class="sxs-lookup"><span data-stu-id="460d2-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="460d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="460d2-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="460d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="460d2-105">DESCRIPTION</span></span>
<span data-ttu-id="460d2-106">**New-Azurermrediscachepatchzamanlama** cmdlet 'ı Azure Redis Cache 'de bir önbelleğe düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="460d2-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="460d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="460d2-107">EXAMPLES</span></span>

### <span data-ttu-id="460d2-108">Örnek 1: önbellekte düzeltme eki zamanlama oluşturma ve ekleme</span><span class="sxs-lookup"><span data-stu-id="460d2-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="460d2-109">Bu komut, RedisCache06 adlı önbelleğe bir düzeltme eki zamanlaması ekler.</span><span class="sxs-lookup"><span data-stu-id="460d2-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="460d2-110">Entries parametresi, bir zamanlama oluşturmak için **New-AzureRmRedisCacheScheduleEntry** kullanan bir komut değeridir.</span><span class="sxs-lookup"><span data-stu-id="460d2-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="460d2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="460d2-111">PARAMETERS</span></span>

### <span data-ttu-id="460d2-112">-Girişler</span><span class="sxs-lookup"><span data-stu-id="460d2-112">-Entries</span></span>
<span data-ttu-id="460d2-113">Bu cmdlet 'in bir önbellekte ayarladığı zamanlama dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="460d2-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="460d2-114">**Psscheduleentry** nesnesi almak için New-AzureRmRedisCacheScheduleEntry cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="460d2-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="460d2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="460d2-115">-Name</span></span>
<span data-ttu-id="460d2-116">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="460d2-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="460d2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460d2-117">-ResourceGroupName</span></span>
<span data-ttu-id="460d2-118">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="460d2-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="460d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460d2-119">-DefaultProfile</span></span>
<span data-ttu-id="460d2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="460d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="460d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460d2-121">CommonParameters</span></span>
<span data-ttu-id="460d2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="460d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460d2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460d2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="460d2-124">INPUTS</span></span>

### <span data-ttu-id="460d2-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="460d2-125">None</span></span>
<span data-ttu-id="460d2-126">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="460d2-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="460d2-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="460d2-127">OUTPUTS</span></span>

### <span data-ttu-id="460d2-128">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="460d2-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="460d2-129">Bu cmdlet, önbellekte ayarlanan düzeltme eki zamanlama girdilerinin döndürür.</span><span class="sxs-lookup"><span data-stu-id="460d2-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="460d2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="460d2-130">NOTES</span></span>
* <span data-ttu-id="460d2-131">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="460d2-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="460d2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="460d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="460d2-133">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="460d2-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="460d2-134">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="460d2-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="460d2-135">Remove-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="460d2-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)

