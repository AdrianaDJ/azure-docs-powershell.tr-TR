---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
ms.openlocfilehash: 2192a03713b82e49f1958a34678353856197b3a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940133"
---
# <span data-ttu-id="61212-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="61212-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="61212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61212-102">SYNOPSIS</span></span>
<span data-ttu-id="61212-103">Otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61212-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61212-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61212-104">SYNTAX</span></span>

### <span data-ttu-id="61212-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="61212-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61212-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="61212-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61212-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="61212-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61212-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61212-108">DESCRIPTION</span></span>
<span data-ttu-id="61212-109">**Yeni-AzureRmAutoscaleProfile** cmdlet 'ı otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61212-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="61212-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61212-110">EXAMPLES</span></span>

### <span data-ttu-id="61212-111">Örnek 1: sabit bir tarih içeren tek bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="61212-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="61212-112">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="61212-113">İkinci komut $Rule kuralı kullanarak, Profile01 adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61212-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="61212-114">Örnek 2: zamanlamaya sahip bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="61212-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="61212-115">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="61212-116">İkinci komut, $Rule kuralı kullanarak bir yinelenen zamanlama içeren Secondprofifilename adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61212-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="61212-117">Örnek 3: iki kuralla profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="61212-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="61212-118">İlk iki komut kurallar oluşturur ve bunları sırasıyla $Rule 1 ve $Rule 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="61212-119">Üçüncü komut, Rule1 ve Rule2 'deki kuralları kullanarak ProgID adlı bir profil oluşturur ve $Profile 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="61212-120">Son komutu, Rule1 ve Rule2 'deki kuralları kullanarak Secondprodosyaadı adlı bir profil oluşturur ve $Profile 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="61212-121">Örnek 4: zamanlama veya sabit tarihi olmayan bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="61212-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="61212-122">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="61212-123">İkinci komut zamanlama veya sabit bir tarih olmadan bir profil oluşturur ve sonra bunu $Profile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61212-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="61212-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61212-124">PARAMETERS</span></span>

### <span data-ttu-id="61212-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="61212-125">-DefaultCapacity</span></span>
<span data-ttu-id="61212-126">Varsayılan kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="61212-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61212-127">-DefaultProfile</span></span>
<span data-ttu-id="61212-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61212-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61212-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="61212-129">-EndTimeWindow</span></span>
<span data-ttu-id="61212-130">Zaman penceresinin sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="61212-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="61212-131">-MaximumCapacity</span></span>
<span data-ttu-id="61212-132">Maksimum kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="61212-133">-Minimumkapasite</span><span class="sxs-lookup"><span data-stu-id="61212-133">-MinimumCapacity</span></span>
<span data-ttu-id="61212-134">En düşük kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="61212-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="61212-135">-Name</span></span>
<span data-ttu-id="61212-136">Oluşturulacak profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="61212-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="61212-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="61212-138">Yinelenme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="61212-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="61212-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61212-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="61212-140">None</span></span>
- <span data-ttu-id="61212-141">İden</span><span class="sxs-lookup"><span data-stu-id="61212-141">Second</span></span>
- <span data-ttu-id="61212-142">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="61212-142">Minute</span></span>
- <span data-ttu-id="61212-143">Saati</span><span class="sxs-lookup"><span data-stu-id="61212-143">Hour</span></span>
- <span data-ttu-id="61212-144">Günündeki</span><span class="sxs-lookup"><span data-stu-id="61212-144">Day</span></span>
- <span data-ttu-id="61212-145">Haftada</span><span class="sxs-lookup"><span data-stu-id="61212-145">Week</span></span>
- <span data-ttu-id="61212-146">Ay</span><span class="sxs-lookup"><span data-stu-id="61212-146">Month</span></span>
- <span data-ttu-id="61212-147">Bu değerlerin tümü desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="61212-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="61212-148">-Kural</span><span class="sxs-lookup"><span data-stu-id="61212-148">-Rule</span></span>
<span data-ttu-id="61212-149">Profile eklenecek kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="61212-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="61212-150">-ScheduleDay</span></span>
<span data-ttu-id="61212-151">Zamanlanan günleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="61212-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="61212-152">-ScheduleHour</span></span>
<span data-ttu-id="61212-153">Zamanlanan saatleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="61212-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="61212-154">-ScheduleMinute</span></span>
<span data-ttu-id="61212-155">Zamanlanan dakikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="61212-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="61212-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="61212-157">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="61212-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="61212-158">-StartTimeWindow</span></span>
<span data-ttu-id="61212-159">Zaman penceresinin başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="61212-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="61212-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="61212-161">Zaman penceresinin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61212-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="61212-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61212-162">CommonParameters</span></span>
<span data-ttu-id="61212-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61212-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61212-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61212-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61212-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61212-165">INPUTS</span></span>

### <span data-ttu-id="61212-166">System. String</span><span class="sxs-lookup"><span data-stu-id="61212-166">System.String</span></span>

### <span data-ttu-id="61212-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="61212-167">System.DateTime</span></span>

### <span data-ttu-id="61212-168">Microsoft. Azure. Management. Monitor. Management. modeller. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="61212-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="61212-169">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="61212-169">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="61212-170">System. Koleksiyonlar. Generic. LIST `1[[System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]], mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="61212-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]], mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="61212-171">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. ScaleRule, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="61212-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="61212-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61212-172">OUTPUTS</span></span>

### <span data-ttu-id="61212-173">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="61212-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="61212-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61212-174">NOTES</span></span>

## <span data-ttu-id="61212-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61212-175">RELATED LINKS</span></span>

[<span data-ttu-id="61212-176">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="61212-176">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="61212-177">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="61212-177">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="61212-178">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="61212-178">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="61212-179">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="61212-179">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="61212-180">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="61212-180">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)

