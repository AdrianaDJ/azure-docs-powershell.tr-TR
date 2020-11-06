---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: e359a99d1d420d9494b16719e61bec4d7ed670a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589835"
---
# <span data-ttu-id="984b1-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="984b1-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="984b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984b1-102">SYNOPSIS</span></span>
<span data-ttu-id="984b1-103">Veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="984b1-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="984b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="984b1-104">SYNTAX</span></span>

### <span data-ttu-id="984b1-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="984b1-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="984b1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="984b1-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="984b1-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="984b1-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="984b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="984b1-108">DESCRIPTION</span></span>
<span data-ttu-id="984b1-109">**Stop-AzureRmDataFactoryV2Trigger** cmdlet 'i veri fabrikasında bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="984b1-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="984b1-110">Tetik ' Started ' durumundaysa, cmdlet tetikleyiciyi durdurur ve artık ardışık düzenler çağırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="984b1-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="984b1-111">Tetik zaten ' durduruldu ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="984b1-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="984b1-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi durdurmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="984b1-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="984b1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="984b1-113">EXAMPLES</span></span>

### <span data-ttu-id="984b1-114">Örnek 1: tetikleyiciyi durdurma</span><span class="sxs-lookup"><span data-stu-id="984b1-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="984b1-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="984b1-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="984b1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="984b1-116">PARAMETERS</span></span>

### <span data-ttu-id="984b1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="984b1-117">-DataFactoryName</span></span>
<span data-ttu-id="984b1-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="984b1-118">The data factory name.</span></span>

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

### <span data-ttu-id="984b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984b1-119">-DefaultProfile</span></span>
<span data-ttu-id="984b1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="984b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="984b1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="984b1-121">-Force</span></span>
<span data-ttu-id="984b1-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="984b1-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="984b1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="984b1-123">-InputObject</span></span>
<span data-ttu-id="984b1-124">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="984b1-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="984b1-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="984b1-125">-Name</span></span>
<span data-ttu-id="984b1-126">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="984b1-126">The trigger name.</span></span>

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

### <span data-ttu-id="984b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="984b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="984b1-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="984b1-128">The resource group name.</span></span>

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

### <span data-ttu-id="984b1-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="984b1-129">-ResourceId</span></span>
<span data-ttu-id="984b1-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="984b1-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="984b1-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="984b1-131">-Confirm</span></span>
<span data-ttu-id="984b1-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="984b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="984b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="984b1-133">-WhatIf</span></span>
<span data-ttu-id="984b1-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="984b1-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="984b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984b1-135">CommonParameters</span></span>
<span data-ttu-id="984b1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="984b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984b1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="984b1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984b1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="984b1-138">INPUTS</span></span>

### <span data-ttu-id="984b1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="984b1-139">System.String</span></span>
<span data-ttu-id="984b1-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="984b1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="984b1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="984b1-141">OUTPUTS</span></span>

### <span data-ttu-id="984b1-142">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfegger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="984b1-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="984b1-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="984b1-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="984b1-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="984b1-144">NOTES</span></span>

## <span data-ttu-id="984b1-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="984b1-145">RELATED LINKS</span></span>

[<span data-ttu-id="984b1-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="984b1-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="984b1-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="984b1-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="984b1-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="984b1-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="984b1-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="984b1-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
