---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: b49ab8a6a08802ec670fb605e707ae46c51ddab2
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938703"
---
# <span data-ttu-id="38460-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="38460-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="38460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38460-102">SYNOPSIS</span></span>
<span data-ttu-id="38460-103">Görevin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38460-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="38460-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38460-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38460-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38460-105">DESCRIPTION</span></span>
<span data-ttu-id="38460-106">**Set-AzBatchTask** cmdlet 'ı, Azure Batch hizmetindeki bir görevin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38460-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="38460-107">Bir **Ince görev** nesnesi almak için Get-AzBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="38460-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="38460-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="38460-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="38460-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38460-109">EXAMPLES</span></span>

### <span data-ttu-id="38460-110">Örnek 1: görevi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="38460-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="38460-111">İlk komut **Get-AzBatchTask** kullanarak bir görevi alır ve $Task değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="38460-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="38460-112">Sonraki iki komut $Task görevin kısıtlamalarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="38460-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="38460-113">Son komutu, toplu Iş hizmetini $Task yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38460-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="38460-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38460-114">PARAMETERS</span></span>

### <span data-ttu-id="38460-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="38460-115">-BatchContext</span></span>
<span data-ttu-id="38460-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="38460-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="38460-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38460-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="38460-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="38460-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="38460-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38460-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="38460-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="38460-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="38460-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38460-121">-DefaultProfile</span></span>
<span data-ttu-id="38460-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38460-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38460-123">-Görev</span><span class="sxs-lookup"><span data-stu-id="38460-123">-Task</span></span>
<span data-ttu-id="38460-124">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pscses görevini** belirtir.</span><span class="sxs-lookup"><span data-stu-id="38460-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38460-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38460-125">CommonParameters</span></span>
<span data-ttu-id="38460-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38460-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38460-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38460-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38460-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38460-128">INPUTS</span></span>

### <span data-ttu-id="38460-129">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="38460-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="38460-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="38460-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="38460-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38460-131">OUTPUTS</span></span>

### <span data-ttu-id="38460-132">System. void</span><span class="sxs-lookup"><span data-stu-id="38460-132">System.Void</span></span>

## <span data-ttu-id="38460-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38460-133">NOTES</span></span>

## <span data-ttu-id="38460-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38460-134">RELATED LINKS</span></span>

[<span data-ttu-id="38460-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="38460-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="38460-136">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="38460-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="38460-137">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="38460-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="38460-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="38460-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="38460-139">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="38460-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="38460-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="38460-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

