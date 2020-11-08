---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937872"
---
# <span data-ttu-id="74b66-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="74b66-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="74b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b66-102">SYNOPSIS</span></span>
<span data-ttu-id="74b66-103">Belirtilen işlem düğümündeki görev zamanlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="74b66-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="74b66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74b66-104">SYNTAX</span></span>

### <span data-ttu-id="74b66-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74b66-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74b66-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="74b66-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b66-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="74b66-107">DESCRIPTION</span></span>
<span data-ttu-id="74b66-108">**Enable-AzBatchComputeNodeScheduling** cmdlet 'i belirtilen işlem düğümündeki görev zamanlama özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="74b66-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="74b66-109">Compute düğümü, belirli bir uygulama iş yüküne adanmış bir Azure sanal makinedir.</span><span class="sxs-lookup"><span data-stu-id="74b66-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="74b66-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74b66-110">EXAMPLES</span></span>

### <span data-ttu-id="74b66-111">Örnek 1: işlem düğümündeki görev zamanlamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="74b66-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="74b66-112">Bu komutlar, COMPUTE node TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="74b66-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="74b66-113">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74b66-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="74b66-114">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="74b66-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="74b66-115">İkinci komut daha sonra bu nesne başvurusunu ve **Enable-AzBatchComputeNodeScheduling** cmdlet 'ini kullanır ve myvm-1783593343_34-20151117t222514z üzerinde görev zamanlamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="74b66-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="74b66-116">Örnek 2: havuzdaki işlem düğümlerinde görev zamanlamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="74b66-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="74b66-117">Bu komutlar, havuz Pool06 bulunan tüm işlem düğümlerinde görev zamanlamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="74b66-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="74b66-118">Bu görevi gerçekleştirmek için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarını içeren bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74b66-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="74b66-119">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="74b66-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="74b66-120">Örnekteki ikinci komut bu nesne başvurusunu kullanır ve Pool06 'da bulunan tüm işlem düğümlerinin bir koleksiyonunu döndürmek için **-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="74b66-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="74b66-121">Bu koleksiyon, koleksiyondaki her bir işlem düğümünde görev zamanlama **özelliğini etkinleştiren Enable-AzBatchComputeNodeScheduling** cmdlet 'ine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="74b66-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="74b66-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74b66-122">PARAMETERS</span></span>

### <span data-ttu-id="74b66-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="74b66-123">-BatchContext</span></span>
<span data-ttu-id="74b66-124">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74b66-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="74b66-125">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="74b66-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="74b66-126">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="74b66-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="74b66-127">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="74b66-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="74b66-128">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="74b66-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="74b66-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="74b66-129">-ComputeNode</span></span>
<span data-ttu-id="74b66-130">Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümüne bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="74b66-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="74b66-131">Bu nesne başvurusu, Get-AzBatchComputeNode cmdlet 'i kullanılarak ve döndürülen COMPUTE node nesnesini bir değişkende saklayarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="74b66-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="74b66-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b66-132">-DefaultProfile</span></span>
<span data-ttu-id="74b66-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74b66-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b66-134">-ID</span><span class="sxs-lookup"><span data-stu-id="74b66-134">-Id</span></span>
<span data-ttu-id="74b66-135">Görev zamanlama özelliğinin etkinleştirildiği COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74b66-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="74b66-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="74b66-136">-PoolId</span></span>
<span data-ttu-id="74b66-137">Görev zamanlama 'nın etkinleştirildiği COMPUTE düğümünü içeren toplu iş havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74b66-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="74b66-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b66-138">CommonParameters</span></span>
<span data-ttu-id="74b66-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74b66-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b66-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="74b66-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b66-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74b66-141">INPUTS</span></span>

### <span data-ttu-id="74b66-142">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="74b66-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="74b66-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="74b66-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="74b66-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74b66-144">OUTPUTS</span></span>

### <span data-ttu-id="74b66-145">System. void</span><span class="sxs-lookup"><span data-stu-id="74b66-145">System.Void</span></span>

## <span data-ttu-id="74b66-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74b66-146">NOTES</span></span>

## <span data-ttu-id="74b66-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74b66-147">RELATED LINKS</span></span>

[<span data-ttu-id="74b66-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="74b66-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)

