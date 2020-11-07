---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 6350505efe3f3e7c571fee6940cf678706c4fc7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764183"
---
# <span data-ttu-id="94286-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="94286-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="94286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94286-102">SYNOPSIS</span></span>
<span data-ttu-id="94286-103">Bir havuzdan işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94286-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94286-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94286-104">SYNTAX</span></span>

### <span data-ttu-id="94286-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94286-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94286-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="94286-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94286-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94286-107">DESCRIPTION</span></span>
<span data-ttu-id="94286-108">**Remove-AzureBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94286-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="94286-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94286-109">EXAMPLES</span></span>

### <span data-ttu-id="94286-110">Örnek 1: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="94286-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="94286-111">Bu komut, KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94286-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="94286-112">Komut, ayırmayı Sonlandır seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="94286-113">Yeniden boyutlandırma zaman aşımı 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="94286-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="94286-114">Örnek 2: ardışık düzeni kullanarak hesaplama düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="94286-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="94286-115">Bu komut, Get-AzureBatchComputeNode cmdlet 'ini kullanarak KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="94286-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="94286-116">Komut bu düğümü ardışık düzeni kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="94286-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="94286-117">Current cmdlet 'i, COMPUTE düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94286-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="94286-118">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="94286-119">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="94286-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="94286-120">Örnek 3: birden çok düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="94286-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="94286-121">Bu komut, Pool07 KIMLIĞINE sahip havuzdan iki compute düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94286-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="94286-122">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="94286-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="94286-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94286-123">PARAMETERS</span></span>

### <span data-ttu-id="94286-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94286-124">-BatchContext</span></span>
<span data-ttu-id="94286-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94286-126">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94286-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94286-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="94286-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94286-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94286-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94286-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="94286-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94286-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="94286-130">-ComputeNode</span></span>
<span data-ttu-id="94286-131">Bu cmdlet 'in kaldırdığı COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94286-132">-Dağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="94286-132">-DeallocationOption</span></span>
<span data-ttu-id="94286-133">Bu cmdlet 'in başladığı kaldırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="94286-134">Varsayılan değer requeue ' dır.</span><span class="sxs-lookup"><span data-stu-id="94286-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="94286-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94286-135">-DefaultProfile</span></span>
<span data-ttu-id="94286-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94286-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94286-137">-Force</span><span class="sxs-lookup"><span data-stu-id="94286-137">-Force</span></span>
<span data-ttu-id="94286-138">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="94286-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94286-139">-Kimlikler</span><span class="sxs-lookup"><span data-stu-id="94286-139">-Ids</span></span>
<span data-ttu-id="94286-140">Bu cmdlet 'in havuzdan kaldırdığı işlem düğümlerinin kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94286-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="94286-141">-PoolId</span></span>
<span data-ttu-id="94286-142">Bu cmdlet 'in kaldırdığı COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94286-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="94286-143">-ResizeTimeout</span></span>
<span data-ttu-id="94286-144">Havuzdan hesaplama düğümlerinin kaldırılması için zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94286-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="94286-145">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="94286-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="94286-146">En küçük değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="94286-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="94286-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="94286-147">-Confirm</span></span>
<span data-ttu-id="94286-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94286-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94286-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94286-149">-WhatIf</span></span>
<span data-ttu-id="94286-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94286-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94286-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94286-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94286-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94286-152">CommonParameters</span></span>
<span data-ttu-id="94286-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94286-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94286-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94286-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94286-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94286-155">INPUTS</span></span>

### <span data-ttu-id="94286-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94286-156">BatchAccountContext</span></span>
<span data-ttu-id="94286-157">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="94286-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="94286-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="94286-158">PSComputeNode</span></span>
<span data-ttu-id="94286-159">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="94286-159">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="94286-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94286-160">OUTPUTS</span></span>

## <span data-ttu-id="94286-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94286-161">NOTES</span></span>

## <span data-ttu-id="94286-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94286-162">RELATED LINKS</span></span>

[<span data-ttu-id="94286-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="94286-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="94286-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="94286-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="94286-165">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="94286-165">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


