---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: d22f1acf8f99f15df83be95aafdc8ff0aefd2a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763996"
---
# <span data-ttu-id="43583-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="43583-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="43583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43583-102">SYNOPSIS</span></span>
<span data-ttu-id="43583-103">Planlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="43583-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43583-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43583-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43583-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43583-105">DESCRIPTION</span></span>
<span data-ttu-id="43583-106">**Get-AzureRmSchedulerJob** cmdlet 'ı Azure Zamanlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="43583-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="43583-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43583-107">EXAMPLES</span></span>

## <span data-ttu-id="43583-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43583-108">PARAMETERS</span></span>

### <span data-ttu-id="43583-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43583-109">-DefaultProfile</span></span>
<span data-ttu-id="43583-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43583-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43583-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="43583-111">-JobCollectionName</span></span>
<span data-ttu-id="43583-112">Alınacak işleri içeren bir iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43583-112">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="43583-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="43583-113">-JobName</span></span>
<span data-ttu-id="43583-114">Alınacak işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43583-114">Specifies the name of a job to get.</span></span>

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

### <span data-ttu-id="43583-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="43583-115">-JobState</span></span>
<span data-ttu-id="43583-116">İşlerin iş durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="43583-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="43583-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="43583-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43583-118">Etkin</span><span class="sxs-lookup"><span data-stu-id="43583-118">Enabled</span></span> 
- <span data-ttu-id="43583-119">DISABLED</span><span class="sxs-lookup"><span data-stu-id="43583-119">Disabled</span></span> 
- <span data-ttu-id="43583-120">Hatalı</span><span class="sxs-lookup"><span data-stu-id="43583-120">Faulted</span></span> 
- <span data-ttu-id="43583-121">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="43583-121">Completed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43583-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43583-122">-ResourceGroupName</span></span>
<span data-ttu-id="43583-123">Alınacak işlerin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="43583-123">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="43583-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43583-124">CommonParameters</span></span>
<span data-ttu-id="43583-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43583-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43583-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43583-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43583-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43583-127">INPUTS</span></span>

### <span data-ttu-id="43583-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43583-128">None</span></span>
<span data-ttu-id="43583-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="43583-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43583-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43583-130">OUTPUTS</span></span>

### <span data-ttu-id="43583-131">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="43583-131">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="43583-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43583-132">NOTES</span></span>

## <span data-ttu-id="43583-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43583-133">RELATED LINKS</span></span>

[<span data-ttu-id="43583-134">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="43583-134">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="43583-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="43583-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="43583-136">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="43583-136">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="43583-137">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="43583-137">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="43583-138">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="43583-138">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="43583-139">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="43583-139">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="43583-140">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="43583-140">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="43583-141">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="43583-141">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="43583-142">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="43583-142">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="43583-143">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="43583-143">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


