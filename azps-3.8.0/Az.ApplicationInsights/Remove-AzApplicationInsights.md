---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: d9aa737a34e106fc8514c0e9bbbcfb70b73f015a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104143"
---
# <span data-ttu-id="8e6aa-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8e6aa-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="8e6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6aa-103">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e6aa-103">Remove an application insights resource</span></span>

## <span data-ttu-id="8e6aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e6aa-104">SYNTAX</span></span>

### <span data-ttu-id="8e6aa-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e6aa-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e6aa-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="8e6aa-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e6aa-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8e6aa-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e6aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e6aa-108">DESCRIPTION</span></span>
<span data-ttu-id="8e6aa-109">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e6aa-109">Remove an application insights resource</span></span>

## <span data-ttu-id="8e6aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e6aa-110">EXAMPLES</span></span>

### <span data-ttu-id="8e6aa-111">Örnek 1 Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e6aa-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="8e6aa-112">"Testgroup" kaynak grubundaki "test" adlı bir Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e6aa-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="8e6aa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e6aa-113">PARAMETERS</span></span>

### <span data-ttu-id="8e6aa-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="8e6aa-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8e6aa-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8e6aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6aa-116">-DefaultProfile</span></span>
<span data-ttu-id="8e6aa-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e6aa-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e6aa-118">-Name</span></span>
<span data-ttu-id="8e6aa-119">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="8e6aa-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8e6aa-120">-PassThru</span></span>
<span data-ttu-id="8e6aa-121">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="8e6aa-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-122">This parameter is optional.</span></span> <span data-ttu-id="8e6aa-123">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-123">Default value is false.</span></span>

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

### <span data-ttu-id="8e6aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e6aa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e6aa-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8e6aa-126">-ResourceId</span></span>
<span data-ttu-id="8e6aa-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8e6aa-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e6aa-128">-Confirm</span></span>
<span data-ttu-id="8e6aa-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e6aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e6aa-130">-WhatIf</span></span>
<span data-ttu-id="8e6aa-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e6aa-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e6aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6aa-133">CommonParameters</span></span>
<span data-ttu-id="8e6aa-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e6aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6aa-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e6aa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6aa-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e6aa-136">INPUTS</span></span>

### <span data-ttu-id="8e6aa-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8e6aa-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8e6aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e6aa-138">System.String</span></span>

## <span data-ttu-id="8e6aa-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e6aa-139">OUTPUTS</span></span>

### <span data-ttu-id="8e6aa-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e6aa-140">System.Boolean</span></span>

## <span data-ttu-id="8e6aa-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e6aa-141">NOTES</span></span>

## <span data-ttu-id="8e6aa-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e6aa-142">RELATED LINKS</span></span>
