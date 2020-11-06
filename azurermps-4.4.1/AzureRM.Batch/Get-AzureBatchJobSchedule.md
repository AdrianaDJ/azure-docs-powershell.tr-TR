---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: 139282332fb1c5d0ace02ddd7b998c1875af931a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590767"
---
# <span data-ttu-id="15925-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="15925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15925-102">SYNOPSIS</span></span>
<span data-ttu-id="15925-103">Toplu iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="15925-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15925-104">SYNTAX</span></span>

### <span data-ttu-id="15925-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15925-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15925-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="15925-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15925-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="15925-107">DESCRIPTION</span></span>
<span data-ttu-id="15925-108">**Get-AzureBatchJobSchedule** cmdlet 'ı *batchcontext* parametresi tarafından belirtilen toplu Iş hesabı için Azure toplu iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="15925-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="15925-109">Tek bir iş zamanlaması almak için bir KIMLIK belirtin.</span><span class="sxs-lookup"><span data-stu-id="15925-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="15925-110">Açık bir veri Protokolü (OData) filtresiyle eşleşen iş zamanlamalarını almak için *filtre* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="15925-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="15925-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15925-111">EXAMPLES</span></span>

### <span data-ttu-id="15925-112">Örnek 1: KIMLIK belirterek iş zamanlaması alma</span><span class="sxs-lookup"><span data-stu-id="15925-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="15925-113">Bu komut, JobSchedule23 KIMLIĞINE sahip iş zamanlamasını alır.</span><span class="sxs-lookup"><span data-stu-id="15925-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="15925-114">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="15925-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="15925-115">Örnek 2: filtre kullanarak iş zamanlamalarını alma</span><span class="sxs-lookup"><span data-stu-id="15925-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="15925-116">Bu komut, *filtre* parametresini belirterek iş Ile başlayan kimlikleri olan tüm iş zamanlamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="15925-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="15925-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15925-117">PARAMETERS</span></span>

### <span data-ttu-id="15925-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="15925-118">-BatchContext</span></span>
<span data-ttu-id="15925-119">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="15925-120">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="15925-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="15925-121">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="15925-121">-Expand</span></span>
<span data-ttu-id="15925-122">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-122">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="15925-123">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="15925-123">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="15925-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="15925-124">-Filter</span></span>
<span data-ttu-id="15925-125">Bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-125">Specifies an OData filter clause.</span></span>
<span data-ttu-id="15925-126">Bu cmdlet, bu parametrenin belirttiği filtreyle eşleşen iş zamanlamaları döndürür.</span><span class="sxs-lookup"><span data-stu-id="15925-126">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="15925-127">Filtre belirtmezseniz, bu cmdlet toplu bağlam için tüm iş zamanlamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="15925-127">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="15925-128">-ID</span><span class="sxs-lookup"><span data-stu-id="15925-128">-Id</span></span>
<span data-ttu-id="15925-129">Bu cmdlet 'in aldığı iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-129">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="15925-130">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="15925-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="15925-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="15925-131">-MaxCount</span></span>
<span data-ttu-id="15925-132">Döndürülecek en fazla iş çizelgesi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-132">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="15925-133">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="15925-133">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="15925-134">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="15925-134">The default value is 1000.</span></span>

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

### <span data-ttu-id="15925-135">-Select</span><span class="sxs-lookup"><span data-stu-id="15925-135">-Select</span></span>
<span data-ttu-id="15925-136">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15925-136">Specifies an OData select clause.</span></span>
<span data-ttu-id="15925-137">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="15925-137">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="15925-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15925-138">-DefaultProfile</span></span>
<span data-ttu-id="15925-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15925-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15925-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15925-140">CommonParameters</span></span>
<span data-ttu-id="15925-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15925-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15925-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15925-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15925-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15925-143">INPUTS</span></span>

### <span data-ttu-id="15925-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="15925-144">BatchAccountContext</span></span>
<span data-ttu-id="15925-145">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="15925-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="15925-146">Dizisi</span><span class="sxs-lookup"><span data-stu-id="15925-146">String</span></span>
<span data-ttu-id="15925-147">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="15925-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="15925-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15925-148">OUTPUTS</span></span>

### <span data-ttu-id="15925-149">Ek zamanlama</span><span class="sxs-lookup"><span data-stu-id="15925-149">PSCloudJobSchedule</span></span>

## <span data-ttu-id="15925-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15925-150">NOTES</span></span>

## <span data-ttu-id="15925-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15925-151">RELATED LINKS</span></span>

[<span data-ttu-id="15925-152">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-152">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="15925-153">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-153">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="15925-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="15925-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="15925-155">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-155">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="15925-156">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-156">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="15925-157">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="15925-157">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="15925-158">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="15925-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


