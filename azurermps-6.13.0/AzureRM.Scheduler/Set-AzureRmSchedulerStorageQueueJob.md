---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: 68747f616971927ab719ec9ccc8eaf8bd9efc370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592263"
---
# <span data-ttu-id="f8e35-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="f8e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e35-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e35-103">Depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8e35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8e35-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8e35-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8e35-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e35-106">**Set-AzureRmSchedulerStorageQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir depolama sırası işini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>
<span data-ttu-id="f8e35-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="f8e35-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="f8e35-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="f8e35-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="f8e35-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f8e35-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="f8e35-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f8e35-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8e35-111">EXAMPLES</span></span>

## <span data-ttu-id="f8e35-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8e35-112">PARAMETERS</span></span>

### <span data-ttu-id="f8e35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e35-113">-DefaultProfile</span></span>
<span data-ttu-id="f8e35-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8e35-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e35-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="f8e35-115">-EndTime</span></span>
<span data-ttu-id="f8e35-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="f8e35-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f8e35-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f8e35-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="f8e35-118">-ErrorActionType</span></span>
<span data-ttu-id="f8e35-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="f8e35-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8e35-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8e35-121">Http</span><span class="sxs-lookup"><span data-stu-id="f8e35-121">Http</span></span> 
- <span data-ttu-id="f8e35-122">Https</span><span class="sxs-lookup"><span data-stu-id="f8e35-122">Https</span></span> 
- <span data-ttu-id="f8e35-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="f8e35-123">StorageQueue</span></span> 
- <span data-ttu-id="f8e35-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f8e35-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="f8e35-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f8e35-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="f8e35-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="f8e35-126">-ExecutionCount</span></span>
<span data-ttu-id="f8e35-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="f8e35-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="f8e35-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="f8e35-129">-Frequency</span></span>
<span data-ttu-id="f8e35-130">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="f8e35-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8e35-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8e35-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="f8e35-132">Minute</span></span> 
- <span data-ttu-id="f8e35-133">Saati</span><span class="sxs-lookup"><span data-stu-id="f8e35-133">Hour</span></span> 
- <span data-ttu-id="f8e35-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="f8e35-134">Day</span></span> 
- <span data-ttu-id="f8e35-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="f8e35-135">Week</span></span> 
- <span data-ttu-id="f8e35-136">Ay</span><span class="sxs-lookup"><span data-stu-id="f8e35-136">Month</span></span>

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

### <span data-ttu-id="f8e35-137">-Aralık</span><span class="sxs-lookup"><span data-stu-id="f8e35-137">-Interval</span></span>
<span data-ttu-id="f8e35-138">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="f8e35-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f8e35-139">-JobCollectionName</span></span>
<span data-ttu-id="f8e35-140">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="f8e35-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="f8e35-141">-JobName</span></span>
<span data-ttu-id="f8e35-142">Bu cmdlet 'in değiştirdiği işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-142">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f8e35-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="f8e35-143">-JobState</span></span>
<span data-ttu-id="f8e35-144">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-144">Specifies the state of the job.</span></span>
<span data-ttu-id="f8e35-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f8e35-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8e35-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="f8e35-146">Enabled</span></span> 
- <span data-ttu-id="f8e35-147">DISABLED</span><span class="sxs-lookup"><span data-stu-id="f8e35-147">Disabled</span></span>

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

### <span data-ttu-id="f8e35-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e35-148">-ResourceGroupName</span></span>
<span data-ttu-id="f8e35-149">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="f8e35-150">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="f8e35-150">-StartTime</span></span>
<span data-ttu-id="f8e35-151">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="f8e35-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="f8e35-152">-StorageQueueAccount</span></span>
<span data-ttu-id="f8e35-153">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="f8e35-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="f8e35-154">-StorageQueueMessage</span></span>
<span data-ttu-id="f8e35-155">Depolama işi için bir kuyruk iletisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-155">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="f8e35-156">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="f8e35-156">-StorageQueueName</span></span>
<span data-ttu-id="f8e35-157">Bir depolama sırası adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="f8e35-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="f8e35-158">-StorageSASToken</span></span>
<span data-ttu-id="f8e35-159">Depolama sırası için paylaşılan bir Access imza belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="f8e35-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8e35-160">-Confirm</span></span>
<span data-ttu-id="f8e35-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8e35-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8e35-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e35-162">-WhatIf</span></span>
<span data-ttu-id="f8e35-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8e35-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e35-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8e35-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8e35-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e35-165">CommonParameters</span></span>
<span data-ttu-id="f8e35-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8e35-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e35-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e35-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e35-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8e35-168">INPUTS</span></span>

### <span data-ttu-id="f8e35-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e35-169">System.String</span></span>

## <span data-ttu-id="f8e35-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8e35-170">OUTPUTS</span></span>

### <span data-ttu-id="f8e35-171">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8e35-171">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="f8e35-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8e35-172">NOTES</span></span>

## <span data-ttu-id="f8e35-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8e35-173">RELATED LINKS</span></span>

[<span data-ttu-id="f8e35-174">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-174">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f8e35-175">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f8e35-175">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f8e35-176">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-176">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f8e35-177">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-177">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="f8e35-178">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-178">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="f8e35-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="f8e35-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f8e35-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="f8e35-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="f8e35-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="f8e35-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


