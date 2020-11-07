---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: 141702ec7c60dcdb2dd94d5e259b2f14c8475316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762806"
---
# <span data-ttu-id="e8fbd-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="e8fbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fbd-103">Toplu işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8fbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8fbd-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8fbd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e8fbd-106">**Disable-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="e8fbd-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="e8fbd-108">Devre dışı bırakılan işler yeni görevleri çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="e8fbd-109">Devre dışı bir işi daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="e8fbd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8fbd-110">EXAMPLES</span></span>

### <span data-ttu-id="e8fbd-111">Örnek 1: toplu işi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e8fbd-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="e8fbd-112">Bu komut, Iş KIMLIĞI-000001 olan işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e8fbd-113">Komut, iş için etkin görevleri sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="e8fbd-114">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e8fbd-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8fbd-115">PARAMETERS</span></span>

### <span data-ttu-id="e8fbd-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e8fbd-116">-BatchContext</span></span>
<span data-ttu-id="e8fbd-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e8fbd-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e8fbd-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e8fbd-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e8fbd-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e8fbd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fbd-122">-DefaultProfile</span></span>
<span data-ttu-id="e8fbd-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8fbd-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="e8fbd-124">-DisableJobOption</span></span>
<span data-ttu-id="e8fbd-125">Bu cmdlet 'in devre dışı olduğu iş ile ilişkili etkin görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="e8fbd-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e8fbd-126">Valid values are:</span></span> 
- <span data-ttu-id="e8fbd-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="e8fbd-127">Requeue</span></span> 
- <span data-ttu-id="e8fbd-128">Ermesini</span><span class="sxs-lookup"><span data-stu-id="e8fbd-128">Terminate</span></span> 
- <span data-ttu-id="e8fbd-129">Yönergesi</span><span class="sxs-lookup"><span data-stu-id="e8fbd-129">Wait</span></span>

```yaml
Type: Microsoft.Azure.Batch.Common.DisableJobOption
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fbd-130">-ID</span><span class="sxs-lookup"><span data-stu-id="e8fbd-130">-Id</span></span>
<span data-ttu-id="e8fbd-131">Bu cmdlet 'in devre dışı bırakacağını belirten KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fbd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fbd-132">CommonParameters</span></span>
<span data-ttu-id="e8fbd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8fbd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fbd-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8fbd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fbd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8fbd-135">INPUTS</span></span>

### <span data-ttu-id="e8fbd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e8fbd-136">System.String</span></span>

### <span data-ttu-id="e8fbd-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e8fbd-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e8fbd-138">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8fbd-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e8fbd-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8fbd-139">OUTPUTS</span></span>

### <span data-ttu-id="e8fbd-140">System. void</span><span class="sxs-lookup"><span data-stu-id="e8fbd-140">System.Void</span></span>

## <span data-ttu-id="e8fbd-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8fbd-141">NOTES</span></span>

## <span data-ttu-id="e8fbd-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8fbd-142">RELATED LINKS</span></span>

[<span data-ttu-id="e8fbd-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="e8fbd-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e8fbd-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e8fbd-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="e8fbd-146">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="e8fbd-147">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="e8fbd-148">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="e8fbd-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="e8fbd-149">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e8fbd-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


