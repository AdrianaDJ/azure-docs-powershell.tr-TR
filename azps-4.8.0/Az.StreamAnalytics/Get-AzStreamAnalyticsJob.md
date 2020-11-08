---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107496"
---
# <span data-ttu-id="93a90-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93a90-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="93a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93a90-102">SYNOPSIS</span></span>
<span data-ttu-id="93a90-103">Stream Analytics iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="93a90-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="93a90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93a90-104">SYNTAX</span></span>

### <span data-ttu-id="93a90-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93a90-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93a90-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="93a90-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93a90-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="93a90-107">DESCRIPTION</span></span>
<span data-ttu-id="93a90-108">**Get-AzStreamAnalyticsJob** cmdlet 'ı, Azure aboneliği veya belirtilen kaynak grubunda tanımlanan tüm akış analizi işlerini listeler veya kaynak grubundaki belirli bir iş hakkında iş bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="93a90-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="93a90-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93a90-109">EXAMPLES</span></span>

### <span data-ttu-id="93a90-110">Örnek 1: abonelikteki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="93a90-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="93a90-111">Bu komut, Azure aboneliğindeki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="93a90-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="93a90-112">Örnek 2: kaynak grubundaki tüm işler hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="93a90-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="93a90-113">Bu komut StreamAnalytics-default-West-US kaynak grubundaki tüm Stream Analytics işleriyle ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="93a90-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="93a90-114">Örnek 3: kaynak grubundaki belirli bir iş hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="93a90-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="93a90-115">Bu komut StreamAnalytics-default-West-US kaynak grubundaki Stream Analytics iş StreamingJob hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="93a90-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="93a90-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93a90-116">PARAMETERS</span></span>

### <span data-ttu-id="93a90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a90-117">-DefaultProfile</span></span>
<span data-ttu-id="93a90-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93a90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93a90-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="93a90-119">-Name</span></span>
<span data-ttu-id="93a90-120">Alınacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93a90-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a90-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="93a90-121">-NoExpand</span></span>
<span data-ttu-id="93a90-122">Cmdlet 'in Azure Stream Analytics işini geri ala, ancak girişleri, çıktıları ve dönüşümdeki bilgileri döndürmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93a90-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="93a90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a90-123">-ResourceGroupName</span></span>
<span data-ttu-id="93a90-124">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93a90-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a90-125">CommonParameters</span></span>
<span data-ttu-id="93a90-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93a90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a90-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a90-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a90-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93a90-128">INPUTS</span></span>

### <span data-ttu-id="93a90-129">System. String</span><span class="sxs-lookup"><span data-stu-id="93a90-129">System.String</span></span>

### <span data-ttu-id="93a90-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93a90-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93a90-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93a90-131">OUTPUTS</span></span>

### <span data-ttu-id="93a90-132">Microsoft. Azure. Commands. StreamAnalytics. modeller. PSJob</span><span class="sxs-lookup"><span data-stu-id="93a90-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="93a90-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93a90-133">NOTES</span></span>

## <span data-ttu-id="93a90-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93a90-134">RELATED LINKS</span></span>

[<span data-ttu-id="93a90-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93a90-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="93a90-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93a90-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="93a90-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93a90-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="93a90-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93a90-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


