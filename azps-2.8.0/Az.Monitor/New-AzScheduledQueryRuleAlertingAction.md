---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932183"
---
# <span data-ttu-id="428f2-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="428f2-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="428f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="428f2-102">SYNOPSIS</span></span>
<span data-ttu-id="428f2-103">Uyarı eylemi türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="428f2-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="428f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="428f2-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="428f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="428f2-105">DESCRIPTION</span></span>
<span data-ttu-id="428f2-106">Uyarı eylemi türünde bir nesne oluşturur bu nesne, günlük uyarısı kuralı oluşturan komuta geçirilecek</span><span class="sxs-lookup"><span data-stu-id="428f2-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="428f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="428f2-107">EXAMPLES</span></span>

### <span data-ttu-id="428f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="428f2-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="428f2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="428f2-109">PARAMETERS</span></span>

### <span data-ttu-id="428f2-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="428f2-110">-AznsAction</span></span>
<span data-ttu-id="428f2-111">AzNS eylem ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="428f2-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428f2-112">-DefaultProfile</span></span>
<span data-ttu-id="428f2-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="428f2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428f2-114">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="428f2-114">-Severity</span></span>
<span data-ttu-id="428f2-115">Bu uyarının önem derecesi</span><span class="sxs-lookup"><span data-stu-id="428f2-115">The severity for this alert</span></span>

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

### <span data-ttu-id="428f2-116">-Azaltındakikalar</span><span class="sxs-lookup"><span data-stu-id="428f2-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="428f2-117">Uyarının kısıtlanacak süre (dakika)</span><span class="sxs-lookup"><span data-stu-id="428f2-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428f2-118">-Tetik</span><span class="sxs-lookup"><span data-stu-id="428f2-118">-Trigger</span></span>
<span data-ttu-id="428f2-119">Uyarı tetik koşulu</span><span class="sxs-lookup"><span data-stu-id="428f2-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="428f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428f2-120">CommonParameters</span></span>
<span data-ttu-id="428f2-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="428f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428f2-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="428f2-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428f2-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="428f2-123">INPUTS</span></span>

### <span data-ttu-id="428f2-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="428f2-124">None</span></span>

## <span data-ttu-id="428f2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="428f2-125">OUTPUTS</span></span>

### <span data-ttu-id="428f2-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="428f2-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="428f2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="428f2-127">NOTES</span></span>

## <span data-ttu-id="428f2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="428f2-128">RELATED LINKS</span></span>
