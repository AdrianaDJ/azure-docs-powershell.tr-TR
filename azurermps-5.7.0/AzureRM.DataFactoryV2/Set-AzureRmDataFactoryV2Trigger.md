---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 17953aa02bf0242f358fd07b1173977db6318d05
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765214"
---
# <span data-ttu-id="20d49-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="20d49-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="20d49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20d49-102">SYNOPSIS</span></span>
<span data-ttu-id="20d49-103">Veri Fabrikası içinde tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20d49-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20d49-104">SYNTAX</span></span>

### <span data-ttu-id="20d49-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20d49-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20d49-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="20d49-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20d49-107">DESCRIPTION</span></span>
<span data-ttu-id="20d49-108">**Set-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası içinde bir tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20d49-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="20d49-109">Zaten var olan bir tetik için ad belirtirseniz, cmdlet tetikleyiciyi değiştirmeden önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="20d49-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="20d49-110">_Force_ parametresini belirtirseniz, cmdlet, onay istemeden mevcut tetikleyiciyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="20d49-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="20d49-111">Tetikleyiciler ' durduruldu ' durumunda oluşturulur ve bunların başvuruda bulundukları ardışık düzenleri hemen çağırmaya başlamalardır.</span><span class="sxs-lookup"><span data-stu-id="20d49-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="20d49-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20d49-112">EXAMPLES</span></span>

### <span data-ttu-id="20d49-113">Örnek 1: tetik oluşturma</span><span class="sxs-lookup"><span data-stu-id="20d49-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="20d49-114">"WikiADF" Veri Fabrikası 'nda "ScheduledTrigger" adındaki yeni bir tetik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="20d49-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="20d49-115">Tetik ' durduruldu ' durumunda oluşturulur ve bu da hemen başlamadır.</span><span class="sxs-lookup"><span data-stu-id="20d49-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="20d49-116">Tetik cmdlet kullanılarak başlatılabilir `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="20d49-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="20d49-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20d49-117">PARAMETERS</span></span>

### <span data-ttu-id="20d49-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="20d49-118">-DataFactoryName</span></span>
<span data-ttu-id="20d49-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="20d49-119">The data factory name.</span></span>

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

### <span data-ttu-id="20d49-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d49-120">-DefaultProfile</span></span>
<span data-ttu-id="20d49-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20d49-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d49-122">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="20d49-122">-DefinitionFile</span></span>
<span data-ttu-id="20d49-123">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="20d49-123">The JSON file path.</span></span>

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

### <span data-ttu-id="20d49-124">-Force</span><span class="sxs-lookup"><span data-stu-id="20d49-124">-Force</span></span>
<span data-ttu-id="20d49-125">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="20d49-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="20d49-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="20d49-126">-Name</span></span>
<span data-ttu-id="20d49-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="20d49-127">The trigger name.</span></span>

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

### <span data-ttu-id="20d49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d49-128">-ResourceGroupName</span></span>
<span data-ttu-id="20d49-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="20d49-129">The resource group name.</span></span>

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

### <span data-ttu-id="20d49-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="20d49-130">-ResourceId</span></span>
<span data-ttu-id="20d49-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="20d49-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="20d49-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="20d49-132">-Confirm</span></span>
<span data-ttu-id="20d49-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20d49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d49-134">-WhatIf</span></span>
<span data-ttu-id="20d49-135">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="20d49-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="20d49-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d49-136">CommonParameters</span></span>
<span data-ttu-id="20d49-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20d49-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d49-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d49-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d49-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20d49-139">INPUTS</span></span>

### <span data-ttu-id="20d49-140">System. String</span><span class="sxs-lookup"><span data-stu-id="20d49-140">System.String</span></span>

## <span data-ttu-id="20d49-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20d49-141">OUTPUTS</span></span>

### <span data-ttu-id="20d49-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="20d49-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="20d49-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20d49-143">NOTES</span></span>

## <span data-ttu-id="20d49-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20d49-144">RELATED LINKS</span></span>

[<span data-ttu-id="20d49-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="20d49-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="20d49-146">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="20d49-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="20d49-147">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="20d49-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="20d49-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="20d49-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
