---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764900"
---
# <span data-ttu-id="19b08-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="19b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19b08-102">SYNOPSIS</span></span>
<span data-ttu-id="19b08-103">İş zamanlaması ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19b08-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19b08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19b08-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19b08-105">DESCRIPTION</span></span>
<span data-ttu-id="19b08-106">**Set-AzureBatchJobSchedule** cmdlet 'ı Azure Batch hizmetinde iş çizelgesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19b08-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="19b08-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19b08-107">EXAMPLES</span></span>

## <span data-ttu-id="19b08-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19b08-108">PARAMETERS</span></span>

### <span data-ttu-id="19b08-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="19b08-109">-BatchContext</span></span>
<span data-ttu-id="19b08-110">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19b08-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="19b08-111">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="19b08-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="19b08-112">-Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="19b08-112">-JobSchedule</span></span>
<span data-ttu-id="19b08-113">İş çizelgesini temsil eden bir **Pschoparlör Iş zamanlaması** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19b08-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="19b08-114">**Pschoparlör** nesnesi almak için Get-AzureBatchJobSchedule cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="19b08-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="19b08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b08-115">-DefaultProfile</span></span>
<span data-ttu-id="19b08-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19b08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b08-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b08-117">CommonParameters</span></span>
<span data-ttu-id="19b08-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19b08-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b08-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b08-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b08-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19b08-120">INPUTS</span></span>

### <span data-ttu-id="19b08-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="19b08-121">BatchAccountContext</span></span>
<span data-ttu-id="19b08-122">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="19b08-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="19b08-123">Ek zamanlama</span><span class="sxs-lookup"><span data-stu-id="19b08-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="19b08-124">' Jobzamanlama ' parametresi ardışık düzenin ' Pscses Jobzamanlama ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="19b08-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="19b08-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19b08-125">OUTPUTS</span></span>

## <span data-ttu-id="19b08-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19b08-126">NOTES</span></span>

## <span data-ttu-id="19b08-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19b08-127">RELATED LINKS</span></span>

[<span data-ttu-id="19b08-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="19b08-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="19b08-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="19b08-131">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="19b08-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="19b08-133">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="19b08-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


