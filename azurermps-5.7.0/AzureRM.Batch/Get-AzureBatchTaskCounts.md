---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587687"
---
# <span data-ttu-id="f1470-101">Get-AzureBatchTaskCounts</span><span class="sxs-lookup"><span data-stu-id="f1470-101">Get-AzureBatchTaskCounts</span></span>

## <span data-ttu-id="f1470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1470-102">SYNOPSIS</span></span>
<span data-ttu-id="f1470-103">Belirtilen iş için görev sayılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f1470-103">Gets the task counts for the specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1470-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1470-104">SYNTAX</span></span>

### <span data-ttu-id="f1470-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="f1470-105">Id</span></span>
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="f1470-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="f1470-106">ParentObject</span></span>
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="f1470-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1470-107">DESCRIPTION</span></span>
<span data-ttu-id="f1470-108">**Get-AzureBatchTaskCounts** cmdlet 'ı bir toplu Iş Için Azure Batch görevlerinin sayımını alır.</span><span class="sxs-lookup"><span data-stu-id="f1470-108">The **Get-AzureBatchTaskCounts** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="f1470-109">İş veya *iş* *parametresinden bir* iş belirtin.</span><span class="sxs-lookup"><span data-stu-id="f1470-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="f1470-110">Görev sayımları etkin, çalışan veya tamamlanan görev durumuna göre görevlerin sayısını ve başarılı veya başarısız olan görevlerin sayısını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f1470-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="f1470-111">Hazırlık durumundaki görevler çalışıyor olarak sayılır.</span><span class="sxs-lookup"><span data-stu-id="f1470-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="f1470-112">ValidationStatus doğrulanırsa, toplu Iş hizmeti durum sayılarını liste görevleri API 'sinde bildirilen görev durumlarına göre denetleyememiştir.</span><span class="sxs-lookup"><span data-stu-id="f1470-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="f1470-113">İş 200.000 ' den fazla görev içeriyorsa doğrulama durumu geçersiz olabilir.</span><span class="sxs-lookup"><span data-stu-id="f1470-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="f1470-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1470-114">EXAMPLES</span></span>

### <span data-ttu-id="f1470-115">Örnek 1: KIMLIĞE göre görev sayımları alma</span><span class="sxs-lookup"><span data-stu-id="f1470-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="f1470-116">Bu komut, iş Job01 için görev sayılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f1470-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="f1470-117">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1470-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f1470-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1470-118">PARAMETERS</span></span>

### <span data-ttu-id="f1470-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f1470-119">-BatchContext</span></span>
<span data-ttu-id="f1470-120">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="f1470-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="f1470-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1470-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="f1470-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f1470-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="f1470-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1470-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="f1470-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1470-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f1470-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1470-125">-DefaultProfile</span></span>
<span data-ttu-id="f1470-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1470-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1470-127">-Job</span><span class="sxs-lookup"><span data-stu-id="f1470-127">-Job</span></span>
<span data-ttu-id="f1470-128">Bu cmdlet 'in aldığı görevleri içeren işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1470-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="f1470-129">Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1470-129">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1470-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="f1470-130">-JobId</span></span>
<span data-ttu-id="f1470-131">Görev sayılarının alınacağı işin kimliği.</span><span class="sxs-lookup"><span data-stu-id="f1470-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f1470-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1470-132">INPUTS</span></span>

### <span data-ttu-id="f1470-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f1470-133">System.String</span></span>
<span data-ttu-id="f1470-134">Microsoft.Azure.Commands.Batch. Modeller. Pscbalajob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f1470-134">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>


## <span data-ttu-id="f1470-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1470-135">OUTPUTS</span></span>

### <span data-ttu-id="f1470-136">Microsoft.Azure.Commands.Batch. Modeller. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="f1470-136">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>


## <span data-ttu-id="f1470-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1470-137">NOTES</span></span>

## <span data-ttu-id="f1470-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1470-138">RELATED LINKS</span></span>

[<span data-ttu-id="f1470-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f1470-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f1470-140">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="f1470-140">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="f1470-141">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f1470-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
