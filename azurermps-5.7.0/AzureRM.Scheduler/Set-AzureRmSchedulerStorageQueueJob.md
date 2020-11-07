---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: d93ceb91ded5161dc962f902434cefe0f2070ae5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762141"
---
# <span data-ttu-id="4fa90-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="4fa90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa90-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa90-103">Depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fa90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fa90-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fa90-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa90-106">**Set-AzureRmSchedulerStorageQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="4fa90-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4fa90-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="4fa90-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="4fa90-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4fa90-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4fa90-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4fa90-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4fa90-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fa90-111">EXAMPLES</span></span>

## <span data-ttu-id="4fa90-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fa90-112">PARAMETERS</span></span>

### <span data-ttu-id="4fa90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa90-113">-DefaultProfile</span></span>
<span data-ttu-id="4fa90-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fa90-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa90-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="4fa90-115">-EndTime</span></span>
<span data-ttu-id="4fa90-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4fa90-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fa90-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4fa90-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4fa90-118">-ErrorActionType</span></span>
<span data-ttu-id="4fa90-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4fa90-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4fa90-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fa90-121">Http</span><span class="sxs-lookup"><span data-stu-id="4fa90-121">Http</span></span> 
- <span data-ttu-id="4fa90-122">Https</span><span class="sxs-lookup"><span data-stu-id="4fa90-122">Https</span></span> 
- <span data-ttu-id="4fa90-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4fa90-123">StorageQueue</span></span> 
- <span data-ttu-id="4fa90-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4fa90-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4fa90-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4fa90-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="4fa90-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4fa90-126">-ExecutionCount</span></span>
<span data-ttu-id="4fa90-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4fa90-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4fa90-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="4fa90-129">-Frequency</span></span>
<span data-ttu-id="4fa90-130">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="4fa90-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4fa90-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fa90-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="4fa90-132">Minute</span></span> 
- <span data-ttu-id="4fa90-133">Saati</span><span class="sxs-lookup"><span data-stu-id="4fa90-133">Hour</span></span> 
- <span data-ttu-id="4fa90-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="4fa90-134">Day</span></span> 
- <span data-ttu-id="4fa90-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="4fa90-135">Week</span></span> 
- <span data-ttu-id="4fa90-136">Ay</span><span class="sxs-lookup"><span data-stu-id="4fa90-136">Month</span></span>

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

### <span data-ttu-id="4fa90-137">-Aralık</span><span class="sxs-lookup"><span data-stu-id="4fa90-137">-Interval</span></span>
<span data-ttu-id="4fa90-138">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="4fa90-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4fa90-139">-JobCollectionName</span></span>
<span data-ttu-id="4fa90-140">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="4fa90-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="4fa90-141">-JobName</span></span>
<span data-ttu-id="4fa90-142">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4fa90-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="4fa90-143">-JobState</span></span>
<span data-ttu-id="4fa90-144">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-144">Specifies the state of the job.</span></span>
<span data-ttu-id="4fa90-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4fa90-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fa90-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="4fa90-146">Enabled</span></span> 
- <span data-ttu-id="4fa90-147">DISABLED</span><span class="sxs-lookup"><span data-stu-id="4fa90-147">Disabled</span></span>

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

### <span data-ttu-id="4fa90-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa90-148">-ResourceGroupName</span></span>
<span data-ttu-id="4fa90-149">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4fa90-150">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4fa90-150">-StartTime</span></span>
<span data-ttu-id="4fa90-151">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="4fa90-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="4fa90-152">-StorageQueueAccount</span></span>
<span data-ttu-id="4fa90-153">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa90-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="4fa90-154">-StorageQueueMessage</span></span>
<span data-ttu-id="4fa90-155">Depolama işi için bir kuyruk iletisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-155">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="4fa90-156">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="4fa90-156">-StorageQueueName</span></span>
<span data-ttu-id="4fa90-157">Bir depolama sırası adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa90-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="4fa90-158">-StorageSASToken</span></span>
<span data-ttu-id="4fa90-159">Depolama sırası için paylaşılan bir Access imza belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa90-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fa90-160">-Confirm</span></span>
<span data-ttu-id="4fa90-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fa90-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa90-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa90-162">-WhatIf</span></span>
<span data-ttu-id="4fa90-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fa90-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fa90-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fa90-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa90-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa90-165">CommonParameters</span></span>
<span data-ttu-id="4fa90-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fa90-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa90-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa90-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa90-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fa90-168">INPUTS</span></span>

### <span data-ttu-id="4fa90-169">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4fa90-169">None</span></span>
<span data-ttu-id="4fa90-170">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4fa90-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fa90-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fa90-171">OUTPUTS</span></span>

### <span data-ttu-id="4fa90-172">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4fa90-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4fa90-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fa90-173">NOTES</span></span>

## <span data-ttu-id="4fa90-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fa90-174">RELATED LINKS</span></span>

[<span data-ttu-id="4fa90-175">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4fa90-176">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa90-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa90-177">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4fa90-178">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4fa90-179">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-179">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4fa90-180">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-180">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4fa90-181">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4fa90-181">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4fa90-182">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-182">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4fa90-183">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4fa90-183">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


