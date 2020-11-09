---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322687"
---
# <span data-ttu-id="5027c-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="5027c-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="5027c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5027c-102">SYNOPSIS</span></span>
<span data-ttu-id="5027c-103">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5027c-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="5027c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5027c-104">SYNTAX</span></span>

### <span data-ttu-id="5027c-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5027c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5027c-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="5027c-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5027c-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5027c-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5027c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5027c-108">DESCRIPTION</span></span>
<span data-ttu-id="5027c-109">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5027c-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="5027c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5027c-110">EXAMPLES</span></span>

### <span data-ttu-id="5027c-111">Örnek 1 bir Application Insights kaynağı için fiyatlandırma planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5027c-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="5027c-112">Fiyatlandırma planını "temel" olarak ayarlama, günlük veri birimi Cap 'yi günde 400 ' e ayarlama ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="5027c-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="5027c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5027c-113">PARAMETERS</span></span>

### <span data-ttu-id="5027c-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="5027c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="5027c-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5027c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="5027c-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="5027c-116">-DailyCapGB</span></span>
<span data-ttu-id="5027c-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="5027c-117">Daily Cap.</span></span>

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

### <span data-ttu-id="5027c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5027c-118">-DefaultProfile</span></span>
<span data-ttu-id="5027c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5027c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5027c-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="5027c-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="5027c-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="5027c-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="5027c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5027c-122">-Name</span></span>
<span data-ttu-id="5027c-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="5027c-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="5027c-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="5027c-124">-PricingPlan</span></span>
<span data-ttu-id="5027c-125">Fiyatlandırma planı adı.</span><span class="sxs-lookup"><span data-stu-id="5027c-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="5027c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5027c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5027c-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5027c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5027c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5027c-128">-ResourceId</span></span>
<span data-ttu-id="5027c-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5027c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="5027c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="5027c-130">-Confirm</span></span>
<span data-ttu-id="5027c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5027c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5027c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5027c-132">-WhatIf</span></span>
<span data-ttu-id="5027c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5027c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5027c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5027c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5027c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5027c-135">CommonParameters</span></span>
<span data-ttu-id="5027c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5027c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5027c-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5027c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5027c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5027c-138">INPUTS</span></span>

### <span data-ttu-id="5027c-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5027c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="5027c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5027c-140">System.String</span></span>

## <span data-ttu-id="5027c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5027c-141">OUTPUTS</span></span>

### <span data-ttu-id="5027c-142">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="5027c-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="5027c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5027c-143">NOTES</span></span>

## <span data-ttu-id="5027c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5027c-144">RELATED LINKS</span></span>
