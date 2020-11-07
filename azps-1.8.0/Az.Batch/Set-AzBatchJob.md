---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761826"
---
# <span data-ttu-id="fc2ad-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="fc2ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2ad-103">Toplu işlemi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-103">Updates a Batch job.</span></span>

## <span data-ttu-id="fc2ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc2ad-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc2ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="fc2ad-106">**Set-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="fc2ad-107">Bir **Ince iş** nesnesi almak için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="fc2ad-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="fc2ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc2ad-109">EXAMPLES</span></span>

### <span data-ttu-id="fc2ad-110">Örnek 1: iş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fc2ad-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="fc2ad-111">İlk komut **Get-AzBatchJob** kullanarak bir iş alır ve ardından $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="fc2ad-112">İkinci komut $Job nesnesindeki öncelik belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="fc2ad-113">Son komutu, toplu Iş hizmetini $Job yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="fc2ad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc2ad-114">PARAMETERS</span></span>

### <span data-ttu-id="fc2ad-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fc2ad-115">-BatchContext</span></span>
<span data-ttu-id="fc2ad-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fc2ad-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fc2ad-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fc2ad-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fc2ad-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fc2ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2ad-121">-DefaultProfile</span></span>
<span data-ttu-id="fc2ad-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc2ad-123">-Job</span><span class="sxs-lookup"><span data-stu-id="fc2ad-123">-Job</span></span>
<span data-ttu-id="fc2ad-124">Bu cmdlet 'in toplu iş hizmetini güncelleştirdiği bir **Pscses işi** belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc2ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2ad-125">CommonParameters</span></span>
<span data-ttu-id="fc2ad-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc2ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2ad-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc2ad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2ad-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc2ad-128">INPUTS</span></span>

### <span data-ttu-id="fc2ad-129">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="fc2ad-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="fc2ad-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fc2ad-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fc2ad-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc2ad-131">OUTPUTS</span></span>

### <span data-ttu-id="fc2ad-132">System. void</span><span class="sxs-lookup"><span data-stu-id="fc2ad-132">System.Void</span></span>

## <span data-ttu-id="fc2ad-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc2ad-133">NOTES</span></span>

## <span data-ttu-id="fc2ad-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc2ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="fc2ad-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="fc2ad-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="fc2ad-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="fc2ad-138">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="fc2ad-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fc2ad-139">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="fc2ad-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="fc2ad-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="fc2ad-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="fc2ad-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fc2ad-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


