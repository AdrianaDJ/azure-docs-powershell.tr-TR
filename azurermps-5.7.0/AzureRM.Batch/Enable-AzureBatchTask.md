---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 09e2c8dd4ce1eab68eb2a4237e022034696f9769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764036"
---
# <span data-ttu-id="d959d-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="d959d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d959d-102">SYNOPSIS</span></span>
<span data-ttu-id="d959d-103">Görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="d959d-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d959d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d959d-104">SYNTAX</span></span>

### <span data-ttu-id="d959d-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="d959d-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d959d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d959d-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d959d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d959d-107">DESCRIPTION</span></span>
<span data-ttu-id="d959d-108">**Enable-AzureBatchTask** cmdlet 'i görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="d959d-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="d959d-109">Bir görev yeniden deneme sayısını tüketdiyse, bu cmdlet yine de çalışır.</span><span class="sxs-lookup"><span data-stu-id="d959d-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="d959d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d959d-110">EXAMPLES</span></span>

### <span data-ttu-id="d959d-111">Örnek 1: görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d959d-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="d959d-112">Bu komut, Task2 görev Job7.</span><span class="sxs-lookup"><span data-stu-id="d959d-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="d959d-113">Örnek 2: ardışık düzeni kullanarak görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d959d-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="d959d-114">Bu komut, Get-AzureBatchTask cmdlet 'ini kullanarak KIMLIĞI Job8 olan Task3 KIMLIĞI olan toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="d959d-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="d959d-115">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d959d-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d959d-116">Komut bu görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="d959d-116">The command reactivates that task.</span></span>

## <span data-ttu-id="d959d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d959d-117">PARAMETERS</span></span>

### <span data-ttu-id="d959d-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d959d-118">-BatchContext</span></span>
<span data-ttu-id="d959d-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d959d-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d959d-120">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d959d-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d959d-121">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="d959d-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d959d-122">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d959d-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d959d-123">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d959d-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d959d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d959d-124">-DefaultProfile</span></span>
<span data-ttu-id="d959d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d959d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d959d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d959d-126">-Id</span></span>
<span data-ttu-id="d959d-127">Yeniden etkinleşen görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d959d-127">Specifies the ID of the task to reactivate.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d959d-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="d959d-128">-JobId</span></span>
<span data-ttu-id="d959d-129">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d959d-129">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d959d-130">-Görev</span><span class="sxs-lookup"><span data-stu-id="d959d-130">-Task</span></span>
<span data-ttu-id="d959d-131">Bu cmdlet 'in yeniden kullandığı görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d959d-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="d959d-132">Bir **Ince görev** nesnesi edinmek için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d959d-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d959d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="d959d-133">-Confirm</span></span>
<span data-ttu-id="d959d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d959d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d959d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d959d-135">-WhatIf</span></span>
<span data-ttu-id="d959d-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d959d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d959d-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d959d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d959d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d959d-138">CommonParameters</span></span>
<span data-ttu-id="d959d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d959d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d959d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d959d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d959d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d959d-141">INPUTS</span></span>

### <span data-ttu-id="d959d-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d959d-142">BatchAccountContext</span></span>
<span data-ttu-id="d959d-143">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d959d-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d959d-144">Ince görev</span><span class="sxs-lookup"><span data-stu-id="d959d-144">PSCloudTask</span></span>
<span data-ttu-id="d959d-145">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="d959d-145">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="d959d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d959d-146">OUTPUTS</span></span>

## <span data-ttu-id="d959d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d959d-147">NOTES</span></span>

## <span data-ttu-id="d959d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d959d-148">RELATED LINKS</span></span>

[<span data-ttu-id="d959d-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d959d-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d959d-150">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-150">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="d959d-151">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-151">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="d959d-152">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-152">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="d959d-153">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-153">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="d959d-154">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d959d-154">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


