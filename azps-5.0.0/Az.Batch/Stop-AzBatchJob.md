---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323968"
---
# <span data-ttu-id="f5524-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="f5524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5524-102">SYNOPSIS</span></span>
<span data-ttu-id="f5524-103">Toplu işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="f5524-103">Stops a Batch job.</span></span>

## <span data-ttu-id="f5524-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5524-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5524-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5524-105">DESCRIPTION</span></span>
<span data-ttu-id="f5524-106">**Stop-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="f5524-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="f5524-107">Bu komut işi tamamlandı olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="f5524-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="f5524-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5524-108">EXAMPLES</span></span>

### <span data-ttu-id="f5524-109">Örnek 1: toplu işi durdurma</span><span class="sxs-lookup"><span data-stu-id="f5524-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="f5524-110">Bu komut, Iş KIMLIĞI-000001 olan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="f5524-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f5524-111">Komut, işi durdurmayı seçtiğiniz bir nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5524-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="f5524-112">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5524-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f5524-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5524-113">PARAMETERS</span></span>

### <span data-ttu-id="f5524-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f5524-114">-BatchContext</span></span>
<span data-ttu-id="f5524-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5524-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f5524-116">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f5524-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f5524-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f5524-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f5524-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f5524-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f5524-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f5524-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f5524-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5524-120">-DefaultProfile</span></span>
<span data-ttu-id="f5524-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5524-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5524-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f5524-122">-Id</span></span>
<span data-ttu-id="f5524-123">Bu cmdlet 'in durduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5524-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="f5524-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="f5524-124">-TerminateReason</span></span>
<span data-ttu-id="f5524-125">İşi durdurmaya karar verdiğiniz nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5524-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="f5524-126">Bu cmdlet, işin **TerminateReason** özelliği olarak bu metni depolar.</span><span class="sxs-lookup"><span data-stu-id="f5524-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5524-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5524-127">CommonParameters</span></span>
<span data-ttu-id="f5524-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5524-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5524-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f5524-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5524-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5524-130">INPUTS</span></span>

### <span data-ttu-id="f5524-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f5524-131">System.String</span></span>

### <span data-ttu-id="f5524-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f5524-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f5524-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5524-133">OUTPUTS</span></span>

### <span data-ttu-id="f5524-134">System. void</span><span class="sxs-lookup"><span data-stu-id="f5524-134">System.Void</span></span>

## <span data-ttu-id="f5524-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5524-135">NOTES</span></span>

## <span data-ttu-id="f5524-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5524-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5524-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="f5524-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="f5524-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f5524-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f5524-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f5524-141">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="f5524-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f5524-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="f5524-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f5524-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
