---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110152"
---
# <span data-ttu-id="3d443-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d443-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="3d443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d443-102">SYNOPSIS</span></span>
<span data-ttu-id="3d443-103">Bir Stream Analytics işinde işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="3d443-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d443-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d443-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d443-105">DESCRIPTION</span></span>
<span data-ttu-id="3d443-106">**Get-AzStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinde tanımlanan işlevlerin listesini veya belirli bir işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="3d443-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d443-107">EXAMPLES</span></span>

### <span data-ttu-id="3d443-108">Örnek 1: tüm akış analizi işlevlerini alma</span><span class="sxs-lookup"><span data-stu-id="3d443-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="3d443-109">Bu komut, StreamJob22 adlı iş üzerinde tanımlanan işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="3d443-110">Örnek 2: belirli bir Stream Analytics işlevi edinme</span><span class="sxs-lookup"><span data-stu-id="3d443-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="3d443-111">Bu komut, StreamJob22 adlı işte tanımlanan ScoreTweet adındaki işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="3d443-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d443-112">PARAMETERS</span></span>

### <span data-ttu-id="3d443-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d443-113">-DefaultProfile</span></span>
<span data-ttu-id="3d443-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d443-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d443-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="3d443-115">-JobName</span></span>
<span data-ttu-id="3d443-116">İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d443-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="3d443-117">Bu cmdlet, bu parametrenin belirttiği iş için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d443-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d443-118">-Name</span></span>
<span data-ttu-id="3d443-119">Bu cmdlet 'in aldığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d443-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3d443-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d443-120">-ResourceGroupName</span></span>
<span data-ttu-id="3d443-121">Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d443-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="3d443-122">Bu cmdlet, bu parametrenin belirttiği grup için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="3d443-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d443-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d443-123">CommonParameters</span></span>
<span data-ttu-id="3d443-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d443-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d443-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d443-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d443-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d443-126">INPUTS</span></span>

### <span data-ttu-id="3d443-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3d443-127">System.String</span></span>

## <span data-ttu-id="3d443-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d443-128">OUTPUTS</span></span>

### <span data-ttu-id="3d443-129">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction</span><span class="sxs-lookup"><span data-stu-id="3d443-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="3d443-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d443-130">NOTES</span></span>

## <span data-ttu-id="3d443-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d443-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d443-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d443-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3d443-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d443-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3d443-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3d443-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


