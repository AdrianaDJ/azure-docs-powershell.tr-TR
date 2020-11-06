---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: aba1086db4fb1b106fb20579fde8fffc4db5591d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590333"
---
# <span data-ttu-id="d249f-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d249f-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="d249f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d249f-102">SYNOPSIS</span></span>
<span data-ttu-id="d249f-103">Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d249f-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d249f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d249f-104">SYNTAX</span></span>

### <span data-ttu-id="d249f-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d249f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d249f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d249f-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d249f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d249f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d249f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d249f-108">DESCRIPTION</span></span>
<span data-ttu-id="d249f-109">**Remove-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası 'ndan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d249f-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="d249f-110">_Force_ parametresi belirtilirse, cmdlet tetikleyiciyi kaldırmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="d249f-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="d249f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d249f-111">EXAMPLES</span></span>

### <span data-ttu-id="d249f-112">Örnek 1: tetikleyiciyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="d249f-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d249f-113">"ScheduledTrigger" adındaki tetiği "WikiADF" olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d249f-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="d249f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d249f-114">PARAMETERS</span></span>

### <span data-ttu-id="d249f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d249f-115">-DataFactoryName</span></span>
<span data-ttu-id="d249f-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d249f-116">The data factory name.</span></span>

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

### <span data-ttu-id="d249f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d249f-117">-DefaultProfile</span></span>
<span data-ttu-id="d249f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d249f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d249f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d249f-119">-Force</span></span>
<span data-ttu-id="d249f-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d249f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d249f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d249f-121">-InputObject</span></span>
<span data-ttu-id="d249f-122">Kaldırılacak tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d249f-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="d249f-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d249f-123">-Name</span></span>
<span data-ttu-id="d249f-124">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="d249f-124">The trigger name.</span></span>

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

### <span data-ttu-id="d249f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d249f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d249f-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d249f-126">The resource group name.</span></span>

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

### <span data-ttu-id="d249f-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d249f-127">-ResourceId</span></span>
<span data-ttu-id="d249f-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d249f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d249f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="d249f-129">-Confirm</span></span>
<span data-ttu-id="d249f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d249f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d249f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d249f-131">-WhatIf</span></span>
<span data-ttu-id="d249f-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="d249f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d249f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d249f-133">CommonParameters</span></span>
<span data-ttu-id="d249f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d249f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d249f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d249f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d249f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d249f-136">INPUTS</span></span>

### <span data-ttu-id="d249f-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="d249f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="d249f-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d249f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d249f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d249f-139">System.String</span></span>

## <span data-ttu-id="d249f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d249f-140">OUTPUTS</span></span>

### <span data-ttu-id="d249f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d249f-141">System.Boolean</span></span>

## <span data-ttu-id="d249f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d249f-142">NOTES</span></span>

## <span data-ttu-id="d249f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d249f-143">RELATED LINKS</span></span>

[<span data-ttu-id="d249f-144">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d249f-144">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d249f-145">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d249f-145">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d249f-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d249f-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d249f-147">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d249f-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

