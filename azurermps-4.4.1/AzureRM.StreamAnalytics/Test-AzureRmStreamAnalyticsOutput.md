---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5c961289267b0680a88cd16d58574c906a9f4408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592161"
---
# <span data-ttu-id="817c3-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="817c3-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="817c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="817c3-102">SYNOPSIS</span></span>
<span data-ttu-id="817c3-103">Çıktının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="817c3-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="817c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="817c3-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="817c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="817c3-105">DESCRIPTION</span></span>
<span data-ttu-id="817c3-106">**Test-AzureRmStreamAnalyticsOutput** cmdlet 'ı, akış çözümlemelerini çıktıya bağlama olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="817c3-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="817c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="817c3-107">EXAMPLES</span></span>

### <span data-ttu-id="817c3-108">Örnek 1: çıktının bağlantı durumunu test etme</span><span class="sxs-lookup"><span data-stu-id="817c3-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="817c3-109">Bu, StreamingJob 'da çıkış çıkışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="817c3-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="817c3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="817c3-110">PARAMETERS</span></span>

### <span data-ttu-id="817c3-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="817c3-111">-JobName</span></span>
<span data-ttu-id="817c3-112">İstenen Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="817c3-112">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="817c3-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="817c3-113">-Name</span></span>
<span data-ttu-id="817c3-114">Sınanacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="817c3-114">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="817c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="817c3-116">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="817c3-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="817c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817c3-117">-DefaultProfile</span></span>
<span data-ttu-id="817c3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="817c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="817c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817c3-119">CommonParameters</span></span>
<span data-ttu-id="817c3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="817c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817c3-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817c3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817c3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="817c3-122">INPUTS</span></span>

## <span data-ttu-id="817c3-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="817c3-123">OUTPUTS</span></span>

### <span data-ttu-id="817c3-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="817c3-124">System.Object</span></span>

## <span data-ttu-id="817c3-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="817c3-125">NOTES</span></span>

## <span data-ttu-id="817c3-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="817c3-126">RELATED LINKS</span></span>

[<span data-ttu-id="817c3-127">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="817c3-127">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="817c3-128">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="817c3-128">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="817c3-129">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="817c3-129">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


