---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586907"
---
# <span data-ttu-id="cd1ae-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd1ae-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="cd1ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1ae-103">Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd1ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd1ae-104">SYNTAX</span></span>

### <span data-ttu-id="cd1ae-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd1ae-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1ae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd1ae-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1ae-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="cd1ae-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd1ae-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1ae-109">**Remove-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="cd1ae-110">_Force_ parametresi belirtilirse, cmdlet tetikleyiciyi kaldırmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="cd1ae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd1ae-111">EXAMPLES</span></span>

### <span data-ttu-id="cd1ae-112">Örnek 1: tetikleyiciyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="cd1ae-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="cd1ae-113">"ScheduledTrigger" adındaki tetiği "WikiADF" olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="cd1ae-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd1ae-114">PARAMETERS</span></span>

### <span data-ttu-id="cd1ae-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd1ae-115">-Confirm</span></span>
<span data-ttu-id="cd1ae-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1ae-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cd1ae-117">-DataFactoryName</span></span>
<span data-ttu-id="cd1ae-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-118">The data factory name.</span></span>

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

### <span data-ttu-id="cd1ae-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cd1ae-119">-Force</span></span>
<span data-ttu-id="cd1ae-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cd1ae-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd1ae-121">-Name</span></span>
<span data-ttu-id="cd1ae-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-122">The trigger name.</span></span>

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

### <span data-ttu-id="cd1ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd1ae-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-124">The resource group name.</span></span>

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

### <span data-ttu-id="cd1ae-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd1ae-125">-ResourceId</span></span>
<span data-ttu-id="cd1ae-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cd1ae-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd1ae-127">-InputObject</span></span>
<span data-ttu-id="cd1ae-128">Kaldırılacak tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="cd1ae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1ae-129">-WhatIf</span></span>
<span data-ttu-id="cd1ae-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cd1ae-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1ae-131">-DefaultProfile</span></span>
<span data-ttu-id="cd1ae-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1ae-133">CommonParameters</span></span>
<span data-ttu-id="cd1ae-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd1ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1ae-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1ae-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd1ae-136">INPUTS</span></span>

### <span data-ttu-id="cd1ae-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="cd1ae-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="cd1ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1ae-138">System.String</span></span>

## <span data-ttu-id="cd1ae-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd1ae-139">OUTPUTS</span></span>

### <span data-ttu-id="cd1ae-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="cd1ae-140">System.Object</span></span>

## <span data-ttu-id="cd1ae-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd1ae-141">NOTES</span></span>

## <span data-ttu-id="cd1ae-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd1ae-142">RELATED LINKS</span></span>

[<span data-ttu-id="cd1ae-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd1ae-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cd1ae-144">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd1ae-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cd1ae-145">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd1ae-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cd1ae-146">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd1ae-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

