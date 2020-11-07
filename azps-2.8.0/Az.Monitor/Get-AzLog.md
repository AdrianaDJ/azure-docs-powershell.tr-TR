---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: 45a2adc34322d80d5b9d103a99e26c9e2638c9af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751329"
---
# <span data-ttu-id="8d5de-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="8d5de-101">Get-AzLog</span></span>

## <span data-ttu-id="8d5de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5de-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5de-103">Olayların günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-103">Gets a log of events.</span></span>

## <span data-ttu-id="8d5de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d5de-104">SYNTAX</span></span>

### <span data-ttu-id="8d5de-105">Getbybağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="8d5de-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5de-106">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8d5de-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d5de-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d5de-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5de-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8d5de-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5de-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="8d5de-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d5de-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d5de-110">DESCRIPTION</span></span>
<span data-ttu-id="8d5de-111">**Get-AzLog** cmdlet 'i olayların günlüğünü alır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-111">The **Get-AzLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="8d5de-112">Olaylar geçerli abonelik KIMLIĞI, bağıntı KIMLIĞI, kaynak grubu, kaynak KIMLIĞI veya kaynak sağlayıcısıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="8d5de-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d5de-113">EXAMPLES</span></span>

### <span data-ttu-id="8d5de-114">Örnek 1: abonelik KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="8d5de-115">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 1000 olaylarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-116">Örnek 2: en fazla etkinlik sayısına göre bir abonelik KIMLIĞI olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxRecord 100
```

<span data-ttu-id="8d5de-117">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 100 olaylarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-118">Örnek 3: başlangıç saati olan abonelik KIMLIĞINE göre olay günlüğü alma.</span><span class="sxs-lookup"><span data-stu-id="8d5de-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="8d5de-119">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan en çok 1000 olayı, bu tarih/saat geçerli tarih/saat 90 günden daha eski bir tarih/saatten daha eski bir tarih</span><span class="sxs-lookup"><span data-stu-id="8d5de-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-120">Örnek 4: başlangıç saati ve bitiş saati olan abonelik KIMLIĞINE göre olay günlüğü alma.</span><span class="sxs-lookup"><span data-stu-id="8d5de-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="8d5de-121">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan veya sonrasında 2017-04-01T10:30 yerel saat, öncesi ve öncesi 2017-04-14T11: tüm tarih/saat aralığının, geçerli tarih/saat 90 günden eski olmadığı durumlarda, (örneğin, bekletme dönemi) en çok 1000.</span><span class="sxs-lookup"><span data-stu-id="8d5de-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8d5de-122">Örnek 5: bağıntı KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="8d5de-123">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="8d5de-124">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8d5de-125">Örnek 6: en fazla etkinlik sayısı</span><span class="sxs-lookup"><span data-stu-id="8d5de-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="8d5de-126">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="8d5de-127">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8d5de-128">Örnek 7: bağıntı KIMLIĞINE ve başlangıç saatine göre bir olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="8d5de-129">Bu komut, 2017-05-22T04 tarihinde veya ondan sonraki belirtilen bağıntı KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="8d5de-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="8d5de-130">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="8d5de-131">Örnek 8: başlangıç zamanı ve bitiş saati olan bağıntı KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="8d5de-132">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen bağıntı KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="8d5de-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8d5de-133">Örnek 9: kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="8d5de-134">Bu komut en çok 1000, geçerli tarih/saatten 7 gün sonraki belirtilen kaynak grubuyla ilişkili olayları listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-135">Örnek 10: en fazla etkinlik sayısına sahip kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="8d5de-136">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak grubuyla ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-137">Örnek 11: başlangıç zamanına göre bir kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="8d5de-138">Bu komut, 2017-05-22T04 tarihinde veya bu tarihten sonra gerçekleşen belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="8d5de-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-139">Örnek 12: başlangıç saati ve bitiş saati olan bir kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8d5de-140">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="8d5de-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8d5de-141">Örnek 13: kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="8d5de-142">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-143">Örnek 14: en fazla etkinlik sayısına göre bir olay günlüğü kaynak KIMLIĞINE göre alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="8d5de-144">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-145">Örnek 15: başlangıç saati olan kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="8d5de-146">Bu komut, %05-22T04 tarihinde veya bu tarihten sonra, belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="8d5de-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-147">Örnek 16: başlangıç saati ve bitiş saati olan kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8d5de-148">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="8d5de-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="8d5de-149">Örnek 17: kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="8d5de-150">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-151">Örnek 18: en fazla etkinlik sayısı olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="8d5de-152">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="8d5de-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-153">Örnek 19: başlangıç zamanı olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="8d5de-154">Bu komut, %05-22T04 tarihinde veya ondan sonra, belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="8d5de-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="8d5de-155">Örnek 20: başlangıç saati ve bitiş saati olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8d5de-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="8d5de-156">Bu komut, 2017-04-15T04 ' i n i n-04-15T04 ' ye geçen belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tam 90 Tarih</span><span class="sxs-lookup"><span data-stu-id="8d5de-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="8d5de-157">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d5de-157">PARAMETERS</span></span>

### <span data-ttu-id="8d5de-158">Arayan</span><span class="sxs-lookup"><span data-stu-id="8d5de-158">-Caller</span></span>
<span data-ttu-id="8d5de-159">Arayan belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="8d5de-160">-Bağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="8d5de-160">-CorrelationId</span></span>
<span data-ttu-id="8d5de-161">Bağıntı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="8d5de-162">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-162">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5de-163">-DefaultProfile</span></span>
<span data-ttu-id="8d5de-164">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8d5de-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d5de-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="8d5de-165">-DetailedOutput</span></span>
<span data-ttu-id="8d5de-166">Bu cmdlet 'in ayrıntılı çıkış görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="8d5de-167">Varsayılan olarak, çıktı özetlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-168">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="8d5de-168">-EndTime</span></span>
<span data-ttu-id="8d5de-169">Yerel saatte sorgunun bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="8d5de-170">Varsayılan değer geçerli süredir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-170">The default value is the current time.</span></span>
<span data-ttu-id="8d5de-171">Değer *StartTime* 'den sonra olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="8d5de-172">**TarihSaat** nesnesini almak için Get-Date cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d5de-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="8d5de-173">-MaxRecord</span></span>
<span data-ttu-id="8d5de-174">Belirtilen filtre için getirilecek kayıtların toplam sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="8d5de-175">Varsayılan değer 1000 ve kabul edilen en yüksek değer 100000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="8d5de-176">Negatif değerler ve 0 yoksayılır ve varsayılan değer kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d5de-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d5de-177">-ResourceGroupName</span></span>
<span data-ttu-id="8d5de-178">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-178">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-179">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8d5de-179">-ResourceId</span></span>
<span data-ttu-id="8d5de-180">Kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-180">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="8d5de-181">-ResourceProvider</span></span>
<span data-ttu-id="8d5de-182">Kaynak sağlayıcıya göre filtre belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-182">Specifies a filter by resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-183">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8d5de-183">-StartTime</span></span>
<span data-ttu-id="8d5de-184">Sorgunun başlangıç saatini yerel saatte belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="8d5de-185">Varsayılan değer *bitişsaati* eksi yedi gün.</span><span class="sxs-lookup"><span data-stu-id="8d5de-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="8d5de-186">**TarihSaat** nesnesini almak için Get-Date cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d5de-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5de-187">-Durum</span><span class="sxs-lookup"><span data-stu-id="8d5de-187">-Status</span></span>
<span data-ttu-id="8d5de-188">Durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d5de-188">Specifies the status.</span></span>

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

### <span data-ttu-id="8d5de-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5de-189">CommonParameters</span></span>
<span data-ttu-id="8d5de-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d5de-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5de-191">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8d5de-191">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5de-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d5de-192">INPUTS</span></span>

### <span data-ttu-id="8d5de-193">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d5de-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d5de-194">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5de-194">System.String</span></span>

### <span data-ttu-id="8d5de-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d5de-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8d5de-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8d5de-196">System.Int32</span></span>

## <span data-ttu-id="8d5de-197">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d5de-197">OUTPUTS</span></span>

### <span data-ttu-id="8d5de-198">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="8d5de-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="8d5de-199">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d5de-199">NOTES</span></span>

## <span data-ttu-id="8d5de-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d5de-200">RELATED LINKS</span></span>
