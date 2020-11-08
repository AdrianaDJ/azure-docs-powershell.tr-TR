---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: a25c31c0b73a42e0d64b567b6bc2529bf4ebf258
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273710"
---
# <span data-ttu-id="971ff-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="971ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="971ff-102">SYNOPSIS</span></span>
<span data-ttu-id="971ff-103">Toplu işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="971ff-103">Disables a Batch job.</span></span>

## <span data-ttu-id="971ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="971ff-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="971ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="971ff-105">DESCRIPTION</span></span>
<span data-ttu-id="971ff-106">**Disable-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="971ff-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="971ff-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="971ff-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="971ff-108">Devre dışı bırakılan işler yeni görevleri çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="971ff-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="971ff-109">Devre dışı bir işi daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="971ff-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="971ff-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="971ff-110">EXAMPLES</span></span>

### <span data-ttu-id="971ff-111">Örnek 1: toplu işi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="971ff-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="971ff-112">Bu komut, Iş KIMLIĞI-000001 olan işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="971ff-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="971ff-113">Komut, iş için etkin görevleri sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="971ff-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="971ff-114">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKey** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="971ff-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="971ff-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="971ff-115">PARAMETERS</span></span>

### <span data-ttu-id="971ff-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="971ff-116">-BatchContext</span></span>
<span data-ttu-id="971ff-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="971ff-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="971ff-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="971ff-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="971ff-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="971ff-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="971ff-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="971ff-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="971ff-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="971ff-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="971ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971ff-122">-DefaultProfile</span></span>
<span data-ttu-id="971ff-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="971ff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971ff-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="971ff-124">-DisableJobOption</span></span>
<span data-ttu-id="971ff-125">Bu cmdlet 'in devre dışı olduğu iş ile ilişkili etkin görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="971ff-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="971ff-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="971ff-126">Valid values are:</span></span>
- <span data-ttu-id="971ff-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="971ff-127">Requeue</span></span>
- <span data-ttu-id="971ff-128">Ermesini</span><span class="sxs-lookup"><span data-stu-id="971ff-128">Terminate</span></span>
- <span data-ttu-id="971ff-129">Yönergesi</span><span class="sxs-lookup"><span data-stu-id="971ff-129">Wait</span></span>

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

### <span data-ttu-id="971ff-130">-ID</span><span class="sxs-lookup"><span data-stu-id="971ff-130">-Id</span></span>
<span data-ttu-id="971ff-131">Bu cmdlet 'in devre dışı bırakacağını belirten KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="971ff-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="971ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971ff-132">CommonParameters</span></span>
<span data-ttu-id="971ff-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="971ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971ff-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="971ff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971ff-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="971ff-135">INPUTS</span></span>

### <span data-ttu-id="971ff-136">System. String</span><span class="sxs-lookup"><span data-stu-id="971ff-136">System.String</span></span>

### <span data-ttu-id="971ff-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="971ff-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="971ff-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="971ff-138">OUTPUTS</span></span>

### <span data-ttu-id="971ff-139">System. void</span><span class="sxs-lookup"><span data-stu-id="971ff-139">System.Void</span></span>

## <span data-ttu-id="971ff-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="971ff-140">NOTES</span></span>

## <span data-ttu-id="971ff-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="971ff-141">RELATED LINKS</span></span>

[<span data-ttu-id="971ff-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="971ff-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="971ff-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="971ff-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="971ff-145">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="971ff-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="971ff-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="971ff-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="971ff-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="971ff-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
