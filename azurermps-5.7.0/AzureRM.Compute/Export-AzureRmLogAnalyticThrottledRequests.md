---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: a8deadf4760950eebbec22626bca475439ab0b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590520"
---
# <span data-ttu-id="ff46b-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="ff46b-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="ff46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff46b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff46b-103">Bu abonelik için toplam kısıtlanmış API isteklerini belirtilen zaman penceresinde gösteren günlükleri dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="ff46b-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff46b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff46b-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff46b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff46b-105">DESCRIPTION</span></span>
<span data-ttu-id="ff46b-106">Bu, toplam kısıtlanmış Microsoft. COMPUTE API çağrılarını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ff46b-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="ff46b-107">Günlükler üç seçenekten daha da toplanamaz: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="ff46b-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="ff46b-108">Bu cmdlet 'in yalnızca CRP günlüklerini topladığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="ff46b-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="ff46b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff46b-109">EXAMPLES</span></span>

### <span data-ttu-id="ff46b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff46b-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="ff46b-111">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 arasındaki toplam azaltıldı</span><span class="sxs-lookup"><span data-stu-id="ff46b-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="ff46b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff46b-112">PARAMETERS</span></span>

### <span data-ttu-id="ff46b-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ff46b-113">-AsJob</span></span>
<span data-ttu-id="ff46b-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ff46b-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="ff46b-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="ff46b-116">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="ff46b-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff46b-117">-DefaultProfile</span></span>
<span data-ttu-id="ff46b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff46b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff46b-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="ff46b-119">-FromTime</span></span>
<span data-ttu-id="ff46b-120">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="ff46b-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="ff46b-121">-GroupByOperationName</span></span>
<span data-ttu-id="ff46b-122">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="ff46b-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="ff46b-123">-GroupByResourceName</span></span>
<span data-ttu-id="ff46b-124">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="ff46b-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="ff46b-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="ff46b-126">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="ff46b-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="ff46b-127">-Location</span></span>
<span data-ttu-id="ff46b-128">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="ff46b-128">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="ff46b-129">-ToTime</span></span>
<span data-ttu-id="ff46b-130">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="ff46b-130">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff46b-131">-Confirm</span></span>
<span data-ttu-id="ff46b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff46b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff46b-133">-WhatIf</span></span>
<span data-ttu-id="ff46b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff46b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff46b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff46b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff46b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff46b-136">CommonParameters</span></span>
<span data-ttu-id="ff46b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff46b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff46b-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff46b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff46b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff46b-139">INPUTS</span></span>

### <span data-ttu-id="ff46b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff46b-140">System.String</span></span>

## <span data-ttu-id="ff46b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff46b-141">OUTPUTS</span></span>

### <span data-ttu-id="ff46b-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="ff46b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="ff46b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff46b-143">NOTES</span></span>

## <span data-ttu-id="ff46b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff46b-144">RELATED LINKS</span></span>
