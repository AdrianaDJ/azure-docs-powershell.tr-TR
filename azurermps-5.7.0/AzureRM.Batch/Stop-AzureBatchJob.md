---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJob.md
ms.openlocfilehash: 0f33807c112ea770e3d02d972d52ca7a166bb791
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587675"
---
# <span data-ttu-id="104fd-101">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-101">Stop-AzureBatchJob</span></span>

## <span data-ttu-id="104fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="104fd-102">SYNOPSIS</span></span>
<span data-ttu-id="104fd-103">Toplu işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="104fd-103">Stops a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="104fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="104fd-104">SYNTAX</span></span>

```
Stop-AzureBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="104fd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="104fd-105">DESCRIPTION</span></span>
<span data-ttu-id="104fd-106">**Stop-AzureBatchJob** cmdlet 'ı bir Azure toplu işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="104fd-106">The **Stop-AzureBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="104fd-107">Bu komut işi tamamlandı olarak işaretler.</span><span class="sxs-lookup"><span data-stu-id="104fd-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="104fd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="104fd-108">EXAMPLES</span></span>

### <span data-ttu-id="104fd-109">Örnek 1: toplu işi durdurma</span><span class="sxs-lookup"><span data-stu-id="104fd-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzureBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="104fd-110">Bu komut, Iş KIMLIĞI-000001 olan işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="104fd-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="104fd-111">Komut, işi durdurmayı seçtiğiniz bir nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="104fd-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="104fd-112">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="104fd-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="104fd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="104fd-113">PARAMETERS</span></span>

### <span data-ttu-id="104fd-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="104fd-114">-BatchContext</span></span>
<span data-ttu-id="104fd-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="104fd-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="104fd-116">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="104fd-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="104fd-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="104fd-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="104fd-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="104fd-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="104fd-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="104fd-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="104fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="104fd-120">-DefaultProfile</span></span>
<span data-ttu-id="104fd-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="104fd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="104fd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="104fd-122">-Id</span></span>
<span data-ttu-id="104fd-123">Bu cmdlet 'in durduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="104fd-123">Specifies the ID of the job that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="104fd-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="104fd-124">-TerminateReason</span></span>
<span data-ttu-id="104fd-125">İşi durdurmaya karar verdiğiniz nedeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="104fd-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="104fd-126">Bu cmdlet, işin **TerminateReason** özelliği olarak bu metni depolar.</span><span class="sxs-lookup"><span data-stu-id="104fd-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="104fd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="104fd-127">CommonParameters</span></span>
<span data-ttu-id="104fd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="104fd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="104fd-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="104fd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="104fd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="104fd-130">INPUTS</span></span>

### <span data-ttu-id="104fd-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="104fd-131">BatchAccountContext</span></span>
<span data-ttu-id="104fd-132">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="104fd-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="104fd-133">Dizisi</span><span class="sxs-lookup"><span data-stu-id="104fd-133">String</span></span>
<span data-ttu-id="104fd-134">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="104fd-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="104fd-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="104fd-135">OUTPUTS</span></span>

## <span data-ttu-id="104fd-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="104fd-136">NOTES</span></span>

## <span data-ttu-id="104fd-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="104fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="104fd-138">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-138">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="104fd-139">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-139">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="104fd-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="104fd-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="104fd-141">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-141">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="104fd-142">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-142">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="104fd-143">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="104fd-143">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="104fd-144">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="104fd-144">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


