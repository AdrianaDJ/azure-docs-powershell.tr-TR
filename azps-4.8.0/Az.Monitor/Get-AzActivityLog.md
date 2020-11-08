---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109538"
---
# <span data-ttu-id="d2076-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="d2076-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="d2076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2076-102">SYNOPSIS</span></span>
<span data-ttu-id="d2076-103">Etkinlik günlüğü olaylarını alma.</span><span class="sxs-lookup"><span data-stu-id="d2076-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="d2076-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2076-104">SYNTAX</span></span>

### <span data-ttu-id="d2076-105">Getbybağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="d2076-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2076-106">Getbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d2076-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2076-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d2076-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2076-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d2076-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2076-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="d2076-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2076-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2076-110">DESCRIPTION</span></span>
<span data-ttu-id="d2076-111">Get-AzActivityLog cmdlet etkinlik günlüğü olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2076-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="d2076-112">Olaylar geçerli abonelik KIMLIĞI, bağıntı KIMLIĞI, kaynak grubu, kaynak KIMLIĞI veya kaynak sağlayıcısıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d2076-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="d2076-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2076-113">EXAMPLES</span></span>

### <span data-ttu-id="d2076-114">Örnek 1: abonelik KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="d2076-115">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 1000 olaylarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-116">Örnek 2: en fazla etkinlik sayısına göre bir abonelik KIMLIĞI olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="d2076-117">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 100 olaylarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-118">Örnek 3: başlangıç saati olan abonelik KIMLIĞINE göre olay günlüğü alma.</span><span class="sxs-lookup"><span data-stu-id="d2076-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="d2076-119">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan en çok 1000 olayı, bu tarih/saat geçerli tarih/saat 90 günden daha eski bir tarih/saatten daha eski bir tarih</span><span class="sxs-lookup"><span data-stu-id="d2076-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-120">Örnek 4: başlangıç saati ve bitiş saati olan abonelik KIMLIĞINE göre olay günlüğü alma.</span><span class="sxs-lookup"><span data-stu-id="d2076-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="d2076-121">Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan veya sonrasında 2017-04-01T10:30 yerel saat, öncesi ve öncesi 2017-04-14T11: tüm tarih/saat aralığının, geçerli tarih/saat 90 günden eski olmadığı durumlarda, (örneğin, bekletme dönemi) en çok 1000.</span><span class="sxs-lookup"><span data-stu-id="d2076-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d2076-122">Örnek 5: bağıntı KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="d2076-123">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d2076-124">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="d2076-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d2076-125">Örnek 6: en fazla etkinlik sayısı</span><span class="sxs-lookup"><span data-stu-id="d2076-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="d2076-126">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="d2076-127">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="d2076-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d2076-128">Örnek 7: bağıntı KIMLIĞINE ve başlangıç saatine göre bir olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d2076-129">Bu komut, 2017-05-22T04 tarihinde veya ondan sonraki belirtilen bağıntı KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="d2076-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="d2076-130">**Not** : Bu genellikle yalnızca bir olaydır.</span><span class="sxs-lookup"><span data-stu-id="d2076-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="d2076-131">Örnek 8: başlangıç zamanı ve bitiş saati olan bağıntı KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="d2076-132">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen bağıntı KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="d2076-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d2076-133">Örnek 9: kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="d2076-134">Bu komut en çok 1000, geçerli tarih/saatten 7 gün sonraki belirtilen kaynak grubuyla ilişkili olayları listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-135">Örnek 10: en fazla etkinlik sayısına sahip kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="d2076-136">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak grubuyla ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-137">Örnek 11: başlangıç zamanına göre bir kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="d2076-138">Bu komut, 2017-05-22T04 tarihinde veya bu tarihten sonra gerçekleşen belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="d2076-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-139">Örnek 12: başlangıç saati ve bitiş saati olan bir kaynak grubu için olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d2076-140">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="d2076-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d2076-141">Örnek 13: kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="d2076-142">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-143">Örnek 14: en fazla etkinlik sayısına göre bir olay günlüğü kaynak KIMLIĞINE göre alma</span><span class="sxs-lookup"><span data-stu-id="d2076-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="d2076-144">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-145">Örnek 15: başlangıç saati olan kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d2076-146">Bu komut, %05-22T04 tarihinde veya bu tarihten sonra, belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="d2076-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-147">Örnek 16: başlangıç saati ve bitiş saati olan kaynak KIMLIĞINE göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d2076-148">Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).</span><span class="sxs-lookup"><span data-stu-id="d2076-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="d2076-149">Örnek 17: kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="d2076-150">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 1000 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-151">Örnek 18: en fazla etkinlik sayısı olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="d2076-152">Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 100 olayı listeler.</span><span class="sxs-lookup"><span data-stu-id="d2076-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-153">Örnek 19: başlangıç zamanı olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="d2076-154">Bu komut, %05-22T04 tarihinde veya ondan sonra, belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.</span><span class="sxs-lookup"><span data-stu-id="d2076-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="d2076-155">Örnek 20: başlangıç saati ve bitiş saati olan kaynak sağlayıcıya göre olay günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="d2076-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="d2076-156">Bu komut, 2017-04-15T04 ' i n i n-04-15T04 ' ye geçen belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tam 90 Tarih</span><span class="sxs-lookup"><span data-stu-id="d2076-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="d2076-157">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2076-157">PARAMETERS</span></span>

