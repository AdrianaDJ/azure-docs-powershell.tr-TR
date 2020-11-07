---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: c752b4fd96ec001467e051fc01be24f592241182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764523"
---
# <span data-ttu-id="d995b-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d995b-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="d995b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d995b-102">SYNOPSIS</span></span>
<span data-ttu-id="d995b-103">Depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d995b-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d995b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d995b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d995b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d995b-105">DESCRIPTION</span></span>
<span data-ttu-id="d995b-106">**Set-AzureRmSchedulerStorageQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d995b-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="d995b-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="d995b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="d995b-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d995b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="d995b-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="d995b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d995b-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="d995b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d995b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d995b-111">EXAMPLES</span></span>

## <span data-ttu-id="d995b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d995b-112">PARAMETERS</span></span>

### <span data-ttu-id="d995b-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d995b-113">-EndTime</span></span>
<span data-ttu-id="d995b-114">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d995b-115">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d995b-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d995b-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d995b-116">-ErrorActionType</span></span>
<span data-ttu-id="d995b-117">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d995b-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d995b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d995b-119">Http</span><span class="sxs-lookup"><span data-stu-id="d995b-119">Http</span></span> 
- <span data-ttu-id="d995b-120">Https</span><span class="sxs-lookup"><span data-stu-id="d995b-120">Https</span></span> 
- <span data-ttu-id="d995b-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d995b-121">StorageQueue</span></span> 
- <span data-ttu-id="d995b-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d995b-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="d995b-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d995b-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d995b-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d995b-124">-ExecutionCount</span></span>
<span data-ttu-id="d995b-125">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d995b-126">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="d995b-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d995b-127">Frekans</span><span class="sxs-lookup"><span data-stu-id="d995b-127">-Frequency</span></span>
<span data-ttu-id="d995b-128">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="d995b-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d995b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d995b-130">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="d995b-130">Minute</span></span> 
- <span data-ttu-id="d995b-131">Saati</span><span class="sxs-lookup"><span data-stu-id="d995b-131">Hour</span></span> 
- <span data-ttu-id="d995b-132">Günündeki</span><span class="sxs-lookup"><span data-stu-id="d995b-132">Day</span></span> 
- <span data-ttu-id="d995b-133">Haftada</span><span class="sxs-lookup"><span data-stu-id="d995b-133">Week</span></span> 
- <span data-ttu-id="d995b-134">Ay</span><span class="sxs-lookup"><span data-stu-id="d995b-134">Month</span></span>

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

### <span data-ttu-id="d995b-135">-Aralık</span><span class="sxs-lookup"><span data-stu-id="d995b-135">-Interval</span></span>
<span data-ttu-id="d995b-136">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d995b-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d995b-137">-JobCollectionName</span></span>
<span data-ttu-id="d995b-138">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d995b-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="d995b-139">-JobName</span></span>
<span data-ttu-id="d995b-140">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d995b-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="d995b-141">-JobState</span></span>
<span data-ttu-id="d995b-142">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-142">Specifies the state of the job.</span></span>
<span data-ttu-id="d995b-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d995b-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d995b-144">Etkin</span><span class="sxs-lookup"><span data-stu-id="d995b-144">Enabled</span></span> 
- <span data-ttu-id="d995b-145">DISABLED</span><span class="sxs-lookup"><span data-stu-id="d995b-145">Disabled</span></span>

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

### <span data-ttu-id="d995b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d995b-146">-ResourceGroupName</span></span>
<span data-ttu-id="d995b-147">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d995b-148">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d995b-148">-StartTime</span></span>
<span data-ttu-id="d995b-149">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d995b-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="d995b-150">-StorageQueueAccount</span></span>
<span data-ttu-id="d995b-151">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-151">Specifies a storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d995b-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="d995b-152">-StorageQueueMessage</span></span>
<span data-ttu-id="d995b-153">Depolama işi için bir kuyruk iletisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-153">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="d995b-154">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="d995b-154">-StorageQueueName</span></span>
<span data-ttu-id="d995b-155">Bir depolama sırası adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-155">Specifies a storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d995b-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="d995b-156">-StorageSASToken</span></span>
<span data-ttu-id="d995b-157">Depolama sırası için paylaşılan bir Access imza belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="d995b-157">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d995b-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="d995b-158">-Confirm</span></span>
<span data-ttu-id="d995b-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d995b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d995b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d995b-160">-WhatIf</span></span>
<span data-ttu-id="d995b-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d995b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d995b-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d995b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d995b-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d995b-163">-DefaultProfile</span></span>
<span data-ttu-id="d995b-164">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d995b-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d995b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d995b-165">CommonParameters</span></span>
<span data-ttu-id="d995b-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d995b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d995b-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d995b-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d995b-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d995b-168">INPUTS</span></span>

## <span data-ttu-id="d995b-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d995b-169">OUTPUTS</span></span>

### <span data-ttu-id="d995b-170">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d995b-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d995b-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d995b-171">NOTES</span></span>

## <span data-ttu-id="d995b-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d995b-172">RELATED LINKS</span></span>

[<span data-ttu-id="d995b-173">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d995b-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d995b-174">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d995b-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d995b-175">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d995b-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d995b-176">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d995b-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d995b-177">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d995b-177">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d995b-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d995b-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d995b-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d995b-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d995b-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d995b-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d995b-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d995b-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

