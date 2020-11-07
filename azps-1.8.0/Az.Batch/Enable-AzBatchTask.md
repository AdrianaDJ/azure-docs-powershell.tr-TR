---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761900"
---
# <span data-ttu-id="f8e99-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="f8e99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e99-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e99-103">Görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-103">Reactivates a task.</span></span>

## <span data-ttu-id="f8e99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8e99-104">SYNTAX</span></span>

### <span data-ttu-id="f8e99-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="f8e99-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8e99-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f8e99-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8e99-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8e99-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e99-108">**Enable-AzBatchTask** cmdlet 'i görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="f8e99-109">Bir görev yeniden deneme sayısını tüketdiyse, bu cmdlet yine de çalışır.</span><span class="sxs-lookup"><span data-stu-id="f8e99-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="f8e99-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8e99-110">EXAMPLES</span></span>

### <span data-ttu-id="f8e99-111">Örnek 1: görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f8e99-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="f8e99-112">Bu komut, Task2 görev Job7.</span><span class="sxs-lookup"><span data-stu-id="f8e99-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="f8e99-113">Örnek 2: ardışık düzeni kullanarak görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f8e99-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="f8e99-114">Bu komut, Get-AzBatchTask cmdlet 'ini kullanarak KIMLIĞI Job8 olan Task3 KIMLIĞI olan toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="f8e99-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="f8e99-115">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f8e99-116">Komut bu görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-116">The command reactivates that task.</span></span>

## <span data-ttu-id="f8e99-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8e99-117">PARAMETERS</span></span>

### <span data-ttu-id="f8e99-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f8e99-118">-BatchContext</span></span>
<span data-ttu-id="f8e99-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f8e99-120">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8e99-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f8e99-121">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f8e99-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f8e99-122">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8e99-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f8e99-123">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f8e99-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f8e99-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e99-124">-DefaultProfile</span></span>
<span data-ttu-id="f8e99-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8e99-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e99-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f8e99-126">-Id</span></span>
<span data-ttu-id="f8e99-127">Yeniden etkinleşen görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="f8e99-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="f8e99-128">-JobId</span></span>
<span data-ttu-id="f8e99-129">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="f8e99-130">-Görev</span><span class="sxs-lookup"><span data-stu-id="f8e99-130">-Task</span></span>
<span data-ttu-id="f8e99-131">Bu cmdlet 'in yeniden kullandığı görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="f8e99-132">Bir **Ince görev** nesnesi edinmek için Get-AzBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f8e99-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="f8e99-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8e99-133">-Confirm</span></span>
<span data-ttu-id="f8e99-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8e99-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8e99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e99-135">-WhatIf</span></span>
<span data-ttu-id="f8e99-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8e99-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e99-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8e99-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8e99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e99-138">CommonParameters</span></span>
<span data-ttu-id="f8e99-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8e99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e99-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e99-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e99-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8e99-141">INPUTS</span></span>

### <span data-ttu-id="f8e99-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e99-142">System.String</span></span>

### <span data-ttu-id="f8e99-143">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="f8e99-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="f8e99-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f8e99-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f8e99-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8e99-145">OUTPUTS</span></span>

### <span data-ttu-id="f8e99-146">System. void</span><span class="sxs-lookup"><span data-stu-id="f8e99-146">System.Void</span></span>

## <span data-ttu-id="f8e99-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8e99-147">NOTES</span></span>

## <span data-ttu-id="f8e99-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8e99-148">RELATED LINKS</span></span>

[<span data-ttu-id="f8e99-149">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="f8e99-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f8e99-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="f8e99-151">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="f8e99-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="f8e99-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="f8e99-154">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f8e99-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

