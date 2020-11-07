---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 54da99c2aeb6909c1a08a98821f621ddfed5199e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935702"
---
# <span data-ttu-id="bd856-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bd856-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bd856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd856-102">SYNOPSIS</span></span>
<span data-ttu-id="bd856-103">Uyarı eylemi türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="bd856-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="bd856-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd856-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd856-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd856-105">DESCRIPTION</span></span>
<span data-ttu-id="bd856-106">Uyarı eylemi türünde bir nesne oluşturur bu nesne, günlük uyarısı kuralı oluşturan komuta geçirilecek</span><span class="sxs-lookup"><span data-stu-id="bd856-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="bd856-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd856-107">EXAMPLES</span></span>

### <span data-ttu-id="bd856-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd856-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="bd856-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd856-109">PARAMETERS</span></span>

### <span data-ttu-id="bd856-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="bd856-110">-AznsAction</span></span>
<span data-ttu-id="bd856-111">AzNS eylem ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="bd856-111">The AzNS action details</span></span>

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

### <span data-ttu-id="bd856-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd856-112">-DefaultProfile</span></span>
<span data-ttu-id="bd856-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd856-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd856-114">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="bd856-114">-Severity</span></span>
<span data-ttu-id="bd856-115">Bu uyarının önem derecesi</span><span class="sxs-lookup"><span data-stu-id="bd856-115">The severity for this alert</span></span>

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

### <span data-ttu-id="bd856-116">-Azaltındakikalar</span><span class="sxs-lookup"><span data-stu-id="bd856-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="bd856-117">Uyarının kısıtlanacak süre (dakika)</span><span class="sxs-lookup"><span data-stu-id="bd856-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="bd856-118">-Tetik</span><span class="sxs-lookup"><span data-stu-id="bd856-118">-Trigger</span></span>
<span data-ttu-id="bd856-119">Uyarı tetik koşulu</span><span class="sxs-lookup"><span data-stu-id="bd856-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="bd856-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd856-120">CommonParameters</span></span>
<span data-ttu-id="bd856-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd856-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd856-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bd856-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd856-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd856-123">INPUTS</span></span>

### <span data-ttu-id="bd856-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bd856-124">None</span></span>

## <span data-ttu-id="bd856-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd856-125">OUTPUTS</span></span>

### <span data-ttu-id="bd856-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bd856-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="bd856-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd856-127">NOTES</span></span>

## <span data-ttu-id="bd856-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd856-128">RELATED LINKS</span></span>
