---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 41cb8c91a38e1e0bf004ece1ed1c2e7618b8c44d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753274"
---
# <span data-ttu-id="38b36-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="38b36-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="38b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b36-102">SYNOPSIS</span></span>
<span data-ttu-id="38b36-103">Otomasyon zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="38b36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38b36-104">SYNTAX</span></span>

### <span data-ttu-id="38b36-105">Günlük (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38b36-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38b36-106">Haftalık</span><span class="sxs-lookup"><span data-stu-id="38b36-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b36-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="38b36-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b36-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="38b36-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b36-109">Saat</span><span class="sxs-lookup"><span data-stu-id="38b36-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b36-110">Saat</span><span class="sxs-lookup"><span data-stu-id="38b36-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38b36-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="38b36-111">DESCRIPTION</span></span>
<span data-ttu-id="38b36-112">**New-Azautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'nda bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="38b36-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38b36-113">EXAMPLES</span></span>

### <span data-ttu-id="38b36-114">Örnek 1: yerel saatte bir kerelik bir zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="38b36-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="38b36-115">İlk komut, sistemden saat dilimi KIMLIĞINI alır ve $TimeZone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38b36-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="38b36-116">İkinci komut, belirli bir saat diliminde 11:00 saatinde geçerli tarihte bir kez çalışan bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="38b36-117">Örnek 2: Yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="38b36-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="38b36-118">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38b36-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="38b36-119">Gelecekte en az beş dakikalık bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="38b36-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="38b36-120">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir Date nesnesi oluşturur ve nesneyi $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38b36-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="38b36-121">Komut gelecekteki bir zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-121">The command specifies a future time.</span></span>
<span data-ttu-id="38b36-122">Son komutu, $StartDate uygulamasında depolanan zamandan başlayıp $EndDate içinde depolanan tarihte sona erecek şekilde Schedule02 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="38b36-123">Örnek 3: haftalık yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="38b36-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="38b36-124">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38b36-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="38b36-125">İkinci komut Pazartesi, Salı, Çarşamba, Perşembe ve Cuma içeren bir hafta günü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="38b36-126">Son komutu, 13:00 'daki her hafta Pazartesi ile Cuma arası Schedule03 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="38b36-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="38b36-127">Zamanlamanın süresi asla dolmayacak.</span><span class="sxs-lookup"><span data-stu-id="38b36-127">The schedule will never expire.</span></span>

## <span data-ttu-id="38b36-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38b36-128">PARAMETERS</span></span>

