---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593589"
---
# <span data-ttu-id="f0d4c-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f0d4c-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="f0d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d4c-103">İş için toplu Iş görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0d4c-104">SYNTAX</span></span>

### <span data-ttu-id="f0d4c-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0d4c-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d4c-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="f0d4c-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d4c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="f0d4c-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d4c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0d4c-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d4c-109">**Get-AzureBatchTask** cmdlet 'ı bir toplu Iş Için Azure toplu iş görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="f0d4c-110">İş veya *iş* *parametresinden bir* iş belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="f0d4c-111">Tek bir görev almak için *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="f0d4c-112">Açık bir veri Protokolü (OData) filtresi ile eşleşen görevleri almak için *filtre* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="f0d4c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0d4c-113">EXAMPLES</span></span>

### <span data-ttu-id="f0d4c-114">Örnek 1: KIMLIĞE göre görev alma</span><span class="sxs-lookup"><span data-stu-id="f0d4c-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
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

<span data-ttu-id="f0d4c-115">Bu komut, iş Job01 altında KIMLIĞI Task03 olan görevi alır.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="f0d4c-116">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f0d4c-117">Örnek 2: belirtilen işten tüm tamamlanmış görevleri alma</span><span class="sxs-lookup"><span data-stu-id="f0d4c-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
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

<span data-ttu-id="f0d4c-118">Bu komut, Job02 KIMLIĞINE sahip olan işten tamamlanmış görevleri alır.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="f0d4c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0d4c-119">PARAMETERS</span></span>

### <span data-ttu-id="f0d4c-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f0d4c-120">-BatchContext</span></span>
<span data-ttu-id="f0d4c-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f0d4c-122">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f0d4c-123">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="f0d4c-123">-Expand</span></span>
<span data-ttu-id="f0d4c-124">Bir OData genişletme yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="f0d4c-125">Ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="f0d4c-126">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f0d4c-126">-Filter</span></span>
<span data-ttu-id="f0d4c-127">Görevler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="f0d4c-128">Filtre belirtmezseniz, bu cmdlet toplu hesap veya işe yönelik tüm görevleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="f0d4c-129">-ID</span><span class="sxs-lookup"><span data-stu-id="f0d4c-129">-Id</span></span>
<span data-ttu-id="f0d4c-130">Bu cmdlet 'in aldığı görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="f0d4c-131">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f0d4c-132">-Job</span><span class="sxs-lookup"><span data-stu-id="f0d4c-132">-Job</span></span>
<span data-ttu-id="f0d4c-133">Bu cmdlet 'in aldığı görevleri içeren işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="f0d4c-134">Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="f0d4c-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="f0d4c-135">-JobId</span></span>
<span data-ttu-id="f0d4c-136">Bu cmdlet 'in aldığı görevleri içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f0d4c-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f0d4c-137">-MaxCount</span></span>
<span data-ttu-id="f0d4c-138">Döndürülecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="f0d4c-139">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f0d4c-140">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-140">The default value is 1000.</span></span>

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

### <span data-ttu-id="f0d4c-141">-Select</span><span class="sxs-lookup"><span data-stu-id="f0d4c-141">-Select</span></span>
<span data-ttu-id="f0d4c-142">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="f0d4c-143">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="f0d4c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d4c-144">-DefaultProfile</span></span>
<span data-ttu-id="f0d4c-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d4c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d4c-146">CommonParameters</span></span>
<span data-ttu-id="f0d4c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0d4c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d4c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d4c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d4c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0d4c-149">INPUTS</span></span>

### <span data-ttu-id="f0d4c-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f0d4c-150">BatchAccountContext</span></span>
<span data-ttu-id="f0d4c-151">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f0d4c-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f0d4c-152">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="f0d4c-152">PSCloudJob</span></span>
<span data-ttu-id="f0d4c-153">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="f0d4c-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="f0d4c-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0d4c-154">OUTPUTS</span></span>

### <span data-ttu-id="f0d4c-155">Ince görev</span><span class="sxs-lookup"><span data-stu-id="f0d4c-155">PSCloudTask</span></span>

## <span data-ttu-id="f0d4c-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0d4c-156">NOTES</span></span>

## <span data-ttu-id="f0d4c-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0d4c-157">RELATED LINKS</span></span>

[<span data-ttu-id="f0d4c-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f0d4c-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f0d4c-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f0d4c-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="f0d4c-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f0d4c-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="f0d4c-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f0d4c-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="f0d4c-162">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f0d4c-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="f0d4c-163">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f0d4c-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


