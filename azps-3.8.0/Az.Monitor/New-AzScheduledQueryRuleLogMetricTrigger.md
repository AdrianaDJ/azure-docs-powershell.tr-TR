---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095869"
---
# <span data-ttu-id="6eb08-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6eb08-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="6eb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb08-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb08-103">Log Metric tetikleyicisi türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6eb08-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="6eb08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6eb08-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eb08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6eb08-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb08-106">Log Metric tetikleyicisi türünde bir nesne oluşturur ve isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6eb08-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="6eb08-107">Bu, Ölçüm Ölçüm türü uyarısı vermeniz gerektiğinde kullanılmak üzere, metrik sorgu kuralı için tetik durumudur.</span><span class="sxs-lookup"><span data-stu-id="6eb08-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="6eb08-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6eb08-108">EXAMPLES</span></span>

### <span data-ttu-id="6eb08-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6eb08-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="6eb08-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6eb08-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb08-111">-DefaultProfile</span></span>
<span data-ttu-id="6eb08-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6eb08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb08-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="6eb08-113">-MetricColumn</span></span>
<span data-ttu-id="6eb08-114">Ölçüm değerinin toplanmakta olduğu sütun.</span><span class="sxs-lookup"><span data-stu-id="6eb08-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="6eb08-115">Giriş doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="6eb08-115">The input is not validated.</span></span> <span data-ttu-id="6eb08-116">New-AzScheduledQueryRule zaman önce doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="6eb08-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="6eb08-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="6eb08-117">-MetricTriggerType</span></span>
<span data-ttu-id="6eb08-118">Ölçüm tetik türü.</span><span class="sxs-lookup"><span data-stu-id="6eb08-118">The metric trigger type.</span></span>
<span data-ttu-id="6eb08-119">Giriş doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="6eb08-119">The input is not validated.</span></span> <span data-ttu-id="6eb08-120">New-AzScheduledQueryRule zaman önce doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="6eb08-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="6eb08-121">Eşiği</span><span class="sxs-lookup"><span data-stu-id="6eb08-121">-Threshold</span></span>
<span data-ttu-id="6eb08-122">Ölçü eşik değeri: ardışık, toplam.</span><span class="sxs-lookup"><span data-stu-id="6eb08-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="6eb08-123">Giriş doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="6eb08-123">The input is not validated.</span></span> <span data-ttu-id="6eb08-124">New-AzScheduledQueryRule zaman önce doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="6eb08-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="6eb08-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="6eb08-125">-ThresholdOperator</span></span>
<span data-ttu-id="6eb08-126">Metrik eşik işleci: GreaterThan, LessThan, eşittir.</span><span class="sxs-lookup"><span data-stu-id="6eb08-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="6eb08-127">Giriş doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="6eb08-127">The input is not validated.</span></span> <span data-ttu-id="6eb08-128">New-AzScheduledQueryRule zaman önce doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="6eb08-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="6eb08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb08-129">CommonParameters</span></span>
<span data-ttu-id="6eb08-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6eb08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb08-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6eb08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb08-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6eb08-132">INPUTS</span></span>

### <span data-ttu-id="6eb08-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6eb08-133">None</span></span>

## <span data-ttu-id="6eb08-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6eb08-134">OUTPUTS</span></span>

### <span data-ttu-id="6eb08-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6eb08-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="6eb08-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6eb08-136">NOTES</span></span>

## <span data-ttu-id="6eb08-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6eb08-137">RELATED LINKS</span></span>
