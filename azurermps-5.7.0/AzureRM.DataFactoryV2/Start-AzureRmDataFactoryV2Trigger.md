---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: ed4769c26363c60aace191d439d4a450a894eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762542"
---
# <span data-ttu-id="2e0aa-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2e0aa-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2e0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0aa-103">Bir veri fabrikası içinde tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e0aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e0aa-104">SYNTAX</span></span>

### <span data-ttu-id="2e0aa-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e0aa-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e0aa-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e0aa-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e0aa-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2e0aa-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e0aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e0aa-108">DESCRIPTION</span></span>
<span data-ttu-id="2e0aa-109">**Start-AzureRmDataFactoryV2Trigger** cmdlet 'i bir veri fabrikası içinde tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="2e0aa-110">Tetik ' durduruldu ' durumundaysa, cmdlet tetikleyiciyi başlatır ve sonuç olarak tanımı temelinde ardışık düzen çağırır.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="2e0aa-111">Tetik zaten ' Started ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="2e0aa-112">Force parametresi belirtilirse, cmdlet tetikleyiciyi başlatmadan önce istemez.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="2e0aa-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e0aa-113">EXAMPLES</span></span>

### <span data-ttu-id="2e0aa-114">Örnek 1: tetik başlatma</span><span class="sxs-lookup"><span data-stu-id="2e0aa-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2e0aa-115">"WikiADF" Veri Fabrikası içinde "ScheduledTrigger" adındaki tetikleyiciyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="2e0aa-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e0aa-116">PARAMETERS</span></span>

### <span data-ttu-id="2e0aa-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2e0aa-117">-DataFactoryName</span></span>
<span data-ttu-id="2e0aa-118">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-118">The data factory name.</span></span>

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

### <span data-ttu-id="2e0aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0aa-119">-DefaultProfile</span></span>
<span data-ttu-id="2e0aa-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e0aa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2e0aa-121">-Force</span></span>
<span data-ttu-id="2e0aa-122">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2e0aa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e0aa-123">-InputObject</span></span>
<span data-ttu-id="2e0aa-124">Tetikleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="2e0aa-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="2e0aa-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e0aa-125">-Name</span></span>
<span data-ttu-id="2e0aa-126">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-126">The trigger name.</span></span>

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

### <span data-ttu-id="2e0aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e0aa-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-128">The resource group name.</span></span>

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

### <span data-ttu-id="2e0aa-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2e0aa-129">-ResourceId</span></span>
<span data-ttu-id="2e0aa-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2e0aa-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e0aa-131">-Confirm</span></span>
<span data-ttu-id="2e0aa-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e0aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e0aa-133">-WhatIf</span></span>
<span data-ttu-id="2e0aa-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2e0aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0aa-135">CommonParameters</span></span>
<span data-ttu-id="2e0aa-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e0aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0aa-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0aa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0aa-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e0aa-138">INPUTS</span></span>

### <span data-ttu-id="2e0aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0aa-139">System.String</span></span>
<span data-ttu-id="2e0aa-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="2e0aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2e0aa-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e0aa-141">OUTPUTS</span></span>

### <span data-ttu-id="2e0aa-142">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfegger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2e0aa-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2e0aa-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="2e0aa-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="2e0aa-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e0aa-144">NOTES</span></span>

## <span data-ttu-id="2e0aa-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e0aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="2e0aa-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2e0aa-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2e0aa-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2e0aa-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2e0aa-148">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2e0aa-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2e0aa-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2e0aa-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
