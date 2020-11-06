---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 0672e7ab292046b79ceaad61446c30c210bcb535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593329"
---
# <span data-ttu-id="d228a-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d228a-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="d228a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d228a-102">SYNOPSIS</span></span>
<span data-ttu-id="d228a-103">Otomasyon zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d228a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d228a-104">SYNTAX</span></span>

### <span data-ttu-id="d228a-105">Günlük (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d228a-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d228a-106">Haftalık</span><span class="sxs-lookup"><span data-stu-id="d228a-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d228a-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="d228a-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d228a-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d228a-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d228a-109">Saat</span><span class="sxs-lookup"><span data-stu-id="d228a-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d228a-110">Saat</span><span class="sxs-lookup"><span data-stu-id="d228a-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d228a-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="d228a-111">DESCRIPTION</span></span>
<span data-ttu-id="d228a-112">**Yeni-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'nda bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="d228a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d228a-113">EXAMPLES</span></span>

### <span data-ttu-id="d228a-114">Örnek 1: yerel saatte bir kerelik bir zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="d228a-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="d228a-115">İlk komut, sistemden saat dilimi KIMLIĞINI alır ve $TimeZone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d228a-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="d228a-116">İkinci komut, belirli bir saat diliminde 11:00 saatinde geçerli tarihte bir kez çalışan bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="d228a-117">Örnek 2: Yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="d228a-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d228a-118">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d228a-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="d228a-119">Gelecekte en az beş dakikalık bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="d228a-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="d228a-120">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir Date nesnesi oluşturur ve nesneyi $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d228a-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="d228a-121">Komut gelecekteki bir zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-121">The command specifies a future time.</span></span>
<span data-ttu-id="d228a-122">Son komutu, $StartDate uygulamasında depolanan zamandan başlayıp $EndDate içinde depolanan tarihte sona erecek şekilde Schedule02 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="d228a-123">Örnek 3: haftalık yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="d228a-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d228a-124">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d228a-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="d228a-125">İkinci komut Pazartesi, Salı, Çarşamba, Perşembe ve Cuma içeren bir hafta günü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="d228a-126">Son komutu, 13:00 'daki her hafta Pazartesi ile Cuma arası Schedule03 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d228a-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="d228a-127">Zamanlamanın süresi asla dolmayacak.</span><span class="sxs-lookup"><span data-stu-id="d228a-127">The schedule will never expire.</span></span>

## <span data-ttu-id="d228a-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d228a-128">PARAMETERS</span></span>

### <span data-ttu-id="d228a-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d228a-129">-AutomationAccountName</span></span>
<span data-ttu-id="d228a-130">Bu cmdlet 'in zamanlama oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="d228a-131">-Dayınterval</span><span class="sxs-lookup"><span data-stu-id="d228a-131">-DayInterval</span></span>
<span data-ttu-id="d228a-132">Zamanlama için gün cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="d228a-133">Bu parametreyi belirtmezseniz ve *Onetime* parametresini belirtmezseniz, varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="d228a-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="d228a-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d228a-134">-DayOfWeek</span></span>
<span data-ttu-id="d228a-135">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="d228a-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="d228a-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="d228a-137">Zamanlamanın çalıştığı ay içinde haftanın oluşumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="d228a-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d228a-138">psdx_paramvalues</span></span>
- <span data-ttu-id="d228a-139">2</span><span class="sxs-lookup"><span data-stu-id="d228a-139">1</span></span>
- <span data-ttu-id="d228a-140">2</span><span class="sxs-lookup"><span data-stu-id="d228a-140">2</span></span>
- <span data-ttu-id="d228a-141">@</span><span class="sxs-lookup"><span data-stu-id="d228a-141">3</span></span>
- <span data-ttu-id="d228a-142">1.921.024</span><span class="sxs-lookup"><span data-stu-id="d228a-142">4</span></span>
- <span data-ttu-id="d228a-143">-1</span><span class="sxs-lookup"><span data-stu-id="d228a-143">-1</span></span>
- <span data-ttu-id="d228a-144">Eklemelisiniz</span><span class="sxs-lookup"><span data-stu-id="d228a-144">First</span></span>
- <span data-ttu-id="d228a-145">İden</span><span class="sxs-lookup"><span data-stu-id="d228a-145">Second</span></span>
- <span data-ttu-id="d228a-146">Üç</span><span class="sxs-lookup"><span data-stu-id="d228a-146">Third</span></span>
- <span data-ttu-id="d228a-147">Dördüncü</span><span class="sxs-lookup"><span data-stu-id="d228a-147">Fourth</span></span>
- <span data-ttu-id="d228a-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="d228a-148">LastDay</span></span>

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

