---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095862"
---
# <span data-ttu-id="e7563-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e7563-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e7563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7563-102">SYNOPSIS</span></span>
<span data-ttu-id="e7563-103">Zamanlama türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="e7563-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="e7563-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7563-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7563-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7563-105">DESCRIPTION</span></span>
<span data-ttu-id="e7563-106">Zamanlama türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7563-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="e7563-107">Bu nesne, günlük uyarı kuralı oluşturan komuta geçirilir.</span><span class="sxs-lookup"><span data-stu-id="e7563-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="e7563-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7563-108">EXAMPLES</span></span>

### <span data-ttu-id="e7563-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7563-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="e7563-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7563-110">PARAMETERS</span></span>

### <span data-ttu-id="e7563-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7563-111">-DefaultProfile</span></span>
<span data-ttu-id="e7563-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7563-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7563-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7563-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="e7563-114">Uyarı sıklığı</span><span class="sxs-lookup"><span data-stu-id="e7563-114">The alert frequency</span></span>

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

### <span data-ttu-id="e7563-115">-Timewindowınminutes</span><span class="sxs-lookup"><span data-stu-id="e7563-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="e7563-116">Uyarı süresi penceresi</span><span class="sxs-lookup"><span data-stu-id="e7563-116">The alert time window</span></span>

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

### <span data-ttu-id="e7563-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7563-117">CommonParameters</span></span>
<span data-ttu-id="e7563-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7563-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7563-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7563-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7563-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7563-120">INPUTS</span></span>

### <span data-ttu-id="e7563-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e7563-121">None</span></span>

## <span data-ttu-id="e7563-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7563-122">OUTPUTS</span></span>

### <span data-ttu-id="e7563-123">Microsoft. Azure. Commands. Insights. OutputClasses. Psscheduledqueryrulezamanlama</span><span class="sxs-lookup"><span data-stu-id="e7563-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="e7563-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7563-124">NOTES</span></span>

## <span data-ttu-id="e7563-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7563-125">RELATED LINKS</span></span>
