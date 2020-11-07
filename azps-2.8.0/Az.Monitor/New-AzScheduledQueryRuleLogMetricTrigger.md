---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: 4873d093411c07af9b1a5389299e39ecca0a5f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932179"
---
# <span data-ttu-id="c0fa9-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c0fa9-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="c0fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fa9-103">Log Metric tetikleyicisi türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="c0fa9-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="c0fa9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0fa9-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0fa9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fa9-106">Log Metric tetikleyicisi türünde bir nesne oluşturur ve isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c0fa9-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="c0fa9-107">Bu, Ölçüm Ölçüm türü uyarısı vermeniz gerektiğinde kullanılmak üzere, metrik sorgu kuralı için tetik durumudur.</span><span class="sxs-lookup"><span data-stu-id="c0fa9-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="c0fa9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0fa9-108">EXAMPLES</span></span>

### <span data-ttu-id="c0fa9-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0fa9-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="c0fa9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="c0fa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fa9-111">-DefaultProfile</span></span>
<span data-ttu-id="c0fa9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0fa9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0fa9-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="c0fa9-113">-MetricColumn</span></span>
<span data-ttu-id="c0fa9-114">Ölçüm değerinin toplanmakta olduğu sütun</span><span class="sxs-lookup"><span data-stu-id="c0fa9-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="c0fa9-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="c0fa9-115">-MetricTriggerType</span></span>
<span data-ttu-id="c0fa9-116">Ölçüm tetik türü</span><span class="sxs-lookup"><span data-stu-id="c0fa9-116">The metric trigger type</span></span>

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

### <span data-ttu-id="c0fa9-117">Eşiği</span><span class="sxs-lookup"><span data-stu-id="c0fa9-117">-Threshold</span></span>
<span data-ttu-id="c0fa9-118">Ölçü eşik değeri</span><span class="sxs-lookup"><span data-stu-id="c0fa9-118">The metric threshold value</span></span>

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

### <span data-ttu-id="c0fa9-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="c0fa9-119">-ThresholdOperator</span></span>
<span data-ttu-id="c0fa9-120">Metrik eşik işleci: GreaterThan, LessThan, eşittir</span><span class="sxs-lookup"><span data-stu-id="c0fa9-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="c0fa9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fa9-121">CommonParameters</span></span>
<span data-ttu-id="c0fa9-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0fa9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fa9-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0fa9-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fa9-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0fa9-124">INPUTS</span></span>

### <span data-ttu-id="c0fa9-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c0fa9-125">None</span></span>

## <span data-ttu-id="c0fa9-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0fa9-126">OUTPUTS</span></span>

### <span data-ttu-id="c0fa9-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="c0fa9-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="c0fa9-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0fa9-128">NOTES</span></span>

## <span data-ttu-id="c0fa9-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0fa9-129">RELATED LINKS</span></span>
