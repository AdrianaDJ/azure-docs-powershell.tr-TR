---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587172"
---
# <span data-ttu-id="50db9-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="50db9-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="50db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50db9-102">SYNOPSIS</span></span>
<span data-ttu-id="50db9-103">Hizmet veri yolu sıra işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50db9-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50db9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50db9-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50db9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50db9-105">DESCRIPTION</span></span>
<span data-ttu-id="50db9-106">**New-AzureRmSchedulerServiceBusQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir hizmet veri yolu kuyruğu işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50db9-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="50db9-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="50db9-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="50db9-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="50db9-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="50db9-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="50db9-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="50db9-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="50db9-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="50db9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50db9-111">EXAMPLES</span></span>

## <span data-ttu-id="50db9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50db9-112">PARAMETERS</span></span>

### <span data-ttu-id="50db9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50db9-113">-DefaultProfile</span></span>
<span data-ttu-id="50db9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50db9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50db9-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="50db9-115">-EndTime</span></span>
<span data-ttu-id="50db9-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="50db9-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="50db9-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="50db9-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="50db9-118">-ErrorActionType</span></span>
<span data-ttu-id="50db9-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="50db9-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50db9-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50db9-121">Http</span><span class="sxs-lookup"><span data-stu-id="50db9-121">Http</span></span> 
- <span data-ttu-id="50db9-122">Https</span><span class="sxs-lookup"><span data-stu-id="50db9-122">Https</span></span> 
- <span data-ttu-id="50db9-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="50db9-123">StorageQueue</span></span> 
- <span data-ttu-id="50db9-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="50db9-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="50db9-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="50db9-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="50db9-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="50db9-126">-ExecutionCount</span></span>
<span data-ttu-id="50db9-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="50db9-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="50db9-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="50db9-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="50db9-129">-Frequency</span></span>
<span data-ttu-id="50db9-130">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="50db9-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50db9-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50db9-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="50db9-132">Minute</span></span> 
- <span data-ttu-id="50db9-133">Saati</span><span class="sxs-lookup"><span data-stu-id="50db9-133">Hour</span></span> 
- <span data-ttu-id="50db9-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="50db9-134">Day</span></span> 
- <span data-ttu-id="50db9-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="50db9-135">Week</span></span> 
- <span data-ttu-id="50db9-136">Ay</span><span class="sxs-lookup"><span data-stu-id="50db9-136">Month</span></span>

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

### <span data-ttu-id="50db9-137">-Aralık</span><span class="sxs-lookup"><span data-stu-id="50db9-137">-Interval</span></span>
<span data-ttu-id="50db9-138">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="50db9-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="50db9-139">-JobCollectionName</span></span>
<span data-ttu-id="50db9-140">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="50db9-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="50db9-141">-JobName</span></span>
<span data-ttu-id="50db9-142">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="50db9-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="50db9-143">-JobState</span></span>
<span data-ttu-id="50db9-144">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-144">Specifies the state of the job.</span></span>
<span data-ttu-id="50db9-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50db9-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50db9-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="50db9-146">Enabled</span></span> 
- <span data-ttu-id="50db9-147">DISABLED</span><span class="sxs-lookup"><span data-stu-id="50db9-147">Disabled</span></span>

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

### <span data-ttu-id="50db9-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50db9-148">-ResourceGroupName</span></span>
<span data-ttu-id="50db9-149">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="50db9-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="50db9-150">-ServiceBusMessage</span></span>
<span data-ttu-id="50db9-151">Hizmet veri yolu sıra iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="50db9-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="50db9-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="50db9-153">Bir hizmet veri yolu ad alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="50db9-154">-Servicebussıraadı</span><span class="sxs-lookup"><span data-stu-id="50db9-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="50db9-155">Hizmet veri yolu sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="50db9-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="50db9-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="50db9-157">Paylaşılan bir Access imza anahtarı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="50db9-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="50db9-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="50db9-159">Paylaşılan bir Access imza anahtarı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="50db9-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="50db9-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="50db9-161">Hizmet veri yolu aktarım türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="50db9-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50db9-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50db9-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="50db9-163">NetMessaging</span></span> 
- <span data-ttu-id="50db9-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="50db9-164">AMQP</span></span>

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

### <span data-ttu-id="50db9-165">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="50db9-165">-StartTime</span></span>
<span data-ttu-id="50db9-166">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="50db9-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="50db9-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="50db9-167">-Confirm</span></span>
<span data-ttu-id="50db9-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50db9-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50db9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50db9-169">-WhatIf</span></span>
<span data-ttu-id="50db9-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50db9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50db9-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50db9-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50db9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50db9-172">CommonParameters</span></span>
<span data-ttu-id="50db9-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50db9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50db9-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50db9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50db9-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50db9-175">INPUTS</span></span>

### <span data-ttu-id="50db9-176">System. String</span><span class="sxs-lookup"><span data-stu-id="50db9-176">System.String</span></span>

## <span data-ttu-id="50db9-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50db9-177">OUTPUTS</span></span>

### <span data-ttu-id="50db9-178">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="50db9-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="50db9-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50db9-179">NOTES</span></span>

## <span data-ttu-id="50db9-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50db9-180">RELATED LINKS</span></span>

[<span data-ttu-id="50db9-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="50db9-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="50db9-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="50db9-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="50db9-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="50db9-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="50db9-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="50db9-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="50db9-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="50db9-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="50db9-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="50db9-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="50db9-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="50db9-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="50db9-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="50db9-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="50db9-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="50db9-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


