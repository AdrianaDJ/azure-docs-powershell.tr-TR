---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: b460eb4377f06cfa7348f06cdd60f2013e5b5e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587678"
---
# <span data-ttu-id="705f8-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="705f8-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="705f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="705f8-102">SYNOPSIS</span></span>
<span data-ttu-id="705f8-103">Havuzu yeniden boyutlandırmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="705f8-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="705f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="705f8-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="705f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="705f8-105">DESCRIPTION</span></span>
<span data-ttu-id="705f8-106">**Start-AzureBatchPoolResize** cmdlet 'i havuzda bir Azure toplu yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="705f8-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="705f8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="705f8-107">EXAMPLES</span></span>

### <span data-ttu-id="705f8-108">Örnek 1: bir havuzu 12 düğüme yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="705f8-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="705f8-109">Bu komut, ContosoPool06 KIMLIĞI olan havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="705f8-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="705f8-110">İşlemin hedefi 12 adanmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="705f8-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="705f8-111">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="705f8-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="705f8-112">Örnek 2: ayırmayı kaldırma seçeneğini kullanarak havuzu yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="705f8-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="705f8-113">Bu cmdlet, havuzu beş ayrılmış işlem düğümüne yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="705f8-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="705f8-114">Komut, Get-AzureBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="705f8-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="705f8-115">Komut, ardışık düzen işlecini kullanarak bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="705f8-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="705f8-116">Komut, havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="705f8-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="705f8-117">Hedef beş ayrılmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="705f8-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="705f8-118">Komut bir saatin zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="705f8-119">Komut sonlandırmaya yönelik ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="705f8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="705f8-120">PARAMETERS</span></span>

### <span data-ttu-id="705f8-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="705f8-121">-BatchContext</span></span>
<span data-ttu-id="705f8-122">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="705f8-123">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="705f8-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="705f8-124">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="705f8-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="705f8-125">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="705f8-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="705f8-126">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="705f8-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="705f8-127">-Computenodedağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="705f8-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="705f8-128">Bu cmdlet 'in başladığı yeniden boyutlandırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705f8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705f8-129">-DefaultProfile</span></span>
<span data-ttu-id="705f8-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="705f8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="705f8-131">-ID</span><span class="sxs-lookup"><span data-stu-id="705f8-131">-Id</span></span>
<span data-ttu-id="705f8-132">Bu cmdlet 'in yeniden boyutlandıraldığı havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="705f8-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="705f8-133">-ResizeTimeout</span></span>
<span data-ttu-id="705f8-134">Yeniden boyutlandırma işlemi için zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="705f8-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="705f8-135">Havuz, hedef boyutu şu anda bağlanamazsa, yeniden boyutlandırma işlemi durur.</span><span class="sxs-lookup"><span data-stu-id="705f8-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705f8-136">-TARGETTE</span><span class="sxs-lookup"><span data-stu-id="705f8-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="705f8-137">Hedef adanmış işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="705f8-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705f8-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="705f8-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="705f8-139">Hedef düşük öncelikli işlem düğümlerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="705f8-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705f8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705f8-140">CommonParameters</span></span>
<span data-ttu-id="705f8-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="705f8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705f8-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705f8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705f8-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="705f8-143">INPUTS</span></span>

### <span data-ttu-id="705f8-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="705f8-144">BatchAccountContext</span></span>
<span data-ttu-id="705f8-145">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="705f8-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="705f8-146">Dizisi</span><span class="sxs-lookup"><span data-stu-id="705f8-146">String</span></span>
<span data-ttu-id="705f8-147">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="705f8-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="705f8-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="705f8-148">OUTPUTS</span></span>

## <span data-ttu-id="705f8-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="705f8-149">NOTES</span></span>

## <span data-ttu-id="705f8-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="705f8-150">RELATED LINKS</span></span>

[<span data-ttu-id="705f8-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="705f8-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="705f8-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="705f8-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="705f8-153">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="705f8-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="705f8-154">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="705f8-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


