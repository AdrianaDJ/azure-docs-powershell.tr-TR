---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 4d15680902cb324561983877fef317d20ed94704
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761838"
---
# <span data-ttu-id="c4e11-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="c4e11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4e11-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e11-103">Toplu iş siler.</span><span class="sxs-lookup"><span data-stu-id="c4e11-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="c4e11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4e11-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4e11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4e11-105">DESCRIPTION</span></span>
<span data-ttu-id="c4e11-106">**Remove-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="c4e11-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="c4e11-107">*Force* parametresini belirtmediğiniz sürece, bu cmdlet bir işi kaldırmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4e11-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="c4e11-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4e11-108">EXAMPLES</span></span>

### <span data-ttu-id="c4e11-109">Örnek 1: toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="c4e11-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="c4e11-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi siler.</span><span class="sxs-lookup"><span data-stu-id="c4e11-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c4e11-111">Komut, işi silmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4e11-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="c4e11-112">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c4e11-112">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c4e11-113">Örnek 2: ardışık düzeni kullanarak onaysız bir toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="c4e11-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="c4e11-114">Bu komut, Get-AzBatchJob cmdlet 'ini kullanarak Iş-000002 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="c4e11-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="c4e11-115">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c4e11-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c4e11-116">Komut bu işi siler.</span><span class="sxs-lookup"><span data-stu-id="c4e11-116">The command deletes that job.</span></span>
<span data-ttu-id="c4e11-117">Komut *Force* parametresini içerdiğinden sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="c4e11-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c4e11-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4e11-118">PARAMETERS</span></span>

### <span data-ttu-id="c4e11-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4e11-119">-BatchContext</span></span>
<span data-ttu-id="c4e11-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4e11-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4e11-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4e11-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c4e11-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="c4e11-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c4e11-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4e11-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c4e11-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c4e11-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c4e11-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e11-125">-DefaultProfile</span></span>
<span data-ttu-id="c4e11-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4e11-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4e11-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c4e11-127">-Force</span></span>
<span data-ttu-id="c4e11-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c4e11-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c4e11-129">-ID</span><span class="sxs-lookup"><span data-stu-id="c4e11-129">-Id</span></span>
<span data-ttu-id="c4e11-130">Bu cmdlet 'in sildiği işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4e11-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="c4e11-131">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4e11-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c4e11-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4e11-132">-Confirm</span></span>
<span data-ttu-id="c4e11-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4e11-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e11-134">-WhatIf</span></span>
<span data-ttu-id="c4e11-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4e11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e11-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4e11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e11-137">CommonParameters</span></span>
<span data-ttu-id="c4e11-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4e11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e11-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e11-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e11-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4e11-140">INPUTS</span></span>

### <span data-ttu-id="c4e11-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e11-141">System.String</span></span>

### <span data-ttu-id="c4e11-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4e11-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c4e11-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4e11-143">OUTPUTS</span></span>

### <span data-ttu-id="c4e11-144">System. void</span><span class="sxs-lookup"><span data-stu-id="c4e11-144">System.Void</span></span>

## <span data-ttu-id="c4e11-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4e11-145">NOTES</span></span>

## <span data-ttu-id="c4e11-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4e11-146">RELATED LINKS</span></span>

[<span data-ttu-id="c4e11-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="c4e11-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="c4e11-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="c4e11-150">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="c4e11-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c4e11-151">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="c4e11-152">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="c4e11-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="c4e11-153">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c4e11-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

