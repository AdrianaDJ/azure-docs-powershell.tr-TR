---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593737"
---
# <span data-ttu-id="da9e5-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da9e5-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="da9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="da9e5-103">Toplu Iş görevini siler.</span><span class="sxs-lookup"><span data-stu-id="da9e5-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da9e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da9e5-104">SYNTAX</span></span>

### <span data-ttu-id="da9e5-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="da9e5-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da9e5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="da9e5-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da9e5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="da9e5-107">DESCRIPTION</span></span>
<span data-ttu-id="da9e5-108">**Remove-AzureBatchTask** cmdlet 'ı bir Azure toplu işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="da9e5-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="da9e5-109">*Force* parametresini belirtmediğiniz sürece, bu cmdlet onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da9e5-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="da9e5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da9e5-110">EXAMPLES</span></span>

### <span data-ttu-id="da9e5-111">Örnek 1: KIMLIĞE göre toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="da9e5-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="da9e5-112">Bu komut, kimliği Iş-000001 olan işin altında KIMLIK Task23 olan bir görevi siler.</span><span class="sxs-lookup"><span data-stu-id="da9e5-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="da9e5-113">Komut sizden onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da9e5-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="da9e5-114">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="da9e5-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="da9e5-115">Örnek 2: onay olmadan ardışık düzeni kullanarak toplu görev silme</span><span class="sxs-lookup"><span data-stu-id="da9e5-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="da9e5-116">Bu komut, **Get-AzureBatchTask** cmdlet 'INI kullanarak kimliği iş-000001 olan Task26 kimliğine sahip toplu görevi alır.</span><span class="sxs-lookup"><span data-stu-id="da9e5-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="da9e5-117">Komut, ardışık düzen işlecini kullanarak bu görevi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="da9e5-118">Komut bu görevi siler.</span><span class="sxs-lookup"><span data-stu-id="da9e5-118">The command deletes that task.</span></span>
<span data-ttu-id="da9e5-119">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="da9e5-120">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="da9e5-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="da9e5-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da9e5-121">PARAMETERS</span></span>

### <span data-ttu-id="da9e5-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da9e5-122">-BatchContext</span></span>
<span data-ttu-id="da9e5-123">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da9e5-124">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da9e5-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da9e5-125">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="da9e5-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da9e5-126">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da9e5-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da9e5-127">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da9e5-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="da9e5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9e5-128">-DefaultProfile</span></span>
<span data-ttu-id="da9e5-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da9e5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da9e5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="da9e5-130">-Force</span></span>
<span data-ttu-id="da9e5-131">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="da9e5-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da9e5-132">-ID</span><span class="sxs-lookup"><span data-stu-id="da9e5-132">-Id</span></span>
<span data-ttu-id="da9e5-133">Bu cmdlet 'in sildiği görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="da9e5-134">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="da9e5-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="da9e5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da9e5-135">-InputObject</span></span>
<span data-ttu-id="da9e5-136">Bu cmdlet 'in sildiği görevi belirtir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="da9e5-137">Bir **Ince görev** nesnesi edinmek için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="da9e5-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="da9e5-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="da9e5-138">-JobId</span></span>
<span data-ttu-id="da9e5-139">Görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="da9e5-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="da9e5-140">-Confirm</span></span>
<span data-ttu-id="da9e5-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da9e5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da9e5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da9e5-142">-WhatIf</span></span>
<span data-ttu-id="da9e5-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da9e5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da9e5-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da9e5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da9e5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9e5-145">CommonParameters</span></span>
<span data-ttu-id="da9e5-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da9e5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9e5-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9e5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9e5-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da9e5-148">INPUTS</span></span>

### <span data-ttu-id="da9e5-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da9e5-149">BatchAccountContext</span></span>
<span data-ttu-id="da9e5-150">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="da9e5-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="da9e5-151">Ince görev</span><span class="sxs-lookup"><span data-stu-id="da9e5-151">PSCloudTask</span></span>
<span data-ttu-id="da9e5-152">' InputObject ' parametresi, ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="da9e5-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="da9e5-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da9e5-153">OUTPUTS</span></span>

## <span data-ttu-id="da9e5-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da9e5-154">NOTES</span></span>

## <span data-ttu-id="da9e5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da9e5-155">RELATED LINKS</span></span>

[<span data-ttu-id="da9e5-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="da9e5-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="da9e5-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da9e5-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="da9e5-158">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da9e5-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="da9e5-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da9e5-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="da9e5-160">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da9e5-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="da9e5-161">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="da9e5-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

