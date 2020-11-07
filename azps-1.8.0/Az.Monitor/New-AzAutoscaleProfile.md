---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: 5fef7a4431c9527fa043ab81490c8251c75ebd9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915615"
---
# <span data-ttu-id="bfe56-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="bfe56-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="bfe56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe56-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe56-103">Otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfe56-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="bfe56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfe56-104">SYNTAX</span></span>

### <span data-ttu-id="bfe56-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="bfe56-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfe56-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="bfe56-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfe56-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="bfe56-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfe56-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfe56-108">DESCRIPTION</span></span>
<span data-ttu-id="bfe56-109">**Yeni-AzAutoscaleProfile** cmdlet 'ı otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfe56-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="bfe56-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfe56-110">EXAMPLES</span></span>

### <span data-ttu-id="bfe56-111">Örnek 1: sabit bir tarih içeren tek bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="bfe56-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="bfe56-112">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bfe56-113">İkinci komut $Rule kuralı kullanarak, Profile01 adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfe56-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="bfe56-114">Örnek 2: zamanlamaya sahip bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="bfe56-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="bfe56-115">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bfe56-116">İkinci komut, $Rule kuralı kullanarak bir yinelenen zamanlama içeren Secondprofifilename adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bfe56-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="bfe56-117">Örnek 3: iki kuralla profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="bfe56-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="bfe56-118">İlk iki komut kurallar oluşturur ve bunları sırasıyla $Rule 1 ve $Rule 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="bfe56-119">Üçüncü komut, Rule1 ve Rule2 'deki kuralları kullanarak ProgID adlı bir profil oluşturur ve $Profile 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="bfe56-120">Son komutu, Rule1 ve Rule2 'deki kuralları kullanarak Secondprodosyaadı adlı bir profil oluşturur ve $Profile 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="bfe56-121">Örnek 4: zamanlama veya sabit tarihi olmayan bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="bfe56-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="bfe56-122">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bfe56-123">İkinci komut zamanlama veya sabit bir tarih olmadan bir profil oluşturur ve sonra bunu $Profile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bfe56-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="bfe56-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfe56-124">PARAMETERS</span></span>

### <span data-ttu-id="bfe56-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="bfe56-125">-DefaultCapacity</span></span>
<span data-ttu-id="bfe56-126">Varsayılan kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="bfe56-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe56-127">-DefaultProfile</span></span>
<span data-ttu-id="bfe56-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bfe56-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfe56-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="bfe56-129">-EndTimeWindow</span></span>
<span data-ttu-id="bfe56-130">Zaman penceresinin sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="bfe56-131">-MaximumCapacity</span></span>
<span data-ttu-id="bfe56-132">Maksimum kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="bfe56-133">-Minimumkapasite</span><span class="sxs-lookup"><span data-stu-id="bfe56-133">-MinimumCapacity</span></span>
<span data-ttu-id="bfe56-134">En düşük kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="bfe56-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfe56-135">-Name</span></span>
<span data-ttu-id="bfe56-136">Oluşturulacak profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="bfe56-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="bfe56-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="bfe56-138">Yinelenme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="bfe56-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bfe56-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bfe56-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bfe56-140">None</span></span>
- <span data-ttu-id="bfe56-141">İden</span><span class="sxs-lookup"><span data-stu-id="bfe56-141">Second</span></span>
- <span data-ttu-id="bfe56-142">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="bfe56-142">Minute</span></span>
- <span data-ttu-id="bfe56-143">Saati</span><span class="sxs-lookup"><span data-stu-id="bfe56-143">Hour</span></span>
- <span data-ttu-id="bfe56-144">Günündeki</span><span class="sxs-lookup"><span data-stu-id="bfe56-144">Day</span></span>
- <span data-ttu-id="bfe56-145">Haftada</span><span class="sxs-lookup"><span data-stu-id="bfe56-145">Week</span></span>
- <span data-ttu-id="bfe56-146">Ay</span><span class="sxs-lookup"><span data-stu-id="bfe56-146">Month</span></span>
- <span data-ttu-id="bfe56-147">Bu değerlerin tümü desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="bfe56-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-148">-Kural</span><span class="sxs-lookup"><span data-stu-id="bfe56-148">-Rule</span></span>
<span data-ttu-id="bfe56-149">Profile eklenecek kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="bfe56-150">-ScheduleDay</span></span>
<span data-ttu-id="bfe56-151">Zamanlanan günleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="bfe56-152">-ScheduleHour</span></span>
<span data-ttu-id="bfe56-153">Zamanlanan saatleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="bfe56-154">-ScheduleMinute</span></span>
<span data-ttu-id="bfe56-155">Zamanlanan dakikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="bfe56-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="bfe56-157">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="bfe56-158">-StartTimeWindow</span></span>
<span data-ttu-id="bfe56-159">Zaman penceresinin başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="bfe56-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="bfe56-161">Zaman penceresinin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfe56-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe56-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe56-162">CommonParameters</span></span>
<span data-ttu-id="bfe56-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfe56-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe56-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe56-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe56-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfe56-165">INPUTS</span></span>

### <span data-ttu-id="bfe56-166">System. String</span><span class="sxs-lookup"><span data-stu-id="bfe56-166">System.String</span></span>

### <span data-ttu-id="bfe56-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bfe56-167">System.DateTime</span></span>

### <span data-ttu-id="bfe56-168">Microsoft. Azure. Management. Monitor. Management. modeller. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="bfe56-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="bfe56-169">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0</span><span class="sxs-lookup"><span data-stu-id="bfe56-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bfe56-170">System. Koleksiyonlar. Generic. LIST `1[[System.Nullable` 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cecbvseç7val 7798e]], System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85din 98e]]</span><span class="sxs-lookup"><span data-stu-id="bfe56-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bfe56-171">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bfe56-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bfe56-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfe56-172">OUTPUTS</span></span>

### <span data-ttu-id="bfe56-173">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="bfe56-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="bfe56-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfe56-174">NOTES</span></span>

## <span data-ttu-id="bfe56-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfe56-175">RELATED LINKS</span></span>

[<span data-ttu-id="bfe56-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfe56-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="bfe56-177">Get-Azotomatik ölçek geçmişi</span><span class="sxs-lookup"><span data-stu-id="bfe56-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="bfe56-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfe56-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="bfe56-179">Yeni-Azotomobil</span><span class="sxs-lookup"><span data-stu-id="bfe56-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="bfe56-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfe56-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


