---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 1a177f0987f27f81f0ab27d5e35db11df17ae005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587690"
---
# <span data-ttu-id="8b252-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b252-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="8b252-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b252-102">SYNOPSIS</span></span>
<span data-ttu-id="8b252-103">İş için toplu Iş görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8b252-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b252-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b252-104">SYNTAX</span></span>

### <span data-ttu-id="8b252-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8b252-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b252-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="8b252-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b252-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8b252-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b252-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b252-108">DESCRIPTION</span></span>
<span data-ttu-id="8b252-109">**Get-AzureBatchTask** cmdlet 'ı bir toplu Iş Için Azure toplu iş görevlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8b252-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="8b252-110">İş veya *iş* *parametresinden bir* iş belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b252-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="8b252-111">Tek bir görev almak için *ID* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b252-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="8b252-112">Açık bir veri Protokolü (OData) filtresi ile eşleşen görevleri almak için *filtre* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b252-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="8b252-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b252-113">EXAMPLES</span></span>

### <span data-ttu-id="8b252-114">Örnek 1: KIMLIĞE göre görev alma</span><span class="sxs-lookup"><span data-stu-id="8b252-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="8b252-115">Bu komut, iş Job01 altında KIMLIĞI Task03 olan görevi alır.</span><span class="sxs-lookup"><span data-stu-id="8b252-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="8b252-116">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8b252-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8b252-117">Örnek 2: belirtilen işten tüm tamamlanmış görevleri alma</span><span class="sxs-lookup"><span data-stu-id="8b252-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="8b252-118">Bu komut, Job02 KIMLIĞINE sahip olan işten tamamlanmış görevleri alır.</span><span class="sxs-lookup"><span data-stu-id="8b252-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="8b252-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b252-119">PARAMETERS</span></span>

### <span data-ttu-id="8b252-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8b252-120">-BatchContext</span></span>
<span data-ttu-id="8b252-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8b252-122">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8b252-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8b252-123">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="8b252-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8b252-124">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8b252-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8b252-125">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8b252-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b252-126">-DefaultProfile</span></span>
<span data-ttu-id="8b252-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b252-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b252-128">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="8b252-128">-Expand</span></span>
<span data-ttu-id="8b252-129">Bir OData genişletme yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="8b252-130">Ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b252-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="8b252-131">-Filter</span></span>
<span data-ttu-id="8b252-132">Görevler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="8b252-133">Filtre belirtmezseniz, bu cmdlet toplu hesap veya işe yönelik tüm görevleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b252-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-134">-ID</span><span class="sxs-lookup"><span data-stu-id="8b252-134">-Id</span></span>
<span data-ttu-id="8b252-135">Bu cmdlet 'in aldığı görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="8b252-136">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b252-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-137">-Job</span><span class="sxs-lookup"><span data-stu-id="8b252-137">-Job</span></span>
<span data-ttu-id="8b252-138">Bu cmdlet 'in aldığı görevleri içeren işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="8b252-139">Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8b252-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="8b252-140">-JobId</span></span>
<span data-ttu-id="8b252-141">Bu cmdlet 'in aldığı görevleri içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8b252-142">-MaxCount</span></span>
<span data-ttu-id="8b252-143">Döndürülecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="8b252-144">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="8b252-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8b252-145">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8b252-145">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-146">-Select</span><span class="sxs-lookup"><span data-stu-id="8b252-146">-Select</span></span>
<span data-ttu-id="8b252-147">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b252-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="8b252-148">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="8b252-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b252-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b252-149">CommonParameters</span></span>
<span data-ttu-id="8b252-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b252-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b252-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b252-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b252-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b252-152">INPUTS</span></span>

### <span data-ttu-id="8b252-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8b252-153">BatchAccountContext</span></span>
<span data-ttu-id="8b252-154">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8b252-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8b252-155">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="8b252-155">PSCloudJob</span></span>
<span data-ttu-id="8b252-156">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8b252-156">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="8b252-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b252-157">OUTPUTS</span></span>

### <span data-ttu-id="8b252-158">Ince görev</span><span class="sxs-lookup"><span data-stu-id="8b252-158">PSCloudTask</span></span>

## <span data-ttu-id="8b252-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b252-159">NOTES</span></span>

## <span data-ttu-id="8b252-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b252-160">RELATED LINKS</span></span>

[<span data-ttu-id="8b252-161">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8b252-161">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8b252-162">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8b252-162">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="8b252-163">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b252-163">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="8b252-164">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b252-164">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="8b252-165">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="8b252-165">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="8b252-166">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8b252-166">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


