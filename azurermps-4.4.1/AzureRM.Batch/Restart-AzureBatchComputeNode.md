---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592671"
---
# <span data-ttu-id="c242f-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c242f-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="c242f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c242f-102">SYNOPSIS</span></span>
<span data-ttu-id="c242f-103">Belirtilen işlem düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c242f-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c242f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c242f-104">SYNTAX</span></span>

### <span data-ttu-id="c242f-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c242f-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c242f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c242f-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c242f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c242f-107">DESCRIPTION</span></span>
<span data-ttu-id="c242f-108">**Restart-AzureBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c242f-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="c242f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c242f-109">EXAMPLES</span></span>

### <span data-ttu-id="c242f-110">Örnek 1: işlem düğümünü yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="c242f-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="c242f-111">Bu komut, havuz havuzundan "TVM-3257026573_2-20150813t200938z" KIMLIĞIYLE COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c242f-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="c242f-112">Örnek 2: havuzda her işlem düğümünü yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="c242f-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="c242f-113">Bu komut, havuz MyPool 'daki tüm işlem düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="c242f-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="c242f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c242f-114">PARAMETERS</span></span>

### <span data-ttu-id="c242f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c242f-115">-BatchContext</span></span>
<span data-ttu-id="c242f-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c242f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c242f-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c242f-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c242f-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c242f-118">-ComputeNode</span></span>
<span data-ttu-id="c242f-119">Yeniden başlatmak için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c242f-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="c242f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c242f-120">-Id</span></span>
<span data-ttu-id="c242f-121">Yeniden başlatmak için hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c242f-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="c242f-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c242f-122">-PoolId</span></span>
<span data-ttu-id="c242f-123">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c242f-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="c242f-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="c242f-124">-RebootOption</span></span>
<span data-ttu-id="c242f-125">Düğümün hangi durumlarda yeniden başlatılacağınızı ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c242f-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="c242f-126">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="c242f-126">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c242f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c242f-127">-DefaultProfile</span></span>
<span data-ttu-id="c242f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c242f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c242f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c242f-129">CommonParameters</span></span>
<span data-ttu-id="c242f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c242f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c242f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c242f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c242f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c242f-132">INPUTS</span></span>

### <span data-ttu-id="c242f-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c242f-133">BatchAccountContext</span></span>
<span data-ttu-id="c242f-134">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c242f-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c242f-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c242f-135">PSComputeNode</span></span>
<span data-ttu-id="c242f-136">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c242f-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="c242f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c242f-137">OUTPUTS</span></span>

## <span data-ttu-id="c242f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c242f-138">NOTES</span></span>

## <span data-ttu-id="c242f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c242f-139">RELATED LINKS</span></span>

[<span data-ttu-id="c242f-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c242f-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c242f-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c242f-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="c242f-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c242f-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


