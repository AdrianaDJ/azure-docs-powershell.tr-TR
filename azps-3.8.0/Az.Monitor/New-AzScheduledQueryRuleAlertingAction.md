---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 41ce3c066651cb2bc6ea13ddd0a7a3bb15d28879
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095870"
---
# <span data-ttu-id="77fc6-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="77fc6-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="77fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="77fc6-103">Uyarı eylemi türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="77fc6-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="77fc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77fc6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77fc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="77fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="77fc6-106">Uyarı eylemi türünde bir nesne oluşturur bu nesne, günlük uyarısı kuralı oluşturan komuta geçirilecek</span><span class="sxs-lookup"><span data-stu-id="77fc6-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="77fc6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="77fc6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="77fc6-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="77fc6-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77fc6-109">PARAMETERS</span></span>

### <span data-ttu-id="77fc6-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="77fc6-110">-AznsAction</span></span>
<span data-ttu-id="77fc6-111">AzNS eylem ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="77fc6-111">The AzNS action details</span></span>

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

### <span data-ttu-id="77fc6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fc6-112">-DefaultProfile</span></span>
<span data-ttu-id="77fc6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="77fc6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77fc6-114">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="77fc6-114">-Severity</span></span>
<span data-ttu-id="77fc6-115">Bu uyarının önem derecesi</span><span class="sxs-lookup"><span data-stu-id="77fc6-115">The severity for this alert</span></span>

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

### <span data-ttu-id="77fc6-116">-Azaltındakikalar</span><span class="sxs-lookup"><span data-stu-id="77fc6-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="77fc6-117">Uyarının kısıtlanacak süre (dakika)</span><span class="sxs-lookup"><span data-stu-id="77fc6-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="77fc6-118">-Tetik</span><span class="sxs-lookup"><span data-stu-id="77fc6-118">-Trigger</span></span>
<span data-ttu-id="77fc6-119">Uyarı tetik koşulu</span><span class="sxs-lookup"><span data-stu-id="77fc6-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="77fc6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fc6-120">CommonParameters</span></span>
<span data-ttu-id="77fc6-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77fc6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fc6-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="77fc6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fc6-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77fc6-123">INPUTS</span></span>

### <span data-ttu-id="77fc6-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="77fc6-124">None</span></span>

## <span data-ttu-id="77fc6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77fc6-125">OUTPUTS</span></span>

### <span data-ttu-id="77fc6-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="77fc6-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="77fc6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77fc6-127">NOTES</span></span>

## <span data-ttu-id="77fc6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77fc6-128">RELATED LINKS</span></span>