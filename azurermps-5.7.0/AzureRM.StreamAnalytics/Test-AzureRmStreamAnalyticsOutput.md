---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592858"
---
# <span data-ttu-id="31f34-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31f34-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="31f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f34-102">SYNOPSIS</span></span>
<span data-ttu-id="31f34-103">Çıktının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="31f34-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31f34-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31f34-105">DESCRIPTION</span></span>
<span data-ttu-id="31f34-106">**Test-AzureRmStreamAnalyticsOutput** cmdlet 'ı, akış çözümlemelerini çıktıya bağlama olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="31f34-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="31f34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31f34-107">EXAMPLES</span></span>

### <span data-ttu-id="31f34-108">Örnek 1: çıktının bağlantı durumunu test etme</span><span class="sxs-lookup"><span data-stu-id="31f34-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="31f34-109">Bu, StreamingJob 'da çıkış çıkışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="31f34-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="31f34-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31f34-110">PARAMETERS</span></span>

### <span data-ttu-id="31f34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f34-111">-DefaultProfile</span></span>
<span data-ttu-id="31f34-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31f34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31f34-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="31f34-113">-JobName</span></span>
<span data-ttu-id="31f34-114">İstenen Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31f34-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="31f34-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="31f34-115">-Name</span></span>
<span data-ttu-id="31f34-116">Sınanacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31f34-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f34-117">-ResourceGroupName</span></span>
<span data-ttu-id="31f34-118">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31f34-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="31f34-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f34-119">CommonParameters</span></span>
<span data-ttu-id="31f34-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31f34-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f34-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f34-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f34-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31f34-122">INPUTS</span></span>

### <span data-ttu-id="31f34-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="31f34-123">None</span></span>
<span data-ttu-id="31f34-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="31f34-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31f34-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31f34-125">OUTPUTS</span></span>

### <span data-ttu-id="31f34-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="31f34-126">System.Object</span></span>

## <span data-ttu-id="31f34-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31f34-127">NOTES</span></span>

## <span data-ttu-id="31f34-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31f34-128">RELATED LINKS</span></span>

[<span data-ttu-id="31f34-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31f34-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="31f34-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31f34-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="31f34-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="31f34-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


