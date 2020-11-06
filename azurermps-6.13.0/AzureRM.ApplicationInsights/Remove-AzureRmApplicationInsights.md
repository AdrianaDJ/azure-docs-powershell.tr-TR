---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573026"
---
# <span data-ttu-id="d92e6-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d92e6-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="d92e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d92e6-103">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d92e6-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d92e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d92e6-104">SYNTAX</span></span>

### <span data-ttu-id="d92e6-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d92e6-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92e6-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="d92e6-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d92e6-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d92e6-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92e6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d92e6-108">DESCRIPTION</span></span>
<span data-ttu-id="d92e6-109">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d92e6-109">Remove an application insights resource</span></span>

## <span data-ttu-id="d92e6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d92e6-110">EXAMPLES</span></span>

### <span data-ttu-id="d92e6-111">Örnek 1 Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d92e6-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="d92e6-112">"Testgroup" kaynak grubunda "test" adlı bir applcıation Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d92e6-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="d92e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d92e6-113">PARAMETERS</span></span>

### <span data-ttu-id="d92e6-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="d92e6-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d92e6-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d92e6-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d92e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92e6-116">-DefaultProfile</span></span>
<span data-ttu-id="d92e6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d92e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d92e6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d92e6-118">-Name</span></span>
<span data-ttu-id="d92e6-119">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="d92e6-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d92e6-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d92e6-120">-PassThru</span></span>
<span data-ttu-id="d92e6-121">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="d92e6-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="d92e6-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d92e6-122">This parameter is optional.</span></span> <span data-ttu-id="d92e6-123">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="d92e6-123">Default value is false.</span></span>

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

### <span data-ttu-id="d92e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="d92e6-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d92e6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d92e6-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d92e6-126">-ResourceId</span></span>
<span data-ttu-id="d92e6-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d92e6-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d92e6-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d92e6-128">-Confirm</span></span>
<span data-ttu-id="d92e6-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d92e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92e6-130">-WhatIf</span></span>
<span data-ttu-id="d92e6-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d92e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92e6-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d92e6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92e6-133">CommonParameters</span></span>
<span data-ttu-id="d92e6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d92e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92e6-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92e6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92e6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d92e6-136">INPUTS</span></span>

### <span data-ttu-id="d92e6-137">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d92e6-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="d92e6-138">Parametreler: Applicationınsightscomponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d92e6-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="d92e6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d92e6-139">System.String</span></span>

## <span data-ttu-id="d92e6-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d92e6-140">OUTPUTS</span></span>

### <span data-ttu-id="d92e6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d92e6-141">System.Boolean</span></span>

## <span data-ttu-id="d92e6-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d92e6-142">NOTES</span></span>

## <span data-ttu-id="d92e6-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d92e6-143">RELATED LINKS</span></span>
