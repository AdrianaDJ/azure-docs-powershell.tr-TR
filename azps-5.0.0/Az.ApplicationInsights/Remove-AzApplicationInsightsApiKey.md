---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279123"
---
# <span data-ttu-id="73dbc-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="73dbc-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="73dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="73dbc-103">Application Insights kaynağı için Application Insights API anahtarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73dbc-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="73dbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73dbc-104">SYNTAX</span></span>

### <span data-ttu-id="73dbc-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73dbc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73dbc-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="73dbc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73dbc-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="73dbc-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73dbc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73dbc-108">DESCRIPTION</span></span>
<span data-ttu-id="73dbc-109">Application Insights kaynağı için Application Insights API anahtarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73dbc-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="73dbc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73dbc-110">EXAMPLES</span></span>

### <span data-ttu-id="73dbc-111">Örnek 1 Application Insights kaynağı için Application Insights API 'sini kaldırma</span><span class="sxs-lookup"><span data-stu-id="73dbc-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="73dbc-112">"TestGroup" kaynak grubundaki "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" kaynak grubundaki belirli Application Insights API 'sini kaldır.</span><span class="sxs-lookup"><span data-stu-id="73dbc-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="73dbc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73dbc-113">PARAMETERS</span></span>

### <span data-ttu-id="73dbc-114">-Apıkeyıd</span><span class="sxs-lookup"><span data-stu-id="73dbc-114">-ApiKeyId</span></span>
<span data-ttu-id="73dbc-115">Application Insights API anahtar KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="73dbc-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="73dbc-116">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="73dbc-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="73dbc-117">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="73dbc-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="73dbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73dbc-118">-DefaultProfile</span></span>
<span data-ttu-id="73dbc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73dbc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73dbc-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="73dbc-120">-Name</span></span>
<span data-ttu-id="73dbc-121">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="73dbc-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="73dbc-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="73dbc-122">-PassThru</span></span>
<span data-ttu-id="73dbc-123">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="73dbc-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="73dbc-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73dbc-124">This parameter is optional.</span></span> <span data-ttu-id="73dbc-125">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="73dbc-125">Default value is false.</span></span>

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

### <span data-ttu-id="73dbc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73dbc-126">-ResourceGroupName</span></span>
<span data-ttu-id="73dbc-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="73dbc-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="73dbc-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73dbc-128">-ResourceId</span></span>
<span data-ttu-id="73dbc-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="73dbc-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="73dbc-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="73dbc-130">-Confirm</span></span>
<span data-ttu-id="73dbc-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73dbc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73dbc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73dbc-132">-WhatIf</span></span>
<span data-ttu-id="73dbc-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73dbc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73dbc-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73dbc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73dbc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73dbc-135">CommonParameters</span></span>
<span data-ttu-id="73dbc-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73dbc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73dbc-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73dbc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73dbc-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73dbc-138">INPUTS</span></span>

### <span data-ttu-id="73dbc-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73dbc-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="73dbc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="73dbc-140">System.String</span></span>

## <span data-ttu-id="73dbc-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73dbc-141">OUTPUTS</span></span>

### <span data-ttu-id="73dbc-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73dbc-142">System.Boolean</span></span>

## <span data-ttu-id="73dbc-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73dbc-143">NOTES</span></span>

## <span data-ttu-id="73dbc-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73dbc-144">RELATED LINKS</span></span>
