---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3054824876ccaff24f319ae14c704cd975e79434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763774"
---
# <span data-ttu-id="003d1-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="003d1-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="003d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="003d1-102">SYNOPSIS</span></span>

<span data-ttu-id="003d1-103">Veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="003d1-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="003d1-104">SYNTAX</span></span>

### <span data-ttu-id="003d1-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="003d1-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="003d1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="003d1-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="003d1-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="003d1-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="003d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="003d1-108">DESCRIPTION</span></span>

<span data-ttu-id="003d1-109">**Stop-AzureRmDataFactoryV2Trigger** cmdlet 'i veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="003d1-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="003d1-110">Tetik ' Started ' durumundaysa, cmdlet tetikleyiciyi durdurur ve artık ardışık düzenler çağırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="003d1-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="003d1-111">Tetik zaten ' durduruldu ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="003d1-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="003d1-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi durdurmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="003d1-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>


## <span data-ttu-id="003d1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="003d1-113">EXAMPLES</span></span>

### <span data-ttu-id="003d1-114">Örnek 1: tetikleyiciyi durdurma</span><span class="sxs-lookup"><span data-stu-id="003d1-114">Example 1: Stop a trigger</span></span>

```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="003d1-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="003d1-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="003d1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="003d1-116">PARAMETERS</span></span>

### <span data-ttu-id="003d1-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="003d1-117">-Confirm</span></span>
<span data-ttu-id="003d1-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="003d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="003d1-119">-DataFactoryName</span></span>
<span data-ttu-id="003d1-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="003d1-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="003d1-121">-Force</span></span>
<span data-ttu-id="003d1-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="003d1-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="003d1-123">-Name</span></span>
<span data-ttu-id="003d1-124">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="003d1-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="003d1-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="003d1-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="003d1-127">-ResourceId</span></span>
<span data-ttu-id="003d1-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="003d1-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="003d1-129">-InputObject</span></span>
<span data-ttu-id="003d1-130">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="003d1-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="003d1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003d1-131">-WhatIf</span></span>
<span data-ttu-id="003d1-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="003d1-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="003d1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="003d1-133">INPUTS</span></span>

### <span data-ttu-id="003d1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="003d1-134">System.String</span></span>
<span data-ttu-id="003d1-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="003d1-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="003d1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="003d1-136">OUTPUTS</span></span>

### <span data-ttu-id="003d1-137">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfegger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="003d1-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="003d1-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="003d1-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="003d1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="003d1-139">NOTES</span></span>

## <span data-ttu-id="003d1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="003d1-140">RELATED LINKS</span></span>
[<span data-ttu-id="003d1-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="003d1-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="003d1-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="003d1-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="003d1-143">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="003d1-143">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="003d1-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="003d1-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
