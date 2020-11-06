---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: e00a1a923afdd8a851416e872028a30ce1e04a55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591424"
---
# <span data-ttu-id="03e79-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="03e79-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="03e79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e79-102">SYNOPSIS</span></span>
<span data-ttu-id="03e79-103">Belirtilen işlem düğümündeki görev zamanlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="03e79-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03e79-104">SYNTAX</span></span>

### <span data-ttu-id="03e79-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03e79-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03e79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="03e79-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03e79-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="03e79-107">DESCRIPTION</span></span>
<span data-ttu-id="03e79-108">**Enable-AzureBatchComputeNodeScheduling** cmdlet 'i belirtilen işlem düğümündeki görev zamanlama özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="03e79-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="03e79-109">Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.</span><span class="sxs-lookup"><span data-stu-id="03e79-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="03e79-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03e79-110">EXAMPLES</span></span>

### <span data-ttu-id="03e79-111">Örnek 1: işlem düğümündeki görev zamanlamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="03e79-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="03e79-112">Bu komutlar, COMPUTE node TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="03e79-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="03e79-113">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03e79-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="03e79-114">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="03e79-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="03e79-115">İkinci komut daha sonra bu nesne başvurusunu ve **Enable-AzureBatchComputeNodeScheduling** cmdlet 'ini kullanarak havuz mypool öğesine bağlanır ve TVM-1783593343_34-20151117t222514z üzerinde görev zamanlamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="03e79-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="03e79-116">Örnek 2: havuzdaki işlem düğümlerinde görev zamanlamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="03e79-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="03e79-117">Bu komutlar, havuz Pool06 bulunan tüm işlem düğümlerinde görev zamanlamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="03e79-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="03e79-118">Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03e79-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="03e79-119">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="03e79-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="03e79-120">Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="03e79-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="03e79-121">Bu koleksiyon, koleksiyondaki her bir işlem düğümünde görev zamanlamayı etkinleştiren **Enable-AzureBatchComputeNodeScheduling** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="03e79-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="03e79-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03e79-122">PARAMETERS</span></span>

### <span data-ttu-id="03e79-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="03e79-123">-BatchContext</span></span>
<span data-ttu-id="03e79-124">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e79-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03e79-125">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="03e79-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="03e79-126">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="03e79-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="03e79-127">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="03e79-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="03e79-128">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="03e79-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="03e79-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e79-129">-ComputeNode</span></span>
<span data-ttu-id="03e79-130">Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümüne bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e79-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="03e79-131">Bu nesne başvurusu, Get-AzureBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="03e79-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="03e79-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e79-132">-DefaultProfile</span></span>
<span data-ttu-id="03e79-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03e79-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e79-134">-ID</span><span class="sxs-lookup"><span data-stu-id="03e79-134">-Id</span></span>
<span data-ttu-id="03e79-135">Görev zamanlama özelliğinin etkinleştirildiği COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e79-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="03e79-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="03e79-136">-PoolId</span></span>
<span data-ttu-id="03e79-137">Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="03e79-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="03e79-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e79-138">CommonParameters</span></span>
<span data-ttu-id="03e79-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03e79-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e79-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e79-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e79-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03e79-141">INPUTS</span></span>

### <span data-ttu-id="03e79-142">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="03e79-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="03e79-143">Parametreler: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03e79-143">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="03e79-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03e79-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="03e79-145">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03e79-145">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="03e79-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03e79-146">OUTPUTS</span></span>

### <span data-ttu-id="03e79-147">System. void</span><span class="sxs-lookup"><span data-stu-id="03e79-147">System.Void</span></span>

## <span data-ttu-id="03e79-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03e79-148">NOTES</span></span>

## <span data-ttu-id="03e79-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03e79-149">RELATED LINKS</span></span>

[<span data-ttu-id="03e79-150">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="03e79-150">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


