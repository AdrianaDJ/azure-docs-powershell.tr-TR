---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 8e3633e88bc3c0972df0d667ed1002571d5ec142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587689"
---
# <span data-ttu-id="6770a-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="6770a-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="6770a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6770a-102">SYNOPSIS</span></span>
<span data-ttu-id="6770a-103">Belirtilen görevin alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6770a-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6770a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6770a-104">SYNTAX</span></span>

### <span data-ttu-id="6770a-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6770a-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6770a-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6770a-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6770a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6770a-107">DESCRIPTION</span></span>
<span data-ttu-id="6770a-108">**Get-AzureBatchSubtask** cmdlet 'i belirtilen görevle ilgili alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6770a-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="6770a-109">Alt görevler tek tek görevler için paralel işleme sağlar ve görev yürütme ve ilerleme durumunu tam olarak izlemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="6770a-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="6770a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6770a-110">EXAMPLES</span></span>

### <span data-ttu-id="6770a-111">Örnek 1: belirtilen görevin tüm alt görevlerini geri döndürme</span><span class="sxs-lookup"><span data-stu-id="6770a-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="6770a-112">Bu komutlar myTask KIMLIĞI olan görevin tüm alt görevlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6770a-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="6770a-113">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6770a-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="6770a-114">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="6770a-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="6770a-115">İkinci komut daha sonra bu nesne başvurusunu ve **Get-AzureBatchSubtask** cmdlet 'Ini kullanarak MyTask için tüm alt görevleri döndürür; iş işi kapsamında çalışan bir görevdir-01.</span><span class="sxs-lookup"><span data-stu-id="6770a-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="6770a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6770a-116">PARAMETERS</span></span>

### <span data-ttu-id="6770a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6770a-117">-BatchContext</span></span>
<span data-ttu-id="6770a-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6770a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6770a-119">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6770a-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6770a-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="6770a-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6770a-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6770a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6770a-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6770a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6770a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6770a-123">-DefaultProfile</span></span>
<span data-ttu-id="6770a-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6770a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6770a-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="6770a-125">-JobId</span></span>
<span data-ttu-id="6770a-126">Bu cmdlet 'in gelen alt görevlerini içeren görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6770a-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6770a-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6770a-127">-MaxCount</span></span>
<span data-ttu-id="6770a-128">Döndürülecek en fazla alt görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6770a-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="6770a-129">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="6770a-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6770a-130">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6770a-130">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6770a-131">-Görev</span><span class="sxs-lookup"><span data-stu-id="6770a-131">-Task</span></span>
<span data-ttu-id="6770a-132">Bu cmdlet 'in döndürdüğü alt görevleri içeren göreve bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6770a-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="6770a-133">Bu nesne başvurusu, Get-AzureBatchTask cmdlet 'i kullanılarak ve döndürülen nesne bir değişkende depolanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6770a-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6770a-134">-TaskID</span><span class="sxs-lookup"><span data-stu-id="6770a-134">-TaskId</span></span>
<span data-ttu-id="6770a-135">Bu cmdlet 'in döndürdüğü görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6770a-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6770a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6770a-136">CommonParameters</span></span>
<span data-ttu-id="6770a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6770a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6770a-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6770a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6770a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6770a-139">INPUTS</span></span>

### <span data-ttu-id="6770a-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6770a-140">BatchAccountContext</span></span>
<span data-ttu-id="6770a-141">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6770a-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6770a-142">Ince görev</span><span class="sxs-lookup"><span data-stu-id="6770a-142">PSCloudTask</span></span>
<span data-ttu-id="6770a-143">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="6770a-143">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="6770a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6770a-144">OUTPUTS</span></span>

###  
<span data-ttu-id="6770a-145">Bu cmdlet, **Pssubtaskınformation** nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="6770a-145">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="6770a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6770a-146">NOTES</span></span>

## <span data-ttu-id="6770a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6770a-147">RELATED LINKS</span></span>

[<span data-ttu-id="6770a-148">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6770a-148">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


