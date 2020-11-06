---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 6928347ab5d78a25d53636f73413f772b9beea4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594566"
---
# <span data-ttu-id="dac0a-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="dac0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dac0a-102">SYNOPSIS</span></span>
<span data-ttu-id="dac0a-103">Hizmet veri yolu kuyruğu işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dac0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dac0a-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac0a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dac0a-105">DESCRIPTION</span></span>
<span data-ttu-id="dac0a-106">**Set-AzureRmSchedulerServiceBusQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir hizmet veri yolu kuyruğu işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="dac0a-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="dac0a-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="dac0a-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="dac0a-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="dac0a-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dac0a-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="dac0a-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dac0a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dac0a-111">EXAMPLES</span></span>

## <span data-ttu-id="dac0a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dac0a-112">PARAMETERS</span></span>

### <span data-ttu-id="dac0a-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="dac0a-113">-EndTime</span></span>
<span data-ttu-id="dac0a-114">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="dac0a-115">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dac0a-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="dac0a-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="dac0a-116">-ErrorActionType</span></span>
<span data-ttu-id="dac0a-117">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="dac0a-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dac0a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dac0a-119">Http</span><span class="sxs-lookup"><span data-stu-id="dac0a-119">Http</span></span> 
- <span data-ttu-id="dac0a-120">Https</span><span class="sxs-lookup"><span data-stu-id="dac0a-120">Https</span></span> 
- <span data-ttu-id="dac0a-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="dac0a-121">StorageQueue</span></span> 
- <span data-ttu-id="dac0a-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="dac0a-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="dac0a-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="dac0a-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="dac0a-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="dac0a-124">-ExecutionCount</span></span>
<span data-ttu-id="dac0a-125">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="dac0a-126">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="dac0a-127">Frekans</span><span class="sxs-lookup"><span data-stu-id="dac0a-127">-Frequency</span></span>
<span data-ttu-id="dac0a-128">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="dac0a-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dac0a-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dac0a-130">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="dac0a-130">Minute</span></span> 
- <span data-ttu-id="dac0a-131">Saati</span><span class="sxs-lookup"><span data-stu-id="dac0a-131">Hour</span></span> 
- <span data-ttu-id="dac0a-132">Günündeki</span><span class="sxs-lookup"><span data-stu-id="dac0a-132">Day</span></span> 
- <span data-ttu-id="dac0a-133">Haftada</span><span class="sxs-lookup"><span data-stu-id="dac0a-133">Week</span></span> 
- <span data-ttu-id="dac0a-134">Ay</span><span class="sxs-lookup"><span data-stu-id="dac0a-134">Month</span></span>

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

### <span data-ttu-id="dac0a-135">-Aralık</span><span class="sxs-lookup"><span data-stu-id="dac0a-135">-Interval</span></span>
<span data-ttu-id="dac0a-136">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="dac0a-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="dac0a-137">-JobCollectionName</span></span>
<span data-ttu-id="dac0a-138">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="dac0a-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="dac0a-139">-JobName</span></span>
<span data-ttu-id="dac0a-140">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dac0a-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="dac0a-141">-JobState</span></span>
<span data-ttu-id="dac0a-142">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-142">Specifies the state of the job.</span></span>
<span data-ttu-id="dac0a-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dac0a-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dac0a-144">Etkin</span><span class="sxs-lookup"><span data-stu-id="dac0a-144">Enabled</span></span> 
- <span data-ttu-id="dac0a-145">DISABLED</span><span class="sxs-lookup"><span data-stu-id="dac0a-145">Disabled</span></span>

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

### <span data-ttu-id="dac0a-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac0a-146">-ResourceGroupName</span></span>
<span data-ttu-id="dac0a-147">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="dac0a-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="dac0a-148">-ServiceBusMessage</span></span>
<span data-ttu-id="dac0a-149">Hizmet veri yolu sıra iletisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="dac0a-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="dac0a-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="dac0a-151">Bir hizmet veri yolu ad alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="dac0a-152">-Servicebussıraadı</span><span class="sxs-lookup"><span data-stu-id="dac0a-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="dac0a-153">Hizmet veri yolu sırasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="dac0a-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="dac0a-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="dac0a-155">Paylaşılan bir Access imza anahtarı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="dac0a-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="dac0a-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="dac0a-157">Paylaşılan bir Access imza anahtarı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="dac0a-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="dac0a-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="dac0a-159">Hizmet veri yolu aktarım türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="dac0a-160">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dac0a-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dac0a-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="dac0a-161">NetMessaging</span></span> 
- <span data-ttu-id="dac0a-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="dac0a-162">AMQP</span></span>

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

### <span data-ttu-id="dac0a-163">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="dac0a-163">-StartTime</span></span>
<span data-ttu-id="dac0a-164">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="dac0a-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="dac0a-165">-Confirm</span></span>
<span data-ttu-id="dac0a-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dac0a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac0a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac0a-167">-WhatIf</span></span>
<span data-ttu-id="dac0a-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dac0a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dac0a-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dac0a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac0a-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac0a-170">-DefaultProfile</span></span>
<span data-ttu-id="dac0a-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dac0a-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dac0a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac0a-172">CommonParameters</span></span>
<span data-ttu-id="dac0a-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dac0a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac0a-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dac0a-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac0a-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dac0a-175">INPUTS</span></span>

## <span data-ttu-id="dac0a-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dac0a-176">OUTPUTS</span></span>

### <span data-ttu-id="dac0a-177">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dac0a-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="dac0a-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dac0a-178">NOTES</span></span>

## <span data-ttu-id="dac0a-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dac0a-179">RELATED LINKS</span></span>

[<span data-ttu-id="dac0a-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="dac0a-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dac0a-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dac0a-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="dac0a-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="dac0a-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="dac0a-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="dac0a-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="dac0a-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="dac0a-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="dac0a-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="dac0a-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