### <span data-ttu-id="38b36-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38b36-129">-AutomationAccountName</span></span>
<span data-ttu-id="38b36-130">Bu cmdlet 'in zamanlama oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-131">-Dayınterval</span><span class="sxs-lookup"><span data-stu-id="38b36-131">-DayInterval</span></span>
<span data-ttu-id="38b36-132">Zamanlama için gün cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="38b36-133">Bu parametreyi belirtmezseniz ve *Onetime* parametresini belirtmezseniz, varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="38b36-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="38b36-134">-DayOfWeek</span></span>
<span data-ttu-id="38b36-135">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="38b36-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="38b36-137">Zamanlamanın çalıştığı ay içinde haftanın oluşumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="38b36-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="38b36-138">psdx_paramvalues</span></span>
- <span data-ttu-id="38b36-139">2</span><span class="sxs-lookup"><span data-stu-id="38b36-139">1</span></span>
- <span data-ttu-id="38b36-140">2</span><span class="sxs-lookup"><span data-stu-id="38b36-140">2</span></span>
- <span data-ttu-id="38b36-141">@</span><span class="sxs-lookup"><span data-stu-id="38b36-141">3</span></span>
- <span data-ttu-id="38b36-142">1.921.024</span><span class="sxs-lookup"><span data-stu-id="38b36-142">4</span></span>
- <span data-ttu-id="38b36-143">-1</span><span class="sxs-lookup"><span data-stu-id="38b36-143">-1</span></span>
- <span data-ttu-id="38b36-144">Eklemelisiniz</span><span class="sxs-lookup"><span data-stu-id="38b36-144">First</span></span>
- <span data-ttu-id="38b36-145">İden</span><span class="sxs-lookup"><span data-stu-id="38b36-145">Second</span></span>
- <span data-ttu-id="38b36-146">Üç</span><span class="sxs-lookup"><span data-stu-id="38b36-146">Third</span></span>
- <span data-ttu-id="38b36-147">Dördüncü</span><span class="sxs-lookup"><span data-stu-id="38b36-147">Fourth</span></span>
- <span data-ttu-id="38b36-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="38b36-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-149">-Daysofay</span><span class="sxs-lookup"><span data-stu-id="38b36-149">-DaysOfMonth</span></span>
<span data-ttu-id="38b36-150">Aylık zamanlama için ayın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-151">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="38b36-151">-DaysOfWeek</span></span>
<span data-ttu-id="38b36-152">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b36-153">-DefaultProfile</span></span>
<span data-ttu-id="38b36-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="38b36-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b36-155">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="38b36-155">-Description</span></span>
<span data-ttu-id="38b36-156">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="38b36-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="38b36-157">-ExpiryTime</span></span>
<span data-ttu-id="38b36-158">Bir zamanlamanın bitiş zamanını **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="38b36-159">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38b36-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="38b36-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="38b36-161">Bu zamanlama nesnesinin yazılım güncelleştirme yapılandırması zamanlamasında kullanılacağını gösterir</span><span class="sxs-lookup"><span data-stu-id="38b36-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="38b36-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="38b36-162">-HourInterval</span></span>
<span data-ttu-id="38b36-163">Zamanlama için zaman aralığını saat olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-164">-Monthınterval</span><span class="sxs-lookup"><span data-stu-id="38b36-164">-MonthInterval</span></span>
<span data-ttu-id="38b36-165">Zamanlama için bir aralığı ay olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="38b36-166">-Name</span></span>
<span data-ttu-id="38b36-167">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="38b36-168">-OneTime</span></span>
<span data-ttu-id="38b36-169">Cmdlet 'in bir kerelik zamanlama oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b36-170">-ResourceGroupName</span></span>
<span data-ttu-id="38b36-171">Bu cmdlet 'in zamanlama oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-172">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="38b36-172">-StartTime</span></span>
<span data-ttu-id="38b36-173">Bir zamanlamanın başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="38b36-174">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38b36-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="38b36-175">*TimeZone* parametresi belirtilmişse, uzaklık gözardı edilir ve belirtilen saat dilimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38b36-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="38b36-176">-TimeZone</span></span>
<span data-ttu-id="38b36-177">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="38b36-178">Bu dize, ıANA KIMLIĞI veya Windows saat dilimi KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="38b36-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="38b36-179">-Haftaaralığı</span><span class="sxs-lookup"><span data-stu-id="38b36-179">-WeekInterval</span></span>
<span data-ttu-id="38b36-180">Zamanlama için hafta cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b36-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b36-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b36-181">CommonParameters</span></span>
<span data-ttu-id="38b36-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38b36-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b36-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b36-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b36-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38b36-184">INPUTS</span></span>

### <span data-ttu-id="38b36-185">System. String</span><span class="sxs-lookup"><span data-stu-id="38b36-185">System.String</span></span>

### <span data-ttu-id="38b36-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="38b36-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="38b36-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="38b36-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="38b36-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38b36-188">OUTPUTS</span></span>

### <span data-ttu-id="38b36-189">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="38b36-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="38b36-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38b36-190">NOTES</span></span>

## <span data-ttu-id="38b36-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38b36-191">RELATED LINKS</span></span>

[<span data-ttu-id="38b36-192">Get-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="38b36-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="38b36-193">Remove-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="38b36-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="38b36-194">Set-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="38b36-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


