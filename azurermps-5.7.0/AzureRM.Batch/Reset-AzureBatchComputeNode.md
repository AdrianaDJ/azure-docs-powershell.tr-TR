---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764722"
---
# <span data-ttu-id="a43c1-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a43c1-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="a43c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a43c1-103">Belirtilen işlem düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="a43c1-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a43c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a43c1-104">SYNTAX</span></span>

### <span data-ttu-id="a43c1-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a43c1-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43c1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a43c1-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43c1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a43c1-107">DESCRIPTION</span></span>
<span data-ttu-id="a43c1-108">**Reset-AzureBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="a43c1-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a43c1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a43c1-109">EXAMPLES</span></span>

### <span data-ttu-id="a43c1-110">Örnek 1: düğümü yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="a43c1-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a43c1-111">Bu komut MyPool adlı havuzda "TVM-3257026573_2-20150813t200938z" KIMLIĞINE sahip COMPUTE düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a43c1-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="a43c1-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a43c1-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a43c1-113">Örnek 2: havuzdaki tüm düğümleri yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="a43c1-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a43c1-114">Bu komut MyPool adlı havuzda her işlem düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a43c1-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="a43c1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a43c1-115">PARAMETERS</span></span>

### <span data-ttu-id="a43c1-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a43c1-116">-BatchContext</span></span>
<span data-ttu-id="a43c1-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a43c1-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a43c1-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a43c1-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a43c1-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="a43c1-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a43c1-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a43c1-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a43c1-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a43c1-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a43c1-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a43c1-122">-ComputeNode</span></span>
<span data-ttu-id="a43c1-123">ReImage için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a43c1-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="a43c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43c1-124">-DefaultProfile</span></span>
<span data-ttu-id="a43c1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a43c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43c1-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a43c1-126">-Id</span></span>
<span data-ttu-id="a43c1-127">Yeniden görüntülenecek hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a43c1-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="a43c1-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a43c1-128">-PoolId</span></span>
<span data-ttu-id="a43c1-129">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a43c1-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a43c1-130">-Reımageoption</span><span class="sxs-lookup"><span data-stu-id="a43c1-130">-ReimageOption</span></span>
<span data-ttu-id="a43c1-131">Düğümün hangi sırada çalışır durumda olduğunu ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a43c1-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a43c1-132">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="a43c1-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43c1-133">CommonParameters</span></span>
<span data-ttu-id="a43c1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a43c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43c1-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43c1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43c1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a43c1-136">INPUTS</span></span>

### <span data-ttu-id="a43c1-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a43c1-137">BatchAccountContext</span></span>
<span data-ttu-id="a43c1-138">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a43c1-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a43c1-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a43c1-139">PSComputeNode</span></span>
<span data-ttu-id="a43c1-140">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a43c1-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="a43c1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a43c1-141">OUTPUTS</span></span>

## <span data-ttu-id="a43c1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a43c1-142">NOTES</span></span>

## <span data-ttu-id="a43c1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a43c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="a43c1-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a43c1-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="a43c1-145">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a43c1-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="a43c1-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a43c1-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


