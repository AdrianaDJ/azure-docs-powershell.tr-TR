---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: a2f577286a411287886c27863eb72e574b771bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763088"
---
# <span data-ttu-id="45d6d-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="45d6d-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="45d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="45d6d-103">Akış analizlerini bir işleve bağlanıp bağlanamamı sınar.</span><span class="sxs-lookup"><span data-stu-id="45d6d-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45d6d-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45d6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45d6d-105">DESCRIPTION</span></span>
<span data-ttu-id="45d6d-106">**Test-AzureRmStreamAnalyticsFunction** cmdlet 'ı Azure Stream analizin bir işleve bağlanıp bağlanamadan sınar.</span><span class="sxs-lookup"><span data-stu-id="45d6d-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="45d6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45d6d-107">EXAMPLES</span></span>

### <span data-ttu-id="45d6d-108">Örnek 1: Stream Analytics işlevini sınama</span><span class="sxs-lookup"><span data-stu-id="45d6d-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="45d6d-109">Bu komut, StreamJob22 adındaki işte ScoreTweet adındaki işlevin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="45d6d-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="45d6d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45d6d-110">PARAMETERS</span></span>

### <span data-ttu-id="45d6d-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="45d6d-111">-JobName</span></span>
<span data-ttu-id="45d6d-112">İşlevin ait olduğu akış analizi işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d6d-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="45d6d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="45d6d-113">-Name</span></span>
<span data-ttu-id="45d6d-114">Bu cmdlet 'in test olduğu Stream Analytics işlevinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d6d-114">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="45d6d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d6d-115">-ResourceGroupName</span></span>
<span data-ttu-id="45d6d-116">Bir Stream Analytics işlevinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45d6d-116">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="45d6d-117">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki bir işlevi sınar.</span><span class="sxs-lookup"><span data-stu-id="45d6d-117">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="45d6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d6d-118">-DefaultProfile</span></span>
<span data-ttu-id="45d6d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45d6d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d6d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d6d-120">CommonParameters</span></span>
<span data-ttu-id="45d6d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45d6d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d6d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d6d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d6d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45d6d-123">INPUTS</span></span>

## <span data-ttu-id="45d6d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45d6d-124">OUTPUTS</span></span>

### <span data-ttu-id="45d6d-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="45d6d-125">System.Object</span></span>

## <span data-ttu-id="45d6d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45d6d-126">NOTES</span></span>

## <span data-ttu-id="45d6d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45d6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="45d6d-128">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="45d6d-128">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="45d6d-129">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="45d6d-129">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="45d6d-130">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="45d6d-130">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


