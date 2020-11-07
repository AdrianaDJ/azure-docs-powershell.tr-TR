---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 836ad4cda6d6631baf0885ac0ec380fdc401fde6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761853"
---
# <span data-ttu-id="f1cda-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f1cda-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f1cda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1cda-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cda-103">Toplu Iş hizmetinde iş çizelgesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1cda-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="f1cda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1cda-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1cda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1cda-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cda-106">**New-Azbatchjobzamanlama** cmdlet 'ı Azure Batch hizmetinde bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1cda-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="f1cda-107">*Batchaccountcontext* parametresi bu cmdlet 'in zamanlamayı oluşturduğu hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="f1cda-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1cda-108">EXAMPLES</span></span>

### <span data-ttu-id="f1cda-109">Örnek 1: iş zamanlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1cda-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="f1cda-110">Bu örnek bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1cda-110">This example creates a job schedule.</span></span>
<span data-ttu-id="f1cda-111">İlk beş komut **Psschedule** , **Psjobspecification** ve **pspoolınformation** nesnelerini oluşturur ve değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="f1cda-112">Komutlar New-Object cmdlet 'ini ve standart Azure PowerShell söz dizimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="f1cda-113">Komutlar, $Schedule ve $JobSpecification değişkenlerinde bu nesneleri depolar.</span><span class="sxs-lookup"><span data-stu-id="f1cda-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="f1cda-114">Son komut JobSchedule17 KIMLIĞINE sahip bir iş zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1cda-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f1cda-115">Bu zamanlama bir günde yinelenme aralığına sahip işler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1cda-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="f1cda-116">İşler, beşinci komutta belirtildiği gibi, ContosoPool06 KIMLIĞINE sahip havuzda çalışır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="f1cda-117">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1cda-117">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f1cda-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1cda-118">PARAMETERS</span></span>

### <span data-ttu-id="f1cda-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f1cda-119">-BatchContext</span></span>
<span data-ttu-id="f1cda-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f1cda-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f1cda-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f1cda-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f1cda-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f1cda-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1cda-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f1cda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cda-125">-DefaultProfile</span></span>
<span data-ttu-id="f1cda-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1cda-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cda-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1cda-127">-DisplayName</span></span>
<span data-ttu-id="f1cda-128">İş zamanlaması için bir görünen ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="f1cda-129">-ID</span><span class="sxs-lookup"><span data-stu-id="f1cda-129">-Id</span></span>
<span data-ttu-id="f1cda-130">Bu cmdlet 'in oluşturduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f1cda-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="f1cda-131">-JobSpecification</span></span>
<span data-ttu-id="f1cda-132">Bu cmdlet 'in iş zamanlamasına eklediği işlerin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="f1cda-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1cda-133">-Metadata</span></span>
<span data-ttu-id="f1cda-134">İş zamanlamasına eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="f1cda-135">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="f1cda-135">The key is the metadata name.</span></span>
<span data-ttu-id="f1cda-136">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="f1cda-137">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="f1cda-137">-Schedule</span></span>
<span data-ttu-id="f1cda-138">Ne zaman iş oluşturulacağını belirleyen zamanlamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1cda-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="f1cda-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cda-139">CommonParameters</span></span>
<span data-ttu-id="f1cda-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1cda-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cda-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cda-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cda-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1cda-142">INPUTS</span></span>

### <span data-ttu-id="f1cda-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f1cda-143">System.String</span></span>

### <span data-ttu-id="f1cda-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f1cda-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f1cda-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1cda-145">OUTPUTS</span></span>

### <span data-ttu-id="f1cda-146">System. void</span><span class="sxs-lookup"><span data-stu-id="f1cda-146">System.Void</span></span>

## <span data-ttu-id="f1cda-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1cda-147">NOTES</span></span>

## <span data-ttu-id="f1cda-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1cda-148">RELATED LINKS</span></span>

[<span data-ttu-id="f1cda-149">Disable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="f1cda-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f1cda-150">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="f1cda-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f1cda-151">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="f1cda-151">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f1cda-152">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="f1cda-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f1cda-153">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="f1cda-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f1cda-154">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="f1cda-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f1cda-155">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f1cda-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


