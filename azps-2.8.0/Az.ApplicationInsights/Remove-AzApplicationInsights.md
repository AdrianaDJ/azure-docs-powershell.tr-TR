---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 5665b85a680411910513663d782791f56b7c1081
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753377"
---
# <span data-ttu-id="73e02-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="73e02-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="73e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e02-102">SYNOPSIS</span></span>
<span data-ttu-id="73e02-103">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73e02-103">Remove an application insights resource</span></span>

## <span data-ttu-id="73e02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73e02-104">SYNTAX</span></span>

### <span data-ttu-id="73e02-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73e02-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73e02-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="73e02-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73e02-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="73e02-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e02-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73e02-108">DESCRIPTION</span></span>
<span data-ttu-id="73e02-109">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73e02-109">Remove an application insights resource</span></span>

## <span data-ttu-id="73e02-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73e02-110">EXAMPLES</span></span>

### <span data-ttu-id="73e02-111">Örnek 1 Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73e02-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="73e02-112">"Testgroup" kaynak grubundaki "test" adlı bir Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="73e02-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="73e02-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73e02-113">PARAMETERS</span></span>

### <span data-ttu-id="73e02-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="73e02-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="73e02-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="73e02-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="73e02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e02-116">-DefaultProfile</span></span>
<span data-ttu-id="73e02-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73e02-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e02-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="73e02-118">-Name</span></span>
<span data-ttu-id="73e02-119">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="73e02-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="73e02-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="73e02-120">-PassThru</span></span>
<span data-ttu-id="73e02-121">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="73e02-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="73e02-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73e02-122">This parameter is optional.</span></span> <span data-ttu-id="73e02-123">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="73e02-123">Default value is false.</span></span>

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

### <span data-ttu-id="73e02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e02-124">-ResourceGroupName</span></span>
<span data-ttu-id="73e02-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="73e02-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="73e02-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73e02-126">-ResourceId</span></span>
<span data-ttu-id="73e02-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="73e02-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="73e02-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="73e02-128">-Confirm</span></span>
<span data-ttu-id="73e02-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73e02-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e02-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e02-130">-WhatIf</span></span>
<span data-ttu-id="73e02-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73e02-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73e02-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73e02-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e02-133">CommonParameters</span></span>
<span data-ttu-id="73e02-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73e02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e02-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e02-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73e02-136">INPUTS</span></span>

### <span data-ttu-id="73e02-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73e02-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="73e02-138">System. String</span><span class="sxs-lookup"><span data-stu-id="73e02-138">System.String</span></span>

## <span data-ttu-id="73e02-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73e02-139">OUTPUTS</span></span>

### <span data-ttu-id="73e02-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73e02-140">System.Boolean</span></span>

## <span data-ttu-id="73e02-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73e02-141">NOTES</span></span>

## <span data-ttu-id="73e02-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73e02-142">RELATED LINKS</span></span>
