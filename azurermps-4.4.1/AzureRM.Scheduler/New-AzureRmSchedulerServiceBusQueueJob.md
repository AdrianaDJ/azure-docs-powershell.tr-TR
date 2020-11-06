---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: a61d745cb748d27baf7b07b6b4389077e50aaa24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593011"
---
# <span data-ttu-id="6d236-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d236-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="6d236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d236-102">SYNOPSIS</span></span>
<span data-ttu-id="6d236-103">Hizmet veri yolu sıra işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d236-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d236-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d236-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d236-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d236-105">DESCRIPTION</span></span>
<span data-ttu-id="6d236-106">**New-AzureRmSchedulerServiceBusQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir hizmet veri yolu kuyruğu işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d236-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="6d236-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="6d236-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="6d236-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6d236-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="6d236-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="6d236-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d236-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="6d236-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d236-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d236-111">EXAMPLES</span></span>

## <span data-ttu-id="6d236-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d236-112">PARAMETERS</span></span>

### <span data-ttu-id="6d236-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="6d236-113">-EndTime</span></span>
<span data-ttu-id="6d236-114">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="6d236-115">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d236-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="6d236-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="6d236-116">-ErrorActionType</span></span>
<span data-ttu-id="6d236-117">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="6d236-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d236-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d236-119">Http</span><span class="sxs-lookup"><span data-stu-id="6d236-119">Http</span></span> 
- <span data-ttu-id="6d236-120">Https</span><span class="sxs-lookup"><span data-stu-id="6d236-120">Https</span></span> 
- <span data-ttu-id="6d236-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="6d236-121">StorageQueue</span></span> 
- <span data-ttu-id="6d236-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6d236-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="6d236-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6d236-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="6d236-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="6d236-124">-ExecutionCount</span></span>
<span data-ttu-id="6d236-125">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="6d236-126">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="6d236-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="6d236-127">Frekans</span><span class="sxs-lookup"><span data-stu-id="6d236-127">-Frequency</span></span>
<span data-ttu-id="6d236-128">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="6d236-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d236-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d236-130">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="6d236-130">Minute</span></span> 
- <span data-ttu-id="6d236-131">Saati</span><span class="sxs-lookup"><span data-stu-id="6d236-131">Hour</span></span> 
- <span data-ttu-id="6d236-132">Günündeki</span><span class="sxs-lookup"><span data-stu-id="6d236-132">Day</span></span> 
- <span data-ttu-id="6d236-133">Haftada</span><span class="sxs-lookup"><span data-stu-id="6d236-133">Week</span></span> 
- <span data-ttu-id="6d236-134">Ay</span><span class="sxs-lookup"><span data-stu-id="6d236-134">Month</span></span>

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

### <span data-ttu-id="6d236-135">-Aralık</span><span class="sxs-lookup"><span data-stu-id="6d236-135">-Interval</span></span>
<span data-ttu-id="6d236-136">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="6d236-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="6d236-137">-JobCollectionName</span></span>
<span data-ttu-id="6d236-138">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="6d236-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="6d236-139">-JobName</span></span>
<span data-ttu-id="6d236-140">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="6d236-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="6d236-141">-JobState</span></span>
<span data-ttu-id="6d236-142">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-142">Specifies the state of the job.</span></span>
<span data-ttu-id="6d236-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d236-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d236-144">Etkin</span><span class="sxs-lookup"><span data-stu-id="6d236-144">Enabled</span></span> 
- <span data-ttu-id="6d236-145">DISABLED</span><span class="sxs-lookup"><span data-stu-id="6d236-145">Disabled</span></span>

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

### <span data-ttu-id="6d236-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d236-146">-ResourceGroupName</span></span>
<span data-ttu-id="6d236-147">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="6d236-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="6d236-148">-ServiceBusMessage</span></span>
<span data-ttu-id="6d236-149">Hizmet veri yolu sıra iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-149">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="6d236-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="6d236-151">Bir hizmet veri yolu ad alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-151">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-152">-Servicebussıraadı</span><span class="sxs-lookup"><span data-stu-id="6d236-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="6d236-153">Hizmet veri yolu sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-153">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="6d236-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="6d236-155">Paylaşılan bir Access imza anahtarı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="6d236-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="6d236-157">Paylaşılan bir Access imza anahtarı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="6d236-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="6d236-159">Hizmet veri yolu aktarım türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="6d236-160">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6d236-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d236-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="6d236-161">NetMessaging</span></span> 
- <span data-ttu-id="6d236-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="6d236-162">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d236-163">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="6d236-163">-StartTime</span></span>
<span data-ttu-id="6d236-164">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d236-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="6d236-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d236-165">-Confirm</span></span>
<span data-ttu-id="6d236-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d236-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d236-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d236-167">-WhatIf</span></span>
<span data-ttu-id="6d236-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d236-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d236-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d236-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d236-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d236-170">-DefaultProfile</span></span>
<span data-ttu-id="6d236-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d236-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d236-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d236-172">CommonParameters</span></span>
<span data-ttu-id="6d236-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d236-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d236-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d236-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d236-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d236-175">INPUTS</span></span>

## <span data-ttu-id="6d236-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d236-176">OUTPUTS</span></span>

### <span data-ttu-id="6d236-177">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6d236-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="6d236-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d236-178">NOTES</span></span>

## <span data-ttu-id="6d236-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d236-179">RELATED LINKS</span></span>

[<span data-ttu-id="6d236-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6d236-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="6d236-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6d236-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6d236-182">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6d236-182">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6d236-183">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d236-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="6d236-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="6d236-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="6d236-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="6d236-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="6d236-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d236-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="6d236-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="6d236-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="6d236-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="6d236-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


