---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: dd2a52167a773b241364311ed4e0e00c03ea8459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589646"
---
# <span data-ttu-id="b749b-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b749b-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="b749b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b749b-102">SYNOPSIS</span></span>
<span data-ttu-id="b749b-103">Bir Stream Analytics işinde işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b749b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b749b-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b749b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b749b-105">DESCRIPTION</span></span>
<span data-ttu-id="b749b-106">**Get-AzureRmStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinde tanımlanan işlevlerin listesini veya belirli bir işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="b749b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b749b-107">EXAMPLES</span></span>

### <span data-ttu-id="b749b-108">Örnek 1: tüm akış analizi işlevlerini alma</span><span class="sxs-lookup"><span data-stu-id="b749b-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="b749b-109">Bu komut, StreamJob22 adlı iş üzerinde tanımlanan işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="b749b-110">Örnek 2: belirli bir Stream Analytics işlevi edinme</span><span class="sxs-lookup"><span data-stu-id="b749b-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="b749b-111">Bu komut, StreamJob22 adlı işte tanımlanan ScoreTweet adındaki işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="b749b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b749b-112">PARAMETERS</span></span>

### <span data-ttu-id="b749b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b749b-113">-DefaultProfile</span></span>
<span data-ttu-id="b749b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b749b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b749b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="b749b-115">-JobName</span></span>
<span data-ttu-id="b749b-116">İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b749b-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="b749b-117">Bu cmdlet, bu parametrenin belirttiği iş için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b749b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b749b-118">-Name</span></span>
<span data-ttu-id="b749b-119">Bu cmdlet 'in aldığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b749b-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b749b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b749b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b749b-121">Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b749b-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="b749b-122">Bu cmdlet, bu parametrenin belirttiği grup için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="b749b-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b749b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b749b-123">CommonParameters</span></span>
<span data-ttu-id="b749b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b749b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b749b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b749b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b749b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b749b-126">INPUTS</span></span>

### <span data-ttu-id="b749b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b749b-127">None</span></span>
<span data-ttu-id="b749b-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b749b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b749b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b749b-129">OUTPUTS</span></span>

### <span data-ttu-id="b749b-130">System. Koleksiyonlar. Generic. LIST [Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. model. Psişlevi</span><span class="sxs-lookup"><span data-stu-id="b749b-130">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="b749b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b749b-131">NOTES</span></span>

## <span data-ttu-id="b749b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b749b-132">RELATED LINKS</span></span>

[<span data-ttu-id="b749b-133">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b749b-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="b749b-134">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b749b-134">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="b749b-135">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="b749b-135">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


