---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: c68911de8d01a654593e72b98ba5d53bf40c76ed
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761824"
---
# <span data-ttu-id="59f1d-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="59f1d-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="59f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="59f1d-103">Havuzu yeniden boyutlandırmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="59f1d-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="59f1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59f1d-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="59f1d-106">**Start-AzBatchPoolResize** cmdlet 'i havuzda bir Azure toplu yeniden boyutlandırma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="59f1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="59f1d-108">Örnek 1: bir havuzu 12 düğüme yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="59f1d-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="59f1d-109">Bu komut, ContosoPool06 KIMLIĞI olan havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="59f1d-110">İşlemin hedefi 12 adanmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="59f1d-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="59f1d-111">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="59f1d-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="59f1d-112">Örnek 2: ayırmayı kaldırma seçeneğini kullanarak havuzu yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="59f1d-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="59f1d-113">Bu cmdlet, havuzu beş ayrılmış işlem düğümüne yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="59f1d-114">Komut, Get-AzBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="59f1d-115">Komut, ardışık düzen işlecini kullanarak bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="59f1d-116">Komut, havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="59f1d-117">Hedef beş ayrılmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="59f1d-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="59f1d-118">Komut bir saatin zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="59f1d-119">Komut sonlandırmaya yönelik ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="59f1d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59f1d-120">PARAMETERS</span></span>

### <span data-ttu-id="59f1d-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="59f1d-121">-BatchContext</span></span>
<span data-ttu-id="59f1d-122">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="59f1d-123">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="59f1d-124">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="59f1d-124">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="59f1d-125">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="59f1d-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="59f1d-126">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="59f1d-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="59f1d-127">-Computenodedağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="59f1d-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="59f1d-128">Bu cmdlet 'in başladığı yeniden boyutlandırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="59f1d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f1d-129">-DefaultProfile</span></span>
<span data-ttu-id="59f1d-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59f1d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f1d-131">-ID</span><span class="sxs-lookup"><span data-stu-id="59f1d-131">-Id</span></span>
<span data-ttu-id="59f1d-132">Bu cmdlet 'in yeniden boyutlandıraldığı havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="59f1d-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="59f1d-133">-ResizeTimeout</span></span>
<span data-ttu-id="59f1d-134">Yeniden boyutlandırma işlemi için zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59f1d-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="59f1d-135">Havuz, hedef boyutu şu anda bağlanamazsa, yeniden boyutlandırma işlemi durur.</span><span class="sxs-lookup"><span data-stu-id="59f1d-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="59f1d-136">-TARGETTE</span><span class="sxs-lookup"><span data-stu-id="59f1d-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="59f1d-137">Hedef adanmış işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="59f1d-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="59f1d-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="59f1d-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="59f1d-139">Hedef düşük öncelikli işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="59f1d-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="59f1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f1d-140">CommonParameters</span></span>
<span data-ttu-id="59f1d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59f1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f1d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f1d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f1d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59f1d-143">INPUTS</span></span>

### <span data-ttu-id="59f1d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="59f1d-144">System.String</span></span>

### <span data-ttu-id="59f1d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="59f1d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="59f1d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59f1d-146">OUTPUTS</span></span>

### <span data-ttu-id="59f1d-147">System. void</span><span class="sxs-lookup"><span data-stu-id="59f1d-147">System.Void</span></span>

## <span data-ttu-id="59f1d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59f1d-148">NOTES</span></span>

## <span data-ttu-id="59f1d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59f1d-149">RELATED LINKS</span></span>

[<span data-ttu-id="59f1d-150">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="59f1d-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="59f1d-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="59f1d-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="59f1d-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="59f1d-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="59f1d-153">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="59f1d-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


