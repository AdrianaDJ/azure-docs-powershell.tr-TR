---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110142"
---
# <span data-ttu-id="9536d-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9536d-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="9536d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9536d-102">SYNOPSIS</span></span>
<span data-ttu-id="9536d-103">Çıktının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="9536d-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="9536d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9536d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9536d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9536d-105">DESCRIPTION</span></span>
<span data-ttu-id="9536d-106">**Test-AzStreamAnalyticsOutput** cmdlet 'ı, akış çözümlemelerini çıktıya bağlama olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="9536d-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="9536d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9536d-107">EXAMPLES</span></span>

### <span data-ttu-id="9536d-108">Örnek 1: çıktının bağlantı durumunu test etme</span><span class="sxs-lookup"><span data-stu-id="9536d-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="9536d-109">Bu, StreamingJob 'da çıkış çıkışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="9536d-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="9536d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9536d-110">PARAMETERS</span></span>

### <span data-ttu-id="9536d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9536d-111">-DefaultProfile</span></span>
<span data-ttu-id="9536d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9536d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9536d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="9536d-113">-JobName</span></span>
<span data-ttu-id="9536d-114">İstenen Azure Stream Analytics çıkışının ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9536d-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9536d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9536d-115">-Name</span></span>
<span data-ttu-id="9536d-116">Sınanacak Azure Stream Analytics çıktısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9536d-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="9536d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9536d-117">-ResourceGroupName</span></span>
<span data-ttu-id="9536d-118">Azure Stream Analytics çıktısının ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9536d-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9536d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9536d-119">CommonParameters</span></span>
<span data-ttu-id="9536d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9536d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9536d-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9536d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9536d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9536d-122">INPUTS</span></span>

### <span data-ttu-id="9536d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9536d-123">System.String</span></span>

## <span data-ttu-id="9536d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9536d-124">OUTPUTS</span></span>

### <span data-ttu-id="9536d-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9536d-125">System.Boolean</span></span>

## <span data-ttu-id="9536d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9536d-126">NOTES</span></span>

## <span data-ttu-id="9536d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9536d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9536d-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9536d-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9536d-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9536d-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9536d-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9536d-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


