---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593519"
---
# <span data-ttu-id="10110-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="10110-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="10110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10110-102">SYNOPSIS</span></span>
<span data-ttu-id="10110-103">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="10110-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10110-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10110-104">SYNTAX</span></span>

### <span data-ttu-id="10110-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10110-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10110-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="10110-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10110-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="10110-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10110-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="10110-108">DESCRIPTION</span></span>
<span data-ttu-id="10110-109">Bir Application Insights kaynağı için fiyat planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="10110-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="10110-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10110-110">EXAMPLES</span></span>

### <span data-ttu-id="10110-111">Örnek 1 bir Application Insights kaynağı için fiyatlandırma planı ve günlük veri birimi bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="10110-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="10110-112">Fiyatlandırma planını "temel" olarak ayarlayın, günlük veri Volumen Cap 'i günde 400 ' e ayarlayın ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="10110-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="10110-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10110-113">PARAMETERS</span></span>

### <span data-ttu-id="10110-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="10110-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="10110-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="10110-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10110-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="10110-116">-Confirm</span></span>
<span data-ttu-id="10110-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10110-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-118">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="10110-118">-DailyCapGB</span></span>
<span data-ttu-id="10110-119">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="10110-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10110-120">-DefaultProfile</span></span>
<span data-ttu-id="10110-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10110-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="10110-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="10110-123">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="10110-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="10110-124">-Name</span></span>
<span data-ttu-id="10110-125">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="10110-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="10110-126">-PricingPlan</span></span>
<span data-ttu-id="10110-127">Fiyatlandırma planı adı.</span><span class="sxs-lookup"><span data-stu-id="10110-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10110-128">-ResourceGroupName</span></span>
<span data-ttu-id="10110-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="10110-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="10110-130">-ResourceId</span></span>
<span data-ttu-id="10110-131">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="10110-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10110-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10110-132">-WhatIf</span></span>
<span data-ttu-id="10110-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10110-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10110-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10110-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10110-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10110-135">CommonParameters</span></span>
<span data-ttu-id="10110-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10110-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10110-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10110-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10110-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10110-138">INPUTS</span></span>

### <span data-ttu-id="10110-139">System. String</span><span class="sxs-lookup"><span data-stu-id="10110-139">System.String</span></span>
<span data-ttu-id="10110-140">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10110-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="10110-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10110-141">OUTPUTS</span></span>

### <span data-ttu-id="10110-142">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="10110-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="10110-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10110-143">NOTES</span></span>

## <span data-ttu-id="10110-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10110-144">RELATED LINKS</span></span>

