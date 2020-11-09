---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324868"
---
# <span data-ttu-id="63652-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="63652-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="63652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63652-102">SYNOPSIS</span></span>
<span data-ttu-id="63652-103">Akış analizlerini bir işleve bağlanıp bağlanamamı sınar.</span><span class="sxs-lookup"><span data-stu-id="63652-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="63652-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63652-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63652-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63652-105">DESCRIPTION</span></span>
<span data-ttu-id="63652-106">**Test-AzStreamAnalyticsFunction** cmdlet 'ı Azure Stream analizin bir işleve bağlanıp bağlanamadan sınar.</span><span class="sxs-lookup"><span data-stu-id="63652-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="63652-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63652-107">EXAMPLES</span></span>

### <span data-ttu-id="63652-108">Örnek 1: Stream Analytics işlevini sınama</span><span class="sxs-lookup"><span data-stu-id="63652-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="63652-109">Bu komut, StreamJob22 adındaki işte ScoreTweet adındaki işlevin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="63652-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="63652-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63652-110">PARAMETERS</span></span>

### <span data-ttu-id="63652-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63652-111">-DefaultProfile</span></span>
<span data-ttu-id="63652-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63652-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63652-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="63652-113">-JobName</span></span>
<span data-ttu-id="63652-114">İşlevin ait olduğu akış analizi işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63652-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="63652-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="63652-115">-Name</span></span>
<span data-ttu-id="63652-116">Bu cmdlet 'in test olduğu Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63652-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="63652-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63652-117">-ResourceGroupName</span></span>
<span data-ttu-id="63652-118">Bir Stream Analytics işlevinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63652-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="63652-119">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bir işlevi sınar.</span><span class="sxs-lookup"><span data-stu-id="63652-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="63652-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63652-120">CommonParameters</span></span>
<span data-ttu-id="63652-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63652-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63652-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63652-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63652-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63652-123">INPUTS</span></span>

### <span data-ttu-id="63652-124">System. String</span><span class="sxs-lookup"><span data-stu-id="63652-124">System.String</span></span>

## <span data-ttu-id="63652-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63652-125">OUTPUTS</span></span>

### <span data-ttu-id="63652-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63652-126">System.Boolean</span></span>

## <span data-ttu-id="63652-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63652-127">NOTES</span></span>

## <span data-ttu-id="63652-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63652-128">RELATED LINKS</span></span>

[<span data-ttu-id="63652-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="63652-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="63652-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="63652-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="63652-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="63652-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


