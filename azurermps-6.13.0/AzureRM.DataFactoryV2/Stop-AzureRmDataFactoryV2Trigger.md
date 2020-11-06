---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 9f1ec54ded16f68c3af2a9449f9c97afb40a520a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590323"
---
# <span data-ttu-id="1739d-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1739d-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="1739d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1739d-102">SYNOPSIS</span></span>
<span data-ttu-id="1739d-103">Veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="1739d-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1739d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1739d-104">SYNTAX</span></span>

### <span data-ttu-id="1739d-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1739d-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1739d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1739d-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1739d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="1739d-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1739d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1739d-108">DESCRIPTION</span></span>
<span data-ttu-id="1739d-109">**Stop-AzureRmDataFactoryV2Trigger** cmdlet 'i veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="1739d-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="1739d-110">Tetik ' Started ' durumundaysa, cmdlet tetikleyiciyi durdurur ve artık ardışık düzenler çağırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="1739d-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="1739d-111">Tetik zaten ' durduruldu ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="1739d-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="1739d-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi durdurmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="1739d-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="1739d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1739d-113">EXAMPLES</span></span>

### <span data-ttu-id="1739d-114">Örnek 1: tetikleyiciyi durdurma</span><span class="sxs-lookup"><span data-stu-id="1739d-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="1739d-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="1739d-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="1739d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1739d-116">PARAMETERS</span></span>

### <span data-ttu-id="1739d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1739d-117">-DataFactoryName</span></span>
<span data-ttu-id="1739d-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="1739d-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1739d-119">-DefaultProfile</span></span>
<span data-ttu-id="1739d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1739d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1739d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1739d-121">-Force</span></span>
<span data-ttu-id="1739d-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="1739d-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1739d-123">-InputObject</span></span>
<span data-ttu-id="1739d-124">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="1739d-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1739d-125">-Name</span></span>
<span data-ttu-id="1739d-126">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="1739d-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1739d-127">-ResourceGroupName</span></span>
<span data-ttu-id="1739d-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1739d-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1739d-129">-ResourceId</span></span>
<span data-ttu-id="1739d-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="1739d-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="1739d-131">-Confirm</span></span>
<span data-ttu-id="1739d-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1739d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1739d-133">-WhatIf</span></span>
<span data-ttu-id="1739d-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="1739d-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1739d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1739d-135">CommonParameters</span></span>
<span data-ttu-id="1739d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1739d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1739d-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1739d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1739d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1739d-138">INPUTS</span></span>

### <span data-ttu-id="1739d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1739d-139">System.String</span></span>

### <span data-ttu-id="1739d-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="1739d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="1739d-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1739d-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1739d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1739d-142">OUTPUTS</span></span>

### <span data-ttu-id="1739d-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="1739d-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1739d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1739d-144">NOTES</span></span>

## <span data-ttu-id="1739d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1739d-145">RELATED LINKS</span></span>

[<span data-ttu-id="1739d-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1739d-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1739d-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1739d-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1739d-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1739d-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1739d-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1739d-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
