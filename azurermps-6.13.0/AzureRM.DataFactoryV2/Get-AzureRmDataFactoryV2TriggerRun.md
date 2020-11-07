---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: caa3cd25db706a3d025ee439aebb6dbb5491f7d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762965"
---
# <span data-ttu-id="0dcae-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0dcae-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="0dcae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dcae-102">SYNOPSIS</span></span>
<span data-ttu-id="0dcae-103">Tetik çalıştırmaları hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="0dcae-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dcae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0dcae-104">SYNTAX</span></span>

### <span data-ttu-id="0dcae-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0dcae-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dcae-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0dcae-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dcae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0dcae-107">DESCRIPTION</span></span>
<span data-ttu-id="0dcae-108">**Get-AzureRmDataFactoryV2TriggerRun** komutu, verilen zaman diliminde belirtilen tetik için tetik çalıştırmaları hakkında ayrıntılı bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0dcae-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="0dcae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0dcae-109">EXAMPLES</span></span>

### <span data-ttu-id="0dcae-110">Örnek 1: tetik çalışması hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="0dcae-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="0dcae-111">Bu komut, "2017-09-01" ile "2019-09-30" arasında başlayan "WikiADF" fabrikası</span><span class="sxs-lookup"><span data-stu-id="0dcae-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="0dcae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0dcae-112">PARAMETERS</span></span>

### <span data-ttu-id="0dcae-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0dcae-113">-DataFactory</span></span>
<span data-ttu-id="0dcae-114">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0dcae-114">The data factory object.</span></span>

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

### <span data-ttu-id="0dcae-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0dcae-115">-DataFactoryName</span></span>
<span data-ttu-id="0dcae-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="0dcae-116">The data factory name.</span></span>

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

### <span data-ttu-id="0dcae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dcae-117">-DefaultProfile</span></span>
<span data-ttu-id="0dcae-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0dcae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dcae-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0dcae-119">-Name</span></span>
<span data-ttu-id="0dcae-120">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="0dcae-120">The trigger name.</span></span>

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

### <span data-ttu-id="0dcae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dcae-121">-ResourceGroupName</span></span>
<span data-ttu-id="0dcae-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0dcae-122">The resource group name.</span></span>

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

### <span data-ttu-id="0dcae-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="0dcae-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="0dcae-124">ISO8601 biçiminde yürütülmeye başladığı sefer veya daha sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="0dcae-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="0dcae-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="0dcae-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="0dcae-126">Tetik çalıştırmasının ISO8601 biçiminde yürütülmeye başladığı saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="0dcae-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="0dcae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dcae-127">CommonParameters</span></span>
<span data-ttu-id="0dcae-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0dcae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dcae-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dcae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dcae-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0dcae-130">INPUTS</span></span>

### <span data-ttu-id="0dcae-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="0dcae-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="0dcae-132">Parametreler: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0dcae-132">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="0dcae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0dcae-133">System.String</span></span>

## <span data-ttu-id="0dcae-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0dcae-134">OUTPUTS</span></span>

### <span data-ttu-id="0dcae-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pçarpıcı Ggerrun</span><span class="sxs-lookup"><span data-stu-id="0dcae-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="0dcae-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0dcae-136">NOTES</span></span>

## <span data-ttu-id="0dcae-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0dcae-137">RELATED LINKS</span></span>

[<span data-ttu-id="0dcae-138">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0dcae-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="0dcae-139">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="0dcae-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

