---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2810a73e54151d8227a115aa71f486d09811def8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588357"
---
# <span data-ttu-id="0180f-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0180f-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="0180f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0180f-102">SYNOPSIS</span></span>
<span data-ttu-id="0180f-103">Bir Zamanlayıcı HTTP işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0180f-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0180f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0180f-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0180f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0180f-105">DESCRIPTION</span></span>
<span data-ttu-id="0180f-106">**Set-AzureRmSchedulerHttpJob** cmdlet 'ı, Azure Zamanlayıcısı 'NDA bir http işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0180f-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="0180f-107">Bu cmdlet, *Erroractiontype* ve *HttpAuthenticationType* parametrelerini temel alan dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0180f-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="0180f-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0180f-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="0180f-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="0180f-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0180f-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="0180f-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0180f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0180f-111">EXAMPLES</span></span>

## <span data-ttu-id="0180f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0180f-112">PARAMETERS</span></span>

### <span data-ttu-id="0180f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0180f-113">-DefaultProfile</span></span>
<span data-ttu-id="0180f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0180f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0180f-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="0180f-115">-EndTime</span></span>
<span data-ttu-id="0180f-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="0180f-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0180f-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0180f-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="0180f-118">-ErrorActionType</span></span>
<span data-ttu-id="0180f-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="0180f-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0180f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0180f-121">Http</span><span class="sxs-lookup"><span data-stu-id="0180f-121">Http</span></span> 
- <span data-ttu-id="0180f-122">Https</span><span class="sxs-lookup"><span data-stu-id="0180f-122">Https</span></span> 
- <span data-ttu-id="0180f-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="0180f-123">StorageQueue</span></span> 
- <span data-ttu-id="0180f-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0180f-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="0180f-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0180f-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="0180f-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="0180f-126">-ExecutionCount</span></span>
<span data-ttu-id="0180f-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="0180f-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="0180f-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="0180f-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="0180f-129">-Frequency</span></span>
<span data-ttu-id="0180f-130">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="0180f-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0180f-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0180f-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="0180f-132">Minute</span></span> 
- <span data-ttu-id="0180f-133">Saati</span><span class="sxs-lookup"><span data-stu-id="0180f-133">Hour</span></span> 
- <span data-ttu-id="0180f-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="0180f-134">Day</span></span> 
- <span data-ttu-id="0180f-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="0180f-135">Week</span></span> 
- <span data-ttu-id="0180f-136">Ay</span><span class="sxs-lookup"><span data-stu-id="0180f-136">Month</span></span>

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

### <span data-ttu-id="0180f-137">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="0180f-137">-Headers</span></span>
<span data-ttu-id="0180f-138">Üst bilgiler içeren bir karma tablo belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-138">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="0180f-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0180f-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="0180f-140">HTTP kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="0180f-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0180f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0180f-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0180f-142">None</span></span> 
- <span data-ttu-id="0180f-143">Mc</span><span class="sxs-lookup"><span data-stu-id="0180f-143">ClientCertificate</span></span> 
- <span data-ttu-id="0180f-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="0180f-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="0180f-145">Ana</span><span class="sxs-lookup"><span data-stu-id="0180f-145">Basic</span></span>

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

### <span data-ttu-id="0180f-146">-Aralık</span><span class="sxs-lookup"><span data-stu-id="0180f-146">-Interval</span></span>
<span data-ttu-id="0180f-147">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="0180f-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0180f-148">-JobCollectionName</span></span>
<span data-ttu-id="0180f-149">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="0180f-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="0180f-150">-JobName</span></span>
<span data-ttu-id="0180f-151">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0180f-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="0180f-152">-JobState</span></span>
<span data-ttu-id="0180f-153">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-153">Specifies the state of the job.</span></span>
<span data-ttu-id="0180f-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0180f-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0180f-155">Etkin</span><span class="sxs-lookup"><span data-stu-id="0180f-155">Enabled</span></span> 
- <span data-ttu-id="0180f-156">DISABLED</span><span class="sxs-lookup"><span data-stu-id="0180f-156">Disabled</span></span>

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

### <span data-ttu-id="0180f-157">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="0180f-157">-Method</span></span>
<span data-ttu-id="0180f-158">Bu işin eylem türlerinin yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="0180f-159">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0180f-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0180f-160">Al</span><span class="sxs-lookup"><span data-stu-id="0180f-160">GET</span></span> 
- <span data-ttu-id="0180f-161">KOYUL</span><span class="sxs-lookup"><span data-stu-id="0180f-161">PUT</span></span> 
- <span data-ttu-id="0180f-162">Yayınla</span><span class="sxs-lookup"><span data-stu-id="0180f-162">POST</span></span> 
- <span data-ttu-id="0180f-163">SILME</span><span class="sxs-lookup"><span data-stu-id="0180f-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0180f-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="0180f-164">-RequestBody</span></span>
<span data-ttu-id="0180f-165">İş gönderme ve gönderme eylemlerinin gövdesinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="0180f-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0180f-166">-ResourceGroupName</span></span>
<span data-ttu-id="0180f-167">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="0180f-168">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="0180f-168">-StartTime</span></span>
<span data-ttu-id="0180f-169">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="0180f-170">-URI</span><span class="sxs-lookup"><span data-stu-id="0180f-170">-Uri</span></span>
<span data-ttu-id="0180f-171">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0180f-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0180f-172">-Onay</span><span class="sxs-lookup"><span data-stu-id="0180f-172">-Confirm</span></span>
<span data-ttu-id="0180f-173">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0180f-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0180f-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0180f-174">-WhatIf</span></span>
<span data-ttu-id="0180f-175">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0180f-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0180f-176">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0180f-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0180f-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0180f-177">CommonParameters</span></span>
<span data-ttu-id="0180f-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0180f-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0180f-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0180f-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0180f-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0180f-180">INPUTS</span></span>

### <span data-ttu-id="0180f-181">System. String</span><span class="sxs-lookup"><span data-stu-id="0180f-181">System.String</span></span>

### <span data-ttu-id="0180f-182">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0180f-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0180f-183">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0180f-183">OUTPUTS</span></span>

### <span data-ttu-id="0180f-184">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0180f-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="0180f-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0180f-185">NOTES</span></span>

## <span data-ttu-id="0180f-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0180f-186">RELATED LINKS</span></span>

[<span data-ttu-id="0180f-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0180f-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0180f-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0180f-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0180f-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0180f-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0180f-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0180f-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0180f-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0180f-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="0180f-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0180f-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0180f-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0180f-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0180f-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0180f-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0180f-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0180f-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


