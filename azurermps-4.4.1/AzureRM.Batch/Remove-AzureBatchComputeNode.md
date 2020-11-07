---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: b134a59a2335eaa3ee95eaddb6b76148739569bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763785"
---
# <span data-ttu-id="b4b83-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b4b83-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="b4b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b83-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b83-103">Bir havuzdan işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4b83-104">SYNTAX</span></span>

### <span data-ttu-id="b4b83-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4b83-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4b83-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4b83-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4b83-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4b83-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b83-108">**Remove-AzureBatchComputeNode** cmdlet 'i bir havuzdan Azure toplu işlem düğümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="b4b83-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4b83-109">EXAMPLES</span></span>

### <span data-ttu-id="b4b83-110">Örnek 1: işlem düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4b83-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="b4b83-111">Bu komut, KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip işlem düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="b4b83-112">Komut, ayırmayı Sonlandır seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="b4b83-113">Yeniden boyutlandırma zaman aşımı 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="b4b83-114">Örnek 2: ardışık düzeni kullanarak hesaplama düğümünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4b83-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="b4b83-115">Bu komut, Get-AzureBatchComputeNode cmdlet 'ini kullanarak KIMLIĞI Pool07 olan havuzdan belirtilen KIMLIĞE sahip COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="b4b83-116">Komut bu düğümü ardışık düzeni kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="b4b83-117">Current cmdlet 'i, COMPUTE düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="b4b83-118">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b4b83-119">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="b4b83-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b4b83-120">Örnek 3: birden çok düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="b4b83-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="b4b83-121">Bu komut, Pool07 KIMLIĞINE sahip havuzdan iki compute düğümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="b4b83-122">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="b4b83-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b4b83-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4b83-123">PARAMETERS</span></span>

### <span data-ttu-id="b4b83-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4b83-124">-BatchContext</span></span>
<span data-ttu-id="b4b83-125">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4b83-126">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4b83-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b4b83-127">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b4b83-127">-ComputeNode</span></span>
<span data-ttu-id="b4b83-128">Bu cmdlet 'in kaldırdığı COMPUTE düğümünü temsil eden **PSComputeNode** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-128">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4b83-129">-Dağıtıkonumseçeneği</span><span class="sxs-lookup"><span data-stu-id="b4b83-129">-DeallocationOption</span></span>
<span data-ttu-id="b4b83-130">Bu cmdlet 'in başladığı kaldırma işlemi için ayırmayı kaldırma seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-130">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="b4b83-131">Varsayılan değer requeue ' dır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-131">The default value is Requeue.</span></span>

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

### <span data-ttu-id="b4b83-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b4b83-132">-Force</span></span>
<span data-ttu-id="b4b83-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b4b83-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4b83-134">-Kimlikler</span><span class="sxs-lookup"><span data-stu-id="b4b83-134">-Ids</span></span>
<span data-ttu-id="b4b83-135">Bu cmdlet 'in havuzdan kaldırdığı işlem düğümlerinin kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-135">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="b4b83-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b4b83-136">-PoolId</span></span>
<span data-ttu-id="b4b83-137">Bu cmdlet 'in kaldırdığı COMPUTE düğümlerini içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-137">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4b83-138">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="b4b83-138">-ResizeTimeout</span></span>
<span data-ttu-id="b4b83-139">Havuzdan hesaplama düğümlerinin kaldırılması için zaman aşımı aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-139">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="b4b83-140">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-140">The default value is 10 minutes.</span></span>
<span data-ttu-id="b4b83-141">En küçük değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b4b83-141">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="b4b83-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4b83-142">-Confirm</span></span>
<span data-ttu-id="b4b83-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4b83-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b83-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b83-144">-WhatIf</span></span>
<span data-ttu-id="b4b83-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4b83-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b83-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4b83-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b83-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b83-147">-DefaultProfile</span></span>
<span data-ttu-id="b4b83-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4b83-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b83-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b83-149">CommonParameters</span></span>
<span data-ttu-id="b4b83-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4b83-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b83-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b83-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b83-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4b83-152">INPUTS</span></span>

### <span data-ttu-id="b4b83-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4b83-153">BatchAccountContext</span></span>
<span data-ttu-id="b4b83-154">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b4b83-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b4b83-155">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b4b83-155">PSComputeNode</span></span>
<span data-ttu-id="b4b83-156">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b4b83-156">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="b4b83-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4b83-157">OUTPUTS</span></span>

## <span data-ttu-id="b4b83-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4b83-158">NOTES</span></span>

## <span data-ttu-id="b4b83-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4b83-159">RELATED LINKS</span></span>

[<span data-ttu-id="b4b83-160">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4b83-160">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b4b83-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b4b83-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="b4b83-162">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b4b83-162">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


