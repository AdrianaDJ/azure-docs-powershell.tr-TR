---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938304"
---
# <span data-ttu-id="d7e55-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d7e55-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="d7e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e55-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e55-103">Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7e55-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="d7e55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7e55-104">SYNTAX</span></span>

### <span data-ttu-id="d7e55-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7e55-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e55-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7e55-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e55-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d7e55-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7e55-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7e55-108">DESCRIPTION</span></span>
<span data-ttu-id="d7e55-109">**Remove-AzDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d7e55-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="d7e55-110">_Force_ parametresi belirtilirse, cmdlet tetikleyiciyi kaldırmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="d7e55-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="d7e55-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7e55-111">EXAMPLES</span></span>

### <span data-ttu-id="d7e55-112">Örnek 1: tetikleyiciyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="d7e55-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d7e55-113">"ScheduledTrigger" adındaki tetiği "WikiADF" olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d7e55-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="d7e55-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7e55-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e55-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d7e55-115">-DataFactoryName</span></span>
<span data-ttu-id="d7e55-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d7e55-116">The data factory name.</span></span>

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

### <span data-ttu-id="d7e55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e55-117">-DefaultProfile</span></span>
<span data-ttu-id="d7e55-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7e55-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7e55-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d7e55-119">-Force</span></span>
<span data-ttu-id="d7e55-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d7e55-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d7e55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7e55-121">-InputObject</span></span>
<span data-ttu-id="d7e55-122">Kaldırılacak tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d7e55-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="d7e55-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7e55-123">-Name</span></span>
<span data-ttu-id="d7e55-124">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="d7e55-124">The trigger name.</span></span>

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

### <span data-ttu-id="d7e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7e55-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7e55-126">The resource group name.</span></span>

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

### <span data-ttu-id="d7e55-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7e55-127">-ResourceId</span></span>
<span data-ttu-id="d7e55-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d7e55-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d7e55-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7e55-129">-Confirm</span></span>
<span data-ttu-id="d7e55-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7e55-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e55-131">-WhatIf</span></span>
<span data-ttu-id="d7e55-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="d7e55-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d7e55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e55-133">CommonParameters</span></span>
<span data-ttu-id="d7e55-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7e55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e55-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e55-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e55-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7e55-136">INPUTS</span></span>

### <span data-ttu-id="d7e55-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="d7e55-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="d7e55-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d7e55-138">System.String</span></span>

## <span data-ttu-id="d7e55-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7e55-139">OUTPUTS</span></span>

### <span data-ttu-id="d7e55-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7e55-140">System.Boolean</span></span>

## <span data-ttu-id="d7e55-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7e55-141">NOTES</span></span>

## <span data-ttu-id="d7e55-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7e55-142">RELATED LINKS</span></span>

[<span data-ttu-id="d7e55-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d7e55-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d7e55-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d7e55-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d7e55-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d7e55-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d7e55-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d7e55-146">Stop-AzDataFactoryV2Trigger</span></span>]()

