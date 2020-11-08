---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: ba64089da3673957eead10ef1301f5c7c4a59467
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938467"
---
# <span data-ttu-id="0f009-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0f009-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="0f009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f009-102">SYNOPSIS</span></span>
<span data-ttu-id="0f009-103">Stream Analytics iş girdilerini alır.</span><span class="sxs-lookup"><span data-stu-id="0f009-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="0f009-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f009-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f009-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f009-105">DESCRIPTION</span></span>
<span data-ttu-id="0f009-106">**Get-AzStreamAnalyticsInput** cmdlet 'ı bir Stream Analytics işinde tanımlanan tüm girdileri listeler veya belirli bir giriş hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0f009-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="0f009-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f009-107">EXAMPLES</span></span>

### <span data-ttu-id="0f009-108">Örnek 1: işte tanımlı girişler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="0f009-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="0f009-109">Bu komut, iş StreamingJob 'da tanımlanan tüm girişlerle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f009-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="0f009-110">Örnek 2: işte tanımlı belirli bir girdi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="0f009-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="0f009-111">Bu komut, iş StreamingJob 'da tanımlanan EntryStream adlı girdi hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="0f009-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="0f009-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f009-112">PARAMETERS</span></span>

### <span data-ttu-id="0f009-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f009-113">-DefaultProfile</span></span>
<span data-ttu-id="0f009-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f009-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f009-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="0f009-115">-JobName</span></span>
<span data-ttu-id="0f009-116">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f009-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0f009-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f009-117">-Name</span></span>
<span data-ttu-id="0f009-118">Alınacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f009-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="0f009-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f009-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f009-120">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f009-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0f009-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f009-121">CommonParameters</span></span>
<span data-ttu-id="0f009-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f009-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f009-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f009-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f009-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f009-124">INPUTS</span></span>

### <span data-ttu-id="0f009-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0f009-125">System.String</span></span>

## <span data-ttu-id="0f009-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f009-126">OUTPUTS</span></span>

### <span data-ttu-id="0f009-127">Microsoft. Azure. Commands. StreamAnalytics. modeller. Psınınput</span><span class="sxs-lookup"><span data-stu-id="0f009-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="0f009-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f009-128">NOTES</span></span>

## <span data-ttu-id="0f009-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f009-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f009-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0f009-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0f009-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0f009-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0f009-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0f009-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)

