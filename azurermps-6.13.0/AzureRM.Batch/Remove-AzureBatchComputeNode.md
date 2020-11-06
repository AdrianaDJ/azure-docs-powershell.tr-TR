---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591410"
---
# <span data-ttu-id="e7f56-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e7f56-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="e7f56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f56-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f56-103">Bir havuzdan işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7f56-104">SYNTAX</span></span>

### <span data-ttu-id="e7f56-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7f56-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7f56-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f56-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f56-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7f56-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f56-108">**Remove-AzureBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="e7f56-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7f56-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f56-110">Örnek 1: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7f56-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="e7f56-111">Bu komut, KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="e7f56-112">Komut, ayırmayı Sonlandır seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="e7f56-113">Yeniden boyutlandırma zaman aşımı 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="e7f56-114">Örnek 2: ardışık düzeni kullanarak hesaplama düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7f56-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="e7f56-115">Bu komut, Get-AzureBatchComputeNode cmdlet 'ini kullanarak KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="e7f56-116">Komut bu düğümü ardışık düzeni kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="e7f56-117">Current cmdlet 'i, COMPUTE düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="e7f56-118">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e7f56-119">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e7f56-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e7f56-120">Örnek 3: birden çok düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="e7f56-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="e7f56-121">Bu komut, Pool07 KIMLIĞINE sahip havuzdan iki compute düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="e7f56-122">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e7f56-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e7f56-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7f56-123">PARAMETERS</span></span>

### <span data-ttu-id="e7f56-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7f56-124">-BatchContext</span></span>
<span data-ttu-id="e7f56-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7f56-126">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e7f56-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e7f56-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e7f56-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e7f56-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e7f56-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e7f56-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e7f56-130">-ComputeNode</span></span>
<span data-ttu-id="e7f56-131">Bu cmdlet 'in kaldırdığı COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e7f56-132">-Dağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="e7f56-132">-DeallocationOption</span></span>
<span data-ttu-id="e7f56-133">Bu cmdlet 'in başladığı kaldırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="e7f56-134">Varsayılan değer requeue ' dır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="e7f56-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f56-135">-DefaultProfile</span></span>
<span data-ttu-id="e7f56-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7f56-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f56-137">-Force</span><span class="sxs-lookup"><span data-stu-id="e7f56-137">-Force</span></span>
<span data-ttu-id="e7f56-138">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e7f56-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f56-139">-Kimlikler</span><span class="sxs-lookup"><span data-stu-id="e7f56-139">-Ids</span></span>
<span data-ttu-id="e7f56-140">Bu cmdlet 'in havuzdan kaldırdığı işlem düğümlerinin kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f56-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e7f56-141">-PoolId</span></span>
<span data-ttu-id="e7f56-142">Bu cmdlet 'in kaldırdığı COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e7f56-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="e7f56-143">-ResizeTimeout</span></span>
<span data-ttu-id="e7f56-144">Havuzdan hesaplama düğümlerinin kaldırılması için zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="e7f56-145">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="e7f56-146">En küçük değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="e7f56-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="e7f56-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7f56-147">-Confirm</span></span>
<span data-ttu-id="e7f56-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7f56-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f56-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f56-149">-WhatIf</span></span>
<span data-ttu-id="e7f56-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7f56-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f56-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7f56-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f56-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f56-152">CommonParameters</span></span>
<span data-ttu-id="e7f56-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7f56-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f56-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f56-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f56-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7f56-155">INPUTS</span></span>

### <span data-ttu-id="e7f56-156">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e7f56-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="e7f56-157">Parametreler: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7f56-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="e7f56-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7f56-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e7f56-159">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7f56-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e7f56-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7f56-160">OUTPUTS</span></span>

### <span data-ttu-id="e7f56-161">System. void</span><span class="sxs-lookup"><span data-stu-id="e7f56-161">System.Void</span></span>

## <span data-ttu-id="e7f56-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7f56-162">NOTES</span></span>

## <span data-ttu-id="e7f56-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7f56-163">RELATED LINKS</span></span>

[<span data-ttu-id="e7f56-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7f56-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e7f56-165">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e7f56-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="e7f56-166">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e7f56-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


