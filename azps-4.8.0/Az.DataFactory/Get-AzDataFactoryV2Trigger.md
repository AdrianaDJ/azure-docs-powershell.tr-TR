---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 989a898605488fc7cfaa828bfd8c5b9b61378a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108349"
---
# <span data-ttu-id="75a30-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="75a30-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="75a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a30-102">SYNOPSIS</span></span>
<span data-ttu-id="75a30-103">Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="75a30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75a30-104">SYNTAX</span></span>

### <span data-ttu-id="75a30-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75a30-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a30-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="75a30-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a30-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="75a30-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75a30-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="75a30-108">DESCRIPTION</span></span>
<span data-ttu-id="75a30-109">**Get-AzDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="75a30-110">Tetikleyicinin adını belirtirseniz, cmdlet bu tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="75a30-111">Ad belirtmezseniz cmdlet, Veri Fabrikası 'ndaki tüm tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="75a30-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75a30-112">EXAMPLES</span></span>

### <span data-ttu-id="75a30-113">Örnek 1: belirli bir tetik hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="75a30-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="75a30-114">"WikiADF" Veri Fabrikası içinde oluşturulmuş tüm tetikleyicilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="75a30-115">Örnek 2: tüm tetikleyiciler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="75a30-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="75a30-116">"WikiADF" Veri Fabrikası "ScheduledTrigger" adındaki tek bir tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="75a30-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="75a30-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75a30-117">PARAMETERS</span></span>

### <span data-ttu-id="75a30-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="75a30-118">-DataFactory</span></span>
<span data-ttu-id="75a30-119">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="75a30-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a30-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="75a30-120">-DataFactoryName</span></span>
<span data-ttu-id="75a30-121">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="75a30-121">The data factory name.</span></span>

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

### <span data-ttu-id="75a30-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a30-122">-DefaultProfile</span></span>
<span data-ttu-id="75a30-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75a30-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a30-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="75a30-124">-Name</span></span>
<span data-ttu-id="75a30-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="75a30-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a30-126">-ResourceGroupName</span></span>
<span data-ttu-id="75a30-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="75a30-127">The resource group name.</span></span>

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

### <span data-ttu-id="75a30-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="75a30-128">-ResourceId</span></span>
<span data-ttu-id="75a30-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="75a30-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="75a30-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a30-130">CommonParameters</span></span>
<span data-ttu-id="75a30-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75a30-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a30-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a30-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a30-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75a30-133">INPUTS</span></span>

### <span data-ttu-id="75a30-134">System. String</span><span class="sxs-lookup"><span data-stu-id="75a30-134">System.String</span></span>

### <span data-ttu-id="75a30-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="75a30-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="75a30-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75a30-136">OUTPUTS</span></span>

### <span data-ttu-id="75a30-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="75a30-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="75a30-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75a30-138">NOTES</span></span>

## <span data-ttu-id="75a30-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75a30-139">RELATED LINKS</span></span>

[<span data-ttu-id="75a30-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="75a30-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="75a30-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="75a30-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="75a30-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="75a30-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="75a30-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="75a30-143">Remove-AzDataFactoryV2Trigger</span></span>]()
