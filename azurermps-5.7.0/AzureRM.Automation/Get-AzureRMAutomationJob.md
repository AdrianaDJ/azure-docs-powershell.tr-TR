---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 3183720cbafc9a8feae5c9687dfb92ab325f8b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586831"
---
# <span data-ttu-id="34859-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34859-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="34859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34859-102">SYNOPSIS</span></span>
<span data-ttu-id="34859-103">Otomasyon Runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="34859-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34859-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34859-104">SYNTAX</span></span>

### <span data-ttu-id="34859-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34859-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34859-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="34859-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34859-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="34859-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34859-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34859-108">DESCRIPTION</span></span>
<span data-ttu-id="34859-109">**Get-AzureRmAutomationJob** cmdlet 'ı, Azure Otomasyonu 'ndaki runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="34859-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="34859-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34859-110">EXAMPLES</span></span>

### <span data-ttu-id="34859-111">Örnek 1: belirli bir runbook işini edinme</span><span class="sxs-lookup"><span data-stu-id="34859-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="34859-112">Bu komut belirtilen GUID 'ye sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="34859-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="34859-113">Örnek 2: runbook için tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="34859-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="34859-114">Bu komut, Runbook02 adındaki runbook ile ilişkili tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="34859-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="34859-115">Örnek 3: çalışan tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="34859-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="34859-116">Bu komut, Contoso17 adlı Otomasyon hesabında çalışan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="34859-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="34859-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34859-117">PARAMETERS</span></span>

### <span data-ttu-id="34859-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34859-118">-AutomationAccountName</span></span>
<span data-ttu-id="34859-119">Bu cmdlet 'in işleri aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="34859-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34859-120">-DefaultProfile</span></span>
<span data-ttu-id="34859-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="34859-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34859-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="34859-122">-EndTime</span></span>
<span data-ttu-id="34859-123">Bir işin bitiş zamanını **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="34859-124">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34859-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="34859-125">Bu cmdlet, bitiş saati olan işleri bu parametrenin belirttiği değerle alır.</span><span class="sxs-lookup"><span data-stu-id="34859-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="34859-126">-ID</span><span class="sxs-lookup"><span data-stu-id="34859-126">-Id</span></span>
<span data-ttu-id="34859-127">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="34859-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34859-128">-ResourceGroupName</span></span>
<span data-ttu-id="34859-129">Bu cmdlet 'in işleri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="34859-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="34859-130">-RunbookName</span></span>
<span data-ttu-id="34859-131">Bu cmdlet 'in işleri aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="34859-132">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="34859-132">-StartTime</span></span>
<span data-ttu-id="34859-133">Bir işin başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="34859-134">Bu cmdlet, başlangıç saati olan veya bu parametrenin belirttiği değerden sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="34859-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="34859-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="34859-135">-Status</span></span>
<span data-ttu-id="34859-136">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34859-136">Specifies the status of a job.</span></span>
<span data-ttu-id="34859-137">Bu cmdlet, Bu parametreyle eşleşen bir durumu olan işleri alır.</span><span class="sxs-lookup"><span data-stu-id="34859-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="34859-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="34859-138">Valid values are:</span></span> 

- <span data-ttu-id="34859-139">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="34859-139">Activating</span></span>
- <span data-ttu-id="34859-140">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="34859-140">Completed</span></span>
- <span data-ttu-id="34859-141">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="34859-141">Failed</span></span>
- <span data-ttu-id="34859-142">Sıradan</span><span class="sxs-lookup"><span data-stu-id="34859-142">Queued</span></span>
- <span data-ttu-id="34859-143">İlirken</span><span class="sxs-lookup"><span data-stu-id="34859-143">Resuming</span></span>
- <span data-ttu-id="34859-144">Çalışması</span><span class="sxs-lookup"><span data-stu-id="34859-144">Running</span></span>
- <span data-ttu-id="34859-145">Başlarken</span><span class="sxs-lookup"><span data-stu-id="34859-145">Starting</span></span>
- <span data-ttu-id="34859-146">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="34859-146">Stopped</span></span>
- <span data-ttu-id="34859-147">Arak</span><span class="sxs-lookup"><span data-stu-id="34859-147">Stopping</span></span>
- <span data-ttu-id="34859-148">Etsin</span><span class="sxs-lookup"><span data-stu-id="34859-148">Suspended</span></span>
- <span data-ttu-id="34859-149">Et</span><span class="sxs-lookup"><span data-stu-id="34859-149">Suspending</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34859-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34859-150">CommonParameters</span></span>
<span data-ttu-id="34859-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34859-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34859-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34859-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34859-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34859-153">INPUTS</span></span>

### <span data-ttu-id="34859-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34859-154">None</span></span>
<span data-ttu-id="34859-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="34859-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34859-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34859-156">OUTPUTS</span></span>

### <span data-ttu-id="34859-157">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="34859-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="34859-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34859-158">NOTES</span></span>

## <span data-ttu-id="34859-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34859-159">RELATED LINKS</span></span>

[<span data-ttu-id="34859-160">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="34859-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="34859-161">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34859-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="34859-162">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34859-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="34859-163">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34859-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


