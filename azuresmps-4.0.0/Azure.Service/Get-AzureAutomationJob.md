---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106369"
---
# <span data-ttu-id="a8dae-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a8dae-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="a8dae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8dae-102">SYNOPSIS</span></span>

<span data-ttu-id="a8dae-103">Bir veya daha fazla Azure Otomasyonu runbook işini alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="a8dae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8dae-104">SYNTAX</span></span>

### <span data-ttu-id="a8dae-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8dae-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a8dae-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="a8dae-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8dae-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a8dae-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8dae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8dae-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a8dae-109">**Get-AzureAutomationJob** cmdlet 'ı, Microsoft Azure Otomasyonu 'nda bir veya birden çok runbook işini alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a8dae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8dae-110">EXAMPLES</span></span>

### <span data-ttu-id="a8dae-111">Örnek 1: belirli bir runbook işini edinme</span><span class="sxs-lookup"><span data-stu-id="a8dae-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="a8dae-112">Bu komut belirtilen GUID 'ye sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="a8dae-113">Örnek 2: runbook için tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="a8dae-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="a8dae-114">Bu komut MyRunbook adlı bir runbook ile ilişkilendirilmiş tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="a8dae-115">Örnek 2: çalışan tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="a8dae-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="a8dae-116">Bu komut, Otomasyon hesabındaki tüm çalışan işleri Contoso17 adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="a8dae-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8dae-117">PARAMETERS</span></span>

### <span data-ttu-id="a8dae-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a8dae-118">-AutomationAccountName</span></span>
<span data-ttu-id="a8dae-119">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="a8dae-120">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="a8dae-120">-EndTime</span></span>
<span data-ttu-id="a8dae-121">İşin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dae-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a8dae-122">-Id</span></span>
<span data-ttu-id="a8dae-123">İşin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dae-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="a8dae-124">-Profile</span></span>
<span data-ttu-id="a8dae-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8dae-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a8dae-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8dae-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a8dae-127">-RunbookName</span></span>
<span data-ttu-id="a8dae-128">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dae-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a8dae-129">-StartTime</span></span>
<span data-ttu-id="a8dae-130">İşin başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dae-131">-Durum</span><span class="sxs-lookup"><span data-stu-id="a8dae-131">-Status</span></span>
<span data-ttu-id="a8dae-132">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8dae-132">Specifies the status of a job.</span></span>
<span data-ttu-id="a8dae-133">Bu cmdlet, Bu parametreyle eşleşen bir durumu olan işleri alır.</span><span class="sxs-lookup"><span data-stu-id="a8dae-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="a8dae-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a8dae-134">Valid values are:</span></span> 

- <span data-ttu-id="a8dae-135">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="a8dae-135">Completed</span></span>
- <span data-ttu-id="a8dae-136">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="a8dae-136">Failed</span></span>
- <span data-ttu-id="a8dae-137">Sıradan</span><span class="sxs-lookup"><span data-stu-id="a8dae-137">Queued</span></span>
- <span data-ttu-id="a8dae-138">Başlarken</span><span class="sxs-lookup"><span data-stu-id="a8dae-138">Starting</span></span>
- <span data-ttu-id="a8dae-139">İlirken</span><span class="sxs-lookup"><span data-stu-id="a8dae-139">Resuming</span></span>
- <span data-ttu-id="a8dae-140">Çalışması</span><span class="sxs-lookup"><span data-stu-id="a8dae-140">Running</span></span>
- <span data-ttu-id="a8dae-141">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="a8dae-141">Stopped</span></span>
- <span data-ttu-id="a8dae-142">Arak</span><span class="sxs-lookup"><span data-stu-id="a8dae-142">Stopping</span></span>
- <span data-ttu-id="a8dae-143">Etsin</span><span class="sxs-lookup"><span data-stu-id="a8dae-143">Suspended</span></span>
- <span data-ttu-id="a8dae-144">Et</span><span class="sxs-lookup"><span data-stu-id="a8dae-144">Suspending</span></span>
- <span data-ttu-id="a8dae-145">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="a8dae-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8dae-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dae-146">CommonParameters</span></span>
<span data-ttu-id="a8dae-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8dae-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dae-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8dae-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dae-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8dae-149">INPUTS</span></span>

## <span data-ttu-id="a8dae-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8dae-150">OUTPUTS</span></span>

### <span data-ttu-id="a8dae-151">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="a8dae-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="a8dae-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8dae-152">NOTES</span></span>

## <span data-ttu-id="a8dae-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8dae-153">RELATED LINKS</span></span>

[<span data-ttu-id="a8dae-154">Özgeçmiş-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a8dae-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="a8dae-155">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a8dae-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="a8dae-156">Askıya alma-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a8dae-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


