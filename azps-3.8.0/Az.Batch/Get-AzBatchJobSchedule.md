---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: a90f437bc593e1abcb6dc2d92292e04dd9c9f74b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107304"
---
# <span data-ttu-id="b11ad-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b11ad-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="b11ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b11ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b11ad-103">Toplu iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="b11ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b11ad-104">SYNTAX</span></span>

### <span data-ttu-id="b11ad-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b11ad-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b11ad-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="b11ad-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b11ad-107">DESCRIPTION</span></span>
<span data-ttu-id="b11ad-108">**Get-Azbatchjobzamanlama** cmdlet 'ı, *batchcontext* parametresi tarafından belirtilen toplu Iş hesabı için Azure toplu iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="b11ad-109">Tek bir iş zamanlaması almak için bir KIMLIK belirtin.</span><span class="sxs-lookup"><span data-stu-id="b11ad-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="b11ad-110">Açık bir veri Protokolü (OData) filtresiyle eşleşen iş zamanlamalarını almak için *filtre* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b11ad-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b11ad-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b11ad-111">EXAMPLES</span></span>

### <span data-ttu-id="b11ad-112">Örnek 1: KIMLIK belirterek iş zamanlaması alma</span><span class="sxs-lookup"><span data-stu-id="b11ad-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="b11ad-113">Bu komut, JobSchedule23 KIMLIĞINE sahip iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="b11ad-114">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b11ad-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b11ad-115">Örnek 2: filtre kullanarak iş zamanlamalarını alma</span><span class="sxs-lookup"><span data-stu-id="b11ad-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="b11ad-116">Bu komut, *filtre* parametresini belirterek iş Ile başlayan kimlikleri olan tüm iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="b11ad-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b11ad-117">PARAMETERS</span></span>

### <span data-ttu-id="b11ad-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b11ad-118">-BatchContext</span></span>
<span data-ttu-id="b11ad-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b11ad-120">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b11ad-121">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b11ad-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b11ad-122">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b11ad-123">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b11ad-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b11ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11ad-124">-DefaultProfile</span></span>
<span data-ttu-id="b11ad-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b11ad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11ad-126">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="b11ad-126">-Expand</span></span>
<span data-ttu-id="b11ad-127">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="b11ad-128">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="b11ad-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11ad-129">-Filtre</span><span class="sxs-lookup"><span data-stu-id="b11ad-129">-Filter</span></span>
<span data-ttu-id="b11ad-130">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b11ad-131">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen iş zamanlamaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="b11ad-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="b11ad-132">Filtre belirtmezseniz, bu cmdlet toplu bağlam için tüm iş zamanlamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b11ad-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11ad-133">-ID</span><span class="sxs-lookup"><span data-stu-id="b11ad-133">-Id</span></span>
<span data-ttu-id="b11ad-134">Bu cmdlet 'in aldığı iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="b11ad-135">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b11ad-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b11ad-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b11ad-136">-MaxCount</span></span>
<span data-ttu-id="b11ad-137">Döndürülecek en fazla iş çizelgesi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="b11ad-138">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="b11ad-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b11ad-139">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b11ad-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11ad-140">-Select</span><span class="sxs-lookup"><span data-stu-id="b11ad-140">-Select</span></span>
<span data-ttu-id="b11ad-141">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b11ad-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="b11ad-142">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="b11ad-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11ad-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11ad-143">CommonParameters</span></span>
<span data-ttu-id="b11ad-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b11ad-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11ad-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b11ad-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11ad-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b11ad-146">INPUTS</span></span>

### <span data-ttu-id="b11ad-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b11ad-147">System.String</span></span>

### <span data-ttu-id="b11ad-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b11ad-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b11ad-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b11ad-149">OUTPUTS</span></span>

### <span data-ttu-id="b11ad-150">Microsoft.Azure.Commands.Batch. Modeller. Pschoparlör iş zamanlaması</span><span class="sxs-lookup"><span data-stu-id="b11ad-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="b11ad-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b11ad-151">NOTES</span></span>

## <span data-ttu-id="b11ad-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b11ad-152">RELATED LINKS</span></span>

[<span data-ttu-id="b11ad-153">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="b11ad-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="b11ad-154">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="b11ad-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="b11ad-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b11ad-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b11ad-156">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="b11ad-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="b11ad-157">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="b11ad-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="b11ad-158">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="b11ad-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="b11ad-159">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b11ad-159">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


