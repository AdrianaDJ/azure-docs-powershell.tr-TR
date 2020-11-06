---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: c4008e9b6587e0b6c5b8ed56057490b0aad8764f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592784"
---
# <span data-ttu-id="8b199-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="8b199-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="8b199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b199-102">SYNOPSIS</span></span>
<span data-ttu-id="8b199-103">Belirtilen zaman penceresinde bu aboneliğin yaptığı API isteklerini gösteren günlükleri dışarı aktarma etkinliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b199-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b199-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b199-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b199-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b199-105">DESCRIPTION</span></span>
<span data-ttu-id="8b199-106">Önceden tanımlanmış zaman aralıklarında, aboneliğin Microsoft. COMPUTE API 'sini başarı, başarısızlık veya daraltıldı ile ilgili istatistiksel verileri dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="8b199-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="8b199-107">Günlükler üç parametre ile daha da gruplandırılabilir: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="8b199-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="8b199-108">Bu cmdlet 'in yalnızca hesaplama kaynak sağlayıcısı günlüklerinin topladığı unutmayın; Ayrıca, disk ve anlık görüntü kaynak türleriyle ilgili veriler henüz kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8b199-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="8b199-109">Hesaplama kaynak sağlayıcısının API azaltması hakkında genel bilgi için bkz https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="8b199-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="8b199-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b199-110">EXAMPLES</span></span>

### <span data-ttu-id="8b199-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8b199-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="8b199-112">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 ile ayrılmış Microsoft. COMPUTE API çağrılarını, verilen SAS URI 'sinde, işlem adına göre toplanmış olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="8b199-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="8b199-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b199-113">PARAMETERS</span></span>

### <span data-ttu-id="8b199-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="8b199-114">-AsJob</span></span>
<span data-ttu-id="8b199-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8b199-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b199-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="8b199-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="8b199-117">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="8b199-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="8b199-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b199-118">-DefaultProfile</span></span>
<span data-ttu-id="8b199-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8b199-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b199-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="8b199-120">-FromTime</span></span>
<span data-ttu-id="8b199-121">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="8b199-121">From time of the query</span></span>

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

### <span data-ttu-id="8b199-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="8b199-122">-GroupByOperationName</span></span>
<span data-ttu-id="8b199-123">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="8b199-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="8b199-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="8b199-124">-GroupByResourceName</span></span>
<span data-ttu-id="8b199-125">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="8b199-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="8b199-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="8b199-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="8b199-127">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="8b199-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="8b199-128">-Interlength uzunluğu</span><span class="sxs-lookup"><span data-stu-id="8b199-128">-IntervalLength</span></span>
<span data-ttu-id="8b199-129">LogAnalytics çağrı hızı günlükleri oluşturmak için kullanılan dakika cinsinden Aralık değeri.</span><span class="sxs-lookup"><span data-stu-id="8b199-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b199-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="8b199-130">-Location</span></span>
<span data-ttu-id="8b199-131">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="8b199-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="8b199-132">-ToTime</span><span class="sxs-lookup"><span data-stu-id="8b199-132">-ToTime</span></span>
<span data-ttu-id="8b199-133">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="8b199-133">To time of the query</span></span>

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

### <span data-ttu-id="8b199-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b199-134">-Confirm</span></span>
<span data-ttu-id="8b199-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b199-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b199-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b199-136">-WhatIf</span></span>
<span data-ttu-id="8b199-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b199-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b199-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b199-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b199-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b199-139">CommonParameters</span></span>
<span data-ttu-id="8b199-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b199-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b199-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b199-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b199-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b199-142">INPUTS</span></span>

### <span data-ttu-id="8b199-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8b199-143">System.String</span></span>

## <span data-ttu-id="8b199-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b199-144">OUTPUTS</span></span>

### <span data-ttu-id="8b199-145">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="8b199-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="8b199-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b199-146">NOTES</span></span>

## <span data-ttu-id="8b199-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b199-147">RELATED LINKS</span></span>
