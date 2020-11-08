---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273677"
---
# <span data-ttu-id="3766a-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3766a-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3766a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3766a-102">SYNOPSIS</span></span>
<span data-ttu-id="3766a-103">Veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="3766a-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="3766a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3766a-104">SYNTAX</span></span>

### <span data-ttu-id="3766a-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3766a-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3766a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3766a-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3766a-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3766a-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3766a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3766a-108">DESCRIPTION</span></span>
<span data-ttu-id="3766a-109">**Stop-AzDataFactoryV2Trigger** cmdlet 'i veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="3766a-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="3766a-110">Tetik ' Started ' durumundaysa, cmdlet tetikleyiciyi durdurur ve artık ardışık düzenler çağırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="3766a-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="3766a-111">Tetik zaten ' durduruldu ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="3766a-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="3766a-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi durdurmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="3766a-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="3766a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3766a-113">EXAMPLES</span></span>

### <span data-ttu-id="3766a-114">Örnek 1: tetikleyiciyi durdurma</span><span class="sxs-lookup"><span data-stu-id="3766a-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="3766a-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="3766a-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="3766a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3766a-116">PARAMETERS</span></span>

### <span data-ttu-id="3766a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3766a-117">-DataFactoryName</span></span>
<span data-ttu-id="3766a-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="3766a-118">The data factory name.</span></span>

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

### <span data-ttu-id="3766a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3766a-119">-DefaultProfile</span></span>
<span data-ttu-id="3766a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3766a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3766a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3766a-121">-Force</span></span>
<span data-ttu-id="3766a-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="3766a-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3766a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3766a-123">-InputObject</span></span>
<span data-ttu-id="3766a-124">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="3766a-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="3766a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3766a-125">-Name</span></span>
<span data-ttu-id="3766a-126">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="3766a-126">The trigger name.</span></span>

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

### <span data-ttu-id="3766a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3766a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3766a-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3766a-128">The resource group name.</span></span>

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

### <span data-ttu-id="3766a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3766a-129">-ResourceId</span></span>
<span data-ttu-id="3766a-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3766a-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3766a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="3766a-131">-Confirm</span></span>
<span data-ttu-id="3766a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3766a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3766a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3766a-133">-WhatIf</span></span>
<span data-ttu-id="3766a-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="3766a-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3766a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3766a-135">CommonParameters</span></span>
<span data-ttu-id="3766a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3766a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3766a-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3766a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3766a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3766a-138">INPUTS</span></span>

### <span data-ttu-id="3766a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3766a-139">System.String</span></span>

### <span data-ttu-id="3766a-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="3766a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3766a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3766a-141">OUTPUTS</span></span>

### <span data-ttu-id="3766a-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="3766a-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3766a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3766a-143">NOTES</span></span>

## <span data-ttu-id="3766a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3766a-144">RELATED LINKS</span></span>

[<span data-ttu-id="3766a-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3766a-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3766a-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3766a-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3766a-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3766a-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3766a-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3766a-148">Remove-AzDataFactoryV2Trigger</span></span>]()
