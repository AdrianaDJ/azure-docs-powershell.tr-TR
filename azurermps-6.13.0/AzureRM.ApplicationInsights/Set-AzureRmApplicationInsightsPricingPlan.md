---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 03c1a556f6b3fc207fbbb612f31d172705e4f42b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588626"
---
# <span data-ttu-id="c725f-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c725f-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="c725f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c725f-102">SYNOPSIS</span></span>
<span data-ttu-id="c725f-103">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c725f-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c725f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c725f-104">SYNTAX</span></span>

### <span data-ttu-id="c725f-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c725f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c725f-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="c725f-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c725f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c725f-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c725f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c725f-108">DESCRIPTION</span></span>
<span data-ttu-id="c725f-109">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c725f-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="c725f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c725f-110">EXAMPLES</span></span>

### <span data-ttu-id="c725f-111">Örnek 1 bir Application Insights kaynağı için fiyatlandırma planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c725f-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="c725f-112">Fiyatlandırma planını "temel" olarak ayarlayın, günlük veri Volumen Cap 'i günde 400 ' e ayarlayın ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="c725f-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c725f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c725f-113">PARAMETERS</span></span>

### <span data-ttu-id="c725f-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="c725f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c725f-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c725f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c725f-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="c725f-116">-DailyCapGB</span></span>
<span data-ttu-id="c725f-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="c725f-117">Daily Cap.</span></span>

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

### <span data-ttu-id="c725f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c725f-118">-DefaultProfile</span></span>
<span data-ttu-id="c725f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c725f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c725f-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="c725f-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="c725f-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="c725f-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="c725f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c725f-122">-Name</span></span>
<span data-ttu-id="c725f-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="c725f-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c725f-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="c725f-124">-PricingPlan</span></span>
<span data-ttu-id="c725f-125">Fiyatlandırma planı adı.</span><span class="sxs-lookup"><span data-stu-id="c725f-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="c725f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c725f-126">-ResourceGroupName</span></span>
<span data-ttu-id="c725f-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c725f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c725f-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c725f-128">-ResourceId</span></span>
<span data-ttu-id="c725f-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c725f-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c725f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c725f-130">-Confirm</span></span>
<span data-ttu-id="c725f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c725f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c725f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c725f-132">-WhatIf</span></span>
<span data-ttu-id="c725f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c725f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c725f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c725f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c725f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c725f-135">CommonParameters</span></span>
<span data-ttu-id="c725f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c725f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c725f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c725f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c725f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c725f-138">INPUTS</span></span>

### <span data-ttu-id="c725f-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c725f-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="c725f-140">Parametreler: Applicationınsightscomponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c725f-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="c725f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c725f-141">System.String</span></span>

## <span data-ttu-id="c725f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c725f-142">OUTPUTS</span></span>

### <span data-ttu-id="c725f-143">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c725f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="c725f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c725f-144">NOTES</span></span>

## <span data-ttu-id="c725f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c725f-145">RELATED LINKS</span></span>
