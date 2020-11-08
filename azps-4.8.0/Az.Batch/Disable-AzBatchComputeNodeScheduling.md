---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266104"
---
# <span data-ttu-id="82f5a-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="82f5a-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="82f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="82f5a-103">Belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="82f5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82f5a-104">SYNTAX</span></span>

### <span data-ttu-id="82f5a-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="82f5a-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82f5a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="82f5a-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82f5a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="82f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="82f5a-108">**Disable-AzBatchComputeNodeScheduling** cmdlet 'i belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="82f5a-109">Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="82f5a-110">Bir işlem düğümündeki görev zamanlamasını devre dışı bıraktıktan sonra, düğümün görev sırasındaki işlere ne yapabileceğinizi belirleme seçeneğiniz de vardır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="82f5a-111">**Disable-AzBatchComputeNodeScheduling** aşağıdakileri yapmanızı sağlar:</span><span class="sxs-lookup"><span data-stu-id="82f5a-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="82f5a-112">Görevleri sonlandırın ve iş kuyruğuna geri yerleştirin.</span><span class="sxs-lookup"><span data-stu-id="82f5a-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="82f5a-113">Bu, bu görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="82f5a-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="82f5a-114">Görevleri sonlandırın ve iş kuyruğundan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="82f5a-115">Bu şekilde durdurulan görevler yeniden planlanamaz.</span><span class="sxs-lookup"><span data-stu-id="82f5a-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="82f5a-116">Yürütülmekte olan tüm görevlerin tamamlanmasını bekleyin ve ardından işlem düğümündeki görev zamanlamasını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="82f5a-117">Tüm çalışan görevlerin tamamlanmasını bekleyin ve tüm veri bekletme dönemleri, işlem düğümündeki görev zamanlamasını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="82f5a-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82f5a-118">EXAMPLES</span></span>

### <span data-ttu-id="82f5a-119">Örnek 1: işlem düğümündeki görev zamanlamasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="82f5a-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="82f5a-120">Bu komutlar, COMPUTE düğümü TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="82f5a-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="82f5a-121">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82f5a-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="82f5a-122">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="82f5a-123">İkinci komut daha sonra bu nesne başvurusunu ve **Disable-AzBatchComputeNodeScheduling** cmdlet 'ini kullanarak havuz myvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="82f5a-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="82f5a-124">*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, şu anda COMPUTE düğümünde çalışan tüm görevler requeued olacaktır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="82f5a-125">Örnek 2: havuzdaki tüm işlem düğümlerinde görev zamanlamasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="82f5a-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="82f5a-126">Bu komutlar, toplu iş havuzu Pool06 tüm bilgisayar düğümlerinde görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="82f5a-127">Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82f5a-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="82f5a-128">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="82f5a-129">Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="82f5a-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="82f5a-130">Bu koleksiyon, koleksiyondaki her işlem düğümündeki görev zamanlamasını devre dışı bırakmak için **-AzBatchComputeNodeScheduling** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="82f5a-131">*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, işlem düğümlerinde çalışmakta olan tüm görevler requeued olacaktır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="82f5a-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82f5a-132">PARAMETERS</span></span>

### <span data-ttu-id="82f5a-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82f5a-133">-BatchContext</span></span>
<span data-ttu-id="82f5a-134">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82f5a-135">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82f5a-136">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82f5a-137">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82f5a-138">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82f5a-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="82f5a-139">-ComputeNode</span></span>
<span data-ttu-id="82f5a-140">Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümüne yönelik bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="82f5a-141">Bu nesne başvurusu, Get-AzBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="82f5a-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f5a-142">-DefaultProfile</span></span>
<span data-ttu-id="82f5a-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82f5a-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82f5a-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="82f5a-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="82f5a-145">Bu cmdlet 'in, zamanlama devre dışı bırakılmakta olan bilgisayar düğümünde çalışmakta olan tüm görevlerle nasıl ilgili olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="82f5a-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="82f5a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82f5a-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="82f5a-147">Requeue.</span></span>
<span data-ttu-id="82f5a-148">Görevler hemen durdurulur ve iş kuyruğuna geri döner.</span><span class="sxs-lookup"><span data-stu-id="82f5a-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="82f5a-149">Bu, görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="82f5a-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="82f5a-150">Bu varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-150">This is the default value.</span></span> 
- <span data-ttu-id="82f5a-151">Ermesini.</span><span class="sxs-lookup"><span data-stu-id="82f5a-151">Terminate.</span></span>
<span data-ttu-id="82f5a-152">Görevler hemen durdurulur ve iş sırasından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="82f5a-153">Bu görevler yeniden planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="82f5a-154">Görevsiz tamamlama.</span><span class="sxs-lookup"><span data-stu-id="82f5a-154">TaskCompletion.</span></span>
<span data-ttu-id="82f5a-155">İşlem düğümündeki görev zamanlama devre dışı bırakılmadan önce çalışmakta olan görevler tamamlayabilecektir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="82f5a-156">Bu düğümde yeni görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="82f5a-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="82f5a-157">RetainedData.</span></span>
<span data-ttu-id="82f5a-158">Şu anda çalışan görevler tamamlayabilecektir ve veri bekletme dönemleri, işlem düğümündeki görev zamanlama devre dışı bırakılmadan önce sona erecek.</span><span class="sxs-lookup"><span data-stu-id="82f5a-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="82f5a-159">Bu düğümde yeni görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="82f5a-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5a-160">-ID</span><span class="sxs-lookup"><span data-stu-id="82f5a-160">-Id</span></span>
<span data-ttu-id="82f5a-161">Görev zamanlama 'nın devre dışı bırakıldığı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5a-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="82f5a-162">-PoolId</span></span>
<span data-ttu-id="82f5a-163">Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="82f5a-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="82f5a-164">*PoolId* parametresini kullanıyorsanız, aynı komutta *ComputeNode* parametresini kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82f5a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f5a-165">CommonParameters</span></span>
<span data-ttu-id="82f5a-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82f5a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f5a-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82f5a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f5a-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82f5a-168">INPUTS</span></span>

### <span data-ttu-id="82f5a-169">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="82f5a-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="82f5a-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82f5a-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="82f5a-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82f5a-171">OUTPUTS</span></span>

### <span data-ttu-id="82f5a-172">System. void</span><span class="sxs-lookup"><span data-stu-id="82f5a-172">System.Void</span></span>

## <span data-ttu-id="82f5a-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82f5a-173">NOTES</span></span>

## <span data-ttu-id="82f5a-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82f5a-174">RELATED LINKS</span></span>

[<span data-ttu-id="82f5a-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="82f5a-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="82f5a-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="82f5a-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


