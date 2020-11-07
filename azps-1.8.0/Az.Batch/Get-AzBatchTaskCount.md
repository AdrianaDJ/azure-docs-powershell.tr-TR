---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: 51e9053737b95113144d5421492f64623b425ff6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761869"
---
# <span data-ttu-id="5e2c8-101">Get-AzBatchTaskCount</span><span class="sxs-lookup"><span data-stu-id="5e2c8-101">Get-AzBatchTaskCount</span></span>

## <span data-ttu-id="5e2c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e2c8-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2c8-103">Belirtilen iş için görev sayılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-103">Gets the task counts for the specified job.</span></span>

## <span data-ttu-id="5e2c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e2c8-104">SYNTAX</span></span>

### <span data-ttu-id="5e2c8-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="5e2c8-105">Id</span></span>
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e2c8-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e2c8-106">ParentObject</span></span>
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e2c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e2c8-107">DESCRIPTION</span></span>
<span data-ttu-id="5e2c8-108">**Get-AzBatchTaskCount** cmdlet 'ı, toplu Iş Için Azure Batch görevlerinin sayımını alır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-108">The **Get-AzBatchTaskCount** cmdlet gets the Azure Batch tasks count for a Batch job.</span></span>
<span data-ttu-id="5e2c8-109">İş veya *iş* *parametresinden bir* iş belirtin.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-109">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="5e2c8-110">Görev sayımları etkin, çalışan veya tamamlanan görev durumuna göre görevlerin sayısını ve başarılı veya başarısız olan görevlerin sayısını sağlar.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-110">Task counts provide a count of the tasks by active, running or completed task state, and a count of tasks which succeeded or failed.</span></span> <span data-ttu-id="5e2c8-111">Hazırlık durumundaki görevler çalışıyor olarak sayılır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-111">Tasks in the preparing state are counted as running.</span></span> <span data-ttu-id="5e2c8-112">ValidationStatus doğrulanırsa, toplu Iş hizmeti durum sayılarını liste görevleri API 'sinde bildirilen görev durumlarına göre denetleyememiştir.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-112">If the validationStatus is unvalidated, then the Batch service has not been able to check state counts against the task states as reported in the List Tasks API.</span></span> <span data-ttu-id="5e2c8-113">İş 200.000 ' den fazla görev içeriyorsa doğrulama durumu geçersiz olabilir.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-113">The validationStatus may be unvalidated if the job contains more than 200,000 tasks.</span></span>

## <span data-ttu-id="5e2c8-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e2c8-114">EXAMPLES</span></span>

### <span data-ttu-id="5e2c8-115">Örnek 1: KIMLIĞE göre görev sayımları alma</span><span class="sxs-lookup"><span data-stu-id="5e2c8-115">Example 1: Get task counts by ID</span></span>
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

<span data-ttu-id="5e2c8-116">Bu komut, iş Job01 için görev sayılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-116">This command gets the task counts for job Job01.</span></span>
<span data-ttu-id="5e2c8-117">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-117">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5e2c8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e2c8-118">PARAMETERS</span></span>

### <span data-ttu-id="5e2c8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e2c8-119">-BatchContext</span></span>
<span data-ttu-id="5e2c8-120">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="5e2c8-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="5e2c8-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="5e2c8-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="5e2c8-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e2c8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2c8-125">-DefaultProfile</span></span>
<span data-ttu-id="5e2c8-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c8-127">-Job</span><span class="sxs-lookup"><span data-stu-id="5e2c8-127">-Job</span></span>
<span data-ttu-id="5e2c8-128">Bu cmdlet 'in aldığı görevleri içeren işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-128">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="5e2c8-129">Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-129">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c8-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="5e2c8-130">-JobId</span></span>
<span data-ttu-id="5e2c8-131">Görev sayılarının alınacağı işin kimliği.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-131">The id of the job for which to get task counts.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2c8-132">CommonParameters</span></span>
<span data-ttu-id="5e2c8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2c8-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2c8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e2c8-135">INPUTS</span></span>

### <span data-ttu-id="5e2c8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5e2c8-136">System.String</span></span>

### <span data-ttu-id="5e2c8-137">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="5e2c8-137">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="5e2c8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e2c8-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5e2c8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e2c8-139">OUTPUTS</span></span>

### <span data-ttu-id="5e2c8-140">Microsoft.Azure.Commands.Batch. Modeller. PSTaskCounts</span><span class="sxs-lookup"><span data-stu-id="5e2c8-140">Microsoft.Azure.Commands.Batch.Models.PSTaskCounts</span></span>

## <span data-ttu-id="5e2c8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e2c8-141">NOTES</span></span>

## <span data-ttu-id="5e2c8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e2c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="5e2c8-143">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="5e2c8-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5e2c8-144">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="5e2c8-144">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="5e2c8-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5e2c8-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
