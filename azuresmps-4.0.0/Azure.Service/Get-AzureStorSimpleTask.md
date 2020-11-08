---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105552"
---
# <span data-ttu-id="93ca3-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="93ca3-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="93ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="93ca3-103">StorSimple aygıtındaki bir görevin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="93ca3-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="93ca3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93ca3-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93ca3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="93ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="93ca3-106">**Get-AzureStorSimpleTask** cmdlet 'ı Azure StorSimple cihazında eş zamanlı olmayan çalışan bir görevin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="93ca3-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="93ca3-107">StorSimple aygıtını yönetirken, çoğu oluşturma, okuma, güncelleştirme ve silme eylemleri zaman uyumsuz olarak çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="93ca3-108">Windows PowerShell bir **TaskID** döndürür.</span><span class="sxs-lookup"><span data-stu-id="93ca3-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="93ca3-109">Görevin geçerli durumunu almak için KIMLIĞI kullanın.</span><span class="sxs-lookup"><span data-stu-id="93ca3-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="93ca3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93ca3-110">EXAMPLES</span></span>

### <span data-ttu-id="93ca3-111">Örnek 1: görevin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="93ca3-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="93ca3-112">Bu komut, belirtilen KIMLIĞE sahip görevin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="93ca3-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="93ca3-113">Sonuçlar görevin tamamlandı durumunu ve başarılı bir sonucu olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="93ca3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93ca3-114">PARAMETERS</span></span>

### <span data-ttu-id="93ca3-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="93ca3-115">-InstanceId</span></span>
<span data-ttu-id="93ca3-116">Bu cmdlet 'in durumu izlediği görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ca3-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="93ca3-117">-Profile</span></span>
<span data-ttu-id="93ca3-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93ca3-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="93ca3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ca3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ca3-120">CommonParameters</span></span>
<span data-ttu-id="93ca3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93ca3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ca3-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ca3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ca3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93ca3-123">INPUTS</span></span>

### <span data-ttu-id="93ca3-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="93ca3-124">None</span></span>

## <span data-ttu-id="93ca3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93ca3-125">OUTPUTS</span></span>

### <span data-ttu-id="93ca3-126">Jobstatusınfo</span><span class="sxs-lookup"><span data-stu-id="93ca3-126">JobStatusInfo</span></span>
<span data-ttu-id="93ca3-127">Bu cmdlet, aşağıdaki alanları içeren bir **Taskstatusınfo** nesnesi döndürür:</span><span class="sxs-lookup"><span data-stu-id="93ca3-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="93ca3-128">**Hatası**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-128">**Error**.</span></span>
<span data-ttu-id="93ca3-129">**Kod** ve **Ileti** içeren **ErrorDetails**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="93ca3-130">**TaskID**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-130">**TaskId**.</span></span>
<span data-ttu-id="93ca3-131">**Dizedir**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-131">**String**.</span></span>
<span data-ttu-id="93ca3-132">Durumu döndürülecek görevin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="93ca3-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="93ca3-133">**Görevadımları**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-133">**TaskSteps**.</span></span>
<span data-ttu-id="93ca3-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="93ca3-135">Her **Taskstep** nesnesi **ayrıntı** , **HataKodu** , **ileti** , **sonuç** ve **durum** içerir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="93ca3-136">**Sonuç**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-136">**Result**.</span></span>
<span data-ttu-id="93ca3-137">Görev **sonucu** , görevin genel sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="93ca3-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="93ca3-138">Geçerli değerler: başarısız, başarılı, PartialSuccess, Iptal edildi ve geçersiz.</span><span class="sxs-lookup"><span data-stu-id="93ca3-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="93ca3-139">**Durumu**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-139">**Status**.</span></span>
<span data-ttu-id="93ca3-140">Görevin genel çalışma durumunu içeren görev **durumu**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="93ca3-141">Geçerli değerler: InProgress, geçersiz ve tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="93ca3-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="93ca3-142">**Görevsonucu**.</span><span class="sxs-lookup"><span data-stu-id="93ca3-142">**TaskResult**.</span></span>
<span data-ttu-id="93ca3-143">**TaskResult** , **sonuç** ve **durumuna** göre hesaplanan bir değer.</span><span class="sxs-lookup"><span data-stu-id="93ca3-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="93ca3-144">Geçerli değerler: başarısız, başarılı, sürüyor, PartialSuccess, Iptal edildi ve geçersiz.</span><span class="sxs-lookup"><span data-stu-id="93ca3-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="93ca3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93ca3-145">NOTES</span></span>

## <span data-ttu-id="93ca3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93ca3-146">RELATED LINKS</span></span>

