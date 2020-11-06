---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 6256fc57d4084a55b2288875b56c6c616b16f8b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593603"
---
# <span data-ttu-id="11487-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="11487-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="11487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11487-102">SYNOPSIS</span></span>
<span data-ttu-id="11487-103">Girişin bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="11487-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11487-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11487-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11487-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11487-105">DESCRIPTION</span></span>
<span data-ttu-id="11487-106">**Test-AzureRmStreamAnalyticsInput** cmdlet 'ı, akış çözümlemelerini bir girişe bağlanma olanağını sınar.</span><span class="sxs-lookup"><span data-stu-id="11487-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="11487-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11487-107">EXAMPLES</span></span>

### <span data-ttu-id="11487-108">Örnek 1: Giriş akışının bağlantı durumunu sınama</span><span class="sxs-lookup"><span data-stu-id="11487-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="11487-109">Bu, StreamingJob 'daki giriş girişi akışının bağlantı durumunu sınar.</span><span class="sxs-lookup"><span data-stu-id="11487-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="11487-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11487-110">PARAMETERS</span></span>

### <span data-ttu-id="11487-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11487-111">-DefaultProfile</span></span>
<span data-ttu-id="11487-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11487-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11487-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="11487-113">-JobName</span></span>
<span data-ttu-id="11487-114">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11487-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="11487-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="11487-115">-Name</span></span>
<span data-ttu-id="11487-116">Sınanacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11487-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="11487-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11487-117">-ResourceGroupName</span></span>
<span data-ttu-id="11487-118">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="11487-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="11487-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11487-119">CommonParameters</span></span>
<span data-ttu-id="11487-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11487-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11487-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11487-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11487-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11487-122">INPUTS</span></span>

### <span data-ttu-id="11487-123">System. String</span><span class="sxs-lookup"><span data-stu-id="11487-123">System.String</span></span>

## <span data-ttu-id="11487-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11487-124">OUTPUTS</span></span>

### <span data-ttu-id="11487-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11487-125">System.Boolean</span></span>

## <span data-ttu-id="11487-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11487-126">NOTES</span></span>

## <span data-ttu-id="11487-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11487-127">RELATED LINKS</span></span>

[<span data-ttu-id="11487-128">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="11487-128">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="11487-129">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="11487-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="11487-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="11487-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


