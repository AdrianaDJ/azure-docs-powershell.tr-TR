---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: a1841fb569cf6ef29bad685679372e0385133568
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594966"
---
# <span data-ttu-id="8f86d-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="8f86d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f86d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f86d-103">Toplu Iş hizmetinde iş çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f86d-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f86d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f86d-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f86d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f86d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f86d-106">**New-AzureBatchJobSchedule** cmdlet 'ı Azure Batch hizmetinde bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f86d-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="8f86d-107">*Batchaccountcontext* parametresi bu cmdlet 'in zamanlamayı oluşturduğu hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="8f86d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f86d-108">EXAMPLES</span></span>

### <span data-ttu-id="8f86d-109">Örnek 1: iş zamanlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f86d-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="8f86d-110">Bu örnek bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f86d-110">This example creates a job schedule.</span></span>

<span data-ttu-id="8f86d-111">İlk beş komut **Psschedule** , **Psjobspecification** ve **pspoolınformation** nesnelerini oluşturur ve değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="8f86d-112">Komutlar New-Object cmdlet 'ini ve standart Azure PowerShell söz dizimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8f86d-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="8f86d-113">Komutlar, $Schedule ve $JobSpecification değişkenlerinde bu nesneleri depolar.</span><span class="sxs-lookup"><span data-stu-id="8f86d-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="8f86d-114">Son komut JobSchedule17 KIMLIĞINE sahip bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f86d-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="8f86d-115">Bu zamanlama bir günde yinelenme aralığına sahip işler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8f86d-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="8f86d-116">İşler, beşinci komutta belirtildiği gibi, ContosoPool06 KIMLIĞINE sahip havuzda çalışır.</span><span class="sxs-lookup"><span data-stu-id="8f86d-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="8f86d-117">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8f86d-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8f86d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f86d-118">PARAMETERS</span></span>

### <span data-ttu-id="8f86d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8f86d-119">-BatchContext</span></span>
<span data-ttu-id="8f86d-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f86d-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8f86d-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f86d-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="8f86d-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f86d-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8f86d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f86d-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8f86d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8f86d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f86d-125">-DefaultProfile</span></span>
<span data-ttu-id="8f86d-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f86d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f86d-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f86d-127">-DisplayName</span></span>
<span data-ttu-id="8f86d-128">İş zamanlaması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-128">Specifies a display name for the job schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f86d-129">-ID</span><span class="sxs-lookup"><span data-stu-id="8f86d-129">-Id</span></span>
<span data-ttu-id="8f86d-130">Bu cmdlet 'in oluşturduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f86d-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="8f86d-131">-JobSpecification</span></span>
<span data-ttu-id="8f86d-132">Bu cmdlet 'in iş zamanlamasına eklediği işlerin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f86d-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8f86d-133">-Metadata</span></span>
<span data-ttu-id="8f86d-134">İş zamanlamasına eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="8f86d-135">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="8f86d-135">The key is the metadata name.</span></span>
<span data-ttu-id="8f86d-136">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-136">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f86d-137">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="8f86d-137">-Schedule</span></span>
<span data-ttu-id="8f86d-138">Ne zaman iş oluşturulacağını belirleyen zamanlamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f86d-138">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f86d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f86d-139">CommonParameters</span></span>
<span data-ttu-id="8f86d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f86d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f86d-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f86d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f86d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f86d-142">INPUTS</span></span>

### <span data-ttu-id="8f86d-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f86d-143">BatchAccountContext</span></span>
<span data-ttu-id="8f86d-144">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8f86d-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8f86d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f86d-145">OUTPUTS</span></span>

## <span data-ttu-id="8f86d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f86d-146">NOTES</span></span>

## <span data-ttu-id="8f86d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f86d-147">RELATED LINKS</span></span>

[<span data-ttu-id="8f86d-148">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-148">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8f86d-149">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-149">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="8f86d-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f86d-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8f86d-151">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-151">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8f86d-152">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-152">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="8f86d-153">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8f86d-153">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="8f86d-154">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8f86d-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


