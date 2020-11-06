---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588578"
---
# <span data-ttu-id="03a71-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="03a71-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="03a71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a71-102">SYNOPSIS</span></span>
<span data-ttu-id="03a71-103">Bu abonelik için toplam kısıtlanmış API isteklerini belirtilen zaman penceresinde gösteren günlükleri dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="03a71-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03a71-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03a71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03a71-105">DESCRIPTION</span></span>
<span data-ttu-id="03a71-106">Bu, toplam kısıtlanmış Microsoft. COMPUTE API çağrılarını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="03a71-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="03a71-107">Günlükler üç seçenekten daha da toplanamaz: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="03a71-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="03a71-108">Bu cmdlet 'in yalnızca CRP günlüklerini topladığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="03a71-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="03a71-109">Hesaplama kaynak sağlayıcısının API azaltması hakkında genel bilgi için bkz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="03a71-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="03a71-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03a71-110">EXAMPLES</span></span>

### <span data-ttu-id="03a71-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="03a71-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="03a71-112">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 arasındaki toplam azaltıldı</span><span class="sxs-lookup"><span data-stu-id="03a71-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="03a71-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03a71-113">PARAMETERS</span></span>

### <span data-ttu-id="03a71-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="03a71-114">-AsJob</span></span>
<span data-ttu-id="03a71-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="03a71-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03a71-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="03a71-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="03a71-117">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="03a71-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a71-118">-DefaultProfile</span></span>
<span data-ttu-id="03a71-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03a71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a71-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="03a71-120">-FromTime</span></span>
<span data-ttu-id="03a71-121">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="03a71-121">From time of the query</span></span>

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

### <span data-ttu-id="03a71-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="03a71-122">-GroupByOperationName</span></span>
<span data-ttu-id="03a71-123">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="03a71-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="03a71-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="03a71-124">-GroupByResourceName</span></span>
<span data-ttu-id="03a71-125">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="03a71-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="03a71-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="03a71-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="03a71-127">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="03a71-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="03a71-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="03a71-128">-Location</span></span>
<span data-ttu-id="03a71-129">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="03a71-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="03a71-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="03a71-130">-ToTime</span></span>
<span data-ttu-id="03a71-131">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="03a71-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a71-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="03a71-132">-Confirm</span></span>
<span data-ttu-id="03a71-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03a71-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a71-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a71-134">-WhatIf</span></span>
<span data-ttu-id="03a71-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03a71-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a71-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03a71-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a71-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a71-137">CommonParameters</span></span>
<span data-ttu-id="03a71-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03a71-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a71-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a71-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a71-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03a71-140">INPUTS</span></span>

### <span data-ttu-id="03a71-141">System. String</span><span class="sxs-lookup"><span data-stu-id="03a71-141">System.String</span></span>

## <span data-ttu-id="03a71-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03a71-142">OUTPUTS</span></span>

### <span data-ttu-id="03a71-143">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="03a71-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="03a71-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03a71-144">NOTES</span></span>

## <span data-ttu-id="03a71-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03a71-145">RELATED LINKS</span></span>
