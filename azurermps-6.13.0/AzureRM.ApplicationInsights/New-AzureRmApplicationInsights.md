---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 48922d3e0cbf8cf322d25657c76ee01e0ee238b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587317"
---
# <span data-ttu-id="c57df-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c57df-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="c57df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c57df-102">SYNOPSIS</span></span>
<span data-ttu-id="c57df-103">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c57df-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c57df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c57df-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c57df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c57df-105">DESCRIPTION</span></span>
<span data-ttu-id="c57df-106">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c57df-106">Create a new application insights resource</span></span>

## <span data-ttu-id="c57df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c57df-107">EXAMPLES</span></span>

### <span data-ttu-id="c57df-108">Örnek 1 yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c57df-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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

<span data-ttu-id="c57df-109">"Testgroup" kaynak grubuna "test" olarak adlandırılan yeni bir Application Insights kaynağı "Java" türü.</span><span class="sxs-lookup"><span data-stu-id="c57df-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="c57df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c57df-110">PARAMETERS</span></span>

### <span data-ttu-id="c57df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57df-111">-DefaultProfile</span></span>
<span data-ttu-id="c57df-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c57df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c57df-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="c57df-113">-Kind</span></span>
<span data-ttu-id="c57df-114">Uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="c57df-114">Application kind.</span></span>

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

### <span data-ttu-id="c57df-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="c57df-115">-Location</span></span>
<span data-ttu-id="c57df-116">Application Insights kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="c57df-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="c57df-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c57df-117">-Name</span></span>
<span data-ttu-id="c57df-118">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c57df-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="c57df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57df-119">-ResourceGroupName</span></span>
<span data-ttu-id="c57df-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c57df-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="c57df-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c57df-121">-Tag</span></span>
<span data-ttu-id="c57df-122">Bileşen etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c57df-122">Component Tags.</span></span>

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

### <span data-ttu-id="c57df-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c57df-123">-Confirm</span></span>
<span data-ttu-id="c57df-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c57df-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57df-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57df-125">-WhatIf</span></span>
<span data-ttu-id="c57df-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c57df-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c57df-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c57df-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57df-128">CommonParameters</span></span>
<span data-ttu-id="c57df-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c57df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57df-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57df-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57df-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c57df-131">INPUTS</span></span>

### <span data-ttu-id="c57df-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c57df-132">None</span></span>

## <span data-ttu-id="c57df-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c57df-133">OUTPUTS</span></span>

### <span data-ttu-id="c57df-134">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c57df-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c57df-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c57df-135">NOTES</span></span>

## <span data-ttu-id="c57df-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c57df-136">RELATED LINKS</span></span>
