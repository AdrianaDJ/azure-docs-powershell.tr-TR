---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: bae5f2b075f8d4f2fa579b38bdccf160cd46caad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762122"
---
# <span data-ttu-id="a7aa7-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7aa7-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="a7aa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="a7aa7-103">Görevin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7aa7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7aa7-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7aa7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="a7aa7-106">**Set-AzureBatchTask** cmdlet 'ı, Azure Batch hizmetindeki bir görevin özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="a7aa7-107">Bir **Ince görev** nesnesi almak için Get-AzureBatchTask cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="a7aa7-108">Bu nesnenin özelliklerini değiştirin ve değişikliklerinizi toplu Iş hizmetine uygulamak için geçerli cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a7aa7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7aa7-109">EXAMPLES</span></span>

### <span data-ttu-id="a7aa7-110">Örnek 1: görevi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a7aa7-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="a7aa7-111">İlk komut **Get-AzureBatchTask** kullanarak bir görevi alır ve $Task değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="a7aa7-112">Sonraki iki komut $Task görevin kısıtlamalarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="a7aa7-113">Son komutu, toplu Iş hizmetini $Task yerel nesneyle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="a7aa7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7aa7-114">PARAMETERS</span></span>

### <span data-ttu-id="a7aa7-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7aa7-115">-BatchContext</span></span>
<span data-ttu-id="a7aa7-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a7aa7-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a7aa7-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a7aa7-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a7aa7-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7aa7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7aa7-121">-DefaultProfile</span></span>
<span data-ttu-id="a7aa7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7aa7-123">-Görev</span><span class="sxs-lookup"><span data-stu-id="a7aa7-123">-Task</span></span>
<span data-ttu-id="a7aa7-124">Bu cmdlet 'in toplu Iş hizmetini güncelleştirdiği **Pscses görevini** belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="a7aa7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7aa7-125">CommonParameters</span></span>
<span data-ttu-id="a7aa7-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7aa7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7aa7-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7aa7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7aa7-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7aa7-128">INPUTS</span></span>

### <span data-ttu-id="a7aa7-129">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="a7aa7-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="a7aa7-130">Parametreler: görev (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7aa7-130">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="a7aa7-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7aa7-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a7aa7-132">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7aa7-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a7aa7-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7aa7-133">OUTPUTS</span></span>

### <span data-ttu-id="a7aa7-134">System. void</span><span class="sxs-lookup"><span data-stu-id="a7aa7-134">System.Void</span></span>

## <span data-ttu-id="a7aa7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7aa7-135">NOTES</span></span>

## <span data-ttu-id="a7aa7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7aa7-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7aa7-137">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7aa7-137">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="a7aa7-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a7aa7-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a7aa7-139">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7aa7-139">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a7aa7-140">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7aa7-140">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a7aa7-141">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a7aa7-141">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="a7aa7-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a7aa7-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


