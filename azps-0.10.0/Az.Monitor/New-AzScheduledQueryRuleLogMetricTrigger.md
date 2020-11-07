---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935704"
---
# <span data-ttu-id="9638d-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="9638d-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="9638d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9638d-102">SYNOPSIS</span></span>
<span data-ttu-id="9638d-103">Log Metric tetikleyicisi türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="9638d-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="9638d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9638d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9638d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9638d-105">DESCRIPTION</span></span>
<span data-ttu-id="9638d-106">Log Metric tetikleyicisi türünde bir nesne oluşturur ve isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9638d-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="9638d-107">Bu, Ölçüm Ölçüm türü uyarısı vermeniz gerektiğinde kullanılmak üzere, metrik sorgu kuralı için tetik durumudur.</span><span class="sxs-lookup"><span data-stu-id="9638d-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="9638d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9638d-108">EXAMPLES</span></span>

### <span data-ttu-id="9638d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9638d-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="9638d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9638d-110">PARAMETERS</span></span>

### <span data-ttu-id="9638d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9638d-111">-DefaultProfile</span></span>
<span data-ttu-id="9638d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9638d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9638d-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="9638d-113">-MetricColumn</span></span>
<span data-ttu-id="9638d-114">Ölçüm değerinin toplanmakta olduğu sütun</span><span class="sxs-lookup"><span data-stu-id="9638d-114">Column on which metric value is being aggregated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9638d-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="9638d-115">-MetricTriggerType</span></span>
<span data-ttu-id="9638d-116">Ölçüm tetik türü</span><span class="sxs-lookup"><span data-stu-id="9638d-116">The metric trigger type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9638d-117">Eşiği</span><span class="sxs-lookup"><span data-stu-id="9638d-117">-Threshold</span></span>
<span data-ttu-id="9638d-118">Ölçü eşik değeri</span><span class="sxs-lookup"><span data-stu-id="9638d-118">The metric threshold value</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9638d-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="9638d-119">-ThresholdOperator</span></span>
<span data-ttu-id="9638d-120">Metrik eşik işleci: GreaterThan, LessThan, eşittir</span><span class="sxs-lookup"><span data-stu-id="9638d-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9638d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9638d-121">CommonParameters</span></span>
<span data-ttu-id="9638d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9638d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9638d-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9638d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9638d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9638d-124">INPUTS</span></span>

### <span data-ttu-id="9638d-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9638d-125">None</span></span>

## <span data-ttu-id="9638d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9638d-126">OUTPUTS</span></span>

### <span data-ttu-id="9638d-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="9638d-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="9638d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9638d-128">NOTES</span></span>

## <span data-ttu-id="9638d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9638d-129">RELATED LINKS</span></span>
