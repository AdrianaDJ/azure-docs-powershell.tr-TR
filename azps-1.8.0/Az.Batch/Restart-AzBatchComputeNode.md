---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 5257076ef13b9a47a7a3729610c55f993bf8d969
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761830"
---
# <span data-ttu-id="609e6-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="609e6-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="609e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609e6-102">SYNOPSIS</span></span>
<span data-ttu-id="609e6-103">Belirtilen işlem düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="609e6-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="609e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="609e6-104">SYNTAX</span></span>

### <span data-ttu-id="609e6-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="609e6-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="609e6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="609e6-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="609e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="609e6-107">DESCRIPTION</span></span>
<span data-ttu-id="609e6-108">**Restart-AzBatchComputeNode** cmdlet 'i belirtilen COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="609e6-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="609e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="609e6-109">EXAMPLES</span></span>

### <span data-ttu-id="609e6-110">Örnek 1: işlem düğümünü yeniden başlatma</span><span class="sxs-lookup"><span data-stu-id="609e6-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="609e6-111">Bu komut, havuz havuzundan "TVM-3257026573_2-20150813t200938z" KIMLIĞIYLE COMPUTE düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="609e6-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="609e6-112">Örnek 2: havuzda her işlem düğümünü yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="609e6-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="609e6-113">Bu komut, havuz MyPool 'daki tüm işlem düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="609e6-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="609e6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="609e6-114">PARAMETERS</span></span>

### <span data-ttu-id="609e6-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="609e6-115">-BatchContext</span></span>
<span data-ttu-id="609e6-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="609e6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="609e6-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="609e6-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="609e6-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="609e6-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="609e6-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="609e6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="609e6-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="609e6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="609e6-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="609e6-121">-ComputeNode</span></span>
<span data-ttu-id="609e6-122">Yeniden başlatmak için COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="609e6-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="609e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609e6-123">-DefaultProfile</span></span>
<span data-ttu-id="609e6-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="609e6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="609e6-125">-ID</span><span class="sxs-lookup"><span data-stu-id="609e6-125">-Id</span></span>
<span data-ttu-id="609e6-126">Yeniden başlatmak için hesaplama düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="609e6-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="609e6-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="609e6-127">-PoolId</span></span>
<span data-ttu-id="609e6-128">Compute düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="609e6-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="609e6-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="609e6-129">-RebootOption</span></span>
<span data-ttu-id="609e6-130">Düğümün hangi durumlarda yeniden başlatılacağınızı ve çalışmakta olan görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="609e6-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="609e6-131">Varsayılan requeue.</span><span class="sxs-lookup"><span data-stu-id="609e6-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="609e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609e6-132">CommonParameters</span></span>
<span data-ttu-id="609e6-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="609e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609e6-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="609e6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609e6-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="609e6-135">INPUTS</span></span>

### <span data-ttu-id="609e6-136">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="609e6-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="609e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="609e6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="609e6-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="609e6-138">OUTPUTS</span></span>

### <span data-ttu-id="609e6-139">System. void</span><span class="sxs-lookup"><span data-stu-id="609e6-139">System.Void</span></span>

## <span data-ttu-id="609e6-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="609e6-140">NOTES</span></span>

## <span data-ttu-id="609e6-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="609e6-141">RELATED LINKS</span></span>

[<span data-ttu-id="609e6-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="609e6-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="609e6-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="609e6-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="609e6-144">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="609e6-144">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


