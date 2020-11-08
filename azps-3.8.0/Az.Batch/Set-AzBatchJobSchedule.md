---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: d6a17588b5718f9a6d735521a7a136cba472ead0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097903"
---
# <span data-ttu-id="81a78-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="81a78-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="81a78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a78-102">SYNOPSIS</span></span>
<span data-ttu-id="81a78-103">İş zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81a78-103">Sets a job schedule.</span></span>

## <span data-ttu-id="81a78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81a78-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81a78-105">DESCRIPTION</span></span>
<span data-ttu-id="81a78-106">**Set-Azbatchjobzamanlama** cmdlet 'ı Azure toplu iş hizmetinde iş zamanlamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81a78-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="81a78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81a78-107">EXAMPLES</span></span>

### <span data-ttu-id="81a78-108">Örnek 1: iş çizelgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="81a78-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="81a78-109">İlk komut **Get-Azbatchjobzamanlama** kullanarak bir iş alır ve ardından $JobSchedule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="81a78-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="81a78-110">İkinci komut, nesnedeki yinelenme aralığını değiştirir `$JobSchedule.Schedule` .</span><span class="sxs-lookup"><span data-stu-id="81a78-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="81a78-111">Son komutu, toplu Iş hizmetini $JobSchedule yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="81a78-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="81a78-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81a78-112">PARAMETERS</span></span>

### <span data-ttu-id="81a78-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="81a78-113">-BatchContext</span></span>
<span data-ttu-id="81a78-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81a78-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81a78-115">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81a78-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81a78-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="81a78-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81a78-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81a78-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81a78-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="81a78-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81a78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a78-119">-DefaultProfile</span></span>
<span data-ttu-id="81a78-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81a78-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a78-121">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="81a78-121">-JobSchedule</span></span>
<span data-ttu-id="81a78-122">İş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81a78-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="81a78-123">**Pschoparlör** nesnesi almak için Get-AzBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81a78-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81a78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a78-124">CommonParameters</span></span>
<span data-ttu-id="81a78-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81a78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a78-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="81a78-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a78-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81a78-127">INPUTS</span></span>

### <span data-ttu-id="81a78-128">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="81a78-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="81a78-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="81a78-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="81a78-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81a78-130">OUTPUTS</span></span>

### <span data-ttu-id="81a78-131">System. void</span><span class="sxs-lookup"><span data-stu-id="81a78-131">System.Void</span></span>

## <span data-ttu-id="81a78-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81a78-132">NOTES</span></span>

## <span data-ttu-id="81a78-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81a78-133">RELATED LINKS</span></span>

[<span data-ttu-id="81a78-134">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="81a78-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="81a78-135">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="81a78-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="81a78-136">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="81a78-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="81a78-137">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="81a78-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="81a78-138">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="81a78-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="81a78-139">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="81a78-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


