---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 94a35c3923debf5ea983e9d1ad276b124ae8c89c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591152"
---
# <span data-ttu-id="dbc71-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="dbc71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc71-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc71-103">Toplu Iş hizmetinde bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc71-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbc71-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbc71-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc71-106">**New-AzureBatchJob** cmdlet 'ı, *batchaccountcontext* parametresiyle belirtilen hesapta Azure Batch hizmetinde bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc71-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="dbc71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbc71-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc71-108">Örnek 1: iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="dbc71-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="dbc71-109">İlk komut, New-Object cmdlet 'ini kullanarak bir **Pspoolınformation** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc71-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="dbc71-110">Komut bu nesneyi $PoolInformation değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dbc71-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="dbc71-111">İkinci komut Pool22 KIMLIĞINE $PoolInformation nesnenin **PoolId** özelliğine atar.</span><span class="sxs-lookup"><span data-stu-id="dbc71-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="dbc71-112">Son komut ContosoJob35 KIMLIĞINE sahip bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc71-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="dbc71-113">İş 'e eklenen Pool22 KIMLIĞI olan havuzda çalışır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="dbc71-114">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dbc71-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dbc71-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbc71-115">PARAMETERS</span></span>

### <span data-ttu-id="dbc71-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dbc71-116">-BatchContext</span></span>
<span data-ttu-id="dbc71-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dbc71-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dbc71-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dbc71-119">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="dbc71-119">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="dbc71-120">Anahtar/değer çiftleri olarak, bu cmdlet işin projedeki tüm görevler için ayarladığı ortak ortam değişkenlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-120">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="dbc71-121">Anahtar, ortam değişkeni adıdır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-121">The key is the environment variable name.</span></span>
<span data-ttu-id="dbc71-122">Değer, ortam değişkeni değeridir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-122">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-123">-Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="dbc71-123">-Constraints</span></span>
<span data-ttu-id="dbc71-124">İş için yürütme kısıtlamalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-124">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dbc71-125">-DisplayName</span></span>
<span data-ttu-id="dbc71-126">İşin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-126">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="dbc71-127">-ID</span><span class="sxs-lookup"><span data-stu-id="dbc71-127">-Id</span></span>
<span data-ttu-id="dbc71-128">İş için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-128">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="dbc71-129">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="dbc71-129">-JobManagerTask</span></span>
<span data-ttu-id="dbc71-130">Iş Yöneticisi görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-130">Specifies the Job Manager task.</span></span>
<span data-ttu-id="dbc71-131">İş başladığında toplu iş hizmeti Iş Yöneticisi görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-131">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-132">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="dbc71-132">-JobPreparationTask</span></span>
<span data-ttu-id="dbc71-133">Iş hazırlığı görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-133">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="dbc71-134">Toplu Iş hizmeti, bu işlem düğümündeki herhangi bir görevi başlatmadan önce işlem düğümündeki Iş hazırlık görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-134">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-135">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="dbc71-135">-JobReleaseTask</span></span>
<span data-ttu-id="dbc71-136">Iş sürümü görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-136">Specifies the Job Release task.</span></span>
<span data-ttu-id="dbc71-137">Toplu iş hizmeti iş sona erdiğinde Iş sürümü görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-137">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="dbc71-138">Toplu iş hizmeti, işin her görevi çalıştırdığı her işlem düğümündeki Iş sürümü görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-138">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-139">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dbc71-139">-Metadata</span></span>
<span data-ttu-id="dbc71-140">İş 'e eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-140">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="dbc71-141">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-141">The key is the metadata name.</span></span>
<span data-ttu-id="dbc71-142">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-142">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-143">-'Alltaskscomplete</span><span class="sxs-lookup"><span data-stu-id="dbc71-143">-OnAllTasksComplete</span></span>
<span data-ttu-id="dbc71-144">İşteki tüm görevlerin tamamlandı durumunda olması durumunda, toplu Iş hizmeti 'nin aldığı eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-144">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-145">-'Taskfailure</span><span class="sxs-lookup"><span data-stu-id="dbc71-145">-OnTaskFailure</span></span>
<span data-ttu-id="dbc71-146">Bir eylem belirtir projedeki herhangi bir görev başarısız olduğunda toplu Iş hizmeti sürer.</span><span class="sxs-lookup"><span data-stu-id="dbc71-146">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-147">-Poolınformation</span><span class="sxs-lookup"><span data-stu-id="dbc71-147">-PoolInformation</span></span>
<span data-ttu-id="dbc71-148">Toplu Iş hizmetinin işin görevlerini çalıştırdığı havuzun ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-148">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-149">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="dbc71-149">-Priority</span></span>
<span data-ttu-id="dbc71-150">İşin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-150">Specifies the priority of the job.</span></span>
<span data-ttu-id="dbc71-151">Geçerli değerler:-1000 ile 1000 arasındaki tamsayılar.</span><span class="sxs-lookup"><span data-stu-id="dbc71-151">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="dbc71-152">-1000 değeri en düşük önceliktir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-152">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="dbc71-153">1000 değeri en yüksek önceliktir.</span><span class="sxs-lookup"><span data-stu-id="dbc71-153">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="dbc71-154">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="dbc71-154">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-155">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="dbc71-155">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc71-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc71-156">-DefaultProfile</span></span>
<span data-ttu-id="dbc71-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbc71-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc71-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc71-158">CommonParameters</span></span>
<span data-ttu-id="dbc71-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbc71-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc71-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc71-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc71-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbc71-161">INPUTS</span></span>

### <span data-ttu-id="dbc71-162">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dbc71-162">BatchAccountContext</span></span>
<span data-ttu-id="dbc71-163">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dbc71-163">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="dbc71-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbc71-164">OUTPUTS</span></span>

## <span data-ttu-id="dbc71-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbc71-165">NOTES</span></span>

## <span data-ttu-id="dbc71-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbc71-166">RELATED LINKS</span></span>

[<span data-ttu-id="dbc71-167">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-167">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="dbc71-168">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-168">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="dbc71-169">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dbc71-169">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dbc71-170">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-170">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="dbc71-171">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbc71-171">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="dbc71-172">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-172">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="dbc71-173">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="dbc71-173">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="dbc71-174">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="dbc71-174">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


