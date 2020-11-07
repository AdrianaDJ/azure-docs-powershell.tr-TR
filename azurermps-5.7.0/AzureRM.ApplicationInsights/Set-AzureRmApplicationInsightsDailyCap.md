---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762391"
---
# <span data-ttu-id="05b9c-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="05b9c-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="05b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="05b9c-103">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="05b9c-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05b9c-104">SYNTAX</span></span>

### <span data-ttu-id="05b9c-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05b9c-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05b9c-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="05b9c-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05b9c-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="05b9c-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05b9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="05b9c-108">DESCRIPTION</span></span>
<span data-ttu-id="05b9c-109">Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="05b9c-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="05b9c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05b9c-110">EXAMPLES</span></span>

### <span data-ttu-id="05b9c-111">Örnek 1 bir Application Insights kaynağı için günlük veri birimi Cap ayarlama</span><span class="sxs-lookup"><span data-stu-id="05b9c-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="05b9c-112">Günlük veri Volumen Cap 'i gün başına 400 ' e ayarlayın ve kaynak grubundaki "test" kaynak grubundaki</span><span class="sxs-lookup"><span data-stu-id="05b9c-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="05b9c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05b9c-113">PARAMETERS</span></span>

### <span data-ttu-id="05b9c-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="05b9c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="05b9c-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05b9c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="05b9c-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="05b9c-116">-Confirm</span></span>
<span data-ttu-id="05b9c-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05b9c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b9c-118">-Günlükcapgb</span><span class="sxs-lookup"><span data-stu-id="05b9c-118">-DailyCapGB</span></span>
<span data-ttu-id="05b9c-119">Günlük uç.</span><span class="sxs-lookup"><span data-stu-id="05b9c-119">Daily Cap.</span></span>

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

### <span data-ttu-id="05b9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b9c-120">-DefaultProfile</span></span>
<span data-ttu-id="05b9c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05b9c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05b9c-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="05b9c-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="05b9c-123">Vurma geldiğinde bildirim göndermeyi durdur.</span><span class="sxs-lookup"><span data-stu-id="05b9c-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="05b9c-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="05b9c-124">-Name</span></span>
<span data-ttu-id="05b9c-125">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="05b9c-125">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="05b9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="05b9c-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="05b9c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="05b9c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="05b9c-128">-ResourceId</span></span>
<span data-ttu-id="05b9c-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="05b9c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="05b9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b9c-130">-WhatIf</span></span>
<span data-ttu-id="05b9c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05b9c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05b9c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05b9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b9c-133">CommonParameters</span></span>
<span data-ttu-id="05b9c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05b9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b9c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b9c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b9c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05b9c-136">INPUTS</span></span>

### <span data-ttu-id="05b9c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="05b9c-137">System.String</span></span>
<span data-ttu-id="05b9c-138">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="05b9c-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="05b9c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05b9c-139">OUTPUTS</span></span>

### <span data-ttu-id="05b9c-140">Microsoft. Azure. Commands. ApplicationInsights. model. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="05b9c-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="05b9c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05b9c-141">NOTES</span></span>

## <span data-ttu-id="05b9c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05b9c-142">RELATED LINKS</span></span>

