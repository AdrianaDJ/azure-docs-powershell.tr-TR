---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762885"
---
# <span data-ttu-id="37289-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="37289-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="37289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37289-102">SYNOPSIS</span></span>
<span data-ttu-id="37289-103">Otomasyon zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37289-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37289-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37289-104">SYNTAX</span></span>

### <span data-ttu-id="37289-105">Günlük (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37289-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37289-106">Haftalık</span><span class="sxs-lookup"><span data-stu-id="37289-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37289-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="37289-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37289-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="37289-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37289-109">Saat</span><span class="sxs-lookup"><span data-stu-id="37289-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37289-110">Saat</span><span class="sxs-lookup"><span data-stu-id="37289-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37289-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="37289-111">DESCRIPTION</span></span>
<span data-ttu-id="37289-112">**Yeni-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'nda bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37289-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="37289-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37289-113">EXAMPLES</span></span>

### <span data-ttu-id="37289-114">Örnek 1: yerel saatte bir kerelik bir zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="37289-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="37289-115">İlk komut, sistemden saat dilimi KIMLIĞINI alır ve $TimeZone değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="37289-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="37289-116">İkinci komut, belirli bir saat diliminde 11:00 saatinde geçerli tarihte bir kez çalışan bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37289-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="37289-117">Örnek 2: Yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="37289-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="37289-118">İlk komut **Get-Date** cmdlet 'ini kullanarak Date nesnesi oluşturur ve nesneyi $StartDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="37289-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="37289-119">Gelecekte en az beş dakikalık bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="37289-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="37289-120">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir Date nesnesi oluşturur ve nesneyi $EndDate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="37289-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="37289-121">Komut gelecekteki bir zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-121">The command specifies a future time.</span></span>

<span data-ttu-id="37289-122">Son komutu, $StartDate uygulamasında depolanan zamandan başlayıp $EndDate içinde depolanan tarihte sona erecek şekilde Schedule01 adlı günlük bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37289-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="37289-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37289-123">PARAMETERS</span></span>

### <span data-ttu-id="37289-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37289-124">-AutomationAccountName</span></span>
<span data-ttu-id="37289-125">Bu cmdlet 'in zamanlama oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="37289-126">-Dayınterval</span><span class="sxs-lookup"><span data-stu-id="37289-126">-DayInterval</span></span>
<span data-ttu-id="37289-127">Zamanlama için gün cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="37289-128">Bu parametreyi belirtmezseniz ve *Onetime* parametresini belirtmezseniz, varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="37289-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="37289-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="37289-129">-DayOfWeek</span></span>
<span data-ttu-id="37289-130">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="37289-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="37289-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="37289-132">Zamanlamanın çalıştığı ay içinde haftanın oluşumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="37289-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="37289-133">psdx_paramvalues</span></span>

- <span data-ttu-id="37289-134">2</span><span class="sxs-lookup"><span data-stu-id="37289-134">1</span></span>
- <span data-ttu-id="37289-135">2</span><span class="sxs-lookup"><span data-stu-id="37289-135">2</span></span>
- <span data-ttu-id="37289-136">@</span><span class="sxs-lookup"><span data-stu-id="37289-136">3</span></span>
- <span data-ttu-id="37289-137">1.921.024</span><span class="sxs-lookup"><span data-stu-id="37289-137">4</span></span>
- <span data-ttu-id="37289-138">-1</span><span class="sxs-lookup"><span data-stu-id="37289-138">-1</span></span>
- <span data-ttu-id="37289-139">Eklemelisiniz</span><span class="sxs-lookup"><span data-stu-id="37289-139">First</span></span>
- <span data-ttu-id="37289-140">İden</span><span class="sxs-lookup"><span data-stu-id="37289-140">Second</span></span>
- <span data-ttu-id="37289-141">Üç</span><span class="sxs-lookup"><span data-stu-id="37289-141">Third</span></span>
- <span data-ttu-id="37289-142">Dördüncü</span><span class="sxs-lookup"><span data-stu-id="37289-142">Fourth</span></span>
- <span data-ttu-id="37289-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="37289-143">LastDay</span></span>

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

### <span data-ttu-id="37289-144">-Daysofay</span><span class="sxs-lookup"><span data-stu-id="37289-144">-DaysOfMonth</span></span>
<span data-ttu-id="37289-145">Aylık zamanlama için ayın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="37289-146">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="37289-146">-DaysOfWeek</span></span>
<span data-ttu-id="37289-147">Haftalık zamanlama için haftanın günleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="37289-148">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="37289-148">-Description</span></span>
<span data-ttu-id="37289-149">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="37289-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="37289-150">-ExpiryTime</span></span>
<span data-ttu-id="37289-151">Bir zamanlamanın sona erme zamanını **Datetimeoffest** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="37289-152">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37289-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="37289-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="37289-153">-HourInterval</span></span>
<span data-ttu-id="37289-154">Zamanlama için zaman aralığını saat olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="37289-155">-Monthınterval</span><span class="sxs-lookup"><span data-stu-id="37289-155">-MonthInterval</span></span>
<span data-ttu-id="37289-156">Zamanlama için bir aralığı ay olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="37289-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="37289-157">-Name</span></span>
<span data-ttu-id="37289-158">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="37289-159">-OneTime</span><span class="sxs-lookup"><span data-stu-id="37289-159">-OneTime</span></span>
<span data-ttu-id="37289-160">Cmdlet 'in bir kerelik zamanlama oluşturacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="37289-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37289-161">-ResourceGroupName</span></span>
<span data-ttu-id="37289-162">Bu cmdlet 'in zamanlama oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="37289-163">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="37289-163">-StartTime</span></span>
<span data-ttu-id="37289-164">Bir zamanlamanın başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="37289-165">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37289-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="37289-166">.</span><span class="sxs-lookup"><span data-stu-id="37289-166">.</span></span> <span data-ttu-id="37289-167">*TimeZone* parametresi belirtilmişse, uzaklık gözardı edilir ve belirtilen saat dilimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37289-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="37289-168">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="37289-168">-TimeZone</span></span>
<span data-ttu-id="37289-169">Zamanlamanın saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="37289-170">Bu dize, ıANA KIMLIĞI veya Windows saat dilimi KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="37289-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="37289-171">-Haftaaralığı</span><span class="sxs-lookup"><span data-stu-id="37289-171">-WeekInterval</span></span>
<span data-ttu-id="37289-172">Zamanlama için hafta cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="37289-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="37289-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37289-173">-DefaultProfile</span></span>
<span data-ttu-id="37289-174">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37289-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37289-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37289-175">CommonParameters</span></span>
<span data-ttu-id="37289-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37289-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37289-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37289-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37289-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37289-178">INPUTS</span></span>

## <span data-ttu-id="37289-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37289-179">OUTPUTS</span></span>

### <span data-ttu-id="37289-180">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="37289-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="37289-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37289-181">NOTES</span></span>

## <span data-ttu-id="37289-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37289-182">RELATED LINKS</span></span>

[<span data-ttu-id="37289-183">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="37289-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="37289-184">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="37289-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="37289-185">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="37289-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


