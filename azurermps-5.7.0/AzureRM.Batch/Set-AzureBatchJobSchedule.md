---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 85e47b9f9bea7a19bb11817c414e5d3b9a35d6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592938"
---
# <span data-ttu-id="14c58-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="14c58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c58-102">SYNOPSIS</span></span>
<span data-ttu-id="14c58-103">İş zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="14c58-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14c58-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14c58-105">DESCRIPTION</span></span>
<span data-ttu-id="14c58-106">**Set-AzureBatchJobSchedule** cmdlet 'ı Azure Batch hizmetinde iş çizelgesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="14c58-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="14c58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14c58-107">EXAMPLES</span></span>

## <span data-ttu-id="14c58-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14c58-108">PARAMETERS</span></span>

### <span data-ttu-id="14c58-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14c58-109">-BatchContext</span></span>
<span data-ttu-id="14c58-110">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14c58-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14c58-111">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="14c58-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14c58-112">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="14c58-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14c58-113">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="14c58-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14c58-114">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="14c58-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c58-115">-DefaultProfile</span></span>
<span data-ttu-id="14c58-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14c58-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c58-117">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="14c58-117">-JobSchedule</span></span>
<span data-ttu-id="14c58-118">İş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14c58-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="14c58-119">**Pschoparlör** nesnesi almak için Get-AzureBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="14c58-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: PSCloudJobSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c58-120">CommonParameters</span></span>
<span data-ttu-id="14c58-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14c58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c58-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c58-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c58-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14c58-123">INPUTS</span></span>

### <span data-ttu-id="14c58-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14c58-124">BatchAccountContext</span></span>
<span data-ttu-id="14c58-125">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="14c58-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="14c58-126">Ek zamanlama</span><span class="sxs-lookup"><span data-stu-id="14c58-126">PSCloudJobSchedule</span></span>
<span data-ttu-id="14c58-127">' Jobzamanlama ' parametresi ardışık düzenin ' Pscses Jobzamanlama ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="14c58-127">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="14c58-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14c58-128">OUTPUTS</span></span>

## <span data-ttu-id="14c58-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14c58-129">NOTES</span></span>

## <span data-ttu-id="14c58-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14c58-130">RELATED LINKS</span></span>

[<span data-ttu-id="14c58-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="14c58-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="14c58-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="14c58-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="14c58-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="14c58-136">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14c58-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


