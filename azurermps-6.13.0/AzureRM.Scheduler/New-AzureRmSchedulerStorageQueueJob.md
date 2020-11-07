---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: ac41336e1acc73050cf55e285054cf1a13ae383f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762286"
---
# <span data-ttu-id="10b72-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10b72-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="10b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10b72-102">SYNOPSIS</span></span>
<span data-ttu-id="10b72-103">Depolama sırası işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10b72-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10b72-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10b72-105">DESCRIPTION</span></span>
<span data-ttu-id="10b72-106">**New-AzureRmSchedulerStorageQueueJob** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir depolama sırası işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10b72-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>
<span data-ttu-id="10b72-107">Bu cmdlet, *Erroractiontype* parametresine dayalı olarak dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="10b72-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="10b72-108">Dinamik parametreler diğer parametre değerlerine göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="10b72-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="10b72-109">Diğer parametreleri belirledikten sonra dinamik parametrelerin adlarını keşfetmek için, kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="10b72-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10b72-110">Gerekli bir parametreyi atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="10b72-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10b72-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10b72-111">EXAMPLES</span></span>

## <span data-ttu-id="10b72-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10b72-112">PARAMETERS</span></span>

### <span data-ttu-id="10b72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b72-113">-DefaultProfile</span></span>
<span data-ttu-id="10b72-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10b72-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b72-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="10b72-115">-EndTime</span></span>
<span data-ttu-id="10b72-116">İş için bir **Tarih saat** nesnesi olarak bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="10b72-117">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="10b72-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="10b72-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="10b72-118">-ErrorActionType</span></span>
<span data-ttu-id="10b72-119">İş için bir hata eylem ayarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="10b72-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10b72-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10b72-121">Http</span><span class="sxs-lookup"><span data-stu-id="10b72-121">Http</span></span> 
- <span data-ttu-id="10b72-122">Https</span><span class="sxs-lookup"><span data-stu-id="10b72-122">Https</span></span> 
- <span data-ttu-id="10b72-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="10b72-123">StorageQueue</span></span> 
- <span data-ttu-id="10b72-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="10b72-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="10b72-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="10b72-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="10b72-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="10b72-126">-ExecutionCount</span></span>
<span data-ttu-id="10b72-127">İşin kaç kez çalışacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="10b72-128">Varsayılan olarak bir iş süresiz olarak yinelenecektir.</span><span class="sxs-lookup"><span data-stu-id="10b72-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="10b72-129">Frekans</span><span class="sxs-lookup"><span data-stu-id="10b72-129">-Frequency</span></span>
<span data-ttu-id="10b72-130">İş için bir sıklık belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="10b72-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10b72-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10b72-132">Dakikanın</span><span class="sxs-lookup"><span data-stu-id="10b72-132">Minute</span></span> 
- <span data-ttu-id="10b72-133">Saati</span><span class="sxs-lookup"><span data-stu-id="10b72-133">Hour</span></span> 
- <span data-ttu-id="10b72-134">Günündeki</span><span class="sxs-lookup"><span data-stu-id="10b72-134">Day</span></span> 
- <span data-ttu-id="10b72-135">Haftada</span><span class="sxs-lookup"><span data-stu-id="10b72-135">Week</span></span> 
- <span data-ttu-id="10b72-136">Ay</span><span class="sxs-lookup"><span data-stu-id="10b72-136">Month</span></span>

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

### <span data-ttu-id="10b72-137">-Aralık</span><span class="sxs-lookup"><span data-stu-id="10b72-137">-Interval</span></span>
<span data-ttu-id="10b72-138">İş için bir yinelenme aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="10b72-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="10b72-139">-JobCollectionName</span></span>
<span data-ttu-id="10b72-140">İşin ait olduğu iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="10b72-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="10b72-141">-JobName</span></span>
<span data-ttu-id="10b72-142">İş için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="10b72-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="10b72-143">-JobState</span></span>
<span data-ttu-id="10b72-144">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-144">Specifies the state of the job.</span></span>
<span data-ttu-id="10b72-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="10b72-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10b72-146">Etkin</span><span class="sxs-lookup"><span data-stu-id="10b72-146">Enabled</span></span> 
- <span data-ttu-id="10b72-147">DISABLED</span><span class="sxs-lookup"><span data-stu-id="10b72-147">Disabled</span></span>

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

### <span data-ttu-id="10b72-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b72-148">-ResourceGroupName</span></span>
<span data-ttu-id="10b72-149">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="10b72-150">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="10b72-150">-StartTime</span></span>
<span data-ttu-id="10b72-151">İş için başlangıç saatini bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="10b72-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="10b72-152">-StorageQueueAccount</span></span>
<span data-ttu-id="10b72-153">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="10b72-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="10b72-154">-StorageQueueMessage</span></span>
<span data-ttu-id="10b72-155">Depolama işi için bir kuyruk iletisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-155">Specifies a queue message for the storage job.</span></span>

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

### <span data-ttu-id="10b72-156">-Storagesıraadı</span><span class="sxs-lookup"><span data-stu-id="10b72-156">-StorageQueueName</span></span>
<span data-ttu-id="10b72-157">Bir depolama sırası adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="10b72-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="10b72-158">-StorageSASToken</span></span>
<span data-ttu-id="10b72-159">Depolama sırası için paylaşılan bir Access imza belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="10b72-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="10b72-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="10b72-160">-Confirm</span></span>
<span data-ttu-id="10b72-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10b72-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b72-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b72-162">-WhatIf</span></span>
<span data-ttu-id="10b72-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10b72-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b72-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10b72-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b72-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b72-165">CommonParameters</span></span>
<span data-ttu-id="10b72-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10b72-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b72-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b72-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b72-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10b72-168">INPUTS</span></span>

### <span data-ttu-id="10b72-169">System. String</span><span class="sxs-lookup"><span data-stu-id="10b72-169">System.String</span></span>

## <span data-ttu-id="10b72-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10b72-170">OUTPUTS</span></span>

### <span data-ttu-id="10b72-171">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10b72-171">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="10b72-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10b72-172">NOTES</span></span>

## <span data-ttu-id="10b72-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10b72-173">RELATED LINKS</span></span>

[<span data-ttu-id="10b72-174">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10b72-174">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="10b72-175">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10b72-175">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10b72-176">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10b72-176">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="10b72-177">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10b72-177">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10b72-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10b72-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="10b72-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10b72-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10b72-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10b72-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="10b72-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10b72-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10b72-182">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10b72-182">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


