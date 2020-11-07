---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJob.md
ms.openlocfilehash: c560964308fe3bb2195f601f2e4138e022aa41e0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938663"
---
# <span data-ttu-id="1fe3b-101">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-101">Disable-AzBatchJob</span></span>

## <span data-ttu-id="1fe3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe3b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe3b-103">Toplu işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-103">Disables a Batch job.</span></span>

## <span data-ttu-id="1fe3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fe3b-104">SYNTAX</span></span>

```
Disable-AzBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fe3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fe3b-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe3b-106">**Disable-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-106">The **Disable-AzBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="1fe3b-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="1fe3b-108">Devre dışı bırakılan işler yeni görevleri çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="1fe3b-109">Devre dışı bir işi daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="1fe3b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fe3b-110">EXAMPLES</span></span>

### <span data-ttu-id="1fe3b-111">Örnek 1: toplu işi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="1fe3b-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="1fe3b-112">Bu komut, Iş KIMLIĞI-000001 olan işi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="1fe3b-113">Komut, iş için etkin görevleri sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="1fe3b-114">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1fe3b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fe3b-115">PARAMETERS</span></span>

### <span data-ttu-id="1fe3b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1fe3b-116">-BatchContext</span></span>
<span data-ttu-id="1fe3b-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1fe3b-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1fe3b-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1fe3b-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1fe3b-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1fe3b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe3b-122">-DefaultProfile</span></span>
<span data-ttu-id="1fe3b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe3b-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="1fe3b-124">-DisableJobOption</span></span>
<span data-ttu-id="1fe3b-125">Bu cmdlet 'in devre dışı olduğu iş ile ilişkili etkin görevlerle ne yapılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="1fe3b-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1fe3b-126">Valid values are:</span></span> 
- <span data-ttu-id="1fe3b-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="1fe3b-127">Requeue</span></span> 
- <span data-ttu-id="1fe3b-128">Ermesini</span><span class="sxs-lookup"><span data-stu-id="1fe3b-128">Terminate</span></span> 
- <span data-ttu-id="1fe3b-129">Yönergesi</span><span class="sxs-lookup"><span data-stu-id="1fe3b-129">Wait</span></span>

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

### <span data-ttu-id="1fe3b-130">-ID</span><span class="sxs-lookup"><span data-stu-id="1fe3b-130">-Id</span></span>
<span data-ttu-id="1fe3b-131">Bu cmdlet 'in devre dışı bırakacağını belirten KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-131">Specifies the ID of the job that this cmdlet disables.</span></span>

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

### <span data-ttu-id="1fe3b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe3b-132">CommonParameters</span></span>
<span data-ttu-id="1fe3b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fe3b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe3b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe3b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe3b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fe3b-135">INPUTS</span></span>

### <span data-ttu-id="1fe3b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1fe3b-136">System.String</span></span>

### <span data-ttu-id="1fe3b-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1fe3b-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1fe3b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fe3b-138">OUTPUTS</span></span>

### <span data-ttu-id="1fe3b-139">System. void</span><span class="sxs-lookup"><span data-stu-id="1fe3b-139">System.Void</span></span>

## <span data-ttu-id="1fe3b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fe3b-140">NOTES</span></span>

## <span data-ttu-id="1fe3b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fe3b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1fe3b-142">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-142">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="1fe3b-143">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="1fe3b-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1fe3b-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1fe3b-145">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-145">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="1fe3b-146">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-146">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="1fe3b-147">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1fe3b-147">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="1fe3b-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1fe3b-148">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


