---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763084"
---
# <span data-ttu-id="2ead4-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2ead4-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="2ead4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ead4-102">SYNOPSIS</span></span>
<span data-ttu-id="2ead4-103">Girişin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="2ead4-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ead4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ead4-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ead4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ead4-105">DESCRIPTION</span></span>
<span data-ttu-id="2ead4-106">**Test-AzureRmStreamAnalyticsInput** cmdlet 'ı, akış çözümlemelerini bir girişe bağlanma olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="2ead4-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="2ead4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ead4-107">EXAMPLES</span></span>

### <span data-ttu-id="2ead4-108">Örnek 1: Giriş akışının bağlantı durumunu sınama</span><span class="sxs-lookup"><span data-stu-id="2ead4-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="2ead4-109">Bu, StreamingJob 'daki giriş girişi akışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="2ead4-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="2ead4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ead4-110">PARAMETERS</span></span>

### <span data-ttu-id="2ead4-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="2ead4-111">-JobName</span></span>
<span data-ttu-id="2ead4-112">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ead4-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2ead4-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ead4-113">-Name</span></span>
<span data-ttu-id="2ead4-114">Sınanacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ead4-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="2ead4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ead4-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ead4-116">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ead4-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2ead4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ead4-117">-DefaultProfile</span></span>
<span data-ttu-id="2ead4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ead4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ead4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ead4-119">CommonParameters</span></span>
<span data-ttu-id="2ead4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ead4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ead4-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ead4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ead4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ead4-122">INPUTS</span></span>

## <span data-ttu-id="2ead4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ead4-123">OUTPUTS</span></span>

### <span data-ttu-id="2ead4-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="2ead4-124">System.Object</span></span>

## <span data-ttu-id="2ead4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ead4-125">NOTES</span></span>

## <span data-ttu-id="2ead4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ead4-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ead4-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2ead4-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2ead4-128">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2ead4-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2ead4-129">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2ead4-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


