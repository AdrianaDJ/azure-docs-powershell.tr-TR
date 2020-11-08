---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: b236f163a6c5c849fcbfcea0a19dac955e15c798
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109163"
---
# <span data-ttu-id="49631-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="49631-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="49631-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49631-102">SYNOPSIS</span></span>
<span data-ttu-id="49631-103">Toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="49631-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="49631-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49631-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49631-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49631-105">DESCRIPTION</span></span>
<span data-ttu-id="49631-106">**Stop-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="49631-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="49631-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49631-107">EXAMPLES</span></span>

### <span data-ttu-id="49631-108">Örnek 1: iş çizelgesini durdurma</span><span class="sxs-lookup"><span data-stu-id="49631-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="49631-109">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="49631-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="49631-110">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="49631-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="49631-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49631-111">PARAMETERS</span></span>

### <span data-ttu-id="49631-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="49631-112">-BatchContext</span></span>
<span data-ttu-id="49631-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="49631-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="49631-114">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49631-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="49631-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="49631-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="49631-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49631-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="49631-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49631-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="49631-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49631-118">-DefaultProfile</span></span>
<span data-ttu-id="49631-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49631-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49631-120">-ID</span><span class="sxs-lookup"><span data-stu-id="49631-120">-Id</span></span>
<span data-ttu-id="49631-121">Bu cmdlet 'in durduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="49631-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="49631-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49631-122">CommonParameters</span></span>
<span data-ttu-id="49631-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49631-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49631-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49631-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49631-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49631-125">INPUTS</span></span>

### <span data-ttu-id="49631-126">System. String</span><span class="sxs-lookup"><span data-stu-id="49631-126">System.String</span></span>

### <span data-ttu-id="49631-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="49631-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="49631-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49631-128">OUTPUTS</span></span>

### <span data-ttu-id="49631-129">System. void</span><span class="sxs-lookup"><span data-stu-id="49631-129">System.Void</span></span>

## <span data-ttu-id="49631-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49631-130">NOTES</span></span>

## <span data-ttu-id="49631-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49631-131">RELATED LINKS</span></span>

[<span data-ttu-id="49631-132">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="49631-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="49631-133">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="49631-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="49631-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="49631-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="49631-135">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="49631-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="49631-136">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="49631-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="49631-137">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="49631-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="49631-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="49631-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
