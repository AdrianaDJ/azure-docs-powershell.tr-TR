---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 40eb6d3cfd3961c876a5da07ced1ebcf383166e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595099"
---
# <span data-ttu-id="9b4dc-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="9b4dc-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="9b4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4dc-103">Belirtilen işlem düğümündeki görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b4dc-104">SYNTAX</span></span>

### <span data-ttu-id="9b4dc-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9b4dc-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b4dc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b4dc-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b4dc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b4dc-107">DESCRIPTION</span></span>
<span data-ttu-id="9b4dc-108">**Disable-AzureBatchComputeNodeScheduling** cmdlet 'i belirtilen COMPUTE düğümündeki görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="9b4dc-109">Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="9b4dc-110">Bir işlem düğümündeki görev zamanlamasını devre dışı bıraktıktan sonra, düğümün görev sırasındaki işlere ne yapabileceğinizi belirleme seçeneğiniz de vardır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="9b4dc-111">**Disable-AzureBatchComputeNodeScheduling** şunları yapmanızı sağlar:</span><span class="sxs-lookup"><span data-stu-id="9b4dc-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="9b4dc-112">Görevleri sonlandırın ve iş kuyruğuna geri yerleştirin.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="9b4dc-113">Bu, bu görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="9b4dc-114">Görevleri sonlandırın ve iş kuyruğundan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="9b4dc-115">Bu şekilde durdurulan görevler yeniden planlanamaz.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="9b4dc-116">Yürütülmekte olan tüm görevlerin tamamlanmasını bekleyin ve ardından işlem düğümündeki görev zamanlamasını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="9b4dc-117">Tüm çalışan görevlerin tamamlanmasını bekleyin ve tüm veri bekletme dönemleri, işlem düğümündeki görev zamanlamasını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="9b4dc-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b4dc-118">EXAMPLES</span></span>

### <span data-ttu-id="9b4dc-119">Örnek 1: işlem düğümündeki görev zamanlamasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9b4dc-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="9b4dc-120">Bu komutlar, COMPUTE düğümü TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="9b4dc-121">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="9b4dc-122">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="9b4dc-123">İkinci komut daha sonra bu nesne başvurusunu ve **Disable-AzureBatchComputeNodeScheduling** cmdlet 'ini kullanarak Pool myvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="9b4dc-124">*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, şu anda COMPUTE düğümünde çalışan tüm görevler requeued olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="9b4dc-125">Örnek 2: havuzdaki tüm işlem düğümlerinde görev zamanlamasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9b4dc-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="9b4dc-126">Bu komutlar, toplu iş havuzu Pool06 tüm bilgisayar düğümlerinde görev zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="9b4dc-127">Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="9b4dc-128">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="9b4dc-129">Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="9b4dc-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="9b4dc-130">Bu koleksiyon daha sonra, koleksiyondaki her işlem düğümündeki görev zamanlamasını devre dışı bırakmak için **-AzureBatchComputeNodeScheduling** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="9b4dc-131">*DisableComputeNodeSchedulingOptions* parametresi eklenmediğinden, işlem düğümlerinde çalışmakta olan tüm görevler requeued olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="9b4dc-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b4dc-132">PARAMETERS</span></span>

### <span data-ttu-id="9b4dc-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9b4dc-133">-BatchContext</span></span>
<span data-ttu-id="9b4dc-134">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b4dc-135">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-135">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b4dc-136">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-136">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b4dc-137">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b4dc-138">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b4dc-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b4dc-139">-ComputeNode</span></span>
<span data-ttu-id="9b4dc-140">Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümüne yönelik bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="9b4dc-141">Bu nesne başvurusu, Get-AzureBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-141">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b4dc-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4dc-142">-DefaultProfile</span></span>
<span data-ttu-id="9b4dc-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b4dc-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="9b4dc-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="9b4dc-145">Bu cmdlet 'in, zamanlama devre dışı bırakılmakta olan bilgisayar düğümünde çalışmakta olan tüm görevlerle nasıl ilgili olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="9b4dc-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9b4dc-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b4dc-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-147">Requeue.</span></span>
<span data-ttu-id="9b4dc-148">Görevler hemen durdurulur ve iş kuyruğuna geri döner.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="9b4dc-149">Bu, görevlerin başka bir hesaplama düğümünde yeniden zamanlanmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="9b4dc-150">Bu varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-150">This is the default value.</span></span> 
- <span data-ttu-id="9b4dc-151">Ermesini.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-151">Terminate.</span></span>
<span data-ttu-id="9b4dc-152">Görevler hemen durdurulur ve iş sırasından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="9b4dc-153">Bu görevler yeniden planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="9b4dc-154">Görevsiz tamamlama.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-154">TaskCompletion.</span></span>
<span data-ttu-id="9b4dc-155">İşlem düğümündeki görev zamanlama devre dışı bırakılmadan önce çalışmakta olan görevler tamamlayabilecektir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="9b4dc-156">Bu düğümde yeni görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="9b4dc-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-157">RetainedData.</span></span>
<span data-ttu-id="9b4dc-158">Şu anda çalışan görevler tamamlayabilecektir ve veri bekletme dönemleri, işlem düğümündeki görev zamanlama devre dışı bırakılmadan önce sona erecek.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="9b4dc-159">Bu düğümde yeni görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: DisableComputeNodeSchedulingOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4dc-160">-ID</span><span class="sxs-lookup"><span data-stu-id="9b4dc-160">-Id</span></span>
<span data-ttu-id="9b4dc-161">Görev zamanlama 'nın devre dışı bırakıldığı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4dc-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9b4dc-162">-PoolId</span></span>
<span data-ttu-id="9b4dc-163">Görev zamanlama 'nın devre dışı bırakıldığı COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="9b4dc-164">*PoolId* parametresini kullanıyorsanız, aynı komutta *ComputeNode* parametresini kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4dc-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4dc-165">CommonParameters</span></span>
<span data-ttu-id="9b4dc-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b4dc-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4dc-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4dc-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4dc-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b4dc-168">INPUTS</span></span>

### <span data-ttu-id="9b4dc-169">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b4dc-169">BatchAccountContext</span></span>
<span data-ttu-id="9b4dc-170">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9b4dc-170">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9b4dc-171">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b4dc-171">PSComputeNode</span></span>
<span data-ttu-id="9b4dc-172">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9b4dc-172">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="9b4dc-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b4dc-173">OUTPUTS</span></span>

## <span data-ttu-id="9b4dc-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b4dc-174">NOTES</span></span>

## <span data-ttu-id="9b4dc-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b4dc-175">RELATED LINKS</span></span>

[<span data-ttu-id="9b4dc-176">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9b4dc-176">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9b4dc-177">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="9b4dc-177">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


