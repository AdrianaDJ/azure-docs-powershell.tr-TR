---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: 3fd4861ed70a010839edbe7bcdffb61961d0bdf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592337"
---
# <span data-ttu-id="a3f8f-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="a3f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f8f-103">Toplu Iş hizmetinde bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3f8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3f8f-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f8f-106">**New-AzureBatchJob** cmdlet 'ı, *batchaccountcontext* parametresiyle belirtilen hesapta Azure Batch hizmetinde bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="a3f8f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f8f-108">Örnek 1: iş oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3f8f-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="a3f8f-109">İlk komut, New-Object cmdlet 'ini kullanarak bir **Pspoolınformation** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="a3f8f-110">Komut bu nesneyi $PoolInformation değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="a3f8f-111">İkinci komut Pool22 KIMLIĞINE $PoolInformation nesnenin **PoolId** özelliğine atar.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="a3f8f-112">Son komut ContosoJob35 KIMLIĞINE sahip bir iş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="a3f8f-113">İş 'e eklenen Pool22 KIMLIĞI olan havuzda çalışır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="a3f8f-114">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a3f8f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3f8f-115">PARAMETERS</span></span>

### <span data-ttu-id="a3f8f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a3f8f-116">-BatchContext</span></span>
<span data-ttu-id="a3f8f-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a3f8f-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a3f8f-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a3f8f-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a3f8f-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a3f8f-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="a3f8f-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="a3f8f-123">Anahtar/değer çiftleri olarak, bu cmdlet işin projedeki tüm görevler için ayarladığı ortak ortam değişkenlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="a3f8f-124">Anahtar, ortam değişkeni adıdır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-124">The key is the environment variable name.</span></span>
<span data-ttu-id="a3f8f-125">Değer, ortam değişkeni değeridir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f8f-126">-Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="a3f8f-126">-Constraints</span></span>
<span data-ttu-id="a3f8f-127">İş için yürütme kısıtlamalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="a3f8f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f8f-128">-DefaultProfile</span></span>
<span data-ttu-id="a3f8f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f8f-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3f8f-130">-DisplayName</span></span>
<span data-ttu-id="a3f8f-131">İşin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="a3f8f-132">-ID</span><span class="sxs-lookup"><span data-stu-id="a3f8f-132">-Id</span></span>
<span data-ttu-id="a3f8f-133">İş için bir KIMLIK belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="a3f8f-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="a3f8f-134">-JobManagerTask</span></span>
<span data-ttu-id="a3f8f-135">Iş Yöneticisi görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="a3f8f-136">İş başladığında toplu iş hizmeti Iş Yöneticisi görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="a3f8f-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="a3f8f-137">-JobPreparationTask</span></span>
<span data-ttu-id="a3f8f-138">Iş hazırlığı görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="a3f8f-139">Toplu Iş hizmeti, bu işlem düğümündeki herhangi bir görevi başlatmadan önce işlem düğümündeki Iş hazırlık görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="a3f8f-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="a3f8f-140">-JobReleaseTask</span></span>
<span data-ttu-id="a3f8f-141">Iş sürümü görevini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="a3f8f-142">Toplu iş hizmeti iş sona erdiğinde Iş sürümü görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="a3f8f-143">Toplu iş hizmeti, işin her görevi çalıştırdığı her işlem düğümündeki Iş sürümü görevini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="a3f8f-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a3f8f-144">-Metadata</span></span>
<span data-ttu-id="a3f8f-145">İş 'e eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="a3f8f-146">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-146">The key is the metadata name.</span></span>
<span data-ttu-id="a3f8f-147">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="a3f8f-148">-'Alltaskscomplete</span><span class="sxs-lookup"><span data-stu-id="a3f8f-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="a3f8f-149">İşteki tüm görevlerin tamamlandı durumunda olması durumunda, toplu Iş hizmeti 'nin aldığı eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="a3f8f-150">-'Taskfailure</span><span class="sxs-lookup"><span data-stu-id="a3f8f-150">-OnTaskFailure</span></span>
<span data-ttu-id="a3f8f-151">Bir eylem belirtir projedeki herhangi bir görev başarısız olduğunda toplu Iş hizmeti sürer.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="a3f8f-152">-Poolınformation</span><span class="sxs-lookup"><span data-stu-id="a3f8f-152">-PoolInformation</span></span>
<span data-ttu-id="a3f8f-153">Toplu Iş hizmetinin işin görevlerini çalıştırdığı havuzun ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="a3f8f-154">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="a3f8f-154">-Priority</span></span>
<span data-ttu-id="a3f8f-155">İşin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="a3f8f-156">Geçerli değerler:-1000 ile 1000 arasındaki tamsayılar.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="a3f8f-157">-1000 değeri en düşük önceliktir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="a3f8f-158">1000 değeri en yüksek önceliktir.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="a3f8f-159">Varsayılan değer 0 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-159">The default value is 0.</span></span>

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

### <span data-ttu-id="a3f8f-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="a3f8f-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="a3f8f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f8f-161">CommonParameters</span></span>
<span data-ttu-id="a3f8f-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f8f-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f8f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f8f-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3f8f-164">INPUTS</span></span>

### <span data-ttu-id="a3f8f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f8f-165">System.String</span></span>

### <span data-ttu-id="a3f8f-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3f8f-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a3f8f-167">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3f8f-167">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a3f8f-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3f8f-168">OUTPUTS</span></span>

### <span data-ttu-id="a3f8f-169">System. void</span><span class="sxs-lookup"><span data-stu-id="a3f8f-169">System.Void</span></span>

## <span data-ttu-id="a3f8f-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3f8f-170">NOTES</span></span>

## <span data-ttu-id="a3f8f-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3f8f-171">RELATED LINKS</span></span>

[<span data-ttu-id="a3f8f-172">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-172">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="a3f8f-173">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-173">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="a3f8f-174">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a3f8f-174">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a3f8f-175">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-175">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="a3f8f-176">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a3f8f-176">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a3f8f-177">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-177">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="a3f8f-178">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="a3f8f-178">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="a3f8f-179">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a3f8f-179">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

