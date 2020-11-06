---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589940"
---
# <span data-ttu-id="52d87-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="52d87-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="52d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d87-102">SYNOPSIS</span></span>
<span data-ttu-id="52d87-103">Bir Stream Analytics işinde işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d87-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d87-105">DESCRIPTION</span></span>
<span data-ttu-id="52d87-106">**Get-AzureRmStreamAnalyticsFunction** cmdlet 'ı bir Azure Stream Analytics işinde tanımlanan işlevlerin listesini veya belirli bir işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="52d87-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d87-107">EXAMPLES</span></span>

### <span data-ttu-id="52d87-108">Örnek 1: tüm akış analizi işlevlerini alma</span><span class="sxs-lookup"><span data-stu-id="52d87-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="52d87-109">Bu komut, StreamJob22 adlı iş üzerinde tanımlanan işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="52d87-110">Örnek 2: belirli bir Stream Analytics işlevi edinme</span><span class="sxs-lookup"><span data-stu-id="52d87-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="52d87-111">Bu komut, StreamJob22 adlı işte tanımlanan ScoreTweet adındaki işlev hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="52d87-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d87-112">PARAMETERS</span></span>

### <span data-ttu-id="52d87-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="52d87-113">-JobName</span></span>
<span data-ttu-id="52d87-114">İşlevlerin ait olduğu Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d87-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="52d87-115">Bu cmdlet, bu parametrenin belirttiği iş için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="52d87-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="52d87-116">-Name</span></span>
<span data-ttu-id="52d87-117">Bu cmdlet 'in aldığı Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d87-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="52d87-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d87-118">-ResourceGroupName</span></span>
<span data-ttu-id="52d87-119">Stream Analytics işlevlerinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d87-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="52d87-120">Bu cmdlet, bu parametrenin belirttiği grup için işlevleri alır.</span><span class="sxs-lookup"><span data-stu-id="52d87-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52d87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d87-121">-DefaultProfile</span></span>
<span data-ttu-id="52d87-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52d87-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d87-123">CommonParameters</span></span>
<span data-ttu-id="52d87-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d87-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d87-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d87-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d87-126">INPUTS</span></span>

## <span data-ttu-id="52d87-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d87-127">OUTPUTS</span></span>

### <span data-ttu-id="52d87-128">System. Koleksiyonlar. Generic. LIST [Microsoft. Azure. Commands. StreamAnalytics. modeller. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. model. Psişlevi</span><span class="sxs-lookup"><span data-stu-id="52d87-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="52d87-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d87-129">NOTES</span></span>

## <span data-ttu-id="52d87-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d87-130">RELATED LINKS</span></span>

[<span data-ttu-id="52d87-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="52d87-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="52d87-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="52d87-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="52d87-133">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="52d87-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


