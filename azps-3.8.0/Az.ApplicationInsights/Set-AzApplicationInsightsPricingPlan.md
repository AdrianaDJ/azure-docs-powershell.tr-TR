---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098221"
---
# <span data-ttu-id="8808b-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8808b-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="8808b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8808b-102">SYNOPSIS</span></span>
<span data-ttu-id="8808b-103">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8808b-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="8808b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8808b-104">SYNTAX</span></span>

### <span data-ttu-id="8808b-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8808b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8808b-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="8808b-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8808b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8808b-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8808b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8808b-108">DESCRIPTION</span></span>
<span data-ttu-id="8808b-109">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8808b-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="8808b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8808b-110">EXAMPLES</span></span>

### <span data-ttu-id="8808b-111">Örnek 1 bir Application Insights kaynağı için fiyatlandırma planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8808b-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="8808b-112">Fiyatlandırma planını "temel" olarak ayarlama, günlük veri birimi Cap 'yi günde 400 ' e ayarlama ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="8808b-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8808b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8808b-113">PARAMETERS</span></span>

### <span data-ttu-id="8808b-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="8808b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8808b-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8808b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8808b-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="8808b-116">-DailyCapGB</span></span>
<span data-ttu-id="8808b-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="8808b-117">Daily Cap.</span></span>

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

### <span data-ttu-id="8808b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8808b-118">-DefaultProfile</span></span>
<span data-ttu-id="8808b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8808b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8808b-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="8808b-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="8808b-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="8808b-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="8808b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8808b-122">-Name</span></span>
<span data-ttu-id="8808b-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="8808b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8808b-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="8808b-124">-PricingPlan</span></span>
<span data-ttu-id="8808b-125">Fiyatlandırma planı adı.</span><span class="sxs-lookup"><span data-stu-id="8808b-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="8808b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8808b-126">-ResourceGroupName</span></span>
<span data-ttu-id="8808b-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8808b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8808b-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8808b-128">-ResourceId</span></span>
<span data-ttu-id="8808b-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8808b-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8808b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8808b-130">-Confirm</span></span>
<span data-ttu-id="8808b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8808b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8808b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8808b-132">-WhatIf</span></span>
<span data-ttu-id="8808b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8808b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8808b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8808b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8808b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8808b-135">CommonParameters</span></span>
<span data-ttu-id="8808b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8808b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8808b-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8808b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8808b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8808b-138">INPUTS</span></span>

### <span data-ttu-id="8808b-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8808b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8808b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8808b-140">System.String</span></span>

## <span data-ttu-id="8808b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8808b-141">OUTPUTS</span></span>

### <span data-ttu-id="8808b-142">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="8808b-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="8808b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8808b-143">NOTES</span></span>

## <span data-ttu-id="8808b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8808b-144">RELATED LINKS</span></span>