### <span data-ttu-id="d2076-158">Arayan</span><span class="sxs-lookup"><span data-stu-id="d2076-158">-Caller</span></span>
<span data-ttu-id="d2076-159">Getirilecek olayları arayan</span><span class="sxs-lookup"><span data-stu-id="d2076-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="d2076-160">-Bağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="d2076-160">-CorrelationId</span></span>
<span data-ttu-id="d2076-161">Bağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="d2076-161">The CorrelationId</span></span>

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

### <span data-ttu-id="d2076-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2076-162">-DefaultProfile</span></span>
<span data-ttu-id="d2076-163">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2076-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2076-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="d2076-164">-DetailedOutput</span></span>
<span data-ttu-id="d2076-165">Olayların tüm ayrıntılarını içeren dönüş nesnesi (varsayılan olarak yalnızca bazı öznitelikleri döndürmeli; Yani, ayrıntı yok)</span><span class="sxs-lookup"><span data-stu-id="d2076-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2076-166">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d2076-166">-EndTime</span></span>
<span data-ttu-id="d2076-167">Sorgunun bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d2076-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2076-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="d2076-168">-MaxRecord</span></span>
<span data-ttu-id="d2076-169">Getirilecek en fazla kayıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="d2076-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="d2076-170">Diğer ad: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="d2076-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2076-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2076-171">-ResourceGroupName</span></span>
<span data-ttu-id="d2076-172">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d2076-172">The resource group name</span></span>

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

### <span data-ttu-id="d2076-173">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d2076-173">-ResourceId</span></span>
<span data-ttu-id="d2076-174">RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d2076-174">The ResourceId</span></span>

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

### <span data-ttu-id="d2076-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="d2076-175">-ResourceProvider</span></span>
<span data-ttu-id="d2076-176">ResourceProvider adı</span><span class="sxs-lookup"><span data-stu-id="d2076-176">The ResourceProvider name</span></span>

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

### <span data-ttu-id="d2076-177">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d2076-177">-StartTime</span></span>
<span data-ttu-id="d2076-178">Sorgunun Bağıntıkimliği</span><span class="sxs-lookup"><span data-stu-id="d2076-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2076-179">-Durum</span><span class="sxs-lookup"><span data-stu-id="d2076-179">-Status</span></span>
<span data-ttu-id="d2076-180">Getirilecek olayların durumu</span><span class="sxs-lookup"><span data-stu-id="d2076-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="d2076-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2076-181">CommonParameters</span></span>
<span data-ttu-id="d2076-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2076-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2076-183">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2076-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2076-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2076-184">INPUTS</span></span>

### <span data-ttu-id="d2076-185">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d2076-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d2076-186">System. String</span><span class="sxs-lookup"><span data-stu-id="d2076-186">System.String</span></span>

### <span data-ttu-id="d2076-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2076-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d2076-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d2076-188">System.Int32</span></span>

## <span data-ttu-id="d2076-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2076-189">OUTPUTS</span></span>

### <span data-ttu-id="d2076-190">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="d2076-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="d2076-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2076-191">NOTES</span></span>

## <span data-ttu-id="d2076-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2076-192">RELATED LINKS</span></span>
