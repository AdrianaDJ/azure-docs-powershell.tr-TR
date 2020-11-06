---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593014"
---
# <span data-ttu-id="a1067-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="a1067-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="a1067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1067-102">SYNOPSIS</span></span>
<span data-ttu-id="a1067-103">İş geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a1067-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1067-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1067-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1067-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1067-105">DESCRIPTION</span></span>
<span data-ttu-id="a1067-106">**Get-AzureRmSchedulerJobHistory** cmdlet 'ı bir Azure Zamanlayıcı işinin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="a1067-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="a1067-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1067-107">EXAMPLES</span></span>

## <span data-ttu-id="a1067-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1067-108">PARAMETERS</span></span>

### <span data-ttu-id="a1067-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a1067-109">-JobCollectionName</span></span>
<span data-ttu-id="a1067-110">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1067-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="a1067-111">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="a1067-111">-JobExecutionStatus</span></span>
<span data-ttu-id="a1067-112">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1067-112">Specifies the status of a job.</span></span>
<span data-ttu-id="a1067-113">Bu cmdlet belirttiğiniz durumla eşleşen geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="a1067-113">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="a1067-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a1067-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1067-115">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="a1067-115">Completed</span></span> 
- <span data-ttu-id="a1067-116">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="a1067-116">Failed</span></span> 
- <span data-ttu-id="a1067-117">Ertelendi</span><span class="sxs-lookup"><span data-stu-id="a1067-117">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1067-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="a1067-118">-JobName</span></span>
<span data-ttu-id="a1067-119">Bu cmdlet 'in geçmişi aldığı bir işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1067-119">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="a1067-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1067-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1067-121">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1067-121">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a1067-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1067-122">-DefaultProfile</span></span>
<span data-ttu-id="a1067-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1067-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1067-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1067-124">CommonParameters</span></span>
<span data-ttu-id="a1067-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1067-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1067-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1067-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1067-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1067-127">INPUTS</span></span>

## <span data-ttu-id="a1067-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1067-128">OUTPUTS</span></span>

### <span data-ttu-id="a1067-129">Microsoft. Azure. Commands. Scheduler. modeller. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="a1067-129">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="a1067-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1067-130">NOTES</span></span>

## <span data-ttu-id="a1067-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1067-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1067-132">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="a1067-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


