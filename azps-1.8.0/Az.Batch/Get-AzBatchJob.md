---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: 332bdb8d32b42d391518d50aef82436675cf3f9e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761892"
---
# <span data-ttu-id="16150-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="16150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16150-102">SYNOPSIS</span></span>
<span data-ttu-id="16150-103">Toplu iş hesabı veya iş zamanlaması için toplu işleri alır.</span><span class="sxs-lookup"><span data-stu-id="16150-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="16150-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16150-104">SYNTAX</span></span>

### <span data-ttu-id="16150-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16150-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16150-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="16150-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16150-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="16150-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16150-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="16150-108">DESCRIPTION</span></span>
<span data-ttu-id="16150-109">**Get-AzBatchJob** cmdlet 'ı, *batchaccountcontext* parametresinde belirtilen toplu hesap için Azure toplu işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="16150-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="16150-110">Tek bir iş almak için *ID* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16150-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="16150-111">Açık bir veri Protokolü (OData) filtresiyle eşleşen işleri almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16150-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="16150-112">İş zamanlaması KIMLIĞI veya **Pschoparlör Iş zamanlaması** örneği sağlarsanız, bu cmdlet yalnızca bu iş zamanlamalarının işlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16150-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="16150-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16150-113">EXAMPLES</span></span>

### <span data-ttu-id="16150-114">Örnek 1: KIMLIĞE göre bir toplu iş alın</span><span class="sxs-lookup"><span data-stu-id="16150-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
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

<span data-ttu-id="16150-115">Bu komut Job01 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="16150-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="16150-116">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="16150-116">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="16150-117">Örnek 2: iş zamanlaması için tüm etkin işleri alma</span><span class="sxs-lookup"><span data-stu-id="16150-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="16150-118">Bu komut, iş zamanlaması için KIMLIĞI JobSchedule27 olan etkin işleri alır.</span><span class="sxs-lookup"><span data-stu-id="16150-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="16150-119">Örnek 3: ardışık düzeni kullanarak iş zamanlamasındaki tüm işleri alır</span><span class="sxs-lookup"><span data-stu-id="16150-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
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

<span data-ttu-id="16150-120">Bu komut, Get-AzBatchJobSchedule cmdlet 'ini kullanarak KIMLIĞI JobSchedule27 olan iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="16150-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="16150-121">Komut, iş çizelgesini ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="16150-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="16150-122">Komut bu iş zamanlaması için tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="16150-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="16150-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16150-123">PARAMETERS</span></span>

### <span data-ttu-id="16150-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="16150-124">-BatchContext</span></span>
<span data-ttu-id="16150-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="16150-126">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="16150-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="16150-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="16150-127">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="16150-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="16150-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="16150-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="16150-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="16150-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16150-130">-DefaultProfile</span></span>
<span data-ttu-id="16150-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16150-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16150-132">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="16150-132">-Expand</span></span>
<span data-ttu-id="16150-133">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="16150-134">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="16150-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="16150-135">-Filtre</span><span class="sxs-lookup"><span data-stu-id="16150-135">-Filter</span></span>
<span data-ttu-id="16150-136">İşler için bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="16150-137">Filtre belirtmezseniz, bu cmdlet toplu hesap veya iş zamanlaması için tüm işleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="16150-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="16150-138">-ID</span><span class="sxs-lookup"><span data-stu-id="16150-138">-Id</span></span>
<span data-ttu-id="16150-139">Bu cmdlet 'in aldığı işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="16150-140">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="16150-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="16150-141">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="16150-141">-JobSchedule</span></span>
<span data-ttu-id="16150-142">İşleri içeren iş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="16150-143">**Pschoparlör** nesnesi almak için Get-AzBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="16150-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="16150-144">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="16150-144">-JobScheduleId</span></span>
<span data-ttu-id="16150-145">İşleri içeren iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="16150-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="16150-146">-MaxCount</span></span>
<span data-ttu-id="16150-147">Döndürülecek en fazla iş sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="16150-148">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="16150-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="16150-149">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="16150-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="16150-150">-Select</span><span class="sxs-lookup"><span data-stu-id="16150-150">-Select</span></span>
<span data-ttu-id="16150-151">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="16150-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="16150-152">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="16150-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="16150-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16150-153">CommonParameters</span></span>
<span data-ttu-id="16150-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16150-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16150-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16150-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16150-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16150-156">INPUTS</span></span>

### <span data-ttu-id="16150-157">System. String</span><span class="sxs-lookup"><span data-stu-id="16150-157">System.String</span></span>

### <span data-ttu-id="16150-158">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="16150-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="16150-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="16150-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16150-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16150-160">OUTPUTS</span></span>

### <span data-ttu-id="16150-161">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="16150-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="16150-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16150-162">NOTES</span></span>

## <span data-ttu-id="16150-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16150-163">RELATED LINKS</span></span>

[<span data-ttu-id="16150-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="16150-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="16150-166">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="16150-166">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="16150-167">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="16150-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="16150-168">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="16150-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="16150-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="16150-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="16150-171">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="16150-171">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


