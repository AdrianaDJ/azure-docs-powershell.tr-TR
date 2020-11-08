---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104146"
---
# <span data-ttu-id="c08fc-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c08fc-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c08fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c08fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c08fc-103">Application Insights kaynağı için Application Insights API anahtarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c08fc-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c08fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c08fc-104">SYNTAX</span></span>

### <span data-ttu-id="c08fc-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c08fc-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08fc-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="c08fc-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08fc-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c08fc-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c08fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c08fc-108">DESCRIPTION</span></span>
<span data-ttu-id="c08fc-109">Application Insights kaynağı için Application Insights API 'si oluşturma</span><span class="sxs-lookup"><span data-stu-id="c08fc-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c08fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c08fc-110">EXAMPLES</span></span>

### <span data-ttu-id="c08fc-111">Örnek 1 Application Insights kaynağı için yeni bir API anahtarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="c08fc-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="c08fc-112">"TestGroup" kaynak grubundaki "test" kaynağının "Readtelemetri", "Write," "</span><span class="sxs-lookup"><span data-stu-id="c08fc-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c08fc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c08fc-113">PARAMETERS</span></span>

### <span data-ttu-id="c08fc-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="c08fc-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c08fc-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c08fc-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c08fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08fc-116">-DefaultProfile</span></span>
<span data-ttu-id="c08fc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c08fc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c08fc-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c08fc-118">-Description</span></span>
<span data-ttu-id="c08fc-119">Bu API anahtarının belirlenmesine yardımcı olacak açıklama.</span><span class="sxs-lookup"><span data-stu-id="c08fc-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08fc-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c08fc-120">-Name</span></span>
<span data-ttu-id="c08fc-121">Bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="c08fc-121">Component Name.</span></span>

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

### <span data-ttu-id="c08fc-122">-İzinler</span><span class="sxs-lookup"><span data-stu-id="c08fc-122">-Permissions</span></span>
<span data-ttu-id="c08fc-123">API anahtarının uygulamalara yapılmasına izin veren izinler.</span><span class="sxs-lookup"><span data-stu-id="c08fc-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="c08fc-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c08fc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c08fc-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c08fc-126">-ResourceId</span></span>
<span data-ttu-id="c08fc-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c08fc-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c08fc-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c08fc-128">-Confirm</span></span>
<span data-ttu-id="c08fc-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c08fc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08fc-130">-WhatIf</span></span>
<span data-ttu-id="c08fc-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c08fc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c08fc-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c08fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08fc-133">CommonParameters</span></span>
<span data-ttu-id="c08fc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c08fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08fc-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08fc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08fc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c08fc-136">INPUTS</span></span>

### <span data-ttu-id="c08fc-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c08fc-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c08fc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c08fc-138">System.String</span></span>

## <span data-ttu-id="c08fc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c08fc-139">OUTPUTS</span></span>

### <span data-ttu-id="c08fc-140">Microsoft. Azure. Commands. ApplicationInsights. model. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c08fc-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c08fc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c08fc-141">NOTES</span></span>

## <span data-ttu-id="c08fc-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c08fc-142">RELATED LINKS</span></span>
