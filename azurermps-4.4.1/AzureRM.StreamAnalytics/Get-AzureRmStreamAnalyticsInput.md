---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: e9f4017156a72b1284de8b62d1ae2ebf7d8321ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589939"
---
# <span data-ttu-id="2061e-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2061e-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="2061e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2061e-102">SYNOPSIS</span></span>
<span data-ttu-id="2061e-103">Stream Analytics iş girdilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2061e-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2061e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2061e-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2061e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2061e-105">DESCRIPTION</span></span>
<span data-ttu-id="2061e-106">**Get-AzureRmStreamAnalyticsInput** cmdlet 'ı bir Stream Analytics işinde tanımlanan tüm girdileri listeler veya belirli bir giriş hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2061e-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="2061e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2061e-107">EXAMPLES</span></span>

### <span data-ttu-id="2061e-108">Örnek 1: işte tanımlı girişler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="2061e-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="2061e-109">Bu komut, iş StreamingJob 'da tanımlanan tüm girişlerle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2061e-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="2061e-110">Örnek 2: işte tanımlı belirli bir girdi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="2061e-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="2061e-111">Bu komut, iş StreamingJob 'da tanımlanan EntryStream adlı girdi hakkındaki bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2061e-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="2061e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2061e-112">PARAMETERS</span></span>

### <span data-ttu-id="2061e-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2061e-113">-JobName</span></span>
<span data-ttu-id="2061e-114">Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2061e-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2061e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="2061e-115">-Name</span></span>
<span data-ttu-id="2061e-116">Alınacak Azure Stream Analytics girişinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2061e-116">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="2061e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2061e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2061e-118">Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2061e-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2061e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2061e-119">-DefaultProfile</span></span>
<span data-ttu-id="2061e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2061e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2061e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2061e-121">CommonParameters</span></span>
<span data-ttu-id="2061e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2061e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2061e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2061e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2061e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2061e-124">INPUTS</span></span>

## <span data-ttu-id="2061e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2061e-125">OUTPUTS</span></span>

### <span data-ttu-id="2061e-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. Psınınput, Microsoft. Azure. Commands. StreamAnalytics]</span><span class="sxs-lookup"><span data-stu-id="2061e-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="2061e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2061e-127">NOTES</span></span>

## <span data-ttu-id="2061e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2061e-128">RELATED LINKS</span></span>

[<span data-ttu-id="2061e-129">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2061e-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2061e-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2061e-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="2061e-131">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2061e-131">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


