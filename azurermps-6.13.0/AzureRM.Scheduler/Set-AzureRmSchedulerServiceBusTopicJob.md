---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 6f1e92654c038cccf49e32b489ad5face70ae011
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765080"
---
# <span data-ttu-id="4c316-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4c316-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="4c316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c316-102">SYNOPSIS</span></span>
<span data-ttu-id="4c316-103">Hizmet veri yolu konu işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c316-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c316-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c316-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c316-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c316-105">DESCRIPTION</span></span>
<span data-ttu-id="4c316-106">**Set-AzureRmSchedulerServiceBusTopicJob** cmdlet 'ı, Azure Zamanlayıcısı 'ndaki bir Service Bus konu işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c316-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>
<span data-ttu-id="4c316-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4c316-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="4c316-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c316-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="4c316-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4c316-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4c316-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4c316-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4c316-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c316-111">EXAMPLES</span></span>

## <span data-ttu-id="4c316-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c316-112">PARAMETERS</span></span>

### <span data-ttu-id="4c316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c316-113">-DefaultProfile</span></span>
<span data-ttu-id="4c316-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c316-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c316-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="4c316-115">-EndTime</span></span>
<span data-ttu-id="4c316-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4c316-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c316-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4c316-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4c316-118">-ErrorActionType</span></span>
<span data-ttu-id="4c316-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4c316-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c316-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c316-121">Http</span><span class="sxs-lookup"><span data-stu-id="4c316-121">Http</span></span> 
- <span data-ttu-id="4c316-122">Https</span><span class="sxs-lookup"><span data-stu-id="4c316-122">Https</span></span> 
- <span data-ttu-id="4c316-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4c316-123">StorageQueue</span></span> 
- <span data-ttu-id="4c316-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4c316-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4c316-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4c316-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="4c316-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4c316-126">-ExecutionCount</span></span>
<span data-ttu-id="4c316-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4c316-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="4c316-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4c316-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="4c316-129">-Frequency</span></span>
<span data-ttu-id="4c316-130">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="4c316-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c316-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c316-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="4c316-132">Minute</span></span> 
- <span data-ttu-id="4c316-133">Saati</span><span class="sxs-lookup"><span data-stu-id="4c316-133">Hour</span></span> 
- <span data-ttu-id="4c316-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="4c316-134">Day</span></span> 
- <span data-ttu-id="4c316-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="4c316-135">Week</span></span> 
- <span data-ttu-id="4c316-136">Ay</span><span class="sxs-lookup"><span data-stu-id="4c316-136">Month</span></span>

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

### <span data-ttu-id="4c316-137">-Aralık</span><span class="sxs-lookup"><span data-stu-id="4c316-137">-Interval</span></span>
<span data-ttu-id="4c316-138">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="4c316-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4c316-139">-JobCollectionName</span></span>
<span data-ttu-id="4c316-140">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="4c316-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="4c316-141">-JobName</span></span>
<span data-ttu-id="4c316-142">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4c316-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="4c316-143">-JobState</span></span>
<span data-ttu-id="4c316-144">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-144">Specifies the state of the job.</span></span>
<span data-ttu-id="4c316-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c316-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c316-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="4c316-146">Enabled</span></span> 
- <span data-ttu-id="4c316-147">DISABLED</span><span class="sxs-lookup"><span data-stu-id="4c316-147">Disabled</span></span>

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

### <span data-ttu-id="4c316-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c316-148">-ResourceGroupName</span></span>
<span data-ttu-id="4c316-149">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4c316-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="4c316-150">-ServiceBusMessage</span></span>
<span data-ttu-id="4c316-151">Hizmet veri yolu konu iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-151">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="4c316-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="4c316-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="4c316-153">Bir hizmet veri yolu ad alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="4c316-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="4c316-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="4c316-155">Paylaşılan bir Access imza anahtarı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="4c316-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="4c316-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="4c316-157">Paylaşılan bir Access imza anahtarı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="4c316-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="4c316-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="4c316-159">Service Bus konu yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-159">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="4c316-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="4c316-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="4c316-161">Hizmet veri yolu aktarım türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="4c316-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c316-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c316-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="4c316-163">NetMessaging</span></span>
- <span data-ttu-id="4c316-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="4c316-164">AMQP</span></span>

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

### <span data-ttu-id="4c316-165">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4c316-165">-StartTime</span></span>
<span data-ttu-id="4c316-166">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c316-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="4c316-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c316-167">-Confirm</span></span>
<span data-ttu-id="4c316-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c316-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c316-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c316-169">-WhatIf</span></span>
<span data-ttu-id="4c316-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c316-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c316-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c316-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c316-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c316-172">CommonParameters</span></span>
<span data-ttu-id="4c316-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c316-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c316-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c316-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c316-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c316-175">INPUTS</span></span>

### <span data-ttu-id="4c316-176">System. String</span><span class="sxs-lookup"><span data-stu-id="4c316-176">System.String</span></span>

## <span data-ttu-id="4c316-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c316-177">OUTPUTS</span></span>

### <span data-ttu-id="4c316-178">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4c316-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4c316-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c316-179">NOTES</span></span>

## <span data-ttu-id="4c316-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c316-180">RELATED LINKS</span></span>

[<span data-ttu-id="4c316-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4c316-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4c316-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4c316-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4c316-183">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c316-183">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4c316-184">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4c316-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4c316-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c316-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4c316-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4c316-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4c316-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4c316-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4c316-188">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c316-188">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4c316-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c316-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


