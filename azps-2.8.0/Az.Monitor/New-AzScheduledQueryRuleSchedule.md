---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 2043a2cf31354c7fc14b1b03794dff6f82af67b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932176"
---
# <span data-ttu-id="a325d-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a325d-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a325d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a325d-102">SYNOPSIS</span></span>
<span data-ttu-id="a325d-103">Zamanlama türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="a325d-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="a325d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a325d-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a325d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a325d-105">DESCRIPTION</span></span>
<span data-ttu-id="a325d-106">Zamanlama türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a325d-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="a325d-107">Bu nesne, günlük uyarı kuralı oluşturan komuta geçirilir.</span><span class="sxs-lookup"><span data-stu-id="a325d-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="a325d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a325d-108">EXAMPLES</span></span>

### <span data-ttu-id="a325d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a325d-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="a325d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a325d-110">PARAMETERS</span></span>

### <span data-ttu-id="a325d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a325d-111">-DefaultProfile</span></span>
<span data-ttu-id="a325d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a325d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a325d-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a325d-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="a325d-114">Uyarı sıklığı</span><span class="sxs-lookup"><span data-stu-id="a325d-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a325d-115">-Timewindowınminutes</span><span class="sxs-lookup"><span data-stu-id="a325d-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="a325d-116">Uyarı süresi penceresi</span><span class="sxs-lookup"><span data-stu-id="a325d-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a325d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a325d-117">CommonParameters</span></span>
<span data-ttu-id="a325d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a325d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a325d-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a325d-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a325d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a325d-120">INPUTS</span></span>

### <span data-ttu-id="a325d-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a325d-121">None</span></span>

## <span data-ttu-id="a325d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a325d-122">OUTPUTS</span></span>

### <span data-ttu-id="a325d-123">Microsoft. Azure. Commands. Insights. OutputClasses. Psscheduledqueryrulezamanlama</span><span class="sxs-lookup"><span data-stu-id="a325d-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="a325d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a325d-124">NOTES</span></span>

## <span data-ttu-id="a325d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a325d-125">RELATED LINKS</span></span>
