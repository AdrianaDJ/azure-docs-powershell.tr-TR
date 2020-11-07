---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764903"
---
# <span data-ttu-id="12175-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="12175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12175-102">SYNOPSIS</span></span>
<span data-ttu-id="12175-103">Görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="12175-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12175-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12175-104">SYNTAX</span></span>

### <span data-ttu-id="12175-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="12175-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12175-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="12175-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12175-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12175-107">DESCRIPTION</span></span>
<span data-ttu-id="12175-108">**Enable-AzureBatchTask** cmdlet 'i görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="12175-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="12175-109">Bir görev yeniden deneme sayısını tüketdiyse, bu cmdlet yine de çalışır.</span><span class="sxs-lookup"><span data-stu-id="12175-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="12175-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12175-110">EXAMPLES</span></span>

### <span data-ttu-id="12175-111">Örnek 1: görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="12175-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="12175-112">Bu komut, Task2 görev Job7.</span><span class="sxs-lookup"><span data-stu-id="12175-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="12175-113">Örnek 2: ardışık düzeni kullanarak görevi yeniden etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="12175-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="12175-114">Bu komut, Get-AzureBatchTask cmdlet 'ini kullanarak KIMLIĞI Job8 olan Task3 KIMLIĞI olan toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="12175-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="12175-115">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="12175-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="12175-116">Komut bu görevi yeniden etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="12175-116">The command reactivates that task.</span></span>

## <span data-ttu-id="12175-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12175-117">PARAMETERS</span></span>

### <span data-ttu-id="12175-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="12175-118">-BatchContext</span></span>
<span data-ttu-id="12175-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12175-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="12175-120">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12175-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="12175-121">-ID</span><span class="sxs-lookup"><span data-stu-id="12175-121">-Id</span></span>
<span data-ttu-id="12175-122">Yeniden etkinleşen görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12175-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="12175-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="12175-123">-JobId</span></span>
<span data-ttu-id="12175-124">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12175-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="12175-125">-Görev</span><span class="sxs-lookup"><span data-stu-id="12175-125">-Task</span></span>
<span data-ttu-id="12175-126">Bu cmdlet 'in yeniden kullandığı görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="12175-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="12175-127">Bir **Ince görev** nesnesi edinmek için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12175-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="12175-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="12175-128">-Confirm</span></span>
<span data-ttu-id="12175-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12175-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12175-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12175-130">-WhatIf</span></span>
<span data-ttu-id="12175-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12175-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12175-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12175-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12175-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12175-133">-DefaultProfile</span></span>
<span data-ttu-id="12175-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12175-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12175-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12175-135">CommonParameters</span></span>
<span data-ttu-id="12175-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12175-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12175-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12175-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12175-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12175-138">INPUTS</span></span>

### <span data-ttu-id="12175-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="12175-139">BatchAccountContext</span></span>
<span data-ttu-id="12175-140">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="12175-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="12175-141">Ince görev</span><span class="sxs-lookup"><span data-stu-id="12175-141">PSCloudTask</span></span>
<span data-ttu-id="12175-142">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="12175-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="12175-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12175-143">OUTPUTS</span></span>

## <span data-ttu-id="12175-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12175-144">NOTES</span></span>

## <span data-ttu-id="12175-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12175-145">RELATED LINKS</span></span>

[<span data-ttu-id="12175-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="12175-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="12175-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="12175-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="12175-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="12175-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="12175-151">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="12175-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


