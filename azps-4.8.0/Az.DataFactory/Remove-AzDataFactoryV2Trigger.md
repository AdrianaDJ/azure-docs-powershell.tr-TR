---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266081"
---
# <span data-ttu-id="5a4bb-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5a4bb-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5a4bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4bb-103">Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="5a4bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-104">SYNTAX</span></span>

### <span data-ttu-id="5a4bb-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a4bb-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4bb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a4bb-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4bb-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="5a4bb-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a4bb-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4bb-109">**Remove-AzDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="5a4bb-110">_Force_ parametresi belirtilirse, cmdlet tetikleyiciyi kaldırmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="5a4bb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a4bb-111">EXAMPLES</span></span>

### <span data-ttu-id="5a4bb-112">Örnek 1: tetikleyiciyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="5a4bb-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5a4bb-113">"ScheduledTrigger" adındaki tetiği "WikiADF" olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="5a4bb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a4bb-114">PARAMETERS</span></span>

### <span data-ttu-id="5a4bb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a4bb-115">-DataFactoryName</span></span>
<span data-ttu-id="5a4bb-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-116">The data factory name.</span></span>

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

### <span data-ttu-id="5a4bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4bb-117">-DefaultProfile</span></span>
<span data-ttu-id="5a4bb-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a4bb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5a4bb-119">-Force</span></span>
<span data-ttu-id="5a4bb-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5a4bb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4bb-121">-InputObject</span></span>
<span data-ttu-id="5a4bb-122">Kaldırılacak tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="5a4bb-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a4bb-123">-Name</span></span>
<span data-ttu-id="5a4bb-124">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a4bb-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-126">The resource group name.</span></span>

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

### <span data-ttu-id="5a4bb-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5a4bb-127">-ResourceId</span></span>
<span data-ttu-id="5a4bb-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5a4bb-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a4bb-129">-Confirm</span></span>
<span data-ttu-id="5a4bb-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4bb-131">-WhatIf</span></span>
<span data-ttu-id="5a4bb-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5a4bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4bb-133">CommonParameters</span></span>
<span data-ttu-id="5a4bb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4bb-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4bb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4bb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-136">INPUTS</span></span>

### <span data-ttu-id="5a4bb-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="5a4bb-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="5a4bb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5a4bb-138">System.String</span></span>

## <span data-ttu-id="5a4bb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a4bb-139">OUTPUTS</span></span>

### <span data-ttu-id="5a4bb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a4bb-140">System.Boolean</span></span>

## <span data-ttu-id="5a4bb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a4bb-141">NOTES</span></span>

## <span data-ttu-id="5a4bb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a4bb-142">RELATED LINKS</span></span>

[<span data-ttu-id="5a4bb-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5a4bb-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5a4bb-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5a4bb-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5a4bb-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5a4bb-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5a4bb-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5a4bb-146">Stop-AzDataFactoryV2Trigger</span></span>]()

