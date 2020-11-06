---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8b63dbd497edce422fc4cf70182ca8259721d8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572594"
---
# <span data-ttu-id="7665b-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7665b-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="7665b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7665b-102">SYNOPSIS</span></span>
<span data-ttu-id="7665b-103">Stream Analytics iş girdilerini alır.</span><span class="sxs-lookup"><span data-stu-id="7665b-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7665b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7665b-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7665b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7665b-105">DESCRIPTION</span></span>
<span data-ttu-id="7665b-106">**Get-AzureRmStreamAnalyticsInput** cmdlet 'ı bir Stream Analytics işinde tanımlanan tüm girdileri listeler veya belirli bir giriş hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7665b-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="7665b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7665b-107">EXAMPLES</span></span>

### <span data-ttu-id="7665b-108">Örnek 1: işte tanımlı girişler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="7665b-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="7665b-109">Bu komut, iş StreamingJob 'da tanımlanan tüm girişlerle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7665b-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="7665b-110">Örnek 2: işte tanımlı belirli bir girdi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="7665b-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="7665b-111">Bu komut, iş StreamingJob 'da tanımlanan EntryStream adlı girdi hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7665b-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="7665b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7665b-112">PARAMETERS</span></span>

### <span data-ttu-id="7665b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7665b-113">-DefaultProfile</span></span>
<span data-ttu-id="7665b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7665b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7665b-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="7665b-115">-JobName</span></span>
<span data-ttu-id="7665b-116">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7665b-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7665b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7665b-117">-Name</span></span>
<span data-ttu-id="7665b-118">Alınacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7665b-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="7665b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7665b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7665b-120">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7665b-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="7665b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7665b-121">CommonParameters</span></span>
<span data-ttu-id="7665b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7665b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7665b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7665b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7665b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7665b-124">INPUTS</span></span>

### <span data-ttu-id="7665b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7665b-125">System.String</span></span>

## <span data-ttu-id="7665b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7665b-126">OUTPUTS</span></span>

### <span data-ttu-id="7665b-127">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psınınput</span><span class="sxs-lookup"><span data-stu-id="7665b-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="7665b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7665b-128">NOTES</span></span>

## <span data-ttu-id="7665b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7665b-129">RELATED LINKS</span></span>

[<span data-ttu-id="7665b-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7665b-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7665b-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7665b-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="7665b-132">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="7665b-132">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


