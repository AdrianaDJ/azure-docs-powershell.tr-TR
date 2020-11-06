---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592251"
---
# <span data-ttu-id="b85de-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="b85de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b85de-102">SYNOPSIS</span></span>
<span data-ttu-id="b85de-103">Toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b85de-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b85de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b85de-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b85de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b85de-105">DESCRIPTION</span></span>
<span data-ttu-id="b85de-106">**Stop-AzureBatchJobSchedule** cmdlet 'ı bir Azure toplu iş çizelgesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b85de-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="b85de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b85de-107">EXAMPLES</span></span>

### <span data-ttu-id="b85de-108">Örnek 1: iş çizelgesini durdurma</span><span class="sxs-lookup"><span data-stu-id="b85de-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="b85de-109">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="b85de-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="b85de-110">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b85de-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="b85de-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b85de-111">PARAMETERS</span></span>

### <span data-ttu-id="b85de-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b85de-112">-BatchContext</span></span>
<span data-ttu-id="b85de-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b85de-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b85de-114">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b85de-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b85de-115">-ID</span><span class="sxs-lookup"><span data-stu-id="b85de-115">-Id</span></span>
<span data-ttu-id="b85de-116">Bu cmdlet 'in durduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b85de-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b85de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85de-117">-DefaultProfile</span></span>
<span data-ttu-id="b85de-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b85de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b85de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85de-119">CommonParameters</span></span>
<span data-ttu-id="b85de-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b85de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85de-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85de-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85de-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b85de-122">INPUTS</span></span>

### <span data-ttu-id="b85de-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b85de-123">BatchAccountContext</span></span>
<span data-ttu-id="b85de-124">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b85de-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b85de-125">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b85de-125">String</span></span>
<span data-ttu-id="b85de-126">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b85de-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b85de-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b85de-127">OUTPUTS</span></span>

## <span data-ttu-id="b85de-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b85de-128">NOTES</span></span>

## <span data-ttu-id="b85de-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b85de-129">RELATED LINKS</span></span>

[<span data-ttu-id="b85de-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b85de-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b85de-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b85de-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b85de-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b85de-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="b85de-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b85de-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="b85de-136">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b85de-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


