---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: fa7dede61cd19ec0ea0a4ccd59f2eca3e0cc8f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762804"
---
# <span data-ttu-id="e6a14-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="e6a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a14-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a14-103">Toplu iş siler.</span><span class="sxs-lookup"><span data-stu-id="e6a14-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6a14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6a14-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6a14-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a14-106">**Remove-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="e6a14-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="e6a14-107">*Force* parametresini belirtmediğiniz sürece, bu cmdlet bir işi kaldırmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6a14-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="e6a14-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6a14-108">EXAMPLES</span></span>

### <span data-ttu-id="e6a14-109">Örnek 1: toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="e6a14-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="e6a14-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi siler.</span><span class="sxs-lookup"><span data-stu-id="e6a14-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e6a14-111">Komut, işi silmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6a14-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="e6a14-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6a14-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e6a14-113">Örnek 2: ardışık düzeni kullanarak onaysız bir toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="e6a14-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="e6a14-114">Bu komut, Get-AzureBatchJob cmdlet 'ini kullanarak Iş-000002 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="e6a14-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="e6a14-115">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="e6a14-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e6a14-116">Komut bu işi siler.</span><span class="sxs-lookup"><span data-stu-id="e6a14-116">The command deletes that job.</span></span>
<span data-ttu-id="e6a14-117">Komut *Force* parametresini içerdiğinden sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e6a14-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e6a14-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6a14-118">PARAMETERS</span></span>

### <span data-ttu-id="e6a14-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e6a14-119">-BatchContext</span></span>
<span data-ttu-id="e6a14-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6a14-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e6a14-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e6a14-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e6a14-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e6a14-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e6a14-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e6a14-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e6a14-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6a14-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e6a14-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a14-125">-DefaultProfile</span></span>
<span data-ttu-id="e6a14-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6a14-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a14-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e6a14-127">-Force</span></span>
<span data-ttu-id="e6a14-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e6a14-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6a14-129">-ID</span><span class="sxs-lookup"><span data-stu-id="e6a14-129">-Id</span></span>
<span data-ttu-id="e6a14-130">Bu cmdlet 'in sildiği işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6a14-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="e6a14-131">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6a14-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a14-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6a14-132">-Confirm</span></span>
<span data-ttu-id="e6a14-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6a14-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a14-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a14-134">-WhatIf</span></span>
<span data-ttu-id="e6a14-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6a14-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a14-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6a14-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a14-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a14-137">CommonParameters</span></span>
<span data-ttu-id="e6a14-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6a14-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a14-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a14-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a14-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6a14-140">INPUTS</span></span>

### <span data-ttu-id="e6a14-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a14-141">System.String</span></span>

### <span data-ttu-id="e6a14-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e6a14-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e6a14-143">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6a14-143">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e6a14-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6a14-144">OUTPUTS</span></span>

### <span data-ttu-id="e6a14-145">System. void</span><span class="sxs-lookup"><span data-stu-id="e6a14-145">System.Void</span></span>

## <span data-ttu-id="e6a14-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6a14-146">NOTES</span></span>

## <span data-ttu-id="e6a14-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6a14-147">RELATED LINKS</span></span>

[<span data-ttu-id="e6a14-148">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-148">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="e6a14-149">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-149">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="e6a14-150">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-150">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e6a14-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6a14-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e6a14-152">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-152">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="e6a14-153">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e6a14-153">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="e6a14-154">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e6a14-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


