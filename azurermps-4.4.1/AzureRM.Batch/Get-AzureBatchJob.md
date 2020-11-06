---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590770"
---
# <span data-ttu-id="5a2a9-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="5a2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2a9-103">Toplu iş hesabı veya iş zamanlaması için toplu işleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a2a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a2a9-104">SYNTAX</span></span>

### <span data-ttu-id="5a2a9-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a2a9-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a2a9-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="5a2a9-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a2a9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a2a9-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a2a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a2a9-108">DESCRIPTION</span></span>
<span data-ttu-id="5a2a9-109">**Get-AzureBatchJob** cmdlet 'ı, *batchaccountcontext* parametresiyle belirtilen toplu hesap için Azure toplu işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="5a2a9-110">Tek bir iş almak için *ID* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="5a2a9-111">Açık bir veri Protokolü (OData) filtresiyle eşleşen işleri almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="5a2a9-112">İş zamanlaması KIMLIĞI veya **Pschoparlör Iş zamanlaması** örneği sağlarsanız, bu cmdlet yalnızca bu iş zamanlamalarının işlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="5a2a9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a2a9-113">EXAMPLES</span></span>

### <span data-ttu-id="5a2a9-114">Örnek 1: KIMLIĞE göre bir toplu iş alın</span><span class="sxs-lookup"><span data-stu-id="5a2a9-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="5a2a9-115">Bu komut Job01 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="5a2a9-116">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="5a2a9-117">Örnek 2: iş zamanlaması için tüm etkin işleri alma</span><span class="sxs-lookup"><span data-stu-id="5a2a9-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="5a2a9-118">Bu komut, iş zamanlaması için KIMLIĞI JobSchedule27 olan etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="5a2a9-119">Örnek 3: ardışık düzeni kullanarak iş zamanlamasındaki tüm işleri alır</span><span class="sxs-lookup"><span data-stu-id="5a2a9-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="5a2a9-120">Bu komut, Get-AzureBatchJobSchedule cmdlet 'ini kullanarak KIMLIĞI JobSchedule27 olan iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="5a2a9-121">Komut, iş çizelgesini ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a2a9-122">Komut bu iş zamanlaması için tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="5a2a9-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a2a9-123">PARAMETERS</span></span>

### <span data-ttu-id="5a2a9-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5a2a9-124">-BatchContext</span></span>
<span data-ttu-id="5a2a9-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5a2a9-126">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5a2a9-127">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="5a2a9-127">-Expand</span></span>
<span data-ttu-id="5a2a9-128">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="5a2a9-129">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="5a2a9-130">-Filtre</span><span class="sxs-lookup"><span data-stu-id="5a2a9-130">-Filter</span></span>
<span data-ttu-id="5a2a9-131">İşler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="5a2a9-132">Filtre belirtmezseniz, bu cmdlet toplu hesap veya iş zamanlaması için tüm işleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="5a2a9-133">-ID</span><span class="sxs-lookup"><span data-stu-id="5a2a9-133">-Id</span></span>
<span data-ttu-id="5a2a9-134">Bu cmdlet 'in aldığı işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="5a2a9-135">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a9-136">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="5a2a9-136">-JobSchedule</span></span>
<span data-ttu-id="5a2a9-137">İşleri içeren iş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="5a2a9-138">**Pschoparlör** nesnesi almak için Get-AzureBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a9-139">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="5a2a9-139">-JobScheduleId</span></span>
<span data-ttu-id="5a2a9-140">İşleri içeren iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a2a9-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5a2a9-141">-MaxCount</span></span>
<span data-ttu-id="5a2a9-142">Döndürülecek en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="5a2a9-143">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="5a2a9-144">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="5a2a9-145">-Select</span><span class="sxs-lookup"><span data-stu-id="5a2a9-145">-Select</span></span>
<span data-ttu-id="5a2a9-146">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="5a2a9-147">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="5a2a9-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2a9-148">-DefaultProfile</span></span>
<span data-ttu-id="5a2a9-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a2a9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2a9-150">CommonParameters</span></span>
<span data-ttu-id="5a2a9-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a2a9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2a9-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a2a9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2a9-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a2a9-153">INPUTS</span></span>

### <span data-ttu-id="5a2a9-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5a2a9-154">BatchAccountContext</span></span>
<span data-ttu-id="5a2a9-155">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5a2a9-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5a2a9-156">Ek zamanlama</span><span class="sxs-lookup"><span data-stu-id="5a2a9-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="5a2a9-157">' Jobzamanlama ' parametresi ardışık düzenin ' Pscses Jobzamanlama ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5a2a9-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="5a2a9-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a2a9-158">OUTPUTS</span></span>

### <span data-ttu-id="5a2a9-159">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="5a2a9-159">PSCloudJob</span></span>

## <span data-ttu-id="5a2a9-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a2a9-160">NOTES</span></span>

## <span data-ttu-id="5a2a9-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a2a9-161">RELATED LINKS</span></span>

[<span data-ttu-id="5a2a9-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="5a2a9-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5a2a9-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a2a9-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5a2a9-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5a2a9-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="5a2a9-166">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5a2a9-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5a2a9-168">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5a2a9-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5a2a9-169">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5a2a9-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


