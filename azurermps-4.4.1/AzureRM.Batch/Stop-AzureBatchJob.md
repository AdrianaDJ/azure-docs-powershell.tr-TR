---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 8893ed4002e576e257cd9b885d5773c5851edde0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592252"
---
# <span data-ttu-id="282ff-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="282ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="282ff-102">SYNOPSIS</span></span>
<span data-ttu-id="282ff-103">Toplu işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="282ff-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="282ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="282ff-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="282ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="282ff-105">DESCRIPTION</span></span>
<span data-ttu-id="282ff-106">**Stop-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="282ff-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="282ff-107">Bu komut işi tamamlandı olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="282ff-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="282ff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="282ff-108">EXAMPLES</span></span>

### <span data-ttu-id="282ff-109">Örnek 1: toplu işi durdurma</span><span class="sxs-lookup"><span data-stu-id="282ff-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="282ff-110">Bu komut, Iş KIMLIĞI-000001 olan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="282ff-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="282ff-111">Komut, işi durdurmayı seçtiğiniz bir nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="282ff-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="282ff-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="282ff-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="282ff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="282ff-113">PARAMETERS</span></span>

### <span data-ttu-id="282ff-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="282ff-114">-BatchContext</span></span>
<span data-ttu-id="282ff-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="282ff-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="282ff-116">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="282ff-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="282ff-117">-ID</span><span class="sxs-lookup"><span data-stu-id="282ff-117">-Id</span></span>
<span data-ttu-id="282ff-118">Bu cmdlet 'in durduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="282ff-118">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="282ff-119">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="282ff-119">-TerminateReason</span></span>
<span data-ttu-id="282ff-120">İşi durdurmaya karar verdiğiniz nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="282ff-120">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="282ff-121">Bu cmdlet, işin **TerminateReason** özelliği olarak bu metni depolar.</span><span class="sxs-lookup"><span data-stu-id="282ff-121">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282ff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282ff-122">-DefaultProfile</span></span>
<span data-ttu-id="282ff-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="282ff-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="282ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282ff-124">CommonParameters</span></span>
<span data-ttu-id="282ff-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="282ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282ff-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="282ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282ff-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="282ff-127">INPUTS</span></span>

### <span data-ttu-id="282ff-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="282ff-128">BatchAccountContext</span></span>
<span data-ttu-id="282ff-129">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="282ff-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="282ff-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="282ff-130">String</span></span>
<span data-ttu-id="282ff-131">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="282ff-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="282ff-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="282ff-132">OUTPUTS</span></span>

## <span data-ttu-id="282ff-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="282ff-133">NOTES</span></span>

## <span data-ttu-id="282ff-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="282ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="282ff-135">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-135">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="282ff-136">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-136">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="282ff-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="282ff-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="282ff-138">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-138">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="282ff-139">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-139">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="282ff-140">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="282ff-140">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="282ff-141">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="282ff-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


