---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593167"
---
# <span data-ttu-id="3a4af-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="3a4af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a4af-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4af-103">Toplu iş siler.</span><span class="sxs-lookup"><span data-stu-id="3a4af-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a4af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a4af-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a4af-105">DESCRIPTION</span></span>
<span data-ttu-id="3a4af-106">**Remove-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="3a4af-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="3a4af-107">*Force* parametresini belirtmediğiniz sürece, bu cmdlet bir işi kaldırmadan önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a4af-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="3a4af-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a4af-108">EXAMPLES</span></span>

### <span data-ttu-id="3a4af-109">Örnek 1: toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="3a4af-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="3a4af-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi siler.</span><span class="sxs-lookup"><span data-stu-id="3a4af-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3a4af-111">Komut, işi silmeden önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a4af-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="3a4af-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a4af-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3a4af-113">Örnek 2: ardışık düzeni kullanarak onaysız bir toplu iş silme</span><span class="sxs-lookup"><span data-stu-id="3a4af-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="3a4af-114">Bu komut, Get-AzureBatchJob cmdlet 'ini kullanarak Iş-000002 KIMLIĞINE sahip işi alır.</span><span class="sxs-lookup"><span data-stu-id="3a4af-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="3a4af-115">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="3a4af-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3a4af-116">Komut bu işi siler.</span><span class="sxs-lookup"><span data-stu-id="3a4af-116">The command deletes that job.</span></span>
<span data-ttu-id="3a4af-117">Komut *Force* parametresini içerdiğinden sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="3a4af-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3a4af-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a4af-118">PARAMETERS</span></span>

### <span data-ttu-id="3a4af-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3a4af-119">-BatchContext</span></span>
<span data-ttu-id="3a4af-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a4af-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3a4af-121">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a4af-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3a4af-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3a4af-122">-Force</span></span>
<span data-ttu-id="3a4af-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3a4af-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a4af-124">-ID</span><span class="sxs-lookup"><span data-stu-id="3a4af-124">-Id</span></span>
<span data-ttu-id="3a4af-125">Bu cmdlet 'in sildiği işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a4af-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="3a4af-126">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a4af-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="3a4af-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a4af-127">-Confirm</span></span>
<span data-ttu-id="3a4af-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a4af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4af-129">-WhatIf</span></span>
<span data-ttu-id="3a4af-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a4af-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4af-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a4af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4af-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4af-132">-DefaultProfile</span></span>
<span data-ttu-id="3a4af-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a4af-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a4af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4af-134">CommonParameters</span></span>
<span data-ttu-id="3a4af-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a4af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4af-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4af-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4af-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a4af-137">INPUTS</span></span>

### <span data-ttu-id="3a4af-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3a4af-138">BatchAccountContext</span></span>
<span data-ttu-id="3a4af-139">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3a4af-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3a4af-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a4af-140">OUTPUTS</span></span>

## <span data-ttu-id="3a4af-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a4af-141">NOTES</span></span>

## <span data-ttu-id="3a4af-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a4af-142">RELATED LINKS</span></span>

[<span data-ttu-id="3a4af-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="3a4af-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="3a4af-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="3a4af-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3a4af-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3a4af-147">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="3a4af-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="3a4af-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="3a4af-149">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="3a4af-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


