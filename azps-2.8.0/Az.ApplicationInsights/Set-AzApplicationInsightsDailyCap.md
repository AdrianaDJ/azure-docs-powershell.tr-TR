---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 0283bfcc0c3eecf3ca7f97a8f5bb2b8813c4ae78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753366"
---
# <span data-ttu-id="f0305-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="f0305-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="f0305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0305-102">SYNOPSIS</span></span>
<span data-ttu-id="f0305-103">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="f0305-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="f0305-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0305-104">SYNTAX</span></span>

### <span data-ttu-id="f0305-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0305-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0305-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="f0305-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0305-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f0305-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0305-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0305-108">DESCRIPTION</span></span>
<span data-ttu-id="f0305-109">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="f0305-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="f0305-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0305-110">EXAMPLES</span></span>

### <span data-ttu-id="f0305-111">Örnek 1 bir Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="f0305-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="f0305-112">Günlük veri birimi Cap 'i gün başına 400 ' e ayarlayın ve "testgroup" kaynak grubundaki "test" kaynağının vuruş</span><span class="sxs-lookup"><span data-stu-id="f0305-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f0305-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0305-113">PARAMETERS</span></span>

### <span data-ttu-id="f0305-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="f0305-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f0305-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f0305-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0305-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="f0305-116">-DailyCapGB</span></span>
<span data-ttu-id="f0305-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="f0305-117">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0305-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0305-118">-DefaultProfile</span></span>
<span data-ttu-id="f0305-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0305-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0305-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="f0305-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="f0305-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="f0305-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="f0305-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0305-122">-Name</span></span>
<span data-ttu-id="f0305-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="f0305-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0305-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0305-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0305-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f0305-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0305-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0305-126">-ResourceId</span></span>
<span data-ttu-id="f0305-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f0305-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0305-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0305-128">-Confirm</span></span>
<span data-ttu-id="f0305-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0305-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0305-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0305-130">-WhatIf</span></span>
<span data-ttu-id="f0305-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0305-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0305-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0305-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0305-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0305-133">CommonParameters</span></span>
<span data-ttu-id="f0305-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0305-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0305-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0305-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0305-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0305-136">INPUTS</span></span>

### <span data-ttu-id="f0305-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f0305-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="f0305-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f0305-138">System.String</span></span>

## <span data-ttu-id="f0305-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0305-139">OUTPUTS</span></span>

### <span data-ttu-id="f0305-140">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="f0305-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="f0305-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0305-141">NOTES</span></span>

## <span data-ttu-id="f0305-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0305-142">RELATED LINKS</span></span>