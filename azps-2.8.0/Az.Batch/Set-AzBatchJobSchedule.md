---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753161"
---
# <span data-ttu-id="6b47a-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6b47a-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="6b47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b47a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b47a-103">İş zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b47a-103">Sets a job schedule.</span></span>

## <span data-ttu-id="6b47a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b47a-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b47a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b47a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b47a-106">**Set-Azbatchjobzamanlama** cmdlet 'ı Azure toplu iş hizmetinde iş zamanlamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6b47a-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="6b47a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b47a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b47a-108">Örnek 1: iş çizelgesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6b47a-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="6b47a-109">İlk komut **Get-Azbatchjobzamanlama** kullanarak bir iş alır ve ardından $JobSchedule değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6b47a-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="6b47a-110">İkinci komut, nesnedeki yinelenme aralığını değiştirir `$JobSchedule.Schedule` .</span><span class="sxs-lookup"><span data-stu-id="6b47a-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="6b47a-111">Son komutu, toplu Iş hizmetini $JobSchedule yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b47a-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="6b47a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b47a-112">PARAMETERS</span></span>

### <span data-ttu-id="6b47a-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b47a-113">-BatchContext</span></span>
<span data-ttu-id="6b47a-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b47a-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b47a-115">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b47a-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6b47a-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="6b47a-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6b47a-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b47a-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6b47a-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b47a-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6b47a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b47a-119">-DefaultProfile</span></span>
<span data-ttu-id="6b47a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b47a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b47a-121">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="6b47a-121">-JobSchedule</span></span>
<span data-ttu-id="6b47a-122">İş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b47a-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="6b47a-123">**Pschoparlör** nesnesi almak için Get-AzBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6b47a-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="6b47a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b47a-124">CommonParameters</span></span>
<span data-ttu-id="6b47a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b47a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b47a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b47a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b47a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b47a-127">INPUTS</span></span>

### <span data-ttu-id="6b47a-128">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="6b47a-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="6b47a-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b47a-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6b47a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b47a-130">OUTPUTS</span></span>

### <span data-ttu-id="6b47a-131">System. void</span><span class="sxs-lookup"><span data-stu-id="6b47a-131">System.Void</span></span>

## <span data-ttu-id="6b47a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b47a-132">NOTES</span></span>

## <span data-ttu-id="6b47a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b47a-133">RELATED LINKS</span></span>

[<span data-ttu-id="6b47a-134">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="6b47a-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="6b47a-135">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="6b47a-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="6b47a-136">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="6b47a-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="6b47a-137">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="6b47a-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="6b47a-138">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="6b47a-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="6b47a-139">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="6b47a-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


