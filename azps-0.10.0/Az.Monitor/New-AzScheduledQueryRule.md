---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: cbaf71a19d0fb823fd44040d34fcde5d68c7c2c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935708"
---
# <span data-ttu-id="a8f15-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a8f15-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a8f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8f15-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f15-103">Günlük uyarısı kuralı oluşturur (zamanlanmış sorgu kuralı türü)</span><span class="sxs-lookup"><span data-stu-id="a8f15-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a8f15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8f15-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f15-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8f15-105">DESCRIPTION</span></span>
<span data-ttu-id="a8f15-106">Günlük uyarısı kuralı oluşturur (zamanlanmış sorgu kuralı türü)</span><span class="sxs-lookup"><span data-stu-id="a8f15-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="a8f15-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8f15-107">EXAMPLES</span></span>

### <span data-ttu-id="a8f15-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8f15-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="a8f15-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8f15-109">PARAMETERS</span></span>

### <span data-ttu-id="a8f15-110">-Eylem</span><span class="sxs-lookup"><span data-stu-id="a8f15-110">-Action</span></span>
<span data-ttu-id="a8f15-111">Zamanlanmış sorgu kuralı uyarısı eylemi</span><span class="sxs-lookup"><span data-stu-id="a8f15-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="a8f15-112">-AsJob</span></span>
<span data-ttu-id="a8f15-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a8f15-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f15-114">-DefaultProfile</span></span>
<span data-ttu-id="a8f15-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8f15-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8f15-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a8f15-116">-Description</span></span>
<span data-ttu-id="a8f15-117">Bu uyarının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a8f15-117">The description for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="a8f15-118">-Enabled</span></span>
<span data-ttu-id="a8f15-119">Azure uyarı durumu-geçerli değerler-$true, $false</span><span class="sxs-lookup"><span data-stu-id="a8f15-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="a8f15-120">-Location</span></span>
<span data-ttu-id="a8f15-121">Bu uyarının konumu</span><span class="sxs-lookup"><span data-stu-id="a8f15-121">The location for this alert</span></span>

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

### <span data-ttu-id="a8f15-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8f15-122">-Name</span></span>
<span data-ttu-id="a8f15-123">Uyarı adı</span><span class="sxs-lookup"><span data-stu-id="a8f15-123">The alert name</span></span>

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

### <span data-ttu-id="a8f15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f15-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8f15-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a8f15-125">The resource group name</span></span>

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

### <span data-ttu-id="a8f15-126">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="a8f15-126">-Schedule</span></span>
<span data-ttu-id="a8f15-127">Zamanlanmış sorgu kuralı zamanlaması</span><span class="sxs-lookup"><span data-stu-id="a8f15-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-128">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="a8f15-128">-Source</span></span>
<span data-ttu-id="a8f15-129">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="a8f15-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a8f15-130">-Tag</span></span>
<span data-ttu-id="a8f15-131">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="a8f15-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8f15-132">-Confirm</span></span>
<span data-ttu-id="a8f15-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8f15-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f15-134">-WhatIf</span></span>
<span data-ttu-id="a8f15-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8f15-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8f15-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8f15-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f15-137">CommonParameters</span></span>
<span data-ttu-id="a8f15-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8f15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f15-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a8f15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f15-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8f15-140">INPUTS</span></span>

### <span data-ttu-id="a8f15-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a8f15-141">System.String</span></span>

## <span data-ttu-id="a8f15-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8f15-142">OUTPUTS</span></span>

### <span data-ttu-id="a8f15-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a8f15-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="a8f15-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8f15-144">NOTES</span></span>

## <span data-ttu-id="a8f15-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8f15-145">RELATED LINKS</span></span>
