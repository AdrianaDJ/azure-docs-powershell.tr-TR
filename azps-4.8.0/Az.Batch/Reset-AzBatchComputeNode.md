---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109180"
---
# <span data-ttu-id="b266e-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b266e-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="b266e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b266e-102">SYNOPSIS</span></span>
<span data-ttu-id="b266e-103">Belirtilen işlem düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="b266e-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="b266e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b266e-104">SYNTAX</span></span>

### <span data-ttu-id="b266e-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b266e-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b266e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b266e-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b266e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b266e-107">DESCRIPTION</span></span>
<span data-ttu-id="b266e-108">**Reset-AzBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="b266e-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="b266e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b266e-109">EXAMPLES</span></span>

### <span data-ttu-id="b266e-110">Örnek 1: düğümü yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="b266e-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="b266e-111">Bu komut MyPool adlı havuzda "TVM-3257026573_2-20150813t200938z" KIMLIĞINE sahip COMPUTE düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b266e-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="b266e-112">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b266e-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b266e-113">Örnek 2: havuzdaki tüm düğümleri yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="b266e-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="b266e-114">Bu komut MyPool adlı havuzda her işlem düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b266e-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="b266e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b266e-115">PARAMETERS</span></span>

### <span data-ttu-id="b266e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b266e-116">-BatchContext</span></span>
<span data-ttu-id="b266e-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b266e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b266e-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b266e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b266e-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b266e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b266e-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b266e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b266e-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b266e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b266e-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b266e-122">-ComputeNode</span></span>
<span data-ttu-id="b266e-123">ReImage için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b266e-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="b266e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b266e-124">-DefaultProfile</span></span>
<span data-ttu-id="b266e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b266e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b266e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b266e-126">-Id</span></span>
<span data-ttu-id="b266e-127">Yeniden görüntülenecek hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b266e-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="b266e-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b266e-128">-PoolId</span></span>
<span data-ttu-id="b266e-129">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b266e-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="b266e-130">-Reımageoption</span><span class="sxs-lookup"><span data-stu-id="b266e-130">-ReimageOption</span></span>
<span data-ttu-id="b266e-131">Düğümün hangi sırada çalışır durumda olduğunu ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b266e-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="b266e-132">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="b266e-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b266e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b266e-133">CommonParameters</span></span>
<span data-ttu-id="b266e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b266e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b266e-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b266e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b266e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b266e-136">INPUTS</span></span>

### <span data-ttu-id="b266e-137">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b266e-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b266e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b266e-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b266e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b266e-139">OUTPUTS</span></span>

### <span data-ttu-id="b266e-140">System. void</span><span class="sxs-lookup"><span data-stu-id="b266e-140">System.Void</span></span>

## <span data-ttu-id="b266e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b266e-141">NOTES</span></span>

## <span data-ttu-id="b266e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b266e-142">RELATED LINKS</span></span>

[<span data-ttu-id="b266e-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b266e-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="b266e-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b266e-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="b266e-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b266e-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
