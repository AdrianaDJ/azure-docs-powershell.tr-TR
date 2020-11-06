---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: c675a8da84e61b659c593cc1f963dd1b07c7f316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572590"
---
# <span data-ttu-id="f1aad-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1aad-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f1aad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1aad-102">SYNOPSIS</span></span>
<span data-ttu-id="f1aad-103">Belirtilen bir Stream Analytics işinde veya çıktısında tanımlanan çıktıları alır.</span><span class="sxs-lookup"><span data-stu-id="f1aad-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1aad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1aad-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1aad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1aad-105">DESCRIPTION</span></span>
<span data-ttu-id="f1aad-106">**Get-AzureRmStreamAnalyticsOutput** cmdlet 'i belirtilen bir Stream Analytics işinde tanımlanan tüm çıktıları listeler veya belirli bir çıkış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f1aad-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="f1aad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1aad-107">EXAMPLES</span></span>

### <span data-ttu-id="f1aad-108">Örnek 1: iş çıktıları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f1aad-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="f1aad-109">Bu komut, iş StreamingJob 'da tanımlanan çıkışlar hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1aad-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="f1aad-110">Örnek 2: belirli bir iş çıkışı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f1aad-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f1aad-111">Bu komut, iş StreamingJob 'da tanımlanan output adındaki çıktı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1aad-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="f1aad-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1aad-112">PARAMETERS</span></span>

### <span data-ttu-id="f1aad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1aad-113">-DefaultProfile</span></span>
<span data-ttu-id="f1aad-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1aad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1aad-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f1aad-115">-JobName</span></span>
<span data-ttu-id="f1aad-116">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1aad-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1aad-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1aad-117">-Name</span></span>
<span data-ttu-id="f1aad-118">Alınacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1aad-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="f1aad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1aad-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1aad-120">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1aad-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f1aad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1aad-121">CommonParameters</span></span>
<span data-ttu-id="f1aad-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1aad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1aad-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1aad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1aad-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1aad-124">INPUTS</span></span>

### <span data-ttu-id="f1aad-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f1aad-125">System.String</span></span>

## <span data-ttu-id="f1aad-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1aad-126">OUTPUTS</span></span>

### <span data-ttu-id="f1aad-127">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput</span><span class="sxs-lookup"><span data-stu-id="f1aad-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="f1aad-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1aad-128">NOTES</span></span>

## <span data-ttu-id="f1aad-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1aad-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1aad-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1aad-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f1aad-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1aad-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f1aad-132">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f1aad-132">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


