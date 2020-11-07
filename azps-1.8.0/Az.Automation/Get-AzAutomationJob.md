---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: ae638c693366568458a4194d1625d19eaac6af93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761613"
---
# <span data-ttu-id="60f75-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="60f75-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="60f75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f75-102">SYNOPSIS</span></span>
<span data-ttu-id="60f75-103">Otomasyon Runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="60f75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60f75-104">SYNTAX</span></span>

### <span data-ttu-id="60f75-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60f75-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60f75-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="60f75-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60f75-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="60f75-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60f75-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60f75-108">DESCRIPTION</span></span>
<span data-ttu-id="60f75-109">**Get-AzAutomationJob** cmdlet 'ı, Azure Otomasyonu 'ndaki runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="60f75-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60f75-110">EXAMPLES</span></span>

### <span data-ttu-id="60f75-111">Örnek 1: belirli bir runbook işini edinme</span><span class="sxs-lookup"><span data-stu-id="60f75-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="60f75-112">Bu komut belirtilen GUID 'ye sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="60f75-113">Örnek 2: runbook için tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="60f75-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="60f75-114">Bu komut, Runbook02 adındaki runbook ile ilişkili tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="60f75-115">Örnek 3: çalışan tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="60f75-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="60f75-116">Bu komut, Contoso17 adlı Otomasyon hesabında çalışan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="60f75-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60f75-117">PARAMETERS</span></span>

### <span data-ttu-id="60f75-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60f75-118">-AutomationAccountName</span></span>
<span data-ttu-id="60f75-119">Bu cmdlet 'in işleri aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="60f75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f75-120">-DefaultProfile</span></span>
<span data-ttu-id="60f75-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="60f75-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f75-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="60f75-122">-EndTime</span></span>
<span data-ttu-id="60f75-123">Bir işin bitiş zamanını **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="60f75-124">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f75-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="60f75-125">Bu cmdlet, bitiş saati olan işleri bu parametrenin belirttiği değerle alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f75-126">-ID</span><span class="sxs-lookup"><span data-stu-id="60f75-126">-Id</span></span>
<span data-ttu-id="60f75-127">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60f75-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f75-128">-ResourceGroupName</span></span>
<span data-ttu-id="60f75-129">Bu cmdlet 'in işleri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="60f75-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="60f75-130">-RunbookName</span></span>
<span data-ttu-id="60f75-131">Bu cmdlet 'in işleri aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f75-132">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="60f75-132">-StartTime</span></span>
<span data-ttu-id="60f75-133">Bir işin başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="60f75-134">Bu cmdlet, başlangıç saati olan veya bu parametrenin belirttiği değerden sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f75-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="60f75-135">-Status</span></span>
<span data-ttu-id="60f75-136">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="60f75-136">Specifies the status of a job.</span></span>
<span data-ttu-id="60f75-137">Bu cmdlet, Bu parametreyle eşleşen bir durumu olan işleri alır.</span><span class="sxs-lookup"><span data-stu-id="60f75-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="60f75-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="60f75-138">Valid values are:</span></span> 
- <span data-ttu-id="60f75-139">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="60f75-139">Activating</span></span>
- <span data-ttu-id="60f75-140">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="60f75-140">Completed</span></span>
- <span data-ttu-id="60f75-141">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="60f75-141">Failed</span></span>
- <span data-ttu-id="60f75-142">Sıradan</span><span class="sxs-lookup"><span data-stu-id="60f75-142">Queued</span></span>
- <span data-ttu-id="60f75-143">İlirken</span><span class="sxs-lookup"><span data-stu-id="60f75-143">Resuming</span></span>
- <span data-ttu-id="60f75-144">Çalışması</span><span class="sxs-lookup"><span data-stu-id="60f75-144">Running</span></span>
- <span data-ttu-id="60f75-145">Başlarken</span><span class="sxs-lookup"><span data-stu-id="60f75-145">Starting</span></span>
- <span data-ttu-id="60f75-146">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="60f75-146">Stopped</span></span>
- <span data-ttu-id="60f75-147">Arak</span><span class="sxs-lookup"><span data-stu-id="60f75-147">Stopping</span></span>
- <span data-ttu-id="60f75-148">Etsin</span><span class="sxs-lookup"><span data-stu-id="60f75-148">Suspended</span></span>
- <span data-ttu-id="60f75-149">Et</span><span class="sxs-lookup"><span data-stu-id="60f75-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f75-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f75-150">CommonParameters</span></span>
<span data-ttu-id="60f75-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60f75-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f75-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f75-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f75-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60f75-153">INPUTS</span></span>

### <span data-ttu-id="60f75-154">System. Guid</span><span class="sxs-lookup"><span data-stu-id="60f75-154">System.Guid</span></span>

### <span data-ttu-id="60f75-155">System. String</span><span class="sxs-lookup"><span data-stu-id="60f75-155">System.String</span></span>

## <span data-ttu-id="60f75-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60f75-156">OUTPUTS</span></span>

### <span data-ttu-id="60f75-157">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="60f75-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="60f75-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60f75-158">NOTES</span></span>

## <span data-ttu-id="60f75-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60f75-159">RELATED LINKS</span></span>

[<span data-ttu-id="60f75-160">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="60f75-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="60f75-161">Özgeçmiş-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="60f75-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="60f75-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="60f75-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="60f75-163">Askıya alma-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="60f75-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


