---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097911"
---
# <span data-ttu-id="4c28b-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c28b-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="4c28b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c28b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c28b-103">Bir havuzdan işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="4c28b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c28b-104">SYNTAX</span></span>

### <span data-ttu-id="4c28b-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c28b-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c28b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4c28b-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c28b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c28b-107">DESCRIPTION</span></span>
<span data-ttu-id="4c28b-108">**Remove-AzBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="4c28b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c28b-109">EXAMPLES</span></span>

### <span data-ttu-id="4c28b-110">Örnek 1: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c28b-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="4c28b-111">Bu komut, KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="4c28b-112">Komut, ayırmayı Sonlandır seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="4c28b-113">Yeniden boyutlandırma zaman aşımı 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="4c28b-114">Örnek 2: ardışık düzeni kullanarak hesaplama düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c28b-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="4c28b-115">Bu komut, Get-AzBatchComputeNode cmdlet 'ini kullanarak KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="4c28b-116">Komut bu düğümü ardışık düzeni kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="4c28b-117">Current cmdlet 'i, COMPUTE düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="4c28b-118">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4c28b-119">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="4c28b-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4c28b-120">Örnek 3: birden çok düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c28b-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="4c28b-121">Bu komut, Pool07 KIMLIĞINE sahip havuzdan iki compute düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="4c28b-122">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="4c28b-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4c28b-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c28b-123">PARAMETERS</span></span>

### <span data-ttu-id="4c28b-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4c28b-124">-BatchContext</span></span>
<span data-ttu-id="4c28b-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4c28b-126">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4c28b-127">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="4c28b-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4c28b-128">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4c28b-129">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4c28b-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4c28b-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c28b-130">-ComputeNode</span></span>
<span data-ttu-id="4c28b-131">Bu cmdlet 'in kaldırdığı COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c28b-132">-Dağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="4c28b-132">-DeallocationOption</span></span>
<span data-ttu-id="4c28b-133">Bu cmdlet 'in başladığı kaldırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="4c28b-134">Varsayılan değer requeue ' dır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="4c28b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c28b-135">-DefaultProfile</span></span>
<span data-ttu-id="4c28b-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c28b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c28b-137">-Force</span><span class="sxs-lookup"><span data-stu-id="4c28b-137">-Force</span></span>
<span data-ttu-id="4c28b-138">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4c28b-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c28b-139">-Kimlikler</span><span class="sxs-lookup"><span data-stu-id="4c28b-139">-Ids</span></span>
<span data-ttu-id="4c28b-140">Bu cmdlet 'in havuzdan kaldırdığı işlem düğümlerinin kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="4c28b-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4c28b-141">-PoolId</span></span>
<span data-ttu-id="4c28b-142">Bu cmdlet 'in kaldırdığı COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c28b-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="4c28b-143">-ResizeTimeout</span></span>
<span data-ttu-id="4c28b-144">Havuzdan hesaplama düğümlerinin kaldırılması için zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="4c28b-145">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="4c28b-146">En küçük değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="4c28b-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="4c28b-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c28b-147">-Confirm</span></span>
<span data-ttu-id="4c28b-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c28b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c28b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c28b-149">-WhatIf</span></span>
<span data-ttu-id="4c28b-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c28b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c28b-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c28b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c28b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c28b-152">CommonParameters</span></span>
<span data-ttu-id="4c28b-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c28b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c28b-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c28b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c28b-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c28b-155">INPUTS</span></span>

### <span data-ttu-id="4c28b-156">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c28b-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="4c28b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4c28b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4c28b-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c28b-158">OUTPUTS</span></span>

### <span data-ttu-id="4c28b-159">System. void</span><span class="sxs-lookup"><span data-stu-id="4c28b-159">System.Void</span></span>

## <span data-ttu-id="4c28b-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c28b-160">NOTES</span></span>

## <span data-ttu-id="4c28b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c28b-161">RELATED LINKS</span></span>

[<span data-ttu-id="4c28b-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4c28b-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4c28b-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c28b-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="4c28b-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="4c28b-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


