---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762882"
---
# <span data-ttu-id="88ff0-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="88ff0-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="88ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="88ff0-103">Belirtilen işlem düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="88ff0-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ff0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88ff0-104">SYNTAX</span></span>

### <span data-ttu-id="88ff0-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88ff0-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88ff0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="88ff0-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ff0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88ff0-107">DESCRIPTION</span></span>
<span data-ttu-id="88ff0-108">**Reset-AzureBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümüne işletim sistemini yeniden yükler.</span><span class="sxs-lookup"><span data-stu-id="88ff0-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="88ff0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88ff0-109">EXAMPLES</span></span>

### <span data-ttu-id="88ff0-110">Örnek 1: düğümü yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="88ff0-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="88ff0-111">Bu komut MyPool adlı havuzda "TVM-3257026573_2-20150813t200938z" KIMLIĞINE sahip COMPUTE düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="88ff0-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="88ff0-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="88ff0-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="88ff0-113">Örnek 2: havuzdaki tüm düğümleri yeniden görüntüler</span><span class="sxs-lookup"><span data-stu-id="88ff0-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="88ff0-114">Bu komut MyPool adlı havuzda her işlem düğümünü yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="88ff0-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="88ff0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88ff0-115">PARAMETERS</span></span>

### <span data-ttu-id="88ff0-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88ff0-116">-BatchContext</span></span>
<span data-ttu-id="88ff0-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ff0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88ff0-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="88ff0-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="88ff0-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="88ff0-119">-ComputeNode</span></span>
<span data-ttu-id="88ff0-120">ReImage için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ff0-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="88ff0-121">-ID</span><span class="sxs-lookup"><span data-stu-id="88ff0-121">-Id</span></span>
<span data-ttu-id="88ff0-122">Yeniden görüntülenecek hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ff0-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="88ff0-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88ff0-123">-PoolId</span></span>
<span data-ttu-id="88ff0-124">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ff0-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="88ff0-125">-Reımageoption</span><span class="sxs-lookup"><span data-stu-id="88ff0-125">-ReimageOption</span></span>
<span data-ttu-id="88ff0-126">Düğümün hangi sırada çalışır durumda olduğunu ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88ff0-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="88ff0-127">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="88ff0-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="88ff0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ff0-128">-DefaultProfile</span></span>
<span data-ttu-id="88ff0-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88ff0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ff0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ff0-130">CommonParameters</span></span>
<span data-ttu-id="88ff0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88ff0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ff0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ff0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ff0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88ff0-133">INPUTS</span></span>

### <span data-ttu-id="88ff0-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88ff0-134">BatchAccountContext</span></span>
<span data-ttu-id="88ff0-135">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="88ff0-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="88ff0-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="88ff0-136">PSComputeNode</span></span>
<span data-ttu-id="88ff0-137">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="88ff0-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="88ff0-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88ff0-138">OUTPUTS</span></span>

## <span data-ttu-id="88ff0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88ff0-139">NOTES</span></span>

## <span data-ttu-id="88ff0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88ff0-140">RELATED LINKS</span></span>

[<span data-ttu-id="88ff0-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="88ff0-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="88ff0-142">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="88ff0-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="88ff0-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="88ff0-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


