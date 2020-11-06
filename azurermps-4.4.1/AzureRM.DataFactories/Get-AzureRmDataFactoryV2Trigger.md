---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588251"
---
# <span data-ttu-id="57ce2-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57ce2-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="57ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="57ce2-103">Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ce2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57ce2-104">SYNTAX</span></span>

### <span data-ttu-id="57ce2-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57ce2-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ce2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57ce2-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ce2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="57ce2-107">DESCRIPTION</span></span>
<span data-ttu-id="57ce2-108">**Get-AzureRmDataFactoryV2Trigger** cmdlet 'i Veri Fabrikası içinde Tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="57ce2-109">Tetikleyicinin adını belirtirseniz, cmdlet bu tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="57ce2-110">Ad belirtmezseniz cmdlet, Veri Fabrikası 'ndaki tüm tetikleyiciler hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="57ce2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57ce2-111">EXAMPLES</span></span>

### <span data-ttu-id="57ce2-112">Örnek 1: belirli bir tetik hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="57ce2-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="57ce2-113">"WikiADF" Veri Fabrikası içinde oluşturulmuş tüm tetikleyicilerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="57ce2-114">Örnek 2: tüm tetikleyiciler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="57ce2-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="57ce2-115">"WikiADF" Veri Fabrikası "ScheduledTrigger" adındaki tek bir tetikleyiciyi alır.</span><span class="sxs-lookup"><span data-stu-id="57ce2-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="57ce2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57ce2-116">PARAMETERS</span></span>

### <span data-ttu-id="57ce2-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="57ce2-117">-DataFactory</span></span>
<span data-ttu-id="57ce2-118">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57ce2-118">The data factory object.</span></span>

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

### <span data-ttu-id="57ce2-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="57ce2-119">-DataFactoryName</span></span>
<span data-ttu-id="57ce2-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="57ce2-120">The data factory name.</span></span>

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

### <span data-ttu-id="57ce2-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="57ce2-121">-Name</span></span>
<span data-ttu-id="57ce2-122">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="57ce2-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57ce2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ce2-123">-ResourceGroupName</span></span>
<span data-ttu-id="57ce2-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57ce2-124">The resource group name.</span></span>

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

### <span data-ttu-id="57ce2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ce2-125">-DefaultProfile</span></span>
<span data-ttu-id="57ce2-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57ce2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ce2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ce2-127">CommonParameters</span></span>
<span data-ttu-id="57ce2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57ce2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ce2-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ce2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ce2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57ce2-130">INPUTS</span></span>

### <span data-ttu-id="57ce2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="57ce2-131">System.String</span></span>
<span data-ttu-id="57ce2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="57ce2-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="57ce2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57ce2-133">OUTPUTS</span></span>

### <span data-ttu-id="57ce2-134">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfegger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="57ce2-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="57ce2-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfei</span><span class="sxs-lookup"><span data-stu-id="57ce2-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="57ce2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57ce2-136">NOTES</span></span>

## <span data-ttu-id="57ce2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57ce2-137">RELATED LINKS</span></span>

[<span data-ttu-id="57ce2-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57ce2-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57ce2-139">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57ce2-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57ce2-140">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57ce2-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57ce2-141">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57ce2-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
