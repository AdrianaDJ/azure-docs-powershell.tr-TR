---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8bf4a713784b367363e4f1f9167cfb144d06c0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595185"
---
# <span data-ttu-id="45a77-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="45a77-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="45a77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a77-102">SYNOPSIS</span></span>
<span data-ttu-id="45a77-103">Veri Fabrikası içinde tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45a77-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45a77-104">SYNTAX</span></span>

### <span data-ttu-id="45a77-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45a77-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="45a77-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="45a77-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="45a77-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="45a77-107">DESCRIPTION</span></span>

<span data-ttu-id="45a77-108">**Set-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası içinde bir tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45a77-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="45a77-109">Zaten var olan bir tetik için ad belirtirseniz, cmdlet tetikleyiciyi değiştirmeden önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="45a77-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="45a77-110">_Force_ parametresini belirtirseniz, cmdlet, onay istemeden mevcut tetikleyiciyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="45a77-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="45a77-111">Tetikleyiciler ' durduruldu ' durumunda oluşturulur ve bunların başvuruda bulundukları ardışık düzenleri hemen çağırmaya başlamalardır.</span><span class="sxs-lookup"><span data-stu-id="45a77-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="45a77-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45a77-112">EXAMPLES</span></span>

### <span data-ttu-id="45a77-113">Örnek 1: tetik oluşturma</span><span class="sxs-lookup"><span data-stu-id="45a77-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

```

<span data-ttu-id="45a77-114">"WikiADF" Veri Fabrikası 'nda "ScheduledTrigger" adındaki yeni bir tetik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="45a77-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="45a77-115">Tetik ' durduruldu ' durumunda oluşturulur ve bu da hemen başlamadır.</span><span class="sxs-lookup"><span data-stu-id="45a77-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="45a77-116">Tetik cmdlet kullanılarak başlatılabilir `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="45a77-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="45a77-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45a77-117">PARAMETERS</span></span>

### <span data-ttu-id="45a77-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="45a77-118">-Confirm</span></span>
<span data-ttu-id="45a77-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45a77-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a77-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="45a77-120">-DataFactoryName</span></span>
<span data-ttu-id="45a77-121">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="45a77-121">The data factory name.</span></span>

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

### <span data-ttu-id="45a77-122">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="45a77-122">-DefinitionFile</span></span>
<span data-ttu-id="45a77-123">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="45a77-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a77-124">-Force</span><span class="sxs-lookup"><span data-stu-id="45a77-124">-Force</span></span>
<span data-ttu-id="45a77-125">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="45a77-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="45a77-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="45a77-126">-Name</span></span>
<span data-ttu-id="45a77-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="45a77-127">The trigger name.</span></span>

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

### <span data-ttu-id="45a77-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a77-128">-ResourceGroupName</span></span>
<span data-ttu-id="45a77-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45a77-129">The resource group name.</span></span>

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

### <span data-ttu-id="45a77-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="45a77-130">-ResourceId</span></span>
<span data-ttu-id="45a77-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="45a77-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="45a77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a77-132">-WhatIf</span></span>
<span data-ttu-id="45a77-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="45a77-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="45a77-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45a77-134">INPUTS</span></span>

### <span data-ttu-id="45a77-135">System. String</span><span class="sxs-lookup"><span data-stu-id="45a77-135">System.String</span></span>


## <span data-ttu-id="45a77-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45a77-136">OUTPUTS</span></span>

### <span data-ttu-id="45a77-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="45a77-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="45a77-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45a77-138">NOTES</span></span>

## <span data-ttu-id="45a77-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45a77-139">RELATED LINKS</span></span>
[<span data-ttu-id="45a77-140">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="45a77-140">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="45a77-141">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="45a77-141">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="45a77-142">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="45a77-142">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="45a77-143">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="45a77-143">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