### <span data-ttu-id="d228a-149">-Daysofay</span><span class="sxs-lookup"><span data-stu-id="d228a-149">-DaysOfMonth</span></span>
<span data-ttu-id="d228a-150">Aylık zamanlama için ayın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="d228a-151">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="d228a-151">-DaysOfWeek</span></span>
<span data-ttu-id="d228a-152">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="d228a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d228a-153">-DefaultProfile</span></span>
<span data-ttu-id="d228a-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d228a-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d228a-155">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d228a-155">-Description</span></span>
<span data-ttu-id="d228a-156">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="d228a-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d228a-157">-ExpiryTime</span></span>
<span data-ttu-id="d228a-158">Bir zamanlamanın sona erme zamanını **Datetimeoffest** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-158">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="d228a-159">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d228a-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="d228a-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d228a-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="d228a-161">Bu zamanlama nesnesinin yazılım güncelleştirme yapılandırması zamanlamasında kullanılacağını gösterir</span><span class="sxs-lookup"><span data-stu-id="d228a-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="d228a-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="d228a-162">-HourInterval</span></span>
<span data-ttu-id="d228a-163">Zamanlama için zaman aralığını saat olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="d228a-164">-Monthınterval</span><span class="sxs-lookup"><span data-stu-id="d228a-164">-MonthInterval</span></span>
<span data-ttu-id="d228a-165">Zamanlama için bir aralığı ay olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="d228a-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="d228a-166">-Name</span></span>
<span data-ttu-id="d228a-167">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="d228a-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="d228a-168">-OneTime</span></span>
<span data-ttu-id="d228a-169">Cmdlet 'in bir kerelik zamanlama oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="d228a-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d228a-170">-ResourceGroupName</span></span>
<span data-ttu-id="d228a-171">Bu cmdlet 'in zamanlama oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="d228a-172">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d228a-172">-StartTime</span></span>
<span data-ttu-id="d228a-173">Bir zamanlamanın başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d228a-174">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d228a-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="d228a-175">*TimeZone* parametresi belirtilmişse, uzaklık gözardı edilir ve belirtilen saat dilimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d228a-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="d228a-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="d228a-176">-TimeZone</span></span>
<span data-ttu-id="d228a-177">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="d228a-178">Bu dize, ıANA KIMLIĞI veya Windows saat dilimi KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="d228a-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="d228a-179">-Haftaaralığı</span><span class="sxs-lookup"><span data-stu-id="d228a-179">-WeekInterval</span></span>
<span data-ttu-id="d228a-180">Zamanlama için hafta cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="d228a-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="d228a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d228a-181">CommonParameters</span></span>
<span data-ttu-id="d228a-182">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d228a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d228a-183">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d228a-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d228a-184">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d228a-184">INPUTS</span></span>

### <span data-ttu-id="d228a-185">System. String</span><span class="sxs-lookup"><span data-stu-id="d228a-185">System.String</span></span>

### <span data-ttu-id="d228a-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d228a-186">System.DateTimeOffset</span></span>

## <span data-ttu-id="d228a-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d228a-187">OUTPUTS</span></span>

### <span data-ttu-id="d228a-188">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="d228a-188">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="d228a-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d228a-189">NOTES</span></span>

## <span data-ttu-id="d228a-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d228a-190">RELATED LINKS</span></span>

[<span data-ttu-id="d228a-191">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d228a-191">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d228a-192">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d228a-192">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d228a-193">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d228a-193">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


