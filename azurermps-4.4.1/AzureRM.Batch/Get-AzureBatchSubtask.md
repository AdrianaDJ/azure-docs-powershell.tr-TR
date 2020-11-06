---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595025"
---
# <span data-ttu-id="692bb-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="692bb-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="692bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="692bb-102">SYNOPSIS</span></span>
<span data-ttu-id="692bb-103">Belirtilen görevin alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="692bb-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="692bb-104">SYNTAX</span></span>

### <span data-ttu-id="692bb-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="692bb-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692bb-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="692bb-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="692bb-107">DESCRIPTION</span></span>
<span data-ttu-id="692bb-108">**Get-AzureBatchSubtask** cmdlet 'i belirtilen görevle ilgili alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="692bb-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="692bb-109">Alt görevler tek tek görevler için paralel işleme sağlar ve görev yürütme ve ilerleme durumunu tam olarak izlemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="692bb-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="692bb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="692bb-110">EXAMPLES</span></span>

### <span data-ttu-id="692bb-111">Örnek 1: belirtilen görevin tüm alt görevlerini geri döndürme</span><span class="sxs-lookup"><span data-stu-id="692bb-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="692bb-112">Bu komutlar myTask KIMLIĞI olan görevin tüm alt görevlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="692bb-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="692bb-113">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="692bb-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="692bb-114">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="692bb-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="692bb-115">İkinci komut daha sonra bu nesne başvurusunu ve **Get-AzureBatchSubtask** cmdlet 'Ini kullanarak MyTask için tüm alt görevleri döndürür; iş işi kapsamında çalışan bir görevdir-01.</span><span class="sxs-lookup"><span data-stu-id="692bb-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="692bb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="692bb-116">PARAMETERS</span></span>

### <span data-ttu-id="692bb-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="692bb-117">-BatchContext</span></span>
<span data-ttu-id="692bb-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="692bb-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="692bb-119">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="692bb-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="692bb-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="692bb-120">-JobId</span></span>
<span data-ttu-id="692bb-121">Bu cmdlet 'in gelen alt görevlerini içeren görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="692bb-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692bb-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="692bb-122">-MaxCount</span></span>
<span data-ttu-id="692bb-123">Döndürülecek en fazla alt görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="692bb-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="692bb-124">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="692bb-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="692bb-125">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="692bb-125">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="692bb-126">-Görev</span><span class="sxs-lookup"><span data-stu-id="692bb-126">-Task</span></span>
<span data-ttu-id="692bb-127">Bu cmdlet 'in döndürdüğü alt görevleri içeren göreve bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="692bb-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="692bb-128">Bu nesne başvurusu, Get-AzureBatchTask cmdlet 'i kullanılarak ve döndürülen nesne bir değişkende depolanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="692bb-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="692bb-129">-TaskID</span><span class="sxs-lookup"><span data-stu-id="692bb-129">-TaskId</span></span>
<span data-ttu-id="692bb-130">Bu cmdlet 'in döndürdüğü görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="692bb-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692bb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692bb-131">-DefaultProfile</span></span>
<span data-ttu-id="692bb-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="692bb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="692bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692bb-133">CommonParameters</span></span>
<span data-ttu-id="692bb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="692bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692bb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692bb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692bb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="692bb-136">INPUTS</span></span>

### <span data-ttu-id="692bb-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="692bb-137">BatchAccountContext</span></span>
<span data-ttu-id="692bb-138">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="692bb-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="692bb-139">Ince görev</span><span class="sxs-lookup"><span data-stu-id="692bb-139">PSCloudTask</span></span>
<span data-ttu-id="692bb-140">Parametre ' görev ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="692bb-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="692bb-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="692bb-141">OUTPUTS</span></span>

###  
<span data-ttu-id="692bb-142">Bu cmdlet, **Pssubtaskınformation** nesnesinin örneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="692bb-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="692bb-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="692bb-143">NOTES</span></span>

## <span data-ttu-id="692bb-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="692bb-144">RELATED LINKS</span></span>

[<span data-ttu-id="692bb-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="692bb-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


