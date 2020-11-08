---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279720"
---
# <span data-ttu-id="afc74-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="afc74-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="afc74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc74-102">SYNOPSIS</span></span>
<span data-ttu-id="afc74-103">Application Insights kaynağında sürekli dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="afc74-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="afc74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afc74-104">SYNTAX</span></span>

### <span data-ttu-id="afc74-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="afc74-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc74-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="afc74-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc74-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="afc74-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="afc74-108">DESCRIPTION</span></span>
<span data-ttu-id="afc74-109">Application Insights kaynağında sürekli dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="afc74-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="afc74-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afc74-110">EXAMPLES</span></span>

### <span data-ttu-id="afc74-111">Örnek 1 Application Insights kaynağında sürekli dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="afc74-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="afc74-112">"Testgroup" kaynak grubundaki "test" adlı kaynak için "uGOoki0jQsyEs3IdQ83Q4QsNr4</span><span class="sxs-lookup"><span data-stu-id="afc74-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="afc74-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afc74-113">PARAMETERS</span></span>

### <span data-ttu-id="afc74-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="afc74-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="afc74-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="afc74-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="afc74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc74-116">-DefaultProfile</span></span>
<span data-ttu-id="afc74-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afc74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afc74-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="afc74-118">-ExportId</span></span>
<span data-ttu-id="afc74-119">Application Insights sürekli dışarı aktarma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="afc74-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="afc74-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="afc74-120">-Name</span></span>
<span data-ttu-id="afc74-121">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="afc74-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="afc74-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="afc74-122">-PassThru</span></span>
<span data-ttu-id="afc74-123">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="afc74-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="afc74-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="afc74-124">This parameter is optional.</span></span> <span data-ttu-id="afc74-125">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="afc74-125">Default value is false.</span></span>

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

### <span data-ttu-id="afc74-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc74-126">-ResourceGroupName</span></span>
<span data-ttu-id="afc74-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="afc74-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="afc74-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="afc74-128">-ResourceId</span></span>
<span data-ttu-id="afc74-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="afc74-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="afc74-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="afc74-130">-Confirm</span></span>
<span data-ttu-id="afc74-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afc74-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc74-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc74-132">-WhatIf</span></span>
<span data-ttu-id="afc74-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afc74-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc74-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afc74-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc74-135">CommonParameters</span></span>
<span data-ttu-id="afc74-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afc74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc74-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afc74-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc74-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afc74-138">INPUTS</span></span>

### <span data-ttu-id="afc74-139">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="afc74-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="afc74-140">System. String</span><span class="sxs-lookup"><span data-stu-id="afc74-140">System.String</span></span>

## <span data-ttu-id="afc74-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afc74-141">OUTPUTS</span></span>

### <span data-ttu-id="afc74-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afc74-142">System.Boolean</span></span>

## <span data-ttu-id="afc74-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afc74-143">NOTES</span></span>

## <span data-ttu-id="afc74-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afc74-144">RELATED LINKS</span></span>
