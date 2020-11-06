---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590594"
---
# <span data-ttu-id="81906-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81906-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="81906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81906-102">SYNOPSIS</span></span>
<span data-ttu-id="81906-103">Stream Analytics iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="81906-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81906-104">SYNTAX</span></span>

### <span data-ttu-id="81906-105">Verilen kaynak grubundaki Stream Analytics nesneleri için</span><span class="sxs-lookup"><span data-stu-id="81906-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81906-106">Verilen abonelikteki Stream Analytics nesneleri için</span><span class="sxs-lookup"><span data-stu-id="81906-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81906-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81906-107">DESCRIPTION</span></span>
<span data-ttu-id="81906-108">**Get-AzureRmStreamAnalyticsJob** cmdlet 'ı, Azure aboneliği veya belirtilen kaynak grubunda tanımlanan tüm akış analizi işlerini listeler veya kaynak grubundaki belirli bir iş hakkında iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="81906-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="81906-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81906-109">EXAMPLES</span></span>

### <span data-ttu-id="81906-110">Örnek 1: abonelikteki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="81906-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="81906-111">Bu komut, Azure aboneliğindeki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="81906-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="81906-112">Örnek 2: kaynak grubundaki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="81906-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="81906-113">Bu komut StreamAnalytics-default-West-US kaynak grubundaki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="81906-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="81906-114">Örnek 3: kaynak grubundaki belirli bir iş hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="81906-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="81906-115">Bu komut StreamAnalytics-default-West-US kaynak grubundaki Stream Analytics iş StreamingJob hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="81906-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="81906-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81906-116">PARAMETERS</span></span>

### <span data-ttu-id="81906-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="81906-117">-Name</span></span>
<span data-ttu-id="81906-118">Alınacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81906-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81906-119">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="81906-119">-NoExpand</span></span>
<span data-ttu-id="81906-120">Cmdlet 'in Azure Stream Analytics işini geri ala, ancak girişleri, çıktıları ve dönüşümdeki bilgileri döndürmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="81906-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81906-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81906-121">-ResourceGroupName</span></span>
<span data-ttu-id="81906-122">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81906-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81906-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81906-123">-DefaultProfile</span></span>
<span data-ttu-id="81906-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81906-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81906-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81906-125">CommonParameters</span></span>
<span data-ttu-id="81906-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81906-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81906-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81906-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81906-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81906-128">INPUTS</span></span>

## <span data-ttu-id="81906-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81906-129">OUTPUTS</span></span>

### <span data-ttu-id="81906-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. PSJob, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="81906-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="81906-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81906-131">NOTES</span></span>

## <span data-ttu-id="81906-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81906-132">RELATED LINKS</span></span>

[<span data-ttu-id="81906-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81906-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="81906-134">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81906-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="81906-135">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81906-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="81906-136">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81906-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


