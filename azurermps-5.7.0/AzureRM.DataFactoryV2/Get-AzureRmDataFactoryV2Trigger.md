---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594098"
---
# <span data-ttu-id="ecc72-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ecc72-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="ecc72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc72-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc72-103">Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecc72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecc72-104">SYNTAX</span></span>

### <span data-ttu-id="ecc72-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ecc72-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecc72-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ecc72-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecc72-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ecc72-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecc72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecc72-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc72-109">**Get-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="ecc72-110">Tetikleyicinin adını belirtirseniz, cmdlet bu tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="ecc72-111">Ad belirtmezseniz cmdlet, Veri Fabrikası 'ndaki tüm tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="ecc72-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecc72-112">EXAMPLES</span></span>

### <span data-ttu-id="ecc72-113">Örnek 1: belirli bir tetik hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="ecc72-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="ecc72-114">"WikiADF" Veri Fabrikası içinde oluşturulmuş tüm tetikleyicilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="ecc72-115">Örnek 2: tüm tetikleyiciler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="ecc72-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="ecc72-116">"WikiADF" Veri Fabrikası "ScheduledTrigger" adındaki tek bir tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="ecc72-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="ecc72-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecc72-117">PARAMETERS</span></span>

### <span data-ttu-id="ecc72-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ecc72-118">-DataFactory</span></span>
<span data-ttu-id="ecc72-119">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ecc72-119">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc72-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ecc72-120">-DataFactoryName</span></span>
<span data-ttu-id="ecc72-121">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="ecc72-121">The data factory name.</span></span>

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

### <span data-ttu-id="ecc72-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc72-122">-DefaultProfile</span></span>
<span data-ttu-id="ecc72-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecc72-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc72-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ecc72-124">-Name</span></span>
<span data-ttu-id="ecc72-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="ecc72-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc72-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc72-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecc72-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ecc72-127">The resource group name.</span></span>

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

### <span data-ttu-id="ecc72-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ecc72-128">-ResourceId</span></span>
<span data-ttu-id="ecc72-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ecc72-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc72-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc72-130">CommonParameters</span></span>
<span data-ttu-id="ecc72-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecc72-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc72-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc72-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc72-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecc72-133">INPUTS</span></span>

### <span data-ttu-id="ecc72-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc72-134">System.String</span></span>
<span data-ttu-id="ecc72-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="ecc72-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ecc72-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecc72-136">OUTPUTS</span></span>

### <span data-ttu-id="ecc72-137">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfegger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ecc72-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ecc72-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="ecc72-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ecc72-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecc72-139">NOTES</span></span>

## <span data-ttu-id="ecc72-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecc72-140">RELATED LINKS</span></span>

[<span data-ttu-id="ecc72-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ecc72-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ecc72-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ecc72-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ecc72-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ecc72-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ecc72-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ecc72-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
