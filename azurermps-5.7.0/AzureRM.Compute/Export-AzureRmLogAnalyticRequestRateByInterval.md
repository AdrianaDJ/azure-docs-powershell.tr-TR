---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: b5e087bf42a2cb7f19980621c6dd0606471374d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590521"
---
# <span data-ttu-id="2fa53-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="2fa53-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="2fa53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa53-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa53-103">Belirtilen zaman penceresinde bu aboneliğin yaptığı API isteklerini gösteren günlükleri dışarı aktarma etkinliklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fa53-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fa53-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fa53-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa53-106">Bu Işlem, Microsoft. COMPUTE API çağrılarını, zaman aralıklarında gösterilen başarı, başarısızlık veya kısıtlanmış ile ayrılmış şekilde dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="2fa53-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="2fa53-107">Günlükler üç parametre ile daha da gruplandırılabilir: GroupByOperationName, GroupByThrottlePolicy veya GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="2fa53-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="2fa53-108">Bu cmdlet 'in yalnızca CRP günlüklerini topladığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2fa53-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="2fa53-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fa53-109">EXAMPLES</span></span>

### <span data-ttu-id="2fa53-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2fa53-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="2fa53-111">Bu komut, 2018-02-20T17:54:14 ve 2018-02-22T17:54:17 ile ayrılmış Microsoft. COMPUTE API çağrılarını, verilen SAS URI 'sinde, işlem adına göre toplanmış olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="2fa53-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="2fa53-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fa53-112">PARAMETERS</span></span>

### <span data-ttu-id="2fa53-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2fa53-113">-AsJob</span></span>
<span data-ttu-id="2fa53-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2fa53-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fa53-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="2fa53-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="2fa53-116">LogAnalytics API 'nın çıkış günlüklerini yazdığı günlük blob kapsayıcısının SAS URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="2fa53-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="2fa53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa53-117">-DefaultProfile</span></span>
<span data-ttu-id="2fa53-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fa53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa53-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="2fa53-119">-FromTime</span></span>
<span data-ttu-id="2fa53-120">Sorgunun başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="2fa53-120">From time of the query</span></span>

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

### <span data-ttu-id="2fa53-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="2fa53-121">-GroupByOperationName</span></span>
<span data-ttu-id="2fa53-122">Işlem adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="2fa53-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="2fa53-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="2fa53-123">-GroupByResourceName</span></span>
<span data-ttu-id="2fa53-124">Kaynak adına göre grup sorgusu sonucu.</span><span class="sxs-lookup"><span data-stu-id="2fa53-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="2fa53-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="2fa53-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="2fa53-126">Grup sorgu sonucu azaltma Ilkesi uygulandı.</span><span class="sxs-lookup"><span data-stu-id="2fa53-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="2fa53-127">-Interlength uzunluğu</span><span class="sxs-lookup"><span data-stu-id="2fa53-127">-IntervalLength</span></span>
<span data-ttu-id="2fa53-128">LogAnalytics çağrı hızı günlükleri oluşturmak için kullanılan dakika cinsinden Aralık değeri.</span><span class="sxs-lookup"><span data-stu-id="2fa53-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa53-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="2fa53-129">-Location</span></span>
<span data-ttu-id="2fa53-130">Günlüğün analitik olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="2fa53-130">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="2fa53-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="2fa53-131">-ToTime</span></span>
<span data-ttu-id="2fa53-132">Sorgunun zamanı</span><span class="sxs-lookup"><span data-stu-id="2fa53-132">To time of the query</span></span>

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

### <span data-ttu-id="2fa53-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fa53-133">-Confirm</span></span>
<span data-ttu-id="2fa53-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fa53-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa53-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa53-135">-WhatIf</span></span>
<span data-ttu-id="2fa53-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fa53-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa53-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fa53-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa53-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa53-138">CommonParameters</span></span>
<span data-ttu-id="2fa53-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fa53-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa53-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa53-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa53-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fa53-141">INPUTS</span></span>

### <span data-ttu-id="2fa53-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa53-142">System.String</span></span>

## <span data-ttu-id="2fa53-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fa53-143">OUTPUTS</span></span>

### <span data-ttu-id="2fa53-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSLOG, Ticsoperationresult</span><span class="sxs-lookup"><span data-stu-id="2fa53-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="2fa53-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fa53-145">NOTES</span></span>

## <span data-ttu-id="2fa53-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fa53-146">RELATED LINKS</span></span>
