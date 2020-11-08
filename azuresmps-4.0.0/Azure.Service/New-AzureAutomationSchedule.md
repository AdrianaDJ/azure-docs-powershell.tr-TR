---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106219"
---
# <span data-ttu-id="3d0a9-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3d0a9-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="3d0a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d0a9-102">SYNOPSIS</span></span>

<span data-ttu-id="3d0a9-103">Otomasyon zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="3d0a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d0a9-104">SYNTAX</span></span>

### <span data-ttu-id="3d0a9-105">Günlük (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d0a9-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d0a9-106">Saat</span><span class="sxs-lookup"><span data-stu-id="3d0a9-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d0a9-107">Saat</span><span class="sxs-lookup"><span data-stu-id="3d0a9-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d0a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d0a9-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3d0a9-109">**New-Azureautomationzamanlama** cmdlet 'ı Microsoft Azure Otomasyonu 'nda bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3d0a9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d0a9-110">EXAMPLES</span></span>

### <span data-ttu-id="3d0a9-111">Örnek 1: tek seferlik zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="3d0a9-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="3d0a9-112">Aşağıdaki komut, 11:00 PM 'deki geçerli tarihte bir kez çalışan bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="3d0a9-113">Örnek 2: Yinelenen zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="3d0a9-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="3d0a9-114">Aşağıdaki komutlar, geçerli günde bir yıl boyunca her gün bir yıl boyunca 1:00 saatinde çalışan yeni bir zamanlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="3d0a9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d0a9-115">PARAMETERS</span></span>

### <span data-ttu-id="3d0a9-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d0a9-116">-AutomationAccountName</span></span>
<span data-ttu-id="3d0a9-117">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-117">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0a9-118">-Dayınterval</span><span class="sxs-lookup"><span data-stu-id="3d0a9-118">-DayInterval</span></span>
<span data-ttu-id="3d0a9-119">Zamanlama için gün cinsinden bir Aralık belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-119">Specifies an interval, in days, for the schedule.</span></span>

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

### <span data-ttu-id="3d0a9-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3d0a9-120">-Description</span></span>
<span data-ttu-id="3d0a9-121">Bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-121">Specifies a description.</span></span>

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

### <span data-ttu-id="3d0a9-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d0a9-122">-ExpiryTime</span></span>
<span data-ttu-id="3d0a9-123">Zamanlamanın sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="3d0a9-124">Dize geçerli bir **DateTime** 'a dönüştürülebildiğinden sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d0a9-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="3d0a9-125">-HourInterval</span></span>
<span data-ttu-id="3d0a9-126">Zamanlama için zaman aralığını saat olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-126">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="3d0a9-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d0a9-127">-Name</span></span>
<span data-ttu-id="3d0a9-128">Zamanlama için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-128">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0a9-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="3d0a9-129">-OneTime</span></span>
<span data-ttu-id="3d0a9-130">Bu işlemin bir kerelik bir zamanlama oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-130">Indicates that this operation creates a one-time schedule.</span></span>

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

### <span data-ttu-id="3d0a9-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d0a9-131">-Profile</span></span>
<span data-ttu-id="3d0a9-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d0a9-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d0a9-134">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="3d0a9-134">-StartTime</span></span>
<span data-ttu-id="3d0a9-135">Zamanlamanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="3d0a9-136">Dize geçerli bir **DateTime** 'a dönüştürülebildiğinden sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0a9-137">CommonParameters</span></span>
<span data-ttu-id="3d0a9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d0a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0a9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d0a9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0a9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d0a9-140">INPUTS</span></span>

## <span data-ttu-id="3d0a9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d0a9-141">OUTPUTS</span></span>

### <span data-ttu-id="3d0a9-142">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="3d0a9-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3d0a9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d0a9-143">NOTES</span></span>

## <span data-ttu-id="3d0a9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d0a9-144">RELATED LINKS</span></span>

[<span data-ttu-id="3d0a9-145">Get-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3d0a9-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="3d0a9-146">Remove-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3d0a9-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="3d0a9-147">Set-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3d0a9-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


