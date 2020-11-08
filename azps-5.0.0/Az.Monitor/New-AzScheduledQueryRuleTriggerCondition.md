---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279921"
---
# <span data-ttu-id="2086c-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2086c-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="2086c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2086c-102">SYNOPSIS</span></span>
<span data-ttu-id="2086c-103">Tetik koşulu türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="2086c-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="2086c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2086c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2086c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2086c-105">DESCRIPTION</span></span>
<span data-ttu-id="2086c-106">Tetik koşulu türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2086c-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="2086c-107">Bu nesne, uyarma eylem nesnesi oluşturan komuta geçirilecek</span><span class="sxs-lookup"><span data-stu-id="2086c-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="2086c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2086c-108">EXAMPLES</span></span>

### <span data-ttu-id="2086c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2086c-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="2086c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2086c-110">PARAMETERS</span></span>

### <span data-ttu-id="2086c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2086c-111">-DefaultProfile</span></span>
<span data-ttu-id="2086c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2086c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2086c-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2086c-113">-MetricTrigger</span></span>
<span data-ttu-id="2086c-114">Ölçüm sorgu kuralı için tetik koşulu</span><span class="sxs-lookup"><span data-stu-id="2086c-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2086c-115">Eşiği</span><span class="sxs-lookup"><span data-stu-id="2086c-115">-Threshold</span></span>
<span data-ttu-id="2086c-116">Uyarının hangi noktada harekete geçirilir</span><span class="sxs-lookup"><span data-stu-id="2086c-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="2086c-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="2086c-117">-ThresholdOperator</span></span>
<span data-ttu-id="2086c-118">Eşik operatörü: GreaterThan, LessThan veya eşittir</span><span class="sxs-lookup"><span data-stu-id="2086c-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="2086c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2086c-119">CommonParameters</span></span>
<span data-ttu-id="2086c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2086c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2086c-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2086c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2086c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2086c-122">INPUTS</span></span>

### <span data-ttu-id="2086c-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2086c-123">None</span></span>

## <span data-ttu-id="2086c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2086c-124">OUTPUTS</span></span>

### <span data-ttu-id="2086c-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2086c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="2086c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2086c-126">NOTES</span></span>

## <span data-ttu-id="2086c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2086c-127">RELATED LINKS</span></span>
