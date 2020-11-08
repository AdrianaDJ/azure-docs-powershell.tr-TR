---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: b16939cdce5a4be471e1ae8133271349884e63a7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938731"
---
# <span data-ttu-id="053ce-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="053ce-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="053ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="053ce-102">SYNOPSIS</span></span>
<span data-ttu-id="053ce-103">İş için toplu Iş görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="053ce-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="053ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="053ce-104">SYNTAX</span></span>

### <span data-ttu-id="053ce-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="053ce-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="053ce-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="053ce-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="053ce-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="053ce-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="053ce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="053ce-108">DESCRIPTION</span></span>
<span data-ttu-id="053ce-109">**Get-AzBatchTask** cmdlet 'ı, toplu Iş Için Azure toplu görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="053ce-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="053ce-110">İş veya *iş* *parametresinden bir* iş belirtin.</span><span class="sxs-lookup"><span data-stu-id="053ce-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="053ce-111">Tek bir görev almak için *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="053ce-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="053ce-112">Açık bir veri Protokolü (OData) filtresi ile eşleşen görevleri almak için *filtre* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="053ce-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="053ce-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="053ce-113">EXAMPLES</span></span>

### <span data-ttu-id="053ce-114">Örnek 1: KIMLIĞE göre görev alma</span><span class="sxs-lookup"><span data-stu-id="053ce-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="053ce-115">Bu komut, iş Job01 altında KIMLIĞI Task03 olan görevi alır.</span><span class="sxs-lookup"><span data-stu-id="053ce-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="053ce-116">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="053ce-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="053ce-117">Örnek 2: belirtilen işten tüm tamamlanmış görevleri alma</span><span class="sxs-lookup"><span data-stu-id="053ce-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="053ce-118">Bu komut, Job02 KIMLIĞINE sahip olan işten tamamlanmış görevleri alır.</span><span class="sxs-lookup"><span data-stu-id="053ce-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="053ce-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="053ce-119">PARAMETERS</span></span>

### <span data-ttu-id="053ce-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="053ce-120">-BatchContext</span></span>
<span data-ttu-id="053ce-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="053ce-122">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="053ce-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="053ce-123">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="053ce-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="053ce-124">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="053ce-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="053ce-125">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="053ce-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053ce-126">-DefaultProfile</span></span>
<span data-ttu-id="053ce-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="053ce-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="053ce-128">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="053ce-128">-Expand</span></span>
<span data-ttu-id="053ce-129">Bir OData genişletme yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="053ce-130">Ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="053ce-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="053ce-131">-Filter</span></span>
<span data-ttu-id="053ce-132">Görevler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="053ce-133">Filtre belirtmezseniz, bu cmdlet toplu hesap veya işe yönelik tüm görevleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="053ce-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-134">-ID</span><span class="sxs-lookup"><span data-stu-id="053ce-134">-Id</span></span>
<span data-ttu-id="053ce-135">Bu cmdlet 'in aldığı görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="053ce-136">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="053ce-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-137">-Job</span><span class="sxs-lookup"><span data-stu-id="053ce-137">-Job</span></span>
<span data-ttu-id="053ce-138">Bu cmdlet 'in aldığı görevleri içeren işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="053ce-139">Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="053ce-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="053ce-140">-JobId</span></span>
<span data-ttu-id="053ce-141">Bu cmdlet 'in aldığı görevleri içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="053ce-142">-MaxCount</span></span>
<span data-ttu-id="053ce-143">Döndürülecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="053ce-144">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="053ce-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="053ce-145">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="053ce-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-146">-Select</span><span class="sxs-lookup"><span data-stu-id="053ce-146">-Select</span></span>
<span data-ttu-id="053ce-147">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="053ce-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="053ce-148">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="053ce-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="053ce-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053ce-149">CommonParameters</span></span>
<span data-ttu-id="053ce-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="053ce-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053ce-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="053ce-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053ce-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="053ce-152">INPUTS</span></span>

### <span data-ttu-id="053ce-153">System. String</span><span class="sxs-lookup"><span data-stu-id="053ce-153">System.String</span></span>

### <span data-ttu-id="053ce-154">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="053ce-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="053ce-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="053ce-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="053ce-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="053ce-156">OUTPUTS</span></span>

### <span data-ttu-id="053ce-157">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="053ce-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="053ce-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="053ce-158">NOTES</span></span>

## <span data-ttu-id="053ce-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="053ce-159">RELATED LINKS</span></span>

[<span data-ttu-id="053ce-160">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="053ce-160">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="053ce-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="053ce-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="053ce-162">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="053ce-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="053ce-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="053ce-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="053ce-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="053ce-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="053ce-165">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="053ce-165">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

