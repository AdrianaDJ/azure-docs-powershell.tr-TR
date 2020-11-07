---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 3f98ff38d5e74b7b167dc3a168a1cc05a42a7a23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752519"
---
# <span data-ttu-id="384bf-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="384bf-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="384bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="384bf-102">SYNOPSIS</span></span>
<span data-ttu-id="384bf-103">Tetik çalıştırmaları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="384bf-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="384bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="384bf-104">SYNTAX</span></span>

### <span data-ttu-id="384bf-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="384bf-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="384bf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="384bf-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="384bf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="384bf-107">DESCRIPTION</span></span>
<span data-ttu-id="384bf-108">**Get-AzDataFactoryV2TriggerRun** komutu, verilen zaman diliminde belirtilen tetik için tetik çalıştırmaları hakkında ayrıntılı bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="384bf-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="384bf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="384bf-109">EXAMPLES</span></span>

### <span data-ttu-id="384bf-110">Örnek 1: tetik çalışması hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="384bf-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="384bf-111">Bu komut, "2017-09-01" ile "2019-09-30" arasında başlayan "WikiADF" fabrikası</span><span class="sxs-lookup"><span data-stu-id="384bf-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="384bf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="384bf-112">PARAMETERS</span></span>

### <span data-ttu-id="384bf-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="384bf-113">-DataFactory</span></span>
<span data-ttu-id="384bf-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="384bf-114">The data factory object.</span></span>

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

### <span data-ttu-id="384bf-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="384bf-115">-DataFactoryName</span></span>
<span data-ttu-id="384bf-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="384bf-116">The data factory name.</span></span>

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

### <span data-ttu-id="384bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384bf-117">-DefaultProfile</span></span>
<span data-ttu-id="384bf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="384bf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384bf-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="384bf-119">-Name</span></span>
<span data-ttu-id="384bf-120">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="384bf-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="384bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="384bf-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="384bf-122">The resource group name.</span></span>

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

### <span data-ttu-id="384bf-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="384bf-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="384bf-124">ISO8601 biçiminde yürütülmeye başladığı sefer veya daha sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="384bf-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384bf-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="384bf-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="384bf-126">Tetik çalıştırmasının ISO8601 biçiminde yürütülmeye başladığı saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="384bf-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="384bf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384bf-127">CommonParameters</span></span>
<span data-ttu-id="384bf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="384bf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384bf-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384bf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384bf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="384bf-130">INPUTS</span></span>

### <span data-ttu-id="384bf-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="384bf-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="384bf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="384bf-132">System.String</span></span>

## <span data-ttu-id="384bf-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="384bf-133">OUTPUTS</span></span>

### <span data-ttu-id="384bf-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="384bf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="384bf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="384bf-135">NOTES</span></span>

## <span data-ttu-id="384bf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="384bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="384bf-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="384bf-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="384bf-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="384bf-138">Stop-AzDataFactoryV2Trigger</span></span>]()
