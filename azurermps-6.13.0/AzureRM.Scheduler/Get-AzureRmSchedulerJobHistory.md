---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 5bf5745270db8cea076ccac9cff2d4e9b7a4bc06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593883"
---
# <span data-ttu-id="f2680-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="f2680-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="f2680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2680-102">SYNOPSIS</span></span>
<span data-ttu-id="f2680-103">İş geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="f2680-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2680-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2680-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2680-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2680-105">DESCRIPTION</span></span>
<span data-ttu-id="f2680-106">**Get-AzureRmSchedulerJobHistory** cmdlet 'ı bir Azure Zamanlayıcı işinin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="f2680-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="f2680-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2680-107">EXAMPLES</span></span>

## <span data-ttu-id="f2680-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2680-108">PARAMETERS</span></span>

### <span data-ttu-id="f2680-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2680-109">-DefaultProfile</span></span>
<span data-ttu-id="f2680-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2680-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2680-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f2680-111">-JobCollectionName</span></span>
<span data-ttu-id="f2680-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2680-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="f2680-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="f2680-113">-JobExecutionStatus</span></span>
<span data-ttu-id="f2680-114">İşin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2680-114">Specifies the status of a job.</span></span>
<span data-ttu-id="f2680-115">Bu cmdlet belirttiğiniz durumla eşleşen geçmişi alır.</span><span class="sxs-lookup"><span data-stu-id="f2680-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="f2680-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f2680-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f2680-117">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="f2680-117">Completed</span></span> 
- <span data-ttu-id="f2680-118">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="f2680-118">Failed</span></span> 
- <span data-ttu-id="f2680-119">Ertelendi</span><span class="sxs-lookup"><span data-stu-id="f2680-119">Postponed</span></span>

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

### <span data-ttu-id="f2680-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="f2680-120">-JobName</span></span>
<span data-ttu-id="f2680-121">Bu cmdlet 'in geçmişi aldığı bir işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2680-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="f2680-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2680-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2680-123">İşin ait olduğu kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2680-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="f2680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2680-124">CommonParameters</span></span>
<span data-ttu-id="f2680-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2680-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2680-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2680-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2680-127">INPUTS</span></span>

### <span data-ttu-id="f2680-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f2680-128">System.String</span></span>

## <span data-ttu-id="f2680-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2680-129">OUTPUTS</span></span>

### <span data-ttu-id="f2680-130">Microsoft. Azure. Commands. Scheduler. modeller. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="f2680-130">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="f2680-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2680-131">NOTES</span></span>

## <span data-ttu-id="f2680-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2680-132">RELATED LINKS</span></span>

[<span data-ttu-id="f2680-133">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="f2680-133">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


