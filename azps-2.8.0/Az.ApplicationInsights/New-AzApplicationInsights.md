---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: d04b2e54e10a88edd3273ecd96697ab993e97c98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753382"
---
# <span data-ttu-id="6beb7-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6beb7-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="6beb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beb7-102">SYNOPSIS</span></span>
<span data-ttu-id="6beb7-103">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6beb7-103">Create a new application insights resource</span></span>

## <span data-ttu-id="6beb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6beb7-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6beb7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6beb7-105">DESCRIPTION</span></span>
<span data-ttu-id="6beb7-106">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6beb7-106">Create a new application insights resource</span></span>

## <span data-ttu-id="6beb7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6beb7-107">EXAMPLES</span></span>

### <span data-ttu-id="6beb7-108">Örnek 1 yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6beb7-108">Example 1 Create a new application insights resource</span></span>
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
```

<span data-ttu-id="6beb7-109">"Testgroup" kaynak grubuna "test" olarak adlandırılan yeni bir Application Insights kaynağı "Java" türü.</span><span class="sxs-lookup"><span data-stu-id="6beb7-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="6beb7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6beb7-110">PARAMETERS</span></span>

### <span data-ttu-id="6beb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beb7-111">-DefaultProfile</span></span>
<span data-ttu-id="6beb7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6beb7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6beb7-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="6beb7-113">-Kind</span></span>
<span data-ttu-id="6beb7-114">Uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="6beb7-114">Application kind.</span></span>

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

### <span data-ttu-id="6beb7-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6beb7-115">-Location</span></span>
<span data-ttu-id="6beb7-116">Application Insights kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="6beb7-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="6beb7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6beb7-117">-Name</span></span>
<span data-ttu-id="6beb7-118">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6beb7-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="6beb7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6beb7-119">-ResourceGroupName</span></span>
<span data-ttu-id="6beb7-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6beb7-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="6beb7-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6beb7-121">-Tag</span></span>
<span data-ttu-id="6beb7-122">Bileşen etiketleri.</span><span class="sxs-lookup"><span data-stu-id="6beb7-122">Component Tags.</span></span>

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

### <span data-ttu-id="6beb7-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6beb7-123">-Confirm</span></span>
<span data-ttu-id="6beb7-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6beb7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6beb7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6beb7-125">-WhatIf</span></span>
<span data-ttu-id="6beb7-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6beb7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6beb7-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6beb7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6beb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beb7-128">CommonParameters</span></span>
<span data-ttu-id="6beb7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6beb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beb7-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6beb7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beb7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6beb7-131">INPUTS</span></span>

### <span data-ttu-id="6beb7-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6beb7-132">None</span></span>

## <span data-ttu-id="6beb7-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6beb7-133">OUTPUTS</span></span>

### <span data-ttu-id="6beb7-134">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6beb7-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="6beb7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6beb7-135">NOTES</span></span>

## <span data-ttu-id="6beb7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6beb7-136">RELATED LINKS</span></span>
