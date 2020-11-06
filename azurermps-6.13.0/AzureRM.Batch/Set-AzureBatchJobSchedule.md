---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572926"
---
# <span data-ttu-id="ba95b-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="ba95b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba95b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba95b-103">İş zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ba95b-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba95b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba95b-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba95b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba95b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba95b-106">**Set-AzureBatchJobSchedule** cmdlet 'ı Azure Batch hizmetinde iş çizelgesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ba95b-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="ba95b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba95b-107">EXAMPLES</span></span>

## <span data-ttu-id="ba95b-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba95b-108">PARAMETERS</span></span>

### <span data-ttu-id="ba95b-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba95b-109">-BatchContext</span></span>
<span data-ttu-id="ba95b-110">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba95b-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba95b-111">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba95b-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba95b-112">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="ba95b-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba95b-113">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba95b-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba95b-114">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ba95b-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba95b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba95b-115">-DefaultProfile</span></span>
<span data-ttu-id="ba95b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba95b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba95b-117">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="ba95b-117">-JobSchedule</span></span>
<span data-ttu-id="ba95b-118">İş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba95b-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="ba95b-119">**Pschoparlör** nesnesi almak için Get-AzureBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba95b-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="ba95b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba95b-120">CommonParameters</span></span>
<span data-ttu-id="ba95b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba95b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba95b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba95b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba95b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba95b-123">INPUTS</span></span>

### <span data-ttu-id="ba95b-124">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="ba95b-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="ba95b-125">Parametreler: Jobzamanlama (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba95b-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="ba95b-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba95b-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ba95b-127">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba95b-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ba95b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba95b-128">OUTPUTS</span></span>

### <span data-ttu-id="ba95b-129">System. void</span><span class="sxs-lookup"><span data-stu-id="ba95b-129">System.Void</span></span>

## <span data-ttu-id="ba95b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba95b-130">NOTES</span></span>

## <span data-ttu-id="ba95b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba95b-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba95b-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="ba95b-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="ba95b-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="ba95b-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="ba95b-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="ba95b-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba95b-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


