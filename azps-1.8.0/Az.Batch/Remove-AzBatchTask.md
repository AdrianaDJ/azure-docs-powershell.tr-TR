---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761833"
---
# <span data-ttu-id="97c0e-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="97c0e-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="97c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="97c0e-103">Toplu Iş görevini siler.</span><span class="sxs-lookup"><span data-stu-id="97c0e-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="97c0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97c0e-104">SYNTAX</span></span>

### <span data-ttu-id="97c0e-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="97c0e-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c0e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="97c0e-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c0e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="97c0e-107">DESCRIPTION</span></span>
<span data-ttu-id="97c0e-108">**Remove-AzBatchTask** cmdlet 'ı bir Azure toplu görevini siler.</span><span class="sxs-lookup"><span data-stu-id="97c0e-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="97c0e-109">*Force* parametresini belirtmediğiniz sürece, bu cmdlet onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97c0e-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="97c0e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="97c0e-111">Örnek 1: KIMLIĞE göre toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="97c0e-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="97c0e-112">Bu komut, kimliği Iş-000001 olan işin altında KIMLIK Task23 olan bir görevi siler.</span><span class="sxs-lookup"><span data-stu-id="97c0e-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="97c0e-113">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97c0e-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="97c0e-114">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="97c0e-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="97c0e-115">Örnek 2: onay olmadan ardışık düzeni kullanarak toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="97c0e-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="97c0e-116">Bu komut, **Get-AzBatchTask** cmdlet 'ini kullanarak 000001 Job-olan Iş 'Te kimliği Task26 olan toplu iş görevini alır.</span><span class="sxs-lookup"><span data-stu-id="97c0e-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="97c0e-117">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="97c0e-118">Komut bu görevi siler.</span><span class="sxs-lookup"><span data-stu-id="97c0e-118">The command deletes that task.</span></span>
<span data-ttu-id="97c0e-119">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="97c0e-120">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="97c0e-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="97c0e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97c0e-121">PARAMETERS</span></span>

### <span data-ttu-id="97c0e-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="97c0e-122">-BatchContext</span></span>
<span data-ttu-id="97c0e-123">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="97c0e-124">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97c0e-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="97c0e-125">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="97c0e-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="97c0e-126">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97c0e-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="97c0e-127">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="97c0e-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="97c0e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c0e-128">-DefaultProfile</span></span>
<span data-ttu-id="97c0e-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97c0e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c0e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="97c0e-130">-Force</span></span>
<span data-ttu-id="97c0e-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="97c0e-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97c0e-132">-ID</span><span class="sxs-lookup"><span data-stu-id="97c0e-132">-Id</span></span>
<span data-ttu-id="97c0e-133">Bu cmdlet 'in sildiği görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="97c0e-134">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="97c0e-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c0e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c0e-135">-InputObject</span></span>
<span data-ttu-id="97c0e-136">Bu cmdlet 'in sildiği görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="97c0e-137">Bir **Ince görev** nesnesi edinmek için Get-AzBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="97c0e-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c0e-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="97c0e-138">-JobId</span></span>
<span data-ttu-id="97c0e-139">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97c0e-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="97c0e-140">-Confirm</span></span>
<span data-ttu-id="97c0e-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97c0e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c0e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c0e-142">-WhatIf</span></span>
<span data-ttu-id="97c0e-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97c0e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c0e-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97c0e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c0e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c0e-145">CommonParameters</span></span>
<span data-ttu-id="97c0e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97c0e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c0e-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c0e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c0e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97c0e-148">INPUTS</span></span>

### <span data-ttu-id="97c0e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="97c0e-149">System.String</span></span>

### <span data-ttu-id="97c0e-150">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="97c0e-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="97c0e-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="97c0e-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="97c0e-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97c0e-152">OUTPUTS</span></span>

### <span data-ttu-id="97c0e-153">System. void</span><span class="sxs-lookup"><span data-stu-id="97c0e-153">System.Void</span></span>

## <span data-ttu-id="97c0e-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97c0e-154">NOTES</span></span>

## <span data-ttu-id="97c0e-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97c0e-155">RELATED LINKS</span></span>

[<span data-ttu-id="97c0e-156">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="97c0e-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="97c0e-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="97c0e-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="97c0e-158">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="97c0e-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="97c0e-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="97c0e-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="97c0e-160">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="97c0e-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="97c0e-161">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="97c0e-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


