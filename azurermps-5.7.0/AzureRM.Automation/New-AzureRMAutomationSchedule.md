---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593755"
---
# <span data-ttu-id="c4fbe-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c4fbe-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="c4fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fbe-103">Otomasyon zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4fbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4fbe-104">SYNTAX</span></span>

### <span data-ttu-id="c4fbe-105">Günlük (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4fbe-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4fbe-106">Haftalık</span><span class="sxs-lookup"><span data-stu-id="c4fbe-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4fbe-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="c4fbe-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4fbe-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="c4fbe-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4fbe-109">Saat</span><span class="sxs-lookup"><span data-stu-id="c4fbe-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4fbe-110">Saat</span><span class="sxs-lookup"><span data-stu-id="c4fbe-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4fbe-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4fbe-111">DESCRIPTION</span></span>
<span data-ttu-id="c4fbe-112">**Yeni-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'nda bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="c4fbe-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4fbe-113">EXAMPLES</span></span>

### <span data-ttu-id="c4fbe-114">Örnek 1: yerel saatte bir kerelik bir zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="c4fbe-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="c4fbe-115">İlk komut, sistemden saat dilimi KIMLIĞINI alır ve $TimeZone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="c4fbe-116">İkinci komut, belirli bir saat diliminde 11:00 saatinde geçerli tarihte bir kez çalışan bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="c4fbe-117">Örnek 2: Yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="c4fbe-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c4fbe-118">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="c4fbe-119">Gelecekte en az beş dakikalık bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="c4fbe-120">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir Date nesnesi oluşturur ve nesneyi $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="c4fbe-121">Komut gelecekteki bir zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-121">The command specifies a future time.</span></span>

<span data-ttu-id="c4fbe-122">Son komutu, $StartDate uygulamasında depolanan zamandan başlayıp $EndDate içinde depolanan tarihte sona erecek şekilde Schedule01 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="c4fbe-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4fbe-123">PARAMETERS</span></span>

### <span data-ttu-id="c4fbe-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4fbe-124">-AutomationAccountName</span></span>
<span data-ttu-id="c4fbe-125">Bu cmdlet 'in zamanlama oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-126">-Dayınterval</span><span class="sxs-lookup"><span data-stu-id="c4fbe-126">-DayInterval</span></span>
<span data-ttu-id="c4fbe-127">Zamanlama için gün cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="c4fbe-128">Bu parametreyi belirtmezseniz ve *Onetime* parametresini belirtmezseniz, varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="c4fbe-129">-DayOfWeek</span></span>
<span data-ttu-id="c4fbe-130">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="c4fbe-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="c4fbe-132">Zamanlamanın çalıştığı ay içinde haftanın oluşumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="c4fbe-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c4fbe-133">psdx_paramvalues</span></span>

- <span data-ttu-id="c4fbe-134">2</span><span class="sxs-lookup"><span data-stu-id="c4fbe-134">1</span></span>
- <span data-ttu-id="c4fbe-135">2</span><span class="sxs-lookup"><span data-stu-id="c4fbe-135">2</span></span>
- <span data-ttu-id="c4fbe-136">@</span><span class="sxs-lookup"><span data-stu-id="c4fbe-136">3</span></span>
- <span data-ttu-id="c4fbe-137">1.921.024</span><span class="sxs-lookup"><span data-stu-id="c4fbe-137">4</span></span>
- <span data-ttu-id="c4fbe-138">-1</span><span class="sxs-lookup"><span data-stu-id="c4fbe-138">-1</span></span>
- <span data-ttu-id="c4fbe-139">Eklemelisiniz</span><span class="sxs-lookup"><span data-stu-id="c4fbe-139">First</span></span>
- <span data-ttu-id="c4fbe-140">İden</span><span class="sxs-lookup"><span data-stu-id="c4fbe-140">Second</span></span>
- <span data-ttu-id="c4fbe-141">Üç</span><span class="sxs-lookup"><span data-stu-id="c4fbe-141">Third</span></span>
- <span data-ttu-id="c4fbe-142">Dördüncü</span><span class="sxs-lookup"><span data-stu-id="c4fbe-142">Fourth</span></span>
- <span data-ttu-id="c4fbe-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="c4fbe-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-144">-Daysofay</span><span class="sxs-lookup"><span data-stu-id="c4fbe-144">-DaysOfMonth</span></span>
<span data-ttu-id="c4fbe-145">Aylık zamanlama için ayın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-146">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="c4fbe-146">-DaysOfWeek</span></span>
<span data-ttu-id="c4fbe-147">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fbe-148">-DefaultProfile</span></span>
<span data-ttu-id="c4fbe-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4fbe-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4fbe-150">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c4fbe-150">-Description</span></span>
<span data-ttu-id="c4fbe-151">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c4fbe-152">-ExpiryTime</span></span>
<span data-ttu-id="c4fbe-153">Bir zamanlamanın sona erme zamanını **Datetimeoffest** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="c4fbe-154">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="c4fbe-155">-HourInterval</span></span>
<span data-ttu-id="c4fbe-156">Zamanlama için zaman aralığını saat olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-157">-Monthınterval</span><span class="sxs-lookup"><span data-stu-id="c4fbe-157">-MonthInterval</span></span>
<span data-ttu-id="c4fbe-158">Zamanlama için bir aralığı ay olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4fbe-159">-Name</span></span>
<span data-ttu-id="c4fbe-160">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-161">-OneTime</span><span class="sxs-lookup"><span data-stu-id="c4fbe-161">-OneTime</span></span>
<span data-ttu-id="c4fbe-162">Cmdlet 'in bir kerelik zamanlama oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fbe-163">-ResourceGroupName</span></span>
<span data-ttu-id="c4fbe-164">Bu cmdlet 'in zamanlama oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-165">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c4fbe-165">-StartTime</span></span>
<span data-ttu-id="c4fbe-166">Bir zamanlamanın başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c4fbe-167">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c4fbe-168">.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-168">.</span></span> <span data-ttu-id="c4fbe-169">*TimeZone* parametresi belirtilmişse, uzaklık gözardı edilir ve belirtilen saat dilimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-170">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c4fbe-170">-TimeZone</span></span>
<span data-ttu-id="c4fbe-171">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="c4fbe-172">Bu dize, ıANA KIMLIĞI veya Windows saat dilimi KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-173">-Haftaaralığı</span><span class="sxs-lookup"><span data-stu-id="c4fbe-173">-WeekInterval</span></span>
<span data-ttu-id="c4fbe-174">Zamanlama için hafta cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4fbe-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fbe-175">CommonParameters</span></span>
<span data-ttu-id="c4fbe-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fbe-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fbe-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fbe-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4fbe-178">INPUTS</span></span>

### <span data-ttu-id="c4fbe-179">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c4fbe-179">None</span></span>
<span data-ttu-id="c4fbe-180">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c4fbe-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4fbe-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4fbe-181">OUTPUTS</span></span>

### <span data-ttu-id="c4fbe-182">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="c4fbe-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="c4fbe-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4fbe-183">NOTES</span></span>

## <span data-ttu-id="c4fbe-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4fbe-184">RELATED LINKS</span></span>

[<span data-ttu-id="c4fbe-185">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="c4fbe-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c4fbe-186">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="c4fbe-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="c4fbe-187">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="c4fbe-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


