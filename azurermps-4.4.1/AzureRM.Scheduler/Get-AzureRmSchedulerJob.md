---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 3357eb154f21bc57de6ef60b243571e05bc0c22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763624"
---
# <span data-ttu-id="c30d2-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="c30d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c30d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c30d2-103">Planlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c30d2-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c30d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c30d2-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c30d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c30d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c30d2-106">**Get-AzureRmSchedulerJob** cmdlet 'ı Azure Zamanlayıcı işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c30d2-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="c30d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c30d2-107">EXAMPLES</span></span>

## <span data-ttu-id="c30d2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c30d2-108">PARAMETERS</span></span>

### <span data-ttu-id="c30d2-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c30d2-109">-JobCollectionName</span></span>
<span data-ttu-id="c30d2-110">Alınacak işleri içeren bir iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c30d2-110">Specifies the name of a job collection that contains jobs to get.</span></span>

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

### <span data-ttu-id="c30d2-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="c30d2-111">-JobName</span></span>
<span data-ttu-id="c30d2-112">Alınacak işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c30d2-112">Specifies the name of a job to get.</span></span>

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

### <span data-ttu-id="c30d2-113">-JobState</span><span class="sxs-lookup"><span data-stu-id="c30d2-113">-JobState</span></span>
<span data-ttu-id="c30d2-114">İşlerin iş durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c30d2-114">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="c30d2-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c30d2-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c30d2-116">Etkin</span><span class="sxs-lookup"><span data-stu-id="c30d2-116">Enabled</span></span> 
- <span data-ttu-id="c30d2-117">DISABLED</span><span class="sxs-lookup"><span data-stu-id="c30d2-117">Disabled</span></span> 
- <span data-ttu-id="c30d2-118">Hatalı</span><span class="sxs-lookup"><span data-stu-id="c30d2-118">Faulted</span></span> 
- <span data-ttu-id="c30d2-119">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="c30d2-119">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="c30d2-121">Alınacak işlerin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c30d2-121">Specifies the resource group of the jobs to get.</span></span>

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

### <span data-ttu-id="c30d2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30d2-122">-DefaultProfile</span></span>
<span data-ttu-id="c30d2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c30d2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c30d2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30d2-124">CommonParameters</span></span>
<span data-ttu-id="c30d2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c30d2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30d2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30d2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30d2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c30d2-127">INPUTS</span></span>

## <span data-ttu-id="c30d2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c30d2-128">OUTPUTS</span></span>

### <span data-ttu-id="c30d2-129">Microsoft. Azure. Commands. Scheduler. modeller. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c30d2-129">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="c30d2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c30d2-130">NOTES</span></span>

## <span data-ttu-id="c30d2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c30d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="c30d2-132">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-132">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c30d2-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c30d2-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c30d2-134">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-134">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c30d2-135">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-135">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c30d2-136">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-136">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="c30d2-137">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-137">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="c30d2-138">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-138">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="c30d2-139">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-139">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="c30d2-140">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-140">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="c30d2-141">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="c30d2-141">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


