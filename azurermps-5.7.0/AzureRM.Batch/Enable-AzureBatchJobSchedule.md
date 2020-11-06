---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593513"
---
# <span data-ttu-id="1a874-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="1a874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a874-102">SYNOPSIS</span></span>
<span data-ttu-id="1a874-103">Toplu iş çizelgesini mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="1a874-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a874-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a874-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a874-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a874-105">DESCRIPTION</span></span>
<span data-ttu-id="1a874-106">**Enable-AzureBatchJobSchedule** cmdlet 'ı Azure toplu iş zamanlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1a874-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="1a874-107">İş çizelgesini etkinleştirdikten sonra, işler bu zamanlamaya göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1a874-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="1a874-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a874-108">EXAMPLES</span></span>

### <span data-ttu-id="1a874-109">Örnek 1: iş çizelgesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1a874-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="1a874-110">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="1a874-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="1a874-111">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a874-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="1a874-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a874-112">PARAMETERS</span></span>

### <span data-ttu-id="1a874-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1a874-113">-BatchContext</span></span>
<span data-ttu-id="1a874-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a874-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1a874-115">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a874-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1a874-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="1a874-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1a874-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a874-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1a874-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1a874-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1a874-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a874-119">-DefaultProfile</span></span>
<span data-ttu-id="1a874-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a874-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a874-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1a874-121">-Id</span></span>
<span data-ttu-id="1a874-122">Bu cmdlet 'in izin aldığı iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a874-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="1a874-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a874-123">CommonParameters</span></span>
<span data-ttu-id="1a874-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a874-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a874-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a874-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a874-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a874-126">INPUTS</span></span>

### <span data-ttu-id="1a874-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1a874-127">BatchAccountContext</span></span>
<span data-ttu-id="1a874-128">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1a874-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1a874-129">Dizisi</span><span class="sxs-lookup"><span data-stu-id="1a874-129">String</span></span>
<span data-ttu-id="1a874-130">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1a874-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="1a874-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a874-131">OUTPUTS</span></span>

## <span data-ttu-id="1a874-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a874-132">NOTES</span></span>

## <span data-ttu-id="1a874-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a874-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a874-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="1a874-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1a874-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1a874-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="1a874-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="1a874-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="1a874-139">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="1a874-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="1a874-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1a874-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


