---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 13bd076488e8bb379e3b365c6c4d7803ea650f40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753364"
---
# <span data-ttu-id="61f2e-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="61f2e-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="61f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="61f2e-103">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="61f2e-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="61f2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61f2e-104">SYNTAX</span></span>

### <span data-ttu-id="61f2e-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61f2e-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f2e-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="61f2e-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f2e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="61f2e-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61f2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61f2e-108">DESCRIPTION</span></span>
<span data-ttu-id="61f2e-109">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="61f2e-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="61f2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61f2e-110">EXAMPLES</span></span>

### <span data-ttu-id="61f2e-111">Örnek 1 bir Application Insights kaynağı için fiyatlandırma planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="61f2e-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="61f2e-112">Fiyatlandırma planını "temel" olarak ayarlama, günlük veri birimi Cap 'yi günde 400 ' e ayarlama ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="61f2e-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="61f2e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61f2e-113">PARAMETERS</span></span>

### <span data-ttu-id="61f2e-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="61f2e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="61f2e-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="61f2e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="61f2e-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="61f2e-116">-DailyCapGB</span></span>
<span data-ttu-id="61f2e-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="61f2e-117">Daily Cap.</span></span>

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

### <span data-ttu-id="61f2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f2e-118">-DefaultProfile</span></span>
<span data-ttu-id="61f2e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61f2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f2e-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="61f2e-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="61f2e-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="61f2e-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="61f2e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="61f2e-122">-Name</span></span>
<span data-ttu-id="61f2e-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="61f2e-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="61f2e-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="61f2e-124">-PricingPlan</span></span>
<span data-ttu-id="61f2e-125">Fiyatlandırma planı adı.</span><span class="sxs-lookup"><span data-stu-id="61f2e-125">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="61f2e-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="61f2e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="61f2e-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="61f2e-128">-ResourceId</span></span>
<span data-ttu-id="61f2e-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="61f2e-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="61f2e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="61f2e-130">-Confirm</span></span>
<span data-ttu-id="61f2e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61f2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f2e-132">-WhatIf</span></span>
<span data-ttu-id="61f2e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f2e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61f2e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61f2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f2e-135">CommonParameters</span></span>
<span data-ttu-id="61f2e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61f2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f2e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f2e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f2e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61f2e-138">INPUTS</span></span>

### <span data-ttu-id="61f2e-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="61f2e-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="61f2e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="61f2e-140">System.String</span></span>

## <span data-ttu-id="61f2e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61f2e-141">OUTPUTS</span></span>

### <span data-ttu-id="61f2e-142">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="61f2e-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="61f2e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61f2e-143">NOTES</span></span>

## <span data-ttu-id="61f2e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61f2e-144">RELATED LINKS</span></span>
