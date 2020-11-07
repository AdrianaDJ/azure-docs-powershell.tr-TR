---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 65a2dd49b0beee557f062201f27a7235c28d5283
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917480"
---
# <span data-ttu-id="22958-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="22958-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="22958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22958-102">SYNOPSIS</span></span>
<span data-ttu-id="22958-103">Bu abonelik için toplam kısıtlanmış API isteklerini belirtilen zaman penceresinde gösteren günlükleri dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="22958-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="22958-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22958-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22958-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22958-105">DESCRIPTION</span></span>
<span data-ttu-id="22958-106">Bu, toplam kısıtlanmış Microsoft. COMPUTE API çağrılarını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="22958-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="22958-107">Günlükler üç seçenekten daha da toplanamaz: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="22958-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="22958-108">Bu cmdlet 'in yalnızca CRP günlüklerini topladığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="22958-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="22958-109">Hesaplama kaynak sağlayıcısının API azaltması hakkında genel bilgi için bkz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="22958-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="22958-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22958-110">EXAMPLES</span></span>

### <span data-ttu-id="22958-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22958-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="22958-112">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 arasındaki toplam azaltıldı</span><span class="sxs-lookup"><span data-stu-id="22958-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="22958-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22958-113">PARAMETERS</span></span>

### <span data-ttu-id="22958-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="22958-114">-AsJob</span></span>
<span data-ttu-id="22958-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="22958-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="22958-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="22958-117">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="22958-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22958-118">-DefaultProfile</span></span>
<span data-ttu-id="22958-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22958-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22958-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="22958-120">-FromTime</span></span>
<span data-ttu-id="22958-121">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="22958-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="22958-122">-GroupByOperationName</span></span>
<span data-ttu-id="22958-123">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="22958-123">Group query result by Operation Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="22958-124">-GroupByResourceName</span></span>
<span data-ttu-id="22958-125">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="22958-125">Group query result by Resource Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="22958-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="22958-127">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="22958-127">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="22958-128">-Location</span></span>
<span data-ttu-id="22958-129">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="22958-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="22958-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="22958-130">-ToTime</span></span>
<span data-ttu-id="22958-131">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="22958-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="22958-132">-Confirm</span></span>
<span data-ttu-id="22958-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22958-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22958-134">-WhatIf</span></span>
<span data-ttu-id="22958-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22958-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22958-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22958-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22958-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22958-137">CommonParameters</span></span>
<span data-ttu-id="22958-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22958-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22958-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22958-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22958-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22958-140">INPUTS</span></span>

### <span data-ttu-id="22958-141">System. String</span><span class="sxs-lookup"><span data-stu-id="22958-141">System.String</span></span>

## <span data-ttu-id="22958-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22958-142">OUTPUTS</span></span>

### <span data-ttu-id="22958-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="22958-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="22958-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22958-144">NOTES</span></span>

## <span data-ttu-id="22958-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22958-145">RELATED LINKS</span></span>
