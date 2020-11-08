---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279223"
---
# <span data-ttu-id="bc52f-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bc52f-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="bc52f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc52f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc52f-103">Havuzu yeniden boyutlandırmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="bc52f-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="bc52f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc52f-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc52f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc52f-105">DESCRIPTION</span></span>
<span data-ttu-id="bc52f-106">**Start-AzBatchPoolResize** cmdlet 'i havuzda bir Azure toplu yeniden boyutlandırma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="bc52f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc52f-107">EXAMPLES</span></span>

### <span data-ttu-id="bc52f-108">Örnek 1: bir havuzu 12 düğüme yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="bc52f-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="bc52f-109">Bu komut, ContosoPool06 KIMLIĞI olan havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="bc52f-110">İşlemin hedefi 12 adanmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="bc52f-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="bc52f-111">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc52f-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bc52f-112">Örnek 2: ayırmayı kaldırma seçeneğini kullanarak havuzu yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="bc52f-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="bc52f-113">Bu cmdlet, havuzu beş ayrılmış işlem düğümüne yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="bc52f-114">Komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="bc52f-115">Komut, ardışık düzen işlecini kullanarak bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc52f-116">Komut, havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="bc52f-117">Hedef beş ayrılmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="bc52f-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="bc52f-118">Komut bir saatin zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="bc52f-119">Komut sonlandırmaya yönelik ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="bc52f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc52f-120">PARAMETERS</span></span>

### <span data-ttu-id="bc52f-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bc52f-121">-BatchContext</span></span>
<span data-ttu-id="bc52f-122">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bc52f-123">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bc52f-124">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="bc52f-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bc52f-125">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc52f-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bc52f-126">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bc52f-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bc52f-127">-Computenodedağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="bc52f-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="bc52f-128">Bu cmdlet 'in başladığı yeniden boyutlandırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc52f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc52f-129">-DefaultProfile</span></span>
<span data-ttu-id="bc52f-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc52f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc52f-131">-ID</span><span class="sxs-lookup"><span data-stu-id="bc52f-131">-Id</span></span>
<span data-ttu-id="bc52f-132">Bu cmdlet 'in yeniden boyutlandıraldığı havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc52f-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="bc52f-133">-ResizeTimeout</span></span>
<span data-ttu-id="bc52f-134">Yeniden boyutlandırma işlemi için zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc52f-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="bc52f-135">Havuz, hedef boyutu şu anda bağlanamazsa, yeniden boyutlandırma işlemi durur.</span><span class="sxs-lookup"><span data-stu-id="bc52f-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc52f-136">-TARGETTE</span><span class="sxs-lookup"><span data-stu-id="bc52f-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="bc52f-137">Hedef adanmış işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="bc52f-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc52f-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="bc52f-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="bc52f-139">Hedef düşük öncelikli işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="bc52f-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc52f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc52f-140">CommonParameters</span></span>
<span data-ttu-id="bc52f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc52f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc52f-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc52f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc52f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc52f-143">INPUTS</span></span>

### <span data-ttu-id="bc52f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bc52f-144">System.String</span></span>

### <span data-ttu-id="bc52f-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bc52f-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bc52f-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc52f-146">OUTPUTS</span></span>

### <span data-ttu-id="bc52f-147">System. void</span><span class="sxs-lookup"><span data-stu-id="bc52f-147">System.Void</span></span>

## <span data-ttu-id="bc52f-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc52f-148">NOTES</span></span>

## <span data-ttu-id="bc52f-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc52f-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc52f-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="bc52f-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bc52f-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="bc52f-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="bc52f-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="bc52f-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="bc52f-153">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bc52f-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
