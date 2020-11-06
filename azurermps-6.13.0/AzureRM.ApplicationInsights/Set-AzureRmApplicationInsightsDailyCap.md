---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588628"
---
# <span data-ttu-id="9ca5b-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="9ca5b-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="9ca5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca5b-103">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="9ca5b-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ca5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ca5b-104">SYNTAX</span></span>

### <span data-ttu-id="9ca5b-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ca5b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca5b-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="9ca5b-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca5b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9ca5b-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ca5b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ca5b-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca5b-109">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="9ca5b-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="9ca5b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ca5b-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca5b-111">Örnek 1 bir Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="9ca5b-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="9ca5b-112">Günlük veri Volumen Cap 'i gün başına 400 ' e ayarlayın ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="9ca5b-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9ca5b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ca5b-113">PARAMETERS</span></span>

### <span data-ttu-id="9ca5b-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="9ca5b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9ca5b-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9ca5b-116">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="9ca5b-116">-DailyCapGB</span></span>
<span data-ttu-id="9ca5b-117">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-117">Daily Cap.</span></span>

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

### <span data-ttu-id="9ca5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca5b-118">-DefaultProfile</span></span>
<span data-ttu-id="9ca5b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ca5b-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="9ca5b-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="9ca5b-121">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="9ca5b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ca5b-122">-Name</span></span>
<span data-ttu-id="9ca5b-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9ca5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ca5b-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ca5b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9ca5b-126">-ResourceId</span></span>
<span data-ttu-id="9ca5b-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9ca5b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ca5b-128">-Confirm</span></span>
<span data-ttu-id="9ca5b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca5b-130">-WhatIf</span></span>
<span data-ttu-id="9ca5b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ca5b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca5b-133">CommonParameters</span></span>
<span data-ttu-id="9ca5b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca5b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ca5b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca5b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ca5b-136">INPUTS</span></span>

### <span data-ttu-id="9ca5b-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9ca5b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="9ca5b-138">Parametreler: Applicationınsightscomponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9ca5b-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="9ca5b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ca5b-139">System.String</span></span>

## <span data-ttu-id="9ca5b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ca5b-140">OUTPUTS</span></span>

### <span data-ttu-id="9ca5b-141">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="9ca5b-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="9ca5b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ca5b-142">NOTES</span></span>

## <span data-ttu-id="9ca5b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ca5b-143">RELATED LINKS</span></span>
