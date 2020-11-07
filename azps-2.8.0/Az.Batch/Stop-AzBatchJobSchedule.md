---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938635"
---
# <span data-ttu-id="d20c0-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d20c0-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="d20c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d20c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d20c0-103">Toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d20c0-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="d20c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d20c0-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d20c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d20c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d20c0-106">**Stop-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="d20c0-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="d20c0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d20c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d20c0-108">Örnek 1: iş çizelgesini durdurma</span><span class="sxs-lookup"><span data-stu-id="d20c0-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d20c0-109">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="d20c0-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d20c0-110">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d20c0-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d20c0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d20c0-111">PARAMETERS</span></span>

### <span data-ttu-id="d20c0-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d20c0-112">-BatchContext</span></span>
<span data-ttu-id="d20c0-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d20c0-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d20c0-114">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d20c0-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d20c0-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="d20c0-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d20c0-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d20c0-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d20c0-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d20c0-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d20c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20c0-118">-DefaultProfile</span></span>
<span data-ttu-id="d20c0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d20c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d20c0-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d20c0-120">-Id</span></span>
<span data-ttu-id="d20c0-121">Bu cmdlet 'in durduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d20c0-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d20c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20c0-122">CommonParameters</span></span>
<span data-ttu-id="d20c0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d20c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20c0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20c0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20c0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d20c0-125">INPUTS</span></span>

### <span data-ttu-id="d20c0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d20c0-126">System.String</span></span>

### <span data-ttu-id="d20c0-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d20c0-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d20c0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d20c0-128">OUTPUTS</span></span>

### <span data-ttu-id="d20c0-129">System. void</span><span class="sxs-lookup"><span data-stu-id="d20c0-129">System.Void</span></span>

## <span data-ttu-id="d20c0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d20c0-130">NOTES</span></span>

## <span data-ttu-id="d20c0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d20c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="d20c0-132">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="d20c0-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="d20c0-133">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="d20c0-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="d20c0-134">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="d20c0-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d20c0-135">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="d20c0-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d20c0-136">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="d20c0-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="d20c0-137">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="d20c0-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="d20c0-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d20c0-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


