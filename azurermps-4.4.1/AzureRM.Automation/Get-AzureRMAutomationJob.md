---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595041"
---
# <span data-ttu-id="c06d3-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c06d3-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="c06d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c06d3-103">Otomasyon Runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c06d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c06d3-104">SYNTAX</span></span>

### <span data-ttu-id="c06d3-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c06d3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c06d3-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="c06d3-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c06d3-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c06d3-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c06d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c06d3-108">DESCRIPTION</span></span>
<span data-ttu-id="c06d3-109">**Get-AzureRmAutomationJob** cmdlet 'ı, Azure Otomasyonu 'ndaki runbook işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="c06d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c06d3-110">EXAMPLES</span></span>

### <span data-ttu-id="c06d3-111">Örnek 1: belirli bir runbook işini edinme</span><span class="sxs-lookup"><span data-stu-id="c06d3-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="c06d3-112">Bu komut belirtilen GUID 'ye sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="c06d3-113">Örnek 2: runbook için tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="c06d3-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="c06d3-114">Bu komut, Runbook02 adındaki runbook ile ilişkili tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="c06d3-115">Örnek 3: çalışan tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="c06d3-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="c06d3-116">Bu komut, Contoso17 adlı Otomasyon hesabında çalışan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c06d3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c06d3-117">PARAMETERS</span></span>

### <span data-ttu-id="c06d3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c06d3-118">-AutomationAccountName</span></span>
<span data-ttu-id="c06d3-119">Bu cmdlet 'in işleri aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c06d3-120">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="c06d3-120">-EndTime</span></span>
<span data-ttu-id="c06d3-121">Bir işin bitiş zamanını **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c06d3-122">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c06d3-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c06d3-123">Bu cmdlet, bitiş saati olan işleri bu parametrenin belirttiği değerle alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c06d3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c06d3-124">-Id</span></span>
<span data-ttu-id="c06d3-125">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c06d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="c06d3-127">Bu cmdlet 'in işleri aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c06d3-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c06d3-128">-RunbookName</span></span>
<span data-ttu-id="c06d3-129">Bu cmdlet 'in işleri aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c06d3-130">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c06d3-130">-StartTime</span></span>
<span data-ttu-id="c06d3-131">Bir işin başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c06d3-132">Bu cmdlet, başlangıç saati olan veya bu parametrenin belirttiği değerden sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="c06d3-133">-Durum</span><span class="sxs-lookup"><span data-stu-id="c06d3-133">-Status</span></span>
<span data-ttu-id="c06d3-134">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c06d3-134">Specifies the status of a job.</span></span>
<span data-ttu-id="c06d3-135">Bu cmdlet, Bu parametreyle eşleşen bir durumu olan işleri alır.</span><span class="sxs-lookup"><span data-stu-id="c06d3-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="c06d3-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c06d3-136">Valid values are:</span></span> 

- <span data-ttu-id="c06d3-137">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="c06d3-137">Activating</span></span>
- <span data-ttu-id="c06d3-138">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="c06d3-138">Completed</span></span>
- <span data-ttu-id="c06d3-139">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="c06d3-139">Failed</span></span>
- <span data-ttu-id="c06d3-140">Sıradan</span><span class="sxs-lookup"><span data-stu-id="c06d3-140">Queued</span></span>
- <span data-ttu-id="c06d3-141">İlirken</span><span class="sxs-lookup"><span data-stu-id="c06d3-141">Resuming</span></span>
- <span data-ttu-id="c06d3-142">Çalışması</span><span class="sxs-lookup"><span data-stu-id="c06d3-142">Running</span></span>
- <span data-ttu-id="c06d3-143">Başlarken</span><span class="sxs-lookup"><span data-stu-id="c06d3-143">Starting</span></span>
- <span data-ttu-id="c06d3-144">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="c06d3-144">Stopped</span></span>
- <span data-ttu-id="c06d3-145">Arak</span><span class="sxs-lookup"><span data-stu-id="c06d3-145">Stopping</span></span>
- <span data-ttu-id="c06d3-146">Etsin</span><span class="sxs-lookup"><span data-stu-id="c06d3-146">Suspended</span></span>
- <span data-ttu-id="c06d3-147">Et</span><span class="sxs-lookup"><span data-stu-id="c06d3-147">Suspending</span></span>

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

### <span data-ttu-id="c06d3-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06d3-148">-DefaultProfile</span></span>
<span data-ttu-id="c06d3-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c06d3-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c06d3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06d3-150">CommonParameters</span></span>
<span data-ttu-id="c06d3-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c06d3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06d3-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c06d3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06d3-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c06d3-153">INPUTS</span></span>

## <span data-ttu-id="c06d3-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c06d3-154">OUTPUTS</span></span>

### <span data-ttu-id="c06d3-155">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="c06d3-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c06d3-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c06d3-156">NOTES</span></span>

## <span data-ttu-id="c06d3-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c06d3-157">RELATED LINKS</span></span>

[<span data-ttu-id="c06d3-158">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="c06d3-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="c06d3-159">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c06d3-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c06d3-160">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c06d3-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="c06d3-161">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c06d3-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


