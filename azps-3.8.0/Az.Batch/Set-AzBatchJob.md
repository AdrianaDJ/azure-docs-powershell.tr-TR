---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: e15dbe0f17f66f6bb8aaad0c4cfb1883ecfb2034
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107246"
---
# <span data-ttu-id="b1b17-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="b1b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b17-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b17-103">Toplu işlemi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-103">Updates a Batch job.</span></span>

## <span data-ttu-id="b1b17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1b17-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b17-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1b17-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b17-106">**Set-AzBatchJob** cmdlet 'ı bir Azure toplu işlemini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="b1b17-107">Bir **Ince iş** nesnesi almak için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1b17-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="b1b17-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1b17-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="b1b17-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1b17-109">EXAMPLES</span></span>

### <span data-ttu-id="b1b17-110">Örnek 1: iş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b1b17-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="b1b17-111">İlk komut **Get-AzBatchJob** kullanarak bir iş alır ve ardından $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b1b17-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="b1b17-112">İkinci komut $Job nesnesindeki öncelik belirtimini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="b1b17-113">Son komutu, toplu Iş hizmetini $Job yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="b1b17-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1b17-114">PARAMETERS</span></span>

### <span data-ttu-id="b1b17-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b1b17-115">-BatchContext</span></span>
<span data-ttu-id="b1b17-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b1b17-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b1b17-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b1b17-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b1b17-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b1b17-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b1b17-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b1b17-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b1b17-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b1b17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b17-121">-DefaultProfile</span></span>
<span data-ttu-id="b1b17-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1b17-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b17-123">-Job</span><span class="sxs-lookup"><span data-stu-id="b1b17-123">-Job</span></span>
<span data-ttu-id="b1b17-124">Bu cmdlet 'in toplu iş hizmetini güncelleştirdiği bir **Pscses işi** belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b17-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="b1b17-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b17-125">CommonParameters</span></span>
<span data-ttu-id="b1b17-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1b17-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b17-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b1b17-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b17-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1b17-128">INPUTS</span></span>

### <span data-ttu-id="b1b17-129">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="b1b17-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="b1b17-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b1b17-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b1b17-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1b17-131">OUTPUTS</span></span>

### <span data-ttu-id="b1b17-132">System. void</span><span class="sxs-lookup"><span data-stu-id="b1b17-132">System.Void</span></span>

## <span data-ttu-id="b1b17-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1b17-133">NOTES</span></span>

## <span data-ttu-id="b1b17-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1b17-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1b17-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="b1b17-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="b1b17-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="b1b17-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b1b17-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b1b17-139">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="b1b17-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="b1b17-141">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="b1b17-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="b1b17-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b1b17-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


