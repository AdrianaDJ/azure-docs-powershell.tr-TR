---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsights.md
ms.openlocfilehash: 1cbe4a76801de23357d6fc2b2c6400b7e0fb5ba6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917643"
---
# <span data-ttu-id="ca1c6-101">Get-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ca1c6-101">Get-AzApplicationInsights</span></span>

## <span data-ttu-id="ca1c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1c6-103">Application Insights kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="ca1c6-103">Get application insights resources</span></span>

## <span data-ttu-id="ca1c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca1c6-104">SYNTAX</span></span>

### <span data-ttu-id="ca1c6-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca1c6-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzApplicationInsights [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca1c6-106">ComponentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca1c6-106">ComponentNameParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Full]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca1c6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ca1c6-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsights [-ResourceId] <String> [-Full] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca1c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca1c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ca1c6-109">Kaynak grubundaki veya belirli bir kaynaktaki Application Insights kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="ca1c6-109">Get application insights resources in a resource group or specific resource</span></span>

## <span data-ttu-id="ca1c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca1c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ca1c6-111">Örnek 1 Application Insights kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="ca1c6-111">Example 1 Get application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test"

Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
```

<span data-ttu-id="ca1c6-112">"Test" adlı uygulama öngörüleri</span><span class="sxs-lookup"><span data-stu-id="ca1c6-112">Get application insights resource named "test" in resoruce group "testgroup"</span></span>

### <span data-ttu-id="ca1c6-113">Örnek 2 fiyatlandırma planı bilgileriyle Application Insights kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="ca1c6-113">Example 2 Get application insights resource with pricing plan information</span></span>
```
PS C:\> Get-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -IncludePricingPlan

Cap                            : 330
ResetTime                      : 0
StopSendNotificationWhenHitCap : True
CapExpirationTime              :
IsCapped                       : False
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test
ResourceGroupName  : testgroup
Name               : test
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 7c8f0641-d307-41bc-b8f2-d30701adb4b3
ApplicationType    : web
Tags               : {}
CreationDate       : 7/5/2017 4:37:22 PM
FlowType           : Redfield
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 1e30d092-4b4b-47c6-ad39-7c10785d80f5
ProvisioningState  : Succeeded
RequestSource      : IbizaAIExtension
SamplingPercentage :
TenantId           : b90b0dec-9b9a-4778-a84e-4ffb73bb17f7
PricingPlan        : Basic
```

<span data-ttu-id="ca1c6-114">Application Insights kaynağını alın ve "test" adlı kaynak için "testgroup" adlı kaynağın fiyat planı bilgilerini ekleyin</span><span class="sxs-lookup"><span data-stu-id="ca1c6-114">Get application insights resource and include pricing plan information for resource named "test" in resoruce group "testgroup"</span></span>

## <span data-ttu-id="ca1c6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca1c6-115">PARAMETERS</span></span>

### <span data-ttu-id="ca1c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1c6-116">-DefaultProfile</span></span>
<span data-ttu-id="ca1c6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca1c6-118">-Full</span><span class="sxs-lookup"><span data-stu-id="ca1c6-118">-Full</span></span>
<span data-ttu-id="ca1c6-119">Belirtilmişse, Application Insights bileşeninin fiyatlandırma planı/günlük Cap ve durumu geri alır.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-119">If specified, it will get back pricing plan/daily cap and status of the application insights component.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ComponentNameParameterSet, ResourceIdParameterSet
Aliases: IncludeDailyCap, IncludeDailyCapStatus, IncludePricingPlan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca1c6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca1c6-120">-Name</span></span>
<span data-ttu-id="ca1c6-121">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-121">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="ca1c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca1c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca1c6-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="ca1c6-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ca1c6-124">-ResourceId</span></span>
<span data-ttu-id="ca1c6-125">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-125">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ca1c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1c6-126">CommonParameters</span></span>
<span data-ttu-id="ca1c6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca1c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1c6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca1c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1c6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca1c6-129">INPUTS</span></span>

### <span data-ttu-id="ca1c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ca1c6-130">System.String</span></span>

## <span data-ttu-id="ca1c6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca1c6-131">OUTPUTS</span></span>

### <span data-ttu-id="ca1c6-132">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ca1c6-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="ca1c6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca1c6-133">NOTES</span></span>

## <span data-ttu-id="ca1c6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca1c6-134">RELATED LINKS</span></span>