---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107974"
---
# <span data-ttu-id="b7735-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b7735-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="b7735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7735-102">SYNOPSIS</span></span>
<span data-ttu-id="b7735-103">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7735-103">Create a new application insights resource</span></span>

## <span data-ttu-id="b7735-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7735-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7735-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7735-105">DESCRIPTION</span></span>
<span data-ttu-id="b7735-106">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7735-106">Create a new application insights resource</span></span>

## <span data-ttu-id="b7735-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7735-107">EXAMPLES</span></span>

### <span data-ttu-id="b7735-108">Örnek 1 yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7735-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="b7735-109">"Testgroup" kaynak grubuna "test" olarak adlandırılan yeni bir Application Insights kaynağı "Java" türü</span><span class="sxs-lookup"><span data-stu-id="b7735-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="b7735-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7735-110">PARAMETERS</span></span>

### <span data-ttu-id="b7735-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7735-111">-DefaultProfile</span></span>
<span data-ttu-id="b7735-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7735-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7735-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="b7735-113">-Kind</span></span>
<span data-ttu-id="b7735-114">Uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="b7735-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="b7735-115">-Location</span></span>
<span data-ttu-id="b7735-116">Application Insights kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="b7735-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7735-117">-Name</span></span>
<span data-ttu-id="b7735-118">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b7735-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="b7735-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="b7735-120">Uygulama öngörülerini uygulamaya erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="b7735-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="b7735-121">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="b7735-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="b7735-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="b7735-123">Application Insights sorgusuna erişmek için ağ erişim türü.</span><span class="sxs-lookup"><span data-stu-id="b7735-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="b7735-124">Değer ' Enabled ' veya ' Disabled ' olmalıdır</span><span class="sxs-lookup"><span data-stu-id="b7735-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7735-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7735-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b7735-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b7735-127">-RetentionInDays</span></span>
<span data-ttu-id="b7735-128">Gün Içinde 90 varsayılan olarak.</span><span class="sxs-lookup"><span data-stu-id="b7735-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b7735-129">-Tag</span></span>
<span data-ttu-id="b7735-130">Bileşen etiketleri.</span><span class="sxs-lookup"><span data-stu-id="b7735-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7735-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7735-131">-Confirm</span></span>
<span data-ttu-id="b7735-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7735-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7735-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7735-133">-WhatIf</span></span>
<span data-ttu-id="b7735-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7735-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7735-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7735-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7735-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7735-136">CommonParameters</span></span>
<span data-ttu-id="b7735-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7735-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7735-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7735-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7735-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7735-139">INPUTS</span></span>

### <span data-ttu-id="b7735-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7735-140">None</span></span>

## <span data-ttu-id="b7735-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7735-141">OUTPUTS</span></span>

### <span data-ttu-id="b7735-142">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b7735-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="b7735-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7735-143">NOTES</span></span>

## <span data-ttu-id="b7735-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7735-144">RELATED LINKS</span></span>
