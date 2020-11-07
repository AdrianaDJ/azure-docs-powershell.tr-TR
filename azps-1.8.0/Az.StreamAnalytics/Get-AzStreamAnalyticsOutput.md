---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: bf4a8734304ce92dac1bc329d6ae0ffa0f30c09c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753940"
---
# <span data-ttu-id="003ee-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="003ee-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="003ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="003ee-102">SYNOPSIS</span></span>
<span data-ttu-id="003ee-103">Belirtilen bir Stream Analytics işinde veya çıktısında tanımlanan çıktıları alır.</span><span class="sxs-lookup"><span data-stu-id="003ee-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="003ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="003ee-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="003ee-105">DESCRIPTION</span></span>
<span data-ttu-id="003ee-106">**Get-AzStreamAnalyticsOutput** cmdlet 'i belirtilen bir Stream Analytics işinde tanımlanan tüm çıktıları listeler veya belirli bir çıkış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="003ee-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="003ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="003ee-107">EXAMPLES</span></span>

### <span data-ttu-id="003ee-108">Örnek 1: iş çıktıları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="003ee-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="003ee-109">Bu komut, iş StreamingJob 'da tanımlanan çıkışlar hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="003ee-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="003ee-110">Örnek 2: belirli bir iş çıkışı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="003ee-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="003ee-111">Bu komut, iş StreamingJob 'da tanımlanan output adındaki çıktı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="003ee-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="003ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="003ee-112">PARAMETERS</span></span>

### <span data-ttu-id="003ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003ee-113">-DefaultProfile</span></span>
<span data-ttu-id="003ee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="003ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="003ee-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="003ee-115">-JobName</span></span>
<span data-ttu-id="003ee-116">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="003ee-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003ee-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="003ee-117">-Name</span></span>
<span data-ttu-id="003ee-118">Alınacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="003ee-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="003ee-120">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="003ee-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003ee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003ee-121">CommonParameters</span></span>
<span data-ttu-id="003ee-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="003ee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003ee-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003ee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003ee-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="003ee-124">INPUTS</span></span>

### <span data-ttu-id="003ee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="003ee-125">System.String</span></span>

## <span data-ttu-id="003ee-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="003ee-126">OUTPUTS</span></span>

### <span data-ttu-id="003ee-127">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput</span><span class="sxs-lookup"><span data-stu-id="003ee-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="003ee-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="003ee-128">NOTES</span></span>

## <span data-ttu-id="003ee-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="003ee-129">RELATED LINKS</span></span>

[<span data-ttu-id="003ee-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="003ee-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="003ee-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="003ee-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="003ee-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="003ee-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


