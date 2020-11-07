---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 23c79f4ceed4e6b9dc537cb6e04fb602fd7a4bbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762876"
---
# <span data-ttu-id="8f849-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8f849-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="8f849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f849-102">SYNOPSIS</span></span>
<span data-ttu-id="8f849-103">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f849-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f849-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f849-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f849-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f849-105">DESCRIPTION</span></span>
<span data-ttu-id="8f849-106">Yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f849-106">Create a new application insights resource</span></span>

## <span data-ttu-id="8f849-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f849-107">EXAMPLES</span></span>

### <span data-ttu-id="8f849-108">Örnek 1 yeni Application Insights kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f849-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="8f849-109">"Testgroup" kaynak grubuna "test" olarak adlandırılan yeni bir Application Insights kaynağı "Java" türü.</span><span class="sxs-lookup"><span data-stu-id="8f849-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="8f849-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f849-110">PARAMETERS</span></span>

### <span data-ttu-id="8f849-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f849-111">-Confirm</span></span>
<span data-ttu-id="8f849-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f849-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f849-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f849-113">-DefaultProfile</span></span>
<span data-ttu-id="8f849-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f849-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f849-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="8f849-115">-Kind</span></span>
<span data-ttu-id="8f849-116">Uygulama türü.</span><span class="sxs-lookup"><span data-stu-id="8f849-116">Application kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f849-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="8f849-117">-Location</span></span>
<span data-ttu-id="8f849-118">Application Insights kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="8f849-118">Application Insights Resource Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f849-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f849-119">-Name</span></span>
<span data-ttu-id="8f849-120">Application Insights kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8f849-120">Application Insights Resource Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f849-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f849-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f849-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8f849-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f849-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8f849-123">-Tag</span></span>
<span data-ttu-id="8f849-124">Bileşen etiketleri.</span><span class="sxs-lookup"><span data-stu-id="8f849-124">Component Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f849-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f849-125">-WhatIf</span></span>
<span data-ttu-id="8f849-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f849-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f849-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f849-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f849-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f849-128">CommonParameters</span></span>
<span data-ttu-id="8f849-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f849-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f849-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f849-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f849-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f849-131">INPUTS</span></span>

### <span data-ttu-id="8f849-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f849-132">System.String</span></span>

## <span data-ttu-id="8f849-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f849-133">OUTPUTS</span></span>

### <span data-ttu-id="8f849-134">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8f849-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="8f849-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f849-135">NOTES</span></span>

## <span data-ttu-id="8f849-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f849-136">RELATED LINKS</span></span>

