---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2B9FEEDB-09AA-40B6-B42C-F9090F54EB3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 3a4c0cfb2e9ec3b41921e42b793a06163b9a8303
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593010"
---
# <span data-ttu-id="5215e-101">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="5215e-101">New-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="5215e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5215e-102">SYNOPSIS</span></span>
<span data-ttu-id="5215e-103">Service Bus konu işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5215e-103">Creates a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5215e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5215e-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5215e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5215e-105">DESCRIPTION</span></span>
<span data-ttu-id="5215e-106">**New-AzureRmSchedulerServiceBusTopicJob** cmdlet 'ı, Azure Scheduler 'da bir Service Bus konu işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5215e-106">The **New-AzureRmSchedulerServiceBusTopicJob** cmdlet creates a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="5215e-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="5215e-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="5215e-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5215e-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="5215e-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="5215e-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5215e-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="5215e-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5215e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5215e-111">EXAMPLES</span></span>

## <span data-ttu-id="5215e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5215e-112">PARAMETERS</span></span>

### <span data-ttu-id="5215e-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="5215e-113">-EndTime</span></span>
<span data-ttu-id="5215e-114">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="5215e-115">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5215e-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="5215e-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="5215e-116">-ErrorActionType</span></span>
<span data-ttu-id="5215e-117">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="5215e-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5215e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5215e-119">Http</span><span class="sxs-lookup"><span data-stu-id="5215e-119">Http</span></span> 
- <span data-ttu-id="5215e-120">Https</span><span class="sxs-lookup"><span data-stu-id="5215e-120">Https</span></span> 
- <span data-ttu-id="5215e-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="5215e-121">StorageQueue</span></span> 
- <span data-ttu-id="5215e-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="5215e-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="5215e-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="5215e-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="5215e-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="5215e-124">-ExecutionCount</span></span>
<span data-ttu-id="5215e-125">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="5215e-126">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="5215e-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="5215e-127">Frekans</span><span class="sxs-lookup"><span data-stu-id="5215e-127">-Frequency</span></span>
<span data-ttu-id="5215e-128">İş için en yüksek frekansı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="5215e-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5215e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5215e-130">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="5215e-130">Minute</span></span> 
- <span data-ttu-id="5215e-131">Saati</span><span class="sxs-lookup"><span data-stu-id="5215e-131">Hour</span></span> 
- <span data-ttu-id="5215e-132">Günündeki</span><span class="sxs-lookup"><span data-stu-id="5215e-132">Day</span></span> 
- <span data-ttu-id="5215e-133">Haftada</span><span class="sxs-lookup"><span data-stu-id="5215e-133">Week</span></span> 
- <span data-ttu-id="5215e-134">Ay</span><span class="sxs-lookup"><span data-stu-id="5215e-134">Month</span></span>

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

### <span data-ttu-id="5215e-135">-Aralık</span><span class="sxs-lookup"><span data-stu-id="5215e-135">-Interval</span></span>
<span data-ttu-id="5215e-136">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="5215e-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="5215e-137">-JobCollectionName</span></span>
<span data-ttu-id="5215e-138">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="5215e-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="5215e-139">-JobName</span></span>
<span data-ttu-id="5215e-140">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-140">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="5215e-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="5215e-141">-JobState</span></span>
<span data-ttu-id="5215e-142">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-142">Specifies the state of the job.</span></span>
<span data-ttu-id="5215e-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5215e-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5215e-144">Etkin</span><span class="sxs-lookup"><span data-stu-id="5215e-144">Enabled</span></span> 
- <span data-ttu-id="5215e-145">DISABLED</span><span class="sxs-lookup"><span data-stu-id="5215e-145">Disabled</span></span>

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

### <span data-ttu-id="5215e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5215e-146">-ResourceGroupName</span></span>
<span data-ttu-id="5215e-147">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="5215e-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="5215e-148">-ServiceBusMessage</span></span>
<span data-ttu-id="5215e-149">Hizmet veri yolu konu iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="5215e-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5215e-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="5215e-151">Bir hizmet veri yolu ad alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="5215e-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="5215e-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="5215e-153">Paylaşılan bir Access imza anahtarı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="5215e-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="5215e-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="5215e-155">Paylaşılan bir Access imza anahtarı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="5215e-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="5215e-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="5215e-157">Service Bus konu yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="5215e-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="5215e-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="5215e-159">Hizmet veri yolu aktarım türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="5215e-160">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5215e-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5215e-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="5215e-161">NetMessaging</span></span>
- <span data-ttu-id="5215e-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="5215e-162">AMQP</span></span>

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

### <span data-ttu-id="5215e-163">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="5215e-163">-StartTime</span></span>
<span data-ttu-id="5215e-164">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5215e-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="5215e-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="5215e-165">-Confirm</span></span>
<span data-ttu-id="5215e-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5215e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5215e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5215e-167">-WhatIf</span></span>
<span data-ttu-id="5215e-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5215e-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5215e-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5215e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5215e-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5215e-170">-DefaultProfile</span></span>
<span data-ttu-id="5215e-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5215e-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5215e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5215e-172">CommonParameters</span></span>
<span data-ttu-id="5215e-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5215e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5215e-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5215e-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5215e-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5215e-175">INPUTS</span></span>

## <span data-ttu-id="5215e-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5215e-176">OUTPUTS</span></span>

### <span data-ttu-id="5215e-177">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5215e-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="5215e-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5215e-178">NOTES</span></span>

## <span data-ttu-id="5215e-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5215e-179">RELATED LINKS</span></span>

[<span data-ttu-id="5215e-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="5215e-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="5215e-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5215e-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="5215e-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="5215e-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="5215e-183">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="5215e-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="5215e-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="5215e-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="5215e-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="5215e-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="5215e-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="5215e-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="5215e-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="5215e-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="5215e-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="5215e-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


