---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5ee7492473cdf36c3d50b08aa770371651f85003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762964"
---
# <span data-ttu-id="84314-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="84314-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="84314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84314-102">SYNOPSIS</span></span>
<span data-ttu-id="84314-103">Bir veri fabrikası içinde tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="84314-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84314-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84314-104">SYNTAX</span></span>

### <span data-ttu-id="84314-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84314-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84314-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84314-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84314-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="84314-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84314-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="84314-108">DESCRIPTION</span></span>
<span data-ttu-id="84314-109">**Start-AzureRmDataFactoryV2Trigger** cmdlet 'i bir veri fabrikası içinde tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="84314-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="84314-110">Tetik ' durduruldu ' durumundaysa, cmdlet tetikleyiciyi başlatır ve sonuç olarak tanımı temelinde ardışık düzen çağırır.</span><span class="sxs-lookup"><span data-stu-id="84314-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="84314-111">Tetik zaten ' Started ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="84314-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="84314-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi başlatmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="84314-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="84314-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84314-113">EXAMPLES</span></span>

### <span data-ttu-id="84314-114">Örnek 1: tetik başlatma</span><span class="sxs-lookup"><span data-stu-id="84314-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="84314-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="84314-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="84314-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84314-116">PARAMETERS</span></span>

### <span data-ttu-id="84314-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84314-117">-DataFactoryName</span></span>
<span data-ttu-id="84314-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="84314-118">The data factory name.</span></span>

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

### <span data-ttu-id="84314-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84314-119">-DefaultProfile</span></span>
<span data-ttu-id="84314-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84314-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84314-121">-Force</span><span class="sxs-lookup"><span data-stu-id="84314-121">-Force</span></span>
<span data-ttu-id="84314-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="84314-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="84314-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84314-123">-InputObject</span></span>
<span data-ttu-id="84314-124">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="84314-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="84314-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="84314-125">-Name</span></span>
<span data-ttu-id="84314-126">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="84314-126">The trigger name.</span></span>

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

### <span data-ttu-id="84314-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84314-127">-ResourceGroupName</span></span>
<span data-ttu-id="84314-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="84314-128">The resource group name.</span></span>

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

### <span data-ttu-id="84314-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="84314-129">-ResourceId</span></span>
<span data-ttu-id="84314-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="84314-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84314-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="84314-131">-Confirm</span></span>
<span data-ttu-id="84314-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84314-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84314-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84314-133">-WhatIf</span></span>
<span data-ttu-id="84314-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="84314-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="84314-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84314-135">CommonParameters</span></span>
<span data-ttu-id="84314-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84314-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84314-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84314-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84314-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84314-138">INPUTS</span></span>

### <span data-ttu-id="84314-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84314-139">System.String</span></span>

### <span data-ttu-id="84314-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="84314-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="84314-141">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84314-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="84314-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84314-142">OUTPUTS</span></span>

### <span data-ttu-id="84314-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="84314-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="84314-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84314-144">NOTES</span></span>

## <span data-ttu-id="84314-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84314-145">RELATED LINKS</span></span>

[<span data-ttu-id="84314-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="84314-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="84314-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="84314-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="84314-148">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="84314-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="84314-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="84314-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
