---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: b19a8359f3267d848d475028fe0cee2123949f7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753906"
---
# <span data-ttu-id="4c46a-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4c46a-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4c46a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c46a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c46a-103">Girişin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="4c46a-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="4c46a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c46a-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c46a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c46a-105">DESCRIPTION</span></span>
<span data-ttu-id="4c46a-106">**Test-AzStreamAnalyticsInput** cmdlet 'ı, akış çözümlemelerini bir girişe bağlanma olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="4c46a-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="4c46a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c46a-107">EXAMPLES</span></span>

### <span data-ttu-id="4c46a-108">Örnek 1: Giriş akışının bağlantı durumunu sınama</span><span class="sxs-lookup"><span data-stu-id="4c46a-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4c46a-109">Bu, StreamingJob 'daki giriş girişi akışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="4c46a-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="4c46a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c46a-110">PARAMETERS</span></span>

### <span data-ttu-id="4c46a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c46a-111">-DefaultProfile</span></span>
<span data-ttu-id="4c46a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c46a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c46a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4c46a-113">-JobName</span></span>
<span data-ttu-id="4c46a-114">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c46a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4c46a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c46a-115">-Name</span></span>
<span data-ttu-id="4c46a-116">Sınanacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c46a-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="4c46a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c46a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c46a-118">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c46a-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4c46a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c46a-119">CommonParameters</span></span>
<span data-ttu-id="4c46a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c46a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c46a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c46a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c46a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c46a-122">INPUTS</span></span>

### <span data-ttu-id="4c46a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4c46a-123">System.String</span></span>

## <span data-ttu-id="4c46a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c46a-124">OUTPUTS</span></span>

### <span data-ttu-id="4c46a-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c46a-125">System.Boolean</span></span>

## <span data-ttu-id="4c46a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c46a-126">NOTES</span></span>

## <span data-ttu-id="4c46a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c46a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c46a-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4c46a-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4c46a-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4c46a-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4c46a-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4c46a-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

