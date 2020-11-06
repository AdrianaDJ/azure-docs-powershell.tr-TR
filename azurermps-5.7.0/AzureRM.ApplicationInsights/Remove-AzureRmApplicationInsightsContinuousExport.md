---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592980"
---
# <span data-ttu-id="66a3c-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="66a3c-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="66a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="66a3c-103">Bir Application Insights kaynağında birlikte gelen bir dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="66a3c-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66a3c-104">SYNTAX</span></span>

### <span data-ttu-id="66a3c-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66a3c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66a3c-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="66a3c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a3c-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="66a3c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a3c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66a3c-108">DESCRIPTION</span></span>
<span data-ttu-id="66a3c-109">Bir Application Insights kaynağında birlikte gelen bir dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="66a3c-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="66a3c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66a3c-110">EXAMPLES</span></span>

### <span data-ttu-id="66a3c-111">Örnek 1 Application Insights kaynağında birlikte gelen bir dışarı aktarma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="66a3c-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="66a3c-112">"Testgroup" kaynak grubundaki "test" adlı kaynak için "uGOoki0jQsyEs3IdQ83Q4QsNr4</span><span class="sxs-lookup"><span data-stu-id="66a3c-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="66a3c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66a3c-113">PARAMETERS</span></span>

### <span data-ttu-id="66a3c-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="66a3c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="66a3c-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="66a3c-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66a3c-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="66a3c-116">-Confirm</span></span>
<span data-ttu-id="66a3c-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66a3c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a3c-118">-DefaultProfile</span></span>
<span data-ttu-id="66a3c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66a3c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a3c-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="66a3c-120">-ExportId</span></span>
<span data-ttu-id="66a3c-121">Application Insights sürekli dışarı aktarma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66a3c-121">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="66a3c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="66a3c-122">-Name</span></span>
<span data-ttu-id="66a3c-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="66a3c-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a3c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66a3c-124">-PassThru</span></span>
<span data-ttu-id="66a3c-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="66a3c-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="66a3c-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="66a3c-126">This parameter is optional.</span></span> <span data-ttu-id="66a3c-127">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="66a3c-127">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a3c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a3c-128">-ResourceGroupName</span></span>
<span data-ttu-id="66a3c-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="66a3c-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a3c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66a3c-130">-ResourceId</span></span>
<span data-ttu-id="66a3c-131">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="66a3c-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a3c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a3c-132">-WhatIf</span></span>
<span data-ttu-id="66a3c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66a3c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a3c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66a3c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a3c-135">CommonParameters</span></span>
<span data-ttu-id="66a3c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66a3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a3c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a3c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a3c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66a3c-138">INPUTS</span></span>

### <span data-ttu-id="66a3c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="66a3c-139">System.String</span></span>

## <span data-ttu-id="66a3c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66a3c-140">OUTPUTS</span></span>

### <span data-ttu-id="66a3c-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="66a3c-141">System.Object</span></span>

## <span data-ttu-id="66a3c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66a3c-142">NOTES</span></span>

## <span data-ttu-id="66a3c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66a3c-143">RELATED LINKS</span></span>

