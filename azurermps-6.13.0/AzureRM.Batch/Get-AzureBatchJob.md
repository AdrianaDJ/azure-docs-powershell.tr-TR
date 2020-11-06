---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591416"
---
# <span data-ttu-id="fa524-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="fa524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa524-102">SYNOPSIS</span></span>
<span data-ttu-id="fa524-103">Toplu iş hesabı veya iş zamanlaması için toplu işleri alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa524-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa524-104">SYNTAX</span></span>

### <span data-ttu-id="fa524-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa524-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa524-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="fa524-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa524-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa524-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa524-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa524-108">DESCRIPTION</span></span>
<span data-ttu-id="fa524-109">**Get-AzureBatchJob** cmdlet 'ı, *batchaccountcontext* parametresiyle belirtilen toplu hesap için Azure toplu işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="fa524-110">Tek bir iş almak için *ID* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa524-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="fa524-111">Açık bir veri Protokolü (OData) filtresiyle eşleşen işleri almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa524-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="fa524-112">İş zamanlaması KIMLIĞI veya **Pschoparlör Iş zamanlaması** örneği sağlarsanız, bu cmdlet yalnızca bu iş zamanlamalarının işlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa524-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="fa524-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa524-113">EXAMPLES</span></span>

### <span data-ttu-id="fa524-114">Örnek 1: KIMLIĞE göre bir toplu iş alın</span><span class="sxs-lookup"><span data-stu-id="fa524-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="fa524-115">Bu komut Job01 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="fa524-116">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa524-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fa524-117">Örnek 2: iş zamanlaması için tüm etkin işleri alma</span><span class="sxs-lookup"><span data-stu-id="fa524-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="fa524-118">Bu komut, iş zamanlaması için KIMLIĞI JobSchedule27 olan etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="fa524-119">Örnek 3: ardışık düzeni kullanarak iş zamanlamasındaki tüm işleri alır</span><span class="sxs-lookup"><span data-stu-id="fa524-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="fa524-120">Bu komut, Get-AzureBatchJobSchedule cmdlet 'ini kullanarak KIMLIĞI JobSchedule27 olan iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="fa524-121">Komut, iş çizelgesini ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="fa524-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fa524-122">Komut bu iş zamanlaması için tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="fa524-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="fa524-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa524-123">PARAMETERS</span></span>

### <span data-ttu-id="fa524-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fa524-124">-BatchContext</span></span>
<span data-ttu-id="fa524-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fa524-126">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fa524-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fa524-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="fa524-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fa524-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fa524-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fa524-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fa524-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fa524-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa524-130">-DefaultProfile</span></span>
<span data-ttu-id="fa524-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa524-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa524-132">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="fa524-132">-Expand</span></span>
<span data-ttu-id="fa524-133">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="fa524-134">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="fa524-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="fa524-135">-Filtre</span><span class="sxs-lookup"><span data-stu-id="fa524-135">-Filter</span></span>
<span data-ttu-id="fa524-136">İşler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="fa524-137">Filtre belirtmezseniz, bu cmdlet toplu hesap veya iş zamanlaması için tüm işleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa524-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="fa524-138">-ID</span><span class="sxs-lookup"><span data-stu-id="fa524-138">-Id</span></span>
<span data-ttu-id="fa524-139">Bu cmdlet 'in aldığı işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="fa524-140">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa524-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="fa524-141">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="fa524-141">-JobSchedule</span></span>
<span data-ttu-id="fa524-142">İşleri içeren iş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="fa524-143">**Pschoparlör** nesnesi almak için Get-AzureBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fa524-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="fa524-144">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="fa524-144">-JobScheduleId</span></span>
<span data-ttu-id="fa524-145">İşleri içeren iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="fa524-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fa524-146">-MaxCount</span></span>
<span data-ttu-id="fa524-147">Döndürülecek en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="fa524-148">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="fa524-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fa524-149">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fa524-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="fa524-150">-Select</span><span class="sxs-lookup"><span data-stu-id="fa524-150">-Select</span></span>
<span data-ttu-id="fa524-151">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa524-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="fa524-152">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="fa524-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="fa524-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa524-153">CommonParameters</span></span>
<span data-ttu-id="fa524-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa524-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa524-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa524-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa524-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa524-156">INPUTS</span></span>

### <span data-ttu-id="fa524-157">System. String</span><span class="sxs-lookup"><span data-stu-id="fa524-157">System.String</span></span>

### <span data-ttu-id="fa524-158">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="fa524-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="fa524-159">Parametreler: Jobzamanlama (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa524-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="fa524-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fa524-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="fa524-161">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa524-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="fa524-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa524-162">OUTPUTS</span></span>

### <span data-ttu-id="fa524-163">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="fa524-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="fa524-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa524-164">NOTES</span></span>

## <span data-ttu-id="fa524-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa524-165">RELATED LINKS</span></span>

[<span data-ttu-id="fa524-166">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="fa524-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="fa524-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fa524-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fa524-169">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fa524-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="fa524-170">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="fa524-171">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="fa524-172">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fa524-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="fa524-173">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fa524-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


