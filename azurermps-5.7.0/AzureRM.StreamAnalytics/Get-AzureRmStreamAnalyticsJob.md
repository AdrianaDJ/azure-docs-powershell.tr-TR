---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588689"
---
# <span data-ttu-id="49e35-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="49e35-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="49e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49e35-102">SYNOPSIS</span></span>
<span data-ttu-id="49e35-103">Stream Analytics iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="49e35-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49e35-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49e35-104">SYNTAX</span></span>

### <span data-ttu-id="49e35-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49e35-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49e35-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="49e35-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49e35-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="49e35-107">DESCRIPTION</span></span>
<span data-ttu-id="49e35-108">**Get-AzureRmStreamAnalyticsJob** cmdlet 'ı, Azure aboneliği veya belirtilen kaynak grubunda tanımlanan tüm akış analizi işlerini listeler veya kaynak grubundaki belirli bir iş hakkında iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="49e35-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="49e35-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49e35-109">EXAMPLES</span></span>

### <span data-ttu-id="49e35-110">Örnek 1: abonelikteki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="49e35-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="49e35-111">Bu komut, Azure aboneliğindeki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="49e35-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="49e35-112">Örnek 2: kaynak grubundaki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="49e35-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="49e35-113">Bu komut StreamAnalytics-default-West-US kaynak grubundaki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="49e35-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="49e35-114">Örnek 3: kaynak grubundaki belirli bir iş hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="49e35-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="49e35-115">Bu komut StreamAnalytics-default-West-US kaynak grubundaki Stream Analytics iş StreamingJob hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="49e35-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="49e35-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49e35-116">PARAMETERS</span></span>

### <span data-ttu-id="49e35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e35-117">-DefaultProfile</span></span>
<span data-ttu-id="49e35-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49e35-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e35-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="49e35-119">-Name</span></span>
<span data-ttu-id="49e35-120">Alınacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49e35-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e35-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="49e35-121">-NoExpand</span></span>
<span data-ttu-id="49e35-122">Cmdlet 'in Azure Stream Analytics işini geri ala, ancak girişleri, çıktıları ve dönüşümdeki bilgileri döndürmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="49e35-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e35-123">-ResourceGroupName</span></span>
<span data-ttu-id="49e35-124">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49e35-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49e35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e35-125">CommonParameters</span></span>
<span data-ttu-id="49e35-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49e35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e35-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e35-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e35-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49e35-128">INPUTS</span></span>

### <span data-ttu-id="49e35-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="49e35-129">None</span></span>
<span data-ttu-id="49e35-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="49e35-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49e35-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49e35-131">OUTPUTS</span></span>

### <span data-ttu-id="49e35-132">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. PSJob, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49e35-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="49e35-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49e35-133">NOTES</span></span>

## <span data-ttu-id="49e35-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49e35-134">RELATED LINKS</span></span>

[<span data-ttu-id="49e35-135">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="49e35-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="49e35-136">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="49e35-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="49e35-137">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="49e35-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="49e35-138">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="49e35-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


