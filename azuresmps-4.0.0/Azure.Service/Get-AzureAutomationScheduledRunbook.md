---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106357"
---
# <span data-ttu-id="e34a8-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e34a8-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="e34a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e34a8-102">SYNOPSIS</span></span>

<span data-ttu-id="e34a8-103">Azure Otomasyonu runbook 'ları ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="e34a8-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="e34a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e34a8-104">SYNTAX</span></span>

### <span data-ttu-id="e34a8-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e34a8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e34a8-106">Byjobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="e34a8-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e34a8-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="e34a8-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e34a8-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="e34a8-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e34a8-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="e34a8-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e34a8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e34a8-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e34a8-111">**Get-AzureAutomationScheduledRunbook** , bir veya daha fazla Azure Automation runbook 'u ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="e34a8-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="e34a8-112">Varsayılan olarak, tüm zamanlanmış runbook 'lar döndürülür.</span><span class="sxs-lookup"><span data-stu-id="e34a8-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="e34a8-113">Belirli bir planlı runbook almak için Runbook adını ve zamanlama adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e34a8-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="e34a8-114">Runbook ile ilişkili tüm zamanlamaları almak için yalnızca runbook adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e34a8-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="e34a8-115">Bir zamanlamayla ilişkilendirilmiş tüm runbook 'ları almak için yalnızca zamanlama adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e34a8-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="e34a8-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e34a8-116">EXAMPLES</span></span>

### <span data-ttu-id="e34a8-117">Örnek 1: tüm zamanlanmış runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="e34a8-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e34a8-118">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="e34a8-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e34a8-119">Örnek 2: runbook ile ilişkili tüm zamanlamaları alma</span><span class="sxs-lookup"><span data-stu-id="e34a8-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="e34a8-120">Bu komut, Contoso17 adındaki Otomasyon hesabındaki runbook Runbk01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="e34a8-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e34a8-121">Örnek 3: zamanlamayla ilişkili tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="e34a8-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="e34a8-122">Bu komut, Contoso17 adındaki Otomasyon hesabındaki zamanlama Schedule01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="e34a8-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e34a8-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e34a8-123">PARAMETERS</span></span>

### <span data-ttu-id="e34a8-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e34a8-124">-AutomationAccountName</span></span>
<span data-ttu-id="e34a8-125">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e34a8-125">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="e34a8-126">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="e34a8-126">-JobScheduleId</span></span>
<span data-ttu-id="e34a8-127">Zamanlanmış işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e34a8-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34a8-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="e34a8-128">-Profile</span></span>
<span data-ttu-id="e34a8-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e34a8-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e34a8-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e34a8-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e34a8-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e34a8-131">-RunbookName</span></span>
<span data-ttu-id="e34a8-132">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e34a8-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34a8-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="e34a8-133">-ScheduleName</span></span>
<span data-ttu-id="e34a8-134">Bir zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e34a8-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e34a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34a8-135">CommonParameters</span></span>
<span data-ttu-id="e34a8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e34a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34a8-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e34a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34a8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e34a8-138">INPUTS</span></span>

## <span data-ttu-id="e34a8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e34a8-139">OUTPUTS</span></span>

### <span data-ttu-id="e34a8-140">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="e34a8-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="e34a8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e34a8-141">NOTES</span></span>

## <span data-ttu-id="e34a8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e34a8-142">RELATED LINKS</span></span>

[<span data-ttu-id="e34a8-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e34a8-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="e34a8-144">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="e34a8-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


