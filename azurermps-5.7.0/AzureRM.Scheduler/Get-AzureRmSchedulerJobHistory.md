---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762513"
---
# <span data-ttu-id="23c27-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="23c27-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="23c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23c27-102">SYNOPSIS</span></span>
<span data-ttu-id="23c27-103">İş geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="23c27-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23c27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23c27-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23c27-105">DESCRIPTION</span></span>
<span data-ttu-id="23c27-106">**Get-AzureRmSchedulerJobHistory** cmdlet 'ı bir Azure Zamanlayıcı işinin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="23c27-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="23c27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23c27-107">EXAMPLES</span></span>

## <span data-ttu-id="23c27-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23c27-108">PARAMETERS</span></span>

### <span data-ttu-id="23c27-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c27-109">-DefaultProfile</span></span>
<span data-ttu-id="23c27-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23c27-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23c27-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="23c27-111">-JobCollectionName</span></span>
<span data-ttu-id="23c27-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23c27-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="23c27-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="23c27-113">-JobExecutionStatus</span></span>
<span data-ttu-id="23c27-114">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="23c27-114">Specifies the status of a job.</span></span>
<span data-ttu-id="23c27-115">Bu cmdlet belirttiğiniz durumla eşleşen geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="23c27-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="23c27-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="23c27-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23c27-117">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="23c27-117">Completed</span></span> 
- <span data-ttu-id="23c27-118">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="23c27-118">Failed</span></span> 
- <span data-ttu-id="23c27-119">Ertelendi</span><span class="sxs-lookup"><span data-stu-id="23c27-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23c27-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="23c27-120">-JobName</span></span>
<span data-ttu-id="23c27-121">Bu cmdlet 'in geçmişi aldığı bir işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23c27-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="23c27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c27-122">-ResourceGroupName</span></span>
<span data-ttu-id="23c27-123">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="23c27-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="23c27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c27-124">CommonParameters</span></span>
<span data-ttu-id="23c27-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23c27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c27-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23c27-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c27-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23c27-127">INPUTS</span></span>

### <span data-ttu-id="23c27-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23c27-128">None</span></span>
<span data-ttu-id="23c27-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="23c27-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23c27-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23c27-130">OUTPUTS</span></span>

### <span data-ttu-id="23c27-131">Microsoft. Azure. Commands. Scheduler. modeller. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="23c27-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="23c27-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23c27-132">NOTES</span></span>

## <span data-ttu-id="23c27-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23c27-133">RELATED LINKS</span></span>

[<span data-ttu-id="23c27-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="23c27-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


