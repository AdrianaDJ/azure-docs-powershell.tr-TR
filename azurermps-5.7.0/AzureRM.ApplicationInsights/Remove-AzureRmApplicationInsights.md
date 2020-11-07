---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763592"
---
# <span data-ttu-id="b133b-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b133b-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="b133b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b133b-102">SYNOPSIS</span></span>
<span data-ttu-id="b133b-103">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b133b-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b133b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b133b-104">SYNTAX</span></span>

### <span data-ttu-id="b133b-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b133b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b133b-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="b133b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b133b-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b133b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b133b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b133b-108">DESCRIPTION</span></span>
<span data-ttu-id="b133b-109">Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b133b-109">Remove an application insights resource</span></span>

## <span data-ttu-id="b133b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b133b-110">EXAMPLES</span></span>

### <span data-ttu-id="b133b-111">Örnek 1 Application Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b133b-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="b133b-112">"Testgroup" kaynak grubunda "test" adlı bir applcıation Insights kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b133b-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="b133b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b133b-113">PARAMETERS</span></span>

### <span data-ttu-id="b133b-114">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="b133b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b133b-115">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b133b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b133b-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="b133b-116">-Confirm</span></span>
<span data-ttu-id="b133b-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b133b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b133b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b133b-118">-DefaultProfile</span></span>
<span data-ttu-id="b133b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b133b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b133b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b133b-120">-Name</span></span>
<span data-ttu-id="b133b-121">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="b133b-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b133b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b133b-122">-PassThru</span></span>
<span data-ttu-id="b133b-123">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="b133b-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b133b-124">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b133b-124">This parameter is optional.</span></span> <span data-ttu-id="b133b-125">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="b133b-125">Default value is false.</span></span>

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

### <span data-ttu-id="b133b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b133b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b133b-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b133b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b133b-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b133b-128">-ResourceId</span></span>
<span data-ttu-id="b133b-129">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b133b-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b133b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b133b-130">-WhatIf</span></span>
<span data-ttu-id="b133b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b133b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b133b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b133b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b133b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b133b-133">CommonParameters</span></span>
<span data-ttu-id="b133b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b133b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b133b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b133b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b133b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b133b-136">INPUTS</span></span>

### <span data-ttu-id="b133b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b133b-137">System.String</span></span>

## <span data-ttu-id="b133b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b133b-138">OUTPUTS</span></span>

### <span data-ttu-id="b133b-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="b133b-139">System.Object</span></span>

## <span data-ttu-id="b133b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b133b-140">NOTES</span></span>

## <span data-ttu-id="b133b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b133b-141">RELATED LINKS</span></span>

