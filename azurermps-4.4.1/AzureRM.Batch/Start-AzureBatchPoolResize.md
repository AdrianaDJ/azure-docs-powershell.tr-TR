---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591800"
---
# <span data-ttu-id="abc83-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="abc83-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="abc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc83-102">SYNOPSIS</span></span>
<span data-ttu-id="abc83-103">Havuzu yeniden boyutlandırmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="abc83-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abc83-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abc83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abc83-105">DESCRIPTION</span></span>
<span data-ttu-id="abc83-106">**Start-AzureBatchPoolResize** cmdlet 'i havuzda bir Azure toplu yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="abc83-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="abc83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abc83-107">EXAMPLES</span></span>

### <span data-ttu-id="abc83-108">Örnek 1: bir havuzu 12 düğüme yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="abc83-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="abc83-109">Bu komut, ContosoPool06 KIMLIĞI olan havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="abc83-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="abc83-110">İşlemin hedefi 12 adanmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="abc83-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="abc83-111">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abc83-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="abc83-112">Örnek 2: ayırmayı kaldırma seçeneğini kullanarak havuzu yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="abc83-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="abc83-113">Bu cmdlet, havuzu beş ayrılmış işlem düğümüne yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="abc83-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="abc83-114">Komut, Get-AzureBatchPool cmdlet 'ini kullanarak KIMLIĞI ContosoPool06 olan havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="abc83-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="abc83-115">Komut, ardışık düzen işlecini kullanarak bu havuz nesnesini geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="abc83-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abc83-116">Komut, havuzda yeniden boyutlandırma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="abc83-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="abc83-117">Hedef beş ayrılmış işlem düğümünüz.</span><span class="sxs-lookup"><span data-stu-id="abc83-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="abc83-118">Komut bir saatin zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="abc83-119">Komut sonlandırmaya yönelik ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="abc83-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abc83-120">PARAMETERS</span></span>

### <span data-ttu-id="abc83-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="abc83-121">-BatchContext</span></span>
<span data-ttu-id="abc83-122">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="abc83-123">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abc83-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="abc83-124">-Computenodedağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="abc83-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="abc83-125">Bu cmdlet 'in başladığı yeniden boyutlandırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="abc83-126">-ID</span><span class="sxs-lookup"><span data-stu-id="abc83-126">-Id</span></span>
<span data-ttu-id="abc83-127">Bu cmdlet 'in yeniden boyutlandıraldığı havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="abc83-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="abc83-128">-ResizeTimeout</span></span>
<span data-ttu-id="abc83-129">Yeniden boyutlandırma işlemi için zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="abc83-130">Havuz, hedef boyutu şu anda bağlanamazsa, yeniden boyutlandırma işlemi durur.</span><span class="sxs-lookup"><span data-stu-id="abc83-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="abc83-131">-Targetadanmış</span><span class="sxs-lookup"><span data-stu-id="abc83-131">-TargetDedicated</span></span>
<span data-ttu-id="abc83-132">Adanmış işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abc83-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc83-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc83-133">-DefaultProfile</span></span>
<span data-ttu-id="abc83-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abc83-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc83-135">CommonParameters</span></span>
<span data-ttu-id="abc83-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abc83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc83-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc83-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc83-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abc83-138">INPUTS</span></span>

### <span data-ttu-id="abc83-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="abc83-139">BatchAccountContext</span></span>
<span data-ttu-id="abc83-140">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="abc83-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="abc83-141">Dizisi</span><span class="sxs-lookup"><span data-stu-id="abc83-141">String</span></span>
<span data-ttu-id="abc83-142">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="abc83-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="abc83-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abc83-143">OUTPUTS</span></span>

## <span data-ttu-id="abc83-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abc83-144">NOTES</span></span>

## <span data-ttu-id="abc83-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abc83-145">RELATED LINKS</span></span>

[<span data-ttu-id="abc83-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="abc83-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="abc83-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="abc83-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="abc83-148">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="abc83-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="abc83-149">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="abc83-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


