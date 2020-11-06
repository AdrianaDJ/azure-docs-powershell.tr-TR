---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 1d0c66d3442d6db03897140849f5713d3107f8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593881"
---
# <span data-ttu-id="8ba73-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="8ba73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba73-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba73-103">Bir HTTP işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ba73-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ba73-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ba73-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba73-106">**New-AzureRmSchedulerHttpJob** cmdlet 'ı, Azure Zamanlayıcısı 'NDA bir http işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ba73-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="8ba73-107">Bu cmdlet, *Erroractiontype* ve *HttpAuthenticationType* parametrelerini temel alan dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8ba73-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="8ba73-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="8ba73-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8ba73-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8ba73-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8ba73-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8ba73-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ba73-111">EXAMPLES</span></span>

## <span data-ttu-id="8ba73-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ba73-112">PARAMETERS</span></span>

### <span data-ttu-id="8ba73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba73-113">-DefaultProfile</span></span>
<span data-ttu-id="8ba73-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ba73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba73-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="8ba73-115">-EndTime</span></span>
<span data-ttu-id="8ba73-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="8ba73-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ba73-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="8ba73-118">-ErrorActionType</span></span>
<span data-ttu-id="8ba73-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="8ba73-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8ba73-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ba73-121">Http</span><span class="sxs-lookup"><span data-stu-id="8ba73-121">Http</span></span> 
- <span data-ttu-id="8ba73-122">Https</span><span class="sxs-lookup"><span data-stu-id="8ba73-122">Https</span></span> 
- <span data-ttu-id="8ba73-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="8ba73-123">StorageQueue</span></span> 
- <span data-ttu-id="8ba73-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8ba73-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="8ba73-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8ba73-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="8ba73-126">-ExecutionCount</span></span>
<span data-ttu-id="8ba73-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="8ba73-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="8ba73-129">-Frequency</span></span>
<span data-ttu-id="8ba73-130">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="8ba73-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8ba73-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ba73-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="8ba73-132">Minute</span></span> 
- <span data-ttu-id="8ba73-133">Saati</span><span class="sxs-lookup"><span data-stu-id="8ba73-133">Hour</span></span> 
- <span data-ttu-id="8ba73-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="8ba73-134">Day</span></span> 
- <span data-ttu-id="8ba73-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="8ba73-135">Week</span></span> 
- <span data-ttu-id="8ba73-136">Ay</span><span class="sxs-lookup"><span data-stu-id="8ba73-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-137">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="8ba73-137">-Headers</span></span>
<span data-ttu-id="8ba73-138">Üst bilgiler içeren bir karma tablo belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8ba73-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="8ba73-140">HTTP kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="8ba73-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8ba73-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ba73-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8ba73-142">None</span></span> 
- <span data-ttu-id="8ba73-143">Mc</span><span class="sxs-lookup"><span data-stu-id="8ba73-143">ClientCertificate</span></span> 
- <span data-ttu-id="8ba73-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="8ba73-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="8ba73-145">Ana</span><span class="sxs-lookup"><span data-stu-id="8ba73-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-146">-Aralık</span><span class="sxs-lookup"><span data-stu-id="8ba73-146">-Interval</span></span>
<span data-ttu-id="8ba73-147">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-147">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8ba73-148">-JobCollectionName</span></span>
<span data-ttu-id="8ba73-149">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-149">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="8ba73-150">-JobName</span></span>
<span data-ttu-id="8ba73-151">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-151">Specifies a name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="8ba73-152">-JobState</span></span>
<span data-ttu-id="8ba73-153">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-153">Specifies the state of the job.</span></span>
<span data-ttu-id="8ba73-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8ba73-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ba73-155">Etkin</span><span class="sxs-lookup"><span data-stu-id="8ba73-155">Enabled</span></span> 
- <span data-ttu-id="8ba73-156">DISABLED</span><span class="sxs-lookup"><span data-stu-id="8ba73-156">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-157">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="8ba73-157">-Method</span></span>
<span data-ttu-id="8ba73-158">İş için eylem türlerinin yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-158">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="8ba73-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8ba73-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ba73-160">Al</span><span class="sxs-lookup"><span data-stu-id="8ba73-160">GET</span></span> 
- <span data-ttu-id="8ba73-161">KOYUL</span><span class="sxs-lookup"><span data-stu-id="8ba73-161">PUT</span></span> 
- <span data-ttu-id="8ba73-162">Yayınla</span><span class="sxs-lookup"><span data-stu-id="8ba73-162">POST</span></span> 
- <span data-ttu-id="8ba73-163">SILME</span><span class="sxs-lookup"><span data-stu-id="8ba73-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="8ba73-164">-RequestBody</span></span>
<span data-ttu-id="8ba73-165">İş gönderme ve gönderme eylemlerinin gövdesinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="8ba73-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba73-166">-ResourceGroupName</span></span>
<span data-ttu-id="8ba73-167">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-167">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-168">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8ba73-168">-StartTime</span></span>
<span data-ttu-id="8ba73-169">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-170">-URI</span><span class="sxs-lookup"><span data-stu-id="8ba73-170">-Uri</span></span>
<span data-ttu-id="8ba73-171">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-172">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ba73-172">-Confirm</span></span>
<span data-ttu-id="8ba73-173">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ba73-173">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba73-174">-WhatIf</span></span>
<span data-ttu-id="8ba73-175">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ba73-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba73-176">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ba73-176">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba73-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba73-177">CommonParameters</span></span>
<span data-ttu-id="8ba73-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ba73-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba73-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba73-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba73-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ba73-180">INPUTS</span></span>

### <span data-ttu-id="8ba73-181">System. String</span><span class="sxs-lookup"><span data-stu-id="8ba73-181">System.String</span></span>

### <span data-ttu-id="8ba73-182">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ba73-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8ba73-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ba73-183">OUTPUTS</span></span>

### <span data-ttu-id="8ba73-184">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8ba73-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="8ba73-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ba73-185">NOTES</span></span>

## <span data-ttu-id="8ba73-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ba73-186">RELATED LINKS</span></span>

[<span data-ttu-id="8ba73-187">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba73-187">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8ba73-188">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-188">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8ba73-189">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-189">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8ba73-190">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-190">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="8ba73-191">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-191">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="8ba73-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba73-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8ba73-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="8ba73-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="8ba73-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="8ba73-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


