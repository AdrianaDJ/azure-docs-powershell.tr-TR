---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589894"
---
# <span data-ttu-id="083df-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="083df-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="083df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="083df-102">SYNOPSIS</span></span>
<span data-ttu-id="083df-103">Belirtilen işlem düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="083df-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="083df-104">SYNTAX</span></span>

### <span data-ttu-id="083df-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="083df-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083df-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="083df-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="083df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="083df-107">DESCRIPTION</span></span>
<span data-ttu-id="083df-108">**Restart-AzureBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="083df-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="083df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="083df-109">EXAMPLES</span></span>

### <span data-ttu-id="083df-110">Örnek 1: işlem düğümünü yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="083df-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="083df-111">Bu komut, havuz havuzundan "TVM-3257026573_2-20150813t200938z" KIMLIĞIYLE COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="083df-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="083df-112">Örnek 2: havuzda her işlem düğümünü yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="083df-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="083df-113">Bu komut, havuz MyPool 'daki tüm işlem düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="083df-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="083df-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="083df-114">PARAMETERS</span></span>

### <span data-ttu-id="083df-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="083df-115">-BatchContext</span></span>
<span data-ttu-id="083df-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="083df-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="083df-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="083df-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="083df-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="083df-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="083df-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="083df-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="083df-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="083df-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="083df-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="083df-121">-ComputeNode</span></span>
<span data-ttu-id="083df-122">Yeniden başlatmak için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="083df-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="083df-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083df-123">-DefaultProfile</span></span>
<span data-ttu-id="083df-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="083df-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="083df-125">-ID</span><span class="sxs-lookup"><span data-stu-id="083df-125">-Id</span></span>
<span data-ttu-id="083df-126">Yeniden başlatmak için hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="083df-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="083df-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="083df-127">-PoolId</span></span>
<span data-ttu-id="083df-128">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="083df-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="083df-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="083df-129">-RebootOption</span></span>
<span data-ttu-id="083df-130">Düğümün hangi durumlarda yeniden başlatılacağınızı ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="083df-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="083df-131">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="083df-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083df-132">CommonParameters</span></span>
<span data-ttu-id="083df-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="083df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083df-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083df-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083df-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="083df-135">INPUTS</span></span>

### <span data-ttu-id="083df-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="083df-136">BatchAccountContext</span></span>
<span data-ttu-id="083df-137">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="083df-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="083df-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="083df-138">PSComputeNode</span></span>
<span data-ttu-id="083df-139">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="083df-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="083df-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="083df-140">OUTPUTS</span></span>

## <span data-ttu-id="083df-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="083df-141">NOTES</span></span>

## <span data-ttu-id="083df-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="083df-142">RELATED LINKS</span></span>

[<span data-ttu-id="083df-143">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="083df-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="083df-144">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="083df-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="083df-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="083df-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


