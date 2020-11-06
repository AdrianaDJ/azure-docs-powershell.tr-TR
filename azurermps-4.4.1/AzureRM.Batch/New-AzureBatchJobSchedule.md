---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591150"
---
# <span data-ttu-id="600c3-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="600c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600c3-102">SYNOPSIS</span></span>
<span data-ttu-id="600c3-103">Toplu Iş hizmetinde iş çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="600c3-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="600c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="600c3-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="600c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="600c3-105">DESCRIPTION</span></span>
<span data-ttu-id="600c3-106">**New-AzureBatchJobSchedule** cmdlet 'ı Azure Batch hizmetinde bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="600c3-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="600c3-107">*Batchaccountcontext* parametresi bu cmdlet 'in zamanlamayı oluşturduğu hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="600c3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="600c3-108">EXAMPLES</span></span>

### <span data-ttu-id="600c3-109">Örnek 1: iş zamanlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="600c3-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="600c3-110">Bu örnek bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="600c3-110">This example creates a job schedule.</span></span>

<span data-ttu-id="600c3-111">İlk beş komut **Psschedule** , **Psjobspecification** ve **pspoolınformation** nesnelerini oluşturur ve değiştirir.</span><span class="sxs-lookup"><span data-stu-id="600c3-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="600c3-112">Komutlar New-Object cmdlet 'ini ve standart Azure PowerShell söz dizimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="600c3-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="600c3-113">Komutlar, $Schedule ve $JobSpecification değişkenlerinde bu nesneleri depolar.</span><span class="sxs-lookup"><span data-stu-id="600c3-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="600c3-114">Son komut JobSchedule17 KIMLIĞINE sahip bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="600c3-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="600c3-115">Bu zamanlama bir günde yinelenme aralığına sahip işler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="600c3-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="600c3-116">İşler, beşinci komutta belirtildiği gibi, ContosoPool06 KIMLIĞINE sahip havuzda çalışır.</span><span class="sxs-lookup"><span data-stu-id="600c3-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="600c3-117">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="600c3-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="600c3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="600c3-118">PARAMETERS</span></span>

### <span data-ttu-id="600c3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="600c3-119">-BatchContext</span></span>
<span data-ttu-id="600c3-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="600c3-121">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="600c3-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="600c3-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="600c3-122">-DisplayName</span></span>
<span data-ttu-id="600c3-123">İş zamanlaması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-123">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="600c3-124">-ID</span><span class="sxs-lookup"><span data-stu-id="600c3-124">-Id</span></span>
<span data-ttu-id="600c3-125">Bu cmdlet 'in oluşturduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600c3-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="600c3-126">-JobSpecification</span></span>
<span data-ttu-id="600c3-127">Bu cmdlet 'in iş zamanlamasına eklediği işlerin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600c3-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="600c3-128">-Metadata</span></span>
<span data-ttu-id="600c3-129">İş zamanlamasına eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="600c3-130">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="600c3-130">The key is the metadata name.</span></span>
<span data-ttu-id="600c3-131">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="600c3-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600c3-132">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="600c3-132">-Schedule</span></span>
<span data-ttu-id="600c3-133">Ne zaman iş oluşturulacağını belirleyen zamanlamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="600c3-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600c3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600c3-134">-DefaultProfile</span></span>
<span data-ttu-id="600c3-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="600c3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="600c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600c3-136">CommonParameters</span></span>
<span data-ttu-id="600c3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="600c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600c3-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600c3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600c3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="600c3-139">INPUTS</span></span>

### <span data-ttu-id="600c3-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="600c3-140">BatchAccountContext</span></span>
<span data-ttu-id="600c3-141">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="600c3-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="600c3-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="600c3-142">OUTPUTS</span></span>

## <span data-ttu-id="600c3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="600c3-143">NOTES</span></span>

## <span data-ttu-id="600c3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="600c3-144">RELATED LINKS</span></span>

[<span data-ttu-id="600c3-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="600c3-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="600c3-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="600c3-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="600c3-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="600c3-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="600c3-150">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="600c3-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="600c3-151">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="600c3-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


