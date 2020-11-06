---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595192"
---
# <span data-ttu-id="2d356-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2d356-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2d356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d356-102">SYNOPSIS</span></span>
<span data-ttu-id="2d356-103">Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2d356-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d356-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d356-104">SYNTAX</span></span>

### <span data-ttu-id="2d356-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d356-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2d356-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d356-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2d356-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2d356-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2d356-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d356-108">DESCRIPTION</span></span>
<span data-ttu-id="2d356-109">**Remove-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2d356-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="2d356-110">_Force_ parametresi belirtilirse, cmdlet tetikleyiciyi kaldırmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="2d356-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="2d356-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d356-111">EXAMPLES</span></span>

### <span data-ttu-id="2d356-112">Örnek 1: tetikleyiciyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="2d356-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2d356-113">"ScheduledTrigger" adındaki tetiği "WikiADF" olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d356-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="2d356-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d356-114">PARAMETERS</span></span>

### <span data-ttu-id="2d356-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d356-115">-Confirm</span></span>
<span data-ttu-id="2d356-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d356-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d356-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2d356-117">-DataFactoryName</span></span>
<span data-ttu-id="2d356-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2d356-118">The data factory name.</span></span>

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

### <span data-ttu-id="2d356-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2d356-119">-Force</span></span>
<span data-ttu-id="2d356-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="2d356-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2d356-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d356-121">-Name</span></span>
<span data-ttu-id="2d356-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="2d356-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d356-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d356-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d356-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2d356-124">The resource group name.</span></span>

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

### <span data-ttu-id="2d356-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2d356-125">-ResourceId</span></span>
<span data-ttu-id="2d356-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2d356-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2d356-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d356-127">-InputObject</span></span>
<span data-ttu-id="2d356-128">Kaldırılacak tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2d356-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="2d356-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d356-129">-WhatIf</span></span>
<span data-ttu-id="2d356-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="2d356-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="2d356-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d356-131">INPUTS</span></span>

### <span data-ttu-id="2d356-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="2d356-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="2d356-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2d356-133">System.String</span></span>


## <span data-ttu-id="2d356-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d356-134">OUTPUTS</span></span>

### <span data-ttu-id="2d356-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="2d356-135">System.Object</span></span>

## <span data-ttu-id="2d356-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d356-136">NOTES</span></span>

## <span data-ttu-id="2d356-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d356-137">RELATED LINKS</span></span>
[<span data-ttu-id="2d356-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2d356-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2d356-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2d356-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2d356-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2d356-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2d356-141">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2d356-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

