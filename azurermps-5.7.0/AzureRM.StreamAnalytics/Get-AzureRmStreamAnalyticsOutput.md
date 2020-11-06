---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: ff9ab6f4efe5794b3f1eca9b8ceab91b5cd11316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591539"
---
# <span data-ttu-id="f52d5-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f52d5-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f52d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f52d5-103">Belirtilen bir Stream Analytics işinde veya çıktısında tanımlanan çıktıları alır.</span><span class="sxs-lookup"><span data-stu-id="f52d5-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f52d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f52d5-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f52d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f52d5-105">DESCRIPTION</span></span>
<span data-ttu-id="f52d5-106">**Get-AzureRmStreamAnalyticsOutput** cmdlet 'i belirtilen bir Stream Analytics işinde tanımlanan tüm çıktıları listeler veya belirli bir çıkış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f52d5-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="f52d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f52d5-107">EXAMPLES</span></span>

### <span data-ttu-id="f52d5-108">Örnek 1: iş çıktıları hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f52d5-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="f52d5-109">Bu komut, iş StreamingJob 'da tanımlanan çıkışlar hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f52d5-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="f52d5-110">Örnek 2: belirli bir iş çıkışı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="f52d5-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f52d5-111">Bu komut, iş StreamingJob 'da tanımlanan output adındaki çıktı hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f52d5-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="f52d5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f52d5-112">PARAMETERS</span></span>

### <span data-ttu-id="f52d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52d5-113">-DefaultProfile</span></span>
<span data-ttu-id="f52d5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f52d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f52d5-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f52d5-115">-JobName</span></span>
<span data-ttu-id="f52d5-116">Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52d5-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f52d5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f52d5-117">-Name</span></span>
<span data-ttu-id="f52d5-118">Alınacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52d5-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="f52d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f52d5-120">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52d5-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f52d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52d5-121">CommonParameters</span></span>
<span data-ttu-id="f52d5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f52d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52d5-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52d5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f52d5-124">INPUTS</span></span>

### <span data-ttu-id="f52d5-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f52d5-125">None</span></span>
<span data-ttu-id="f52d5-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f52d5-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f52d5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f52d5-127">OUTPUTS</span></span>

### <span data-ttu-id="f52d5-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modeller. Psoutınput</span><span class="sxs-lookup"><span data-stu-id="f52d5-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="f52d5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f52d5-129">NOTES</span></span>

## <span data-ttu-id="f52d5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f52d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="f52d5-131">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f52d5-131">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f52d5-132">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f52d5-132">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f52d5-133">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f52d5-133">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


