---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2debabbcd4ae9b5418436e7846e8490926f37b1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590650"
---
# <span data-ttu-id="79314-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="79314-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="79314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79314-102">SYNOPSIS</span></span>
<span data-ttu-id="79314-103">Bir Zamanlayıcı HTTP işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79314-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79314-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79314-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79314-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79314-105">DESCRIPTION</span></span>
<span data-ttu-id="79314-106">**Set-AzureRmSchedulerHttpJob** cmdlet 'ı, Azure Zamanlayıcısı 'NDA bir http işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79314-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="79314-107">Bu cmdlet, *Erroractiontype* ve *HttpAuthenticationType* parametrelerini temel alan dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="79314-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="79314-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="79314-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="79314-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="79314-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="79314-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="79314-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="79314-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79314-111">EXAMPLES</span></span>

## <span data-ttu-id="79314-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79314-112">PARAMETERS</span></span>

### <span data-ttu-id="79314-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="79314-113">-EndTime</span></span>
<span data-ttu-id="79314-114">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="79314-115">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79314-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="79314-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="79314-116">-ErrorActionType</span></span>
<span data-ttu-id="79314-117">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="79314-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79314-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79314-119">Http</span><span class="sxs-lookup"><span data-stu-id="79314-119">Http</span></span> 
- <span data-ttu-id="79314-120">Https</span><span class="sxs-lookup"><span data-stu-id="79314-120">Https</span></span> 
- <span data-ttu-id="79314-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="79314-121">StorageQueue</span></span> 
- <span data-ttu-id="79314-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="79314-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="79314-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="79314-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="79314-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="79314-124">-ExecutionCount</span></span>
<span data-ttu-id="79314-125">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="79314-126">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="79314-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="79314-127">Frekans</span><span class="sxs-lookup"><span data-stu-id="79314-127">-Frequency</span></span>
<span data-ttu-id="79314-128">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-128">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="79314-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79314-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79314-130">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="79314-130">Minute</span></span> 
- <span data-ttu-id="79314-131">Saati</span><span class="sxs-lookup"><span data-stu-id="79314-131">Hour</span></span> 
- <span data-ttu-id="79314-132">Günündeki</span><span class="sxs-lookup"><span data-stu-id="79314-132">Day</span></span> 
- <span data-ttu-id="79314-133">Haftada</span><span class="sxs-lookup"><span data-stu-id="79314-133">Week</span></span> 
- <span data-ttu-id="79314-134">Ay</span><span class="sxs-lookup"><span data-stu-id="79314-134">Month</span></span>

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

### <span data-ttu-id="79314-135">-Üstbilgiler</span><span class="sxs-lookup"><span data-stu-id="79314-135">-Headers</span></span>
<span data-ttu-id="79314-136">Üst bilgiler içeren bir karma tablo belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="79314-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="79314-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="79314-138">HTTP kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="79314-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79314-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79314-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="79314-140">None</span></span> 
- <span data-ttu-id="79314-141">Mc</span><span class="sxs-lookup"><span data-stu-id="79314-141">ClientCertificate</span></span> 
- <span data-ttu-id="79314-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="79314-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="79314-143">Ana</span><span class="sxs-lookup"><span data-stu-id="79314-143">Basic</span></span>

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

### <span data-ttu-id="79314-144">-Aralık</span><span class="sxs-lookup"><span data-stu-id="79314-144">-Interval</span></span>
<span data-ttu-id="79314-145">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="79314-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="79314-146">-JobCollectionName</span></span>
<span data-ttu-id="79314-147">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="79314-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="79314-148">-JobName</span></span>
<span data-ttu-id="79314-149">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-149">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="79314-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="79314-150">-JobState</span></span>
<span data-ttu-id="79314-151">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-151">Specifies the state of the job.</span></span>
<span data-ttu-id="79314-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79314-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79314-153">Etkin</span><span class="sxs-lookup"><span data-stu-id="79314-153">Enabled</span></span> 
- <span data-ttu-id="79314-154">DISABLED</span><span class="sxs-lookup"><span data-stu-id="79314-154">Disabled</span></span>

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

### <span data-ttu-id="79314-155">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="79314-155">-Method</span></span>
<span data-ttu-id="79314-156">Bu işin eylem türlerinin yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-156">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="79314-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="79314-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79314-158">Al</span><span class="sxs-lookup"><span data-stu-id="79314-158">GET</span></span> 
- <span data-ttu-id="79314-159">KOYUL</span><span class="sxs-lookup"><span data-stu-id="79314-159">PUT</span></span> 
- <span data-ttu-id="79314-160">Yayınla</span><span class="sxs-lookup"><span data-stu-id="79314-160">POST</span></span> 
- <span data-ttu-id="79314-161">SILME</span><span class="sxs-lookup"><span data-stu-id="79314-161">DELETE</span></span>

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

### <span data-ttu-id="79314-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="79314-162">-RequestBody</span></span>
<span data-ttu-id="79314-163">İş gönderme ve gönderme eylemlerinin gövdesinin değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="79314-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79314-164">-ResourceGroupName</span></span>
<span data-ttu-id="79314-165">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="79314-166">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="79314-166">-StartTime</span></span>
<span data-ttu-id="79314-167">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="79314-168">-URI</span><span class="sxs-lookup"><span data-stu-id="79314-168">-Uri</span></span>
<span data-ttu-id="79314-169">İş eyleminin URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79314-169">Specifies a URI for the job action.</span></span>

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

### <span data-ttu-id="79314-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="79314-170">-Confirm</span></span>
<span data-ttu-id="79314-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79314-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79314-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79314-172">-WhatIf</span></span>
<span data-ttu-id="79314-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79314-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79314-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79314-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79314-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79314-175">-DefaultProfile</span></span>
<span data-ttu-id="79314-176">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79314-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79314-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79314-177">CommonParameters</span></span>
<span data-ttu-id="79314-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79314-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79314-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79314-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79314-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79314-180">INPUTS</span></span>

## <span data-ttu-id="79314-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79314-181">OUTPUTS</span></span>

### <span data-ttu-id="79314-182">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="79314-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="79314-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79314-183">NOTES</span></span>

## <span data-ttu-id="79314-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79314-184">RELATED LINKS</span></span>

[<span data-ttu-id="79314-185">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="79314-185">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="79314-186">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="79314-186">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="79314-187">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="79314-187">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="79314-188">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="79314-188">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="79314-189">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="79314-189">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="79314-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="79314-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="79314-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="79314-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="79314-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="79314-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="79314-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="79314-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


