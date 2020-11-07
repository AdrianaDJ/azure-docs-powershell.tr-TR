---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937063"
---
# <span data-ttu-id="90a51-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="90a51-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="90a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a51-102">SYNOPSIS</span></span>
<span data-ttu-id="90a51-103">Bu abonelik için toplam kısıtlanmış API isteklerini belirtilen zaman penceresinde gösteren günlükleri dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="90a51-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="90a51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90a51-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90a51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90a51-105">DESCRIPTION</span></span>
<span data-ttu-id="90a51-106">Bu, toplam kısıtlanmış Microsoft. COMPUTE API çağrılarını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="90a51-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="90a51-107">Günlükler üç seçenekten daha da toplanamaz: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="90a51-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="90a51-108">Bu cmdlet 'in yalnızca CRP günlüklerini topladığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="90a51-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="90a51-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90a51-109">EXAMPLES</span></span>

### <span data-ttu-id="90a51-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90a51-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="90a51-111">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 arasındaki toplam azaltıldı</span><span class="sxs-lookup"><span data-stu-id="90a51-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="90a51-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90a51-112">PARAMETERS</span></span>

### <span data-ttu-id="90a51-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="90a51-113">-AsJob</span></span>
<span data-ttu-id="90a51-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="90a51-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90a51-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="90a51-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="90a51-116">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="90a51-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="90a51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a51-117">-DefaultProfile</span></span>
<span data-ttu-id="90a51-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90a51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90a51-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="90a51-119">-FromTime</span></span>
<span data-ttu-id="90a51-120">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="90a51-120">From time of the query</span></span>

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

### <span data-ttu-id="90a51-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="90a51-121">-GroupByOperationName</span></span>
<span data-ttu-id="90a51-122">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="90a51-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="90a51-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="90a51-123">-GroupByResourceName</span></span>
<span data-ttu-id="90a51-124">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="90a51-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="90a51-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="90a51-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="90a51-126">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="90a51-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="90a51-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="90a51-127">-Location</span></span>
<span data-ttu-id="90a51-128">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="90a51-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="90a51-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="90a51-129">-ToTime</span></span>
<span data-ttu-id="90a51-130">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="90a51-130">To time of the query</span></span>

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

### <span data-ttu-id="90a51-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="90a51-131">-Confirm</span></span>
<span data-ttu-id="90a51-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90a51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a51-133">-WhatIf</span></span>
<span data-ttu-id="90a51-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90a51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a51-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90a51-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a51-136">CommonParameters</span></span>
<span data-ttu-id="90a51-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90a51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a51-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a51-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a51-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90a51-139">INPUTS</span></span>

### <span data-ttu-id="90a51-140">System. String</span><span class="sxs-lookup"><span data-stu-id="90a51-140">System.String</span></span>

## <span data-ttu-id="90a51-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90a51-141">OUTPUTS</span></span>

### <span data-ttu-id="90a51-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="90a51-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="90a51-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90a51-143">NOTES</span></span>

## <span data-ttu-id="90a51-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90a51-144">RELATED LINKS</span></span>

