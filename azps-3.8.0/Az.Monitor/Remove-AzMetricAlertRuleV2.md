---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: d2b34063f5ece370d52b8a4c3c0dab35cff77c54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937276"
---
# <span data-ttu-id="5bff0-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5bff0-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="5bff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bff0-102">SYNOPSIS</span></span>
<span data-ttu-id="5bff0-103">V2 (klasik olmayan) ölçüm uyarısı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5bff0-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="5bff0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bff0-104">SYNTAX</span></span>

### <span data-ttu-id="5bff0-105">ByMetricRuleResourceName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5bff0-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bff0-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="5bff0-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bff0-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="5bff0-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bff0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bff0-108">DESCRIPTION</span></span>
<span data-ttu-id="5bff0-109">**Remove-AzMetricAlertRuleV2** cmdlet 'i bir uyarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5bff0-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="5bff0-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="5bff0-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5bff0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bff0-111">EXAMPLES</span></span>

### <span data-ttu-id="5bff0-112">Örnek 1: bir uyarı kuralını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="5bff0-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="5bff0-113">Bu komut, PsSdk adındaki uyarı kuralını kaldırır</span><span class="sxs-lookup"><span data-stu-id="5bff0-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="5bff0-114">Örnek 2: bir uyarı kuralını KIMLIĞE göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="5bff0-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="5bff0-115">Bu komut, `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="5bff0-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="5bff0-116">Örnek 3: bir uyarı alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="5bff0-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="5bff0-117">Bu komut bir uyarıyı alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5bff0-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="5bff0-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bff0-118">PARAMETERS</span></span>

### <span data-ttu-id="5bff0-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="5bff0-119">-AsJob</span></span>
<span data-ttu-id="5bff0-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5bff0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bff0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bff0-121">-DefaultProfile</span></span>
<span data-ttu-id="5bff0-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bff0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bff0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bff0-123">-InputObject</span></span>
<span data-ttu-id="5bff0-124">Ölçüm kuralı nesnesi</span><span class="sxs-lookup"><span data-stu-id="5bff0-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bff0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5bff0-125">-Name</span></span>
<span data-ttu-id="5bff0-126">Ölçü uyarısı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="5bff0-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bff0-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5bff0-127">-PassThru</span></span>
<span data-ttu-id="5bff0-128">Başarılı bir şekilde silme işlemi</span><span class="sxs-lookup"><span data-stu-id="5bff0-128">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="5bff0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bff0-129">-ResourceGroupName</span></span>
<span data-ttu-id="5bff0-130">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bff0-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bff0-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5bff0-131">-ResourceId</span></span>
<span data-ttu-id="5bff0-132">RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="5bff0-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bff0-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="5bff0-133">-Confirm</span></span>
<span data-ttu-id="5bff0-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5bff0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bff0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bff0-135">-WhatIf</span></span>
<span data-ttu-id="5bff0-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5bff0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bff0-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5bff0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bff0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bff0-138">CommonParameters</span></span>
<span data-ttu-id="5bff0-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bff0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bff0-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5bff0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bff0-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bff0-141">INPUTS</span></span>

### <span data-ttu-id="5bff0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5bff0-142">System.String</span></span>

### <span data-ttu-id="5bff0-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5bff0-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="5bff0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bff0-144">OUTPUTS</span></span>

### <span data-ttu-id="5bff0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bff0-145">System.Boolean</span></span>

## <span data-ttu-id="5bff0-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bff0-146">NOTES</span></span>

## <span data-ttu-id="5bff0-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bff0-147">RELATED LINKS</span></span>
