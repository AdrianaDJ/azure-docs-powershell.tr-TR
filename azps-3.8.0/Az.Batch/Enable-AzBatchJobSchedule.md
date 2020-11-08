---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 0684652dd5e5a0232e5808119ae8453be8f9ade8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107184"
---
# <span data-ttu-id="50795-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="50795-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="50795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50795-102">SYNOPSIS</span></span>
<span data-ttu-id="50795-103">Toplu iş çizelgesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="50795-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="50795-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50795-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50795-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50795-105">DESCRIPTION</span></span>
<span data-ttu-id="50795-106">**Enable-Azbatchjobzamanlama** cmdlet 'ı Azure toplu iş zamanlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="50795-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="50795-107">İş çizelgesini etkinleştirdikten sonra, işler bu zamanlamaya göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="50795-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="50795-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50795-108">EXAMPLES</span></span>

### <span data-ttu-id="50795-109">Örnek 1: iş çizelgesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="50795-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="50795-110">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="50795-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="50795-111">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKey** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="50795-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="50795-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50795-112">PARAMETERS</span></span>

### <span data-ttu-id="50795-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50795-113">-BatchContext</span></span>
<span data-ttu-id="50795-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50795-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50795-115">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50795-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="50795-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="50795-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="50795-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50795-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="50795-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="50795-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="50795-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50795-119">-DefaultProfile</span></span>
<span data-ttu-id="50795-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50795-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50795-121">-ID</span><span class="sxs-lookup"><span data-stu-id="50795-121">-Id</span></span>
<span data-ttu-id="50795-122">Bu cmdlet 'in izin aldığı iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="50795-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="50795-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50795-123">CommonParameters</span></span>
<span data-ttu-id="50795-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50795-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50795-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50795-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50795-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50795-126">INPUTS</span></span>

### <span data-ttu-id="50795-127">System. String</span><span class="sxs-lookup"><span data-stu-id="50795-127">System.String</span></span>

### <span data-ttu-id="50795-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50795-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="50795-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50795-129">OUTPUTS</span></span>

### <span data-ttu-id="50795-130">System. void</span><span class="sxs-lookup"><span data-stu-id="50795-130">System.Void</span></span>

## <span data-ttu-id="50795-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50795-131">NOTES</span></span>

## <span data-ttu-id="50795-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50795-132">RELATED LINKS</span></span>

[<span data-ttu-id="50795-133">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="50795-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="50795-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="50795-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="50795-135">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="50795-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="50795-136">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="50795-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="50795-137">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="50795-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="50795-138">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="50795-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="50795-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="50795-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


