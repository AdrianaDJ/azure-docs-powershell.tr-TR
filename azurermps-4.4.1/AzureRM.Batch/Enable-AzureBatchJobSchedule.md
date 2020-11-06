---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594829"
---
# <span data-ttu-id="6e66d-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="6e66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e66d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e66d-103">Toplu iş çizelgesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="6e66d-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e66d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e66d-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e66d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e66d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e66d-106">**Enable-AzureBatchJobSchedule** cmdlet 'ı Azure toplu iş zamanlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6e66d-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="6e66d-107">İş çizelgesini etkinleştirdikten sonra, işler bu zamanlamaya göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="6e66d-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="6e66d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e66d-108">EXAMPLES</span></span>

### <span data-ttu-id="6e66d-109">Örnek 1: iş çizelgesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6e66d-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="6e66d-110">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="6e66d-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="6e66d-111">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e66d-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="6e66d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e66d-112">PARAMETERS</span></span>

### <span data-ttu-id="6e66d-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e66d-113">-BatchContext</span></span>
<span data-ttu-id="6e66d-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e66d-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e66d-115">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e66d-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6e66d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6e66d-116">-Id</span></span>
<span data-ttu-id="6e66d-117">Bu cmdlet 'in izin aldığı iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e66d-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="6e66d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e66d-118">-DefaultProfile</span></span>
<span data-ttu-id="6e66d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e66d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e66d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e66d-120">CommonParameters</span></span>
<span data-ttu-id="6e66d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e66d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e66d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e66d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e66d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e66d-123">INPUTS</span></span>

### <span data-ttu-id="6e66d-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e66d-124">BatchAccountContext</span></span>
<span data-ttu-id="6e66d-125">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6e66d-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6e66d-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="6e66d-126">String</span></span>
<span data-ttu-id="6e66d-127">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6e66d-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6e66d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e66d-128">OUTPUTS</span></span>

## <span data-ttu-id="6e66d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e66d-129">NOTES</span></span>

## <span data-ttu-id="6e66d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e66d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6e66d-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="6e66d-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e66d-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6e66d-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="6e66d-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="6e66d-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="6e66d-136">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="6e66d-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="6e66d-137">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6e66d-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


