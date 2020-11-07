---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761465"
---
# <span data-ttu-id="56da4-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="56da4-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="56da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56da4-102">SYNOPSIS</span></span>
<span data-ttu-id="56da4-103">Belirtilen görevin alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="56da4-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="56da4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56da4-104">SYNTAX</span></span>

### <span data-ttu-id="56da4-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56da4-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56da4-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="56da4-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56da4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56da4-107">DESCRIPTION</span></span>
<span data-ttu-id="56da4-108">**Get-Azbatchalt görev** cmdlet 'i belirtilen görevle ilgili alt görev bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="56da4-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="56da4-109">Alt görevler tek tek görevler için paralel işleme sağlar ve görev yürütme ve ilerleme durumunu tam olarak izlemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="56da4-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="56da4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56da4-110">EXAMPLES</span></span>

### <span data-ttu-id="56da4-111">Örnek 1: belirtilen görevin tüm alt görevlerini geri döndürme</span><span class="sxs-lookup"><span data-stu-id="56da4-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="56da4-112">Bu komutlar myTask KIMLIĞI olan görevin tüm alt görevlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="56da4-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="56da4-113">Bunu yapmak için örnekteki ilk komut, contosobatchaccount toplu iş hesabındaki hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="56da4-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="56da4-114">Bu nesne başvurusu $context adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="56da4-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="56da4-115">İkinci komut daha sonra bu nesne başvurusunu ve **Get-Azbatchalt görev** cmdlet 'Ini kullanarak MyTask için tüm alt görevleri (iş işinin bir parçası olarak çalışan bir görev) döndürür.</span><span class="sxs-lookup"><span data-stu-id="56da4-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="56da4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56da4-116">PARAMETERS</span></span>

### <span data-ttu-id="56da4-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="56da4-117">-BatchContext</span></span>
<span data-ttu-id="56da4-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="56da4-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="56da4-119">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="56da4-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="56da4-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="56da4-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="56da4-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="56da4-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="56da4-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56da4-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="56da4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56da4-123">-DefaultProfile</span></span>
<span data-ttu-id="56da4-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56da4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56da4-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="56da4-125">-JobId</span></span>
<span data-ttu-id="56da4-126">Bu cmdlet 'in gelen alt görevlerini içeren görevi içeren işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="56da4-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="56da4-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="56da4-127">-MaxCount</span></span>
<span data-ttu-id="56da4-128">Döndürülecek en fazla alt görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56da4-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="56da4-129">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="56da4-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="56da4-130">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="56da4-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="56da4-131">-Görev</span><span class="sxs-lookup"><span data-stu-id="56da4-131">-Task</span></span>
<span data-ttu-id="56da4-132">Bu cmdlet 'in döndürdüğü alt görevleri içeren göreve bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="56da4-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="56da4-133">Bu nesne başvurusu, Get-AzBatchTask cmdlet 'i kullanılarak ve döndürülen nesne bir değişkende depolanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="56da4-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="56da4-134">-TaskID</span><span class="sxs-lookup"><span data-stu-id="56da4-134">-TaskId</span></span>
<span data-ttu-id="56da4-135">Bu cmdlet 'in döndürdüğü görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="56da4-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="56da4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56da4-136">CommonParameters</span></span>
<span data-ttu-id="56da4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56da4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56da4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56da4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56da4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56da4-139">INPUTS</span></span>

### <span data-ttu-id="56da4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56da4-140">System.String</span></span>

### <span data-ttu-id="56da4-141">Microsoft.Azure.Commands.Batch. Modeller. Ince görev</span><span class="sxs-lookup"><span data-stu-id="56da4-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="56da4-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="56da4-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="56da4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56da4-143">OUTPUTS</span></span>

### <span data-ttu-id="56da4-144">Microsoft.Azure.Commands.Batch. Modeller. Pssubtaskınformation</span><span class="sxs-lookup"><span data-stu-id="56da4-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="56da4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56da4-145">NOTES</span></span>

## <span data-ttu-id="56da4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56da4-146">RELATED LINKS</span></span>

[<span data-ttu-id="56da4-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="56da4-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


