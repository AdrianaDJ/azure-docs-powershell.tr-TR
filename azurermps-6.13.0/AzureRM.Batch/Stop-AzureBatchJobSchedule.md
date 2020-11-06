---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 33ae727ea31d533652943240cd9cd25014635533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592336"
---
# <span data-ttu-id="132e7-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="132e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="132e7-102">SYNOPSIS</span></span>
<span data-ttu-id="132e7-103">Toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="132e7-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="132e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="132e7-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="132e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="132e7-105">DESCRIPTION</span></span>
<span data-ttu-id="132e7-106">**Stop-AzureBatchJobSchedule** cmdlet 'ı bir Azure toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="132e7-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="132e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="132e7-107">EXAMPLES</span></span>

### <span data-ttu-id="132e7-108">Örnek 1: iş çizelgesini durdurma</span><span class="sxs-lookup"><span data-stu-id="132e7-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="132e7-109">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="132e7-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="132e7-110">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="132e7-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="132e7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="132e7-111">PARAMETERS</span></span>

### <span data-ttu-id="132e7-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="132e7-112">-BatchContext</span></span>
<span data-ttu-id="132e7-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="132e7-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="132e7-114">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="132e7-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="132e7-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="132e7-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="132e7-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="132e7-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="132e7-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="132e7-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="132e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132e7-118">-DefaultProfile</span></span>
<span data-ttu-id="132e7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="132e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="132e7-120">-ID</span><span class="sxs-lookup"><span data-stu-id="132e7-120">-Id</span></span>
<span data-ttu-id="132e7-121">Bu cmdlet 'in durduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="132e7-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="132e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132e7-122">CommonParameters</span></span>
<span data-ttu-id="132e7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="132e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132e7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132e7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132e7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="132e7-125">INPUTS</span></span>

### <span data-ttu-id="132e7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="132e7-126">System.String</span></span>

### <span data-ttu-id="132e7-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="132e7-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="132e7-128">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="132e7-128">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="132e7-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="132e7-129">OUTPUTS</span></span>

### <span data-ttu-id="132e7-130">System. void</span><span class="sxs-lookup"><span data-stu-id="132e7-130">System.Void</span></span>

## <span data-ttu-id="132e7-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="132e7-131">NOTES</span></span>

## <span data-ttu-id="132e7-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="132e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="132e7-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="132e7-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="132e7-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="132e7-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="132e7-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="132e7-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="132e7-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="132e7-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="132e7-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="132e7-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


