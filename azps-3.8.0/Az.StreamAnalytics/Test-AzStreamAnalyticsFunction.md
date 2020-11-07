---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937904"
---
# <span data-ttu-id="1b557-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1b557-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1b557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b557-102">SYNOPSIS</span></span>
<span data-ttu-id="1b557-103">Akış analizlerini bir işleve bağlanıp bağlanamamı sınar.</span><span class="sxs-lookup"><span data-stu-id="1b557-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1b557-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b557-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b557-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b557-105">DESCRIPTION</span></span>
<span data-ttu-id="1b557-106">**Test-AzStreamAnalyticsFunction** cmdlet 'ı Azure Stream analizin bir işleve bağlanıp bağlanamadan sınar.</span><span class="sxs-lookup"><span data-stu-id="1b557-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="1b557-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b557-107">EXAMPLES</span></span>

### <span data-ttu-id="1b557-108">Örnek 1: Stream Analytics işlevini sınama</span><span class="sxs-lookup"><span data-stu-id="1b557-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1b557-109">Bu komut, StreamJob22 adındaki işte ScoreTweet adındaki işlevin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="1b557-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="1b557-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b557-110">PARAMETERS</span></span>

### <span data-ttu-id="1b557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b557-111">-DefaultProfile</span></span>
<span data-ttu-id="1b557-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b557-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b557-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1b557-113">-JobName</span></span>
<span data-ttu-id="1b557-114">İşlevin ait olduğu akış analizi işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b557-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="1b557-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b557-115">-Name</span></span>
<span data-ttu-id="1b557-116">Bu cmdlet 'in test olduğu Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b557-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b557-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b557-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b557-118">Bir Stream Analytics işlevinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b557-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1b557-119">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bir işlevi sınar.</span><span class="sxs-lookup"><span data-stu-id="1b557-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b557-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b557-120">CommonParameters</span></span>
<span data-ttu-id="1b557-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b557-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b557-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b557-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b557-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b557-123">INPUTS</span></span>

### <span data-ttu-id="1b557-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1b557-124">System.String</span></span>

## <span data-ttu-id="1b557-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b557-125">OUTPUTS</span></span>

### <span data-ttu-id="1b557-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b557-126">System.Boolean</span></span>

## <span data-ttu-id="1b557-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b557-127">NOTES</span></span>

## <span data-ttu-id="1b557-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b557-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b557-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1b557-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1b557-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1b557-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1b557-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1b557-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


