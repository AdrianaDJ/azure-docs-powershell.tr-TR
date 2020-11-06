---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594276"
---
# <span data-ttu-id="f424d-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f424d-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="f424d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f424d-102">SYNOPSIS</span></span>
<span data-ttu-id="f424d-103">Otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f424d-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f424d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f424d-104">SYNTAX</span></span>

### <span data-ttu-id="f424d-105">Zamanlanmış saatler olmadan New-AzureRmAutoscaleProfile cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="f424d-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f424d-106">Düzeltme tarihi zamanlama kullanarak New-AzureRmAutoscaleProfile cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="f424d-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f424d-107">Yinelenen zamanlama kullanarak New-AzureRmAutoscaleProfile cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="f424d-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f424d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f424d-108">DESCRIPTION</span></span>
<span data-ttu-id="f424d-109">**Yeni-AzureRmAutoscaleProfile** cmdlet 'ı otomatik ölçeklendirme profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f424d-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="f424d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f424d-110">EXAMPLES</span></span>

### <span data-ttu-id="f424d-111">Örnek 1: sabit bir tarih içeren tek bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="f424d-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="f424d-112">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f424d-113">İkinci komut $Rule kuralı kullanarak, Profile01 adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f424d-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="f424d-114">Örnek 2: zamanlamaya sahip bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="f424d-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="f424d-115">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f424d-116">İkinci komut, $Rule kuralı kullanarak bir yinelenen zamanlama içeren Secondprofifilename adlı bir profil oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f424d-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="f424d-117">Örnek 3: iki kuralla profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="f424d-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="f424d-118">İlk iki komut kurallar oluşturur ve bunları sırasıyla $Rule 1 ve $Rule 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="f424d-119">Üçüncü komut, Rule1 ve Rule2 'deki kuralları kullanarak ProgID adlı bir profil oluşturur ve $Profile 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="f424d-120">Son komutu, Rule1 ve Rule2 'deki kuralları kullanarak Secondprodosyaadı adlı bir profil oluşturur ve $Profile 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="f424d-121">Örnek 4: zamanlama veya sabit tarihi olmayan bir profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="f424d-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="f424d-122">İlk komut Istekler adlı bir otomatik ölçeklendirme kuralı oluşturur ve $Rule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f424d-123">İkinci komut zamanlama veya sabit bir tarih olmadan bir profil oluşturur ve sonra bunu $Profile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f424d-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="f424d-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f424d-124">PARAMETERS</span></span>

### <span data-ttu-id="f424d-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="f424d-125">-DefaultCapacity</span></span>
<span data-ttu-id="f424d-126">Varsayılan kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="f424d-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f424d-127">-EndTimeWindow</span></span>
<span data-ttu-id="f424d-128">Zaman penceresinin sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="f424d-129">-MaximumCapacity</span></span>
<span data-ttu-id="f424d-130">Maksimum kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="f424d-131">-Minimumkapasite</span><span class="sxs-lookup"><span data-stu-id="f424d-131">-MinimumCapacity</span></span>
<span data-ttu-id="f424d-132">En düşük kapasiteyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="f424d-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="f424d-133">-Name</span></span>
<span data-ttu-id="f424d-134">Oluşturulacak profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="f424d-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="f424d-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="f424d-136">Yinelenme sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="f424d-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f424d-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f424d-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f424d-138">None</span></span>
- <span data-ttu-id="f424d-139">İden</span><span class="sxs-lookup"><span data-stu-id="f424d-139">Second</span></span>
- <span data-ttu-id="f424d-140">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="f424d-140">Minute</span></span>
- <span data-ttu-id="f424d-141">Saati</span><span class="sxs-lookup"><span data-stu-id="f424d-141">Hour</span></span>
- <span data-ttu-id="f424d-142">Günündeki</span><span class="sxs-lookup"><span data-stu-id="f424d-142">Day</span></span>
- <span data-ttu-id="f424d-143">Haftada</span><span class="sxs-lookup"><span data-stu-id="f424d-143">Week</span></span>
- <span data-ttu-id="f424d-144">Ay</span><span class="sxs-lookup"><span data-stu-id="f424d-144">Month</span></span>
- <span data-ttu-id="f424d-145">Yılındaki</span><span class="sxs-lookup"><span data-stu-id="f424d-145">Year</span></span>

<span data-ttu-id="f424d-146">Bu değerlerin tümü desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="f424d-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-147">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="f424d-147">-Rules</span></span>
<span data-ttu-id="f424d-148">Profile eklenecek kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="f424d-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="f424d-149">-ScheduleDays</span></span>
<span data-ttu-id="f424d-150">Zamanlanan günleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="f424d-151">-ScheduleHours</span></span>
<span data-ttu-id="f424d-152">Zamanlanan saatleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-153">-Scheduledakika</span><span class="sxs-lookup"><span data-stu-id="f424d-153">-ScheduleMinutes</span></span>
<span data-ttu-id="f424d-154">Zamanlanan dakikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="f424d-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="f424d-156">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f424d-157">-StartTimeWindow</span></span>
<span data-ttu-id="f424d-158">Zaman penceresinin başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="f424d-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="f424d-160">Zaman penceresinin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f424d-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f424d-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f424d-161">-DefaultProfile</span></span>
<span data-ttu-id="f424d-162">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f424d-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f424d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f424d-163">CommonParameters</span></span>
<span data-ttu-id="f424d-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f424d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f424d-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f424d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f424d-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f424d-166">INPUTS</span></span>

## <span data-ttu-id="f424d-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f424d-167">OUTPUTS</span></span>

### <span data-ttu-id="f424d-168">Microsoft. Azure. Management. Monitor. Management. modeller. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f424d-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="f424d-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f424d-169">NOTES</span></span>

## <span data-ttu-id="f424d-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f424d-170">RELATED LINKS</span></span>

[<span data-ttu-id="f424d-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f424d-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="f424d-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="f424d-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="f424d-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f424d-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="f424d-174">Yeni-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="f424d-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="f424d-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f424d-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


