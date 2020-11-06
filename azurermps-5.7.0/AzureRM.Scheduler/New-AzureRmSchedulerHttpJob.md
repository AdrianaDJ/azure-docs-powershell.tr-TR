---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: a3fdbb3732def98bbf885cb58bf6f00dcb61eb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587444"
---
# <span data-ttu-id="6d5f4-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="6d5f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5f4-103">Bir HTTP işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d5f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d5f4-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d5f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5f4-106">**New-AzureRmSchedulerHttpJob** cmdlet 'ı, Azure Zamanlayıcısı 'NDA bir http işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="6d5f4-107">Bu cmdlet, *Erroractiontype* ve *HttpAuthenticationType* parametrelerini temel alan dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="6d5f4-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="6d5f4-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d5f4-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d5f4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d5f4-111">EXAMPLES</span></span>

## <span data-ttu-id="6d5f4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d5f4-112">PARAMETERS</span></span>

### <span data-ttu-id="6d5f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5f4-113">-DefaultProfile</span></span>
<span data-ttu-id="6d5f4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d5f4-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="6d5f4-115">-EndTime</span></span>
<span data-ttu-id="6d5f4-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="6d5f4-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="6d5f4-118">-ErrorActionType</span></span>
<span data-ttu-id="6d5f4-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="6d5f4-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d5f4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d5f4-121">Http</span><span class="sxs-lookup"><span data-stu-id="6d5f4-121">Http</span></span> 
- <span data-ttu-id="6d5f4-122">Https</span><span class="sxs-lookup"><span data-stu-id="6d5f4-122">Https</span></span> 
- <span data-ttu-id="6d5f4-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="6d5f4-123">StorageQueue</span></span> 
- <span data-ttu-id="6d5f4-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6d5f4-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="6d5f4-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6d5f4-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="6d5f4-126">-ExecutionCount</span></span>
<span data-ttu-id="6d5f4-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="6d5f4-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="6d5f4-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="6d5f4-129">-Frequency</span></span>
<span data-ttu-id="6d5f4-130">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="6d5f4-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d5f4-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d5f4-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="6d5f4-132">Minute</span></span> 
- <span data-ttu-id="6d5f4-133">Saati</span><span class="sxs-lookup"><span data-stu-id="6d5f4-133">Hour</span></span> 
- <span data-ttu-id="6d5f4-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="6d5f4-134">Day</span></span> 
- <span data-ttu-id="6d5f4-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="6d5f4-135">Week</span></span> 
- <span data-ttu-id="6d5f4-136">Ay</span><span class="sxs-lookup"><span data-stu-id="6d5f4-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-137">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="6d5f4-137">-Headers</span></span>
<span data-ttu-id="6d5f4-138">Üst bilgiler içeren bir karma tablo belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="6d5f4-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="6d5f4-140">HTTP kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="6d5f4-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d5f4-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d5f4-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d5f4-142">None</span></span> 
- <span data-ttu-id="6d5f4-143">Mc</span><span class="sxs-lookup"><span data-stu-id="6d5f4-143">ClientCertificate</span></span> 
- <span data-ttu-id="6d5f4-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="6d5f4-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="6d5f4-145">Ana</span><span class="sxs-lookup"><span data-stu-id="6d5f4-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-146">-Aralık</span><span class="sxs-lookup"><span data-stu-id="6d5f4-146">-Interval</span></span>
<span data-ttu-id="6d5f4-147">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="6d5f4-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6d5f4-148">-JobCollectionName</span></span>
<span data-ttu-id="6d5f4-149">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-149">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="6d5f4-150">-JobName</span></span>
<span data-ttu-id="6d5f4-151">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-151">Specifies a name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="6d5f4-152">-JobState</span></span>
<span data-ttu-id="6d5f4-153">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-153">Specifies the state of the job.</span></span>
<span data-ttu-id="6d5f4-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d5f4-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d5f4-155">Etkin</span><span class="sxs-lookup"><span data-stu-id="6d5f4-155">Enabled</span></span> 
- <span data-ttu-id="6d5f4-156">DISABLED</span><span class="sxs-lookup"><span data-stu-id="6d5f4-156">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-157">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="6d5f4-157">-Method</span></span>
<span data-ttu-id="6d5f4-158">İş için eylem türlerinin yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="6d5f4-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d5f4-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d5f4-160">Al</span><span class="sxs-lookup"><span data-stu-id="6d5f4-160">GET</span></span> 
- <span data-ttu-id="6d5f4-161">KOYUL</span><span class="sxs-lookup"><span data-stu-id="6d5f4-161">PUT</span></span> 
- <span data-ttu-id="6d5f4-162">Yayınla</span><span class="sxs-lookup"><span data-stu-id="6d5f4-162">POST</span></span> 
- <span data-ttu-id="6d5f4-163">SILME</span><span class="sxs-lookup"><span data-stu-id="6d5f4-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="6d5f4-164">-RequestBody</span></span>
<span data-ttu-id="6d5f4-165">İş gönderme ve gönderme eylemlerinin gövdesinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="6d5f4-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5f4-166">-ResourceGroupName</span></span>
<span data-ttu-id="6d5f4-167">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-167">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-168">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="6d5f4-168">-StartTime</span></span>
<span data-ttu-id="6d5f4-169">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-170">-URI</span><span class="sxs-lookup"><span data-stu-id="6d5f4-170">-Uri</span></span>
<span data-ttu-id="6d5f4-171">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-172">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d5f4-172">-Confirm</span></span>
<span data-ttu-id="6d5f4-173">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5f4-174">-WhatIf</span></span>
<span data-ttu-id="6d5f4-175">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5f4-176">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-176">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d5f4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5f4-177">CommonParameters</span></span>
<span data-ttu-id="6d5f4-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5f4-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5f4-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5f4-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d5f4-180">INPUTS</span></span>

### <span data-ttu-id="6d5f4-181">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d5f4-181">None</span></span>
<span data-ttu-id="6d5f4-182">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6d5f4-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d5f4-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d5f4-183">OUTPUTS</span></span>

### <span data-ttu-id="6d5f4-184">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6d5f4-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="6d5f4-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d5f4-185">NOTES</span></span>

## <span data-ttu-id="6d5f4-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d5f4-186">RELATED LINKS</span></span>

[<span data-ttu-id="6d5f4-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6d5f4-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6d5f4-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="6d5f4-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6d5f4-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="6d5f4-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="6d5f4-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6d5f4-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6d5f4-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="6d5f4-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6d5f4-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d5f4-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


