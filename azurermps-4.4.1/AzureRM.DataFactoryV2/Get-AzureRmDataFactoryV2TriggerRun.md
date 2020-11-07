---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764075"
---
# <span data-ttu-id="f81af-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="f81af-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="f81af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f81af-102">SYNOPSIS</span></span>
<span data-ttu-id="f81af-103">Tetik çalıştırmaları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="f81af-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f81af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f81af-104">SYNTAX</span></span>

### <span data-ttu-id="f81af-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f81af-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="f81af-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f81af-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="f81af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f81af-107">DESCRIPTION</span></span>
<span data-ttu-id="f81af-108">**Get-AzureRmDataFactoryV2TriggerRun** komutu, verilen zaman diliminde belirtilen tetik için tetik çalıştırmaları hakkında ayrıntılı bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f81af-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="f81af-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f81af-109">EXAMPLES</span></span>

### <span data-ttu-id="f81af-110">Örnek 1: tetik çalışması hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f81af-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="f81af-111">Bu komut, "2017-09-01" ile "2019-09-30" arasında başlayan "WikiADF" fabrikası</span><span class="sxs-lookup"><span data-stu-id="f81af-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="f81af-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f81af-112">PARAMETERS</span></span>

### <span data-ttu-id="f81af-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f81af-113">-DataFactory</span></span>
<span data-ttu-id="f81af-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f81af-114">The data factory object.</span></span>

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

### <span data-ttu-id="f81af-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f81af-115">-DataFactoryName</span></span>
<span data-ttu-id="f81af-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="f81af-116">The data factory name.</span></span>

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

### <span data-ttu-id="f81af-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f81af-117">-Name</span></span>
<span data-ttu-id="f81af-118">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="f81af-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81af-119">-ResourceGroupName</span></span>
<span data-ttu-id="f81af-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f81af-120">The resource group name.</span></span>

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

### <span data-ttu-id="f81af-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="f81af-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="f81af-122">ISO8601 biçiminde yürütülmeye başladığı sefer veya daha sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="f81af-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f81af-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="f81af-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="f81af-124">Tetik çalıştırmasının ISO8601 biçiminde yürütülmeye başladığı saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="f81af-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f81af-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f81af-125">INPUTS</span></span>

### <span data-ttu-id="f81af-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f81af-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="f81af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f81af-127">System.String</span></span>


## <span data-ttu-id="f81af-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f81af-128">OUTPUTS</span></span>

### <span data-ttu-id="f81af-129">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Pfeggerrun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f81af-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f81af-130">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="f81af-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="f81af-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f81af-131">NOTES</span></span>

## <span data-ttu-id="f81af-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f81af-132">RELATED LINKS</span></span>
[<span data-ttu-id="f81af-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f81af-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f81af-134">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f81af-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

