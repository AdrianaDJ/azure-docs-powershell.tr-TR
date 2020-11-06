---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592985"
---
# <span data-ttu-id="b8c1f-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b8c1f-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="b8c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c1f-103">Application Insights kaynağı için Application Insights API anahtarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8c1f-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8c1f-104">SYNTAX</span></span>

### <span data-ttu-id="b8c1f-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8c1f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c1f-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="b8c1f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c1f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b8c1f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c1f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8c1f-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c1f-109">Application Insights kaynağı için Application Insights API anahtarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8c1f-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b8c1f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c1f-111">Örnek 1 Application Insights kaynağı için Application Insights API 'sini kaldırma</span><span class="sxs-lookup"><span data-stu-id="b8c1f-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="b8c1f-112">"TestGroup" kaynak grubundaki "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" kaynak grubundaki belirli Application Insights API 'sini kaldır.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="b8c1f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8c1f-113">PARAMETERS</span></span>

### <span data-ttu-id="b8c1f-114">-Apıkeyıd</span><span class="sxs-lookup"><span data-stu-id="b8c1f-114">-ApiKeyId</span></span>
<span data-ttu-id="b8c1f-115">Application Insights API anahtar KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="b8c1f-116">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="b8c1f-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b8c1f-117">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b8c1f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8c1f-118">-Confirm</span></span>
<span data-ttu-id="b8c1f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c1f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c1f-120">-DefaultProfile</span></span>
<span data-ttu-id="b8c1f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c1f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8c1f-122">-Name</span></span>
<span data-ttu-id="b8c1f-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b8c1f-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b8c1f-124">-PassThru</span></span>
<span data-ttu-id="b8c1f-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b8c1f-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-126">This parameter is optional.</span></span> <span data-ttu-id="b8c1f-127">Varsayılan değer: false.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-127">Default value is false.</span></span>

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

### <span data-ttu-id="b8c1f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c1f-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8c1f-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b8c1f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b8c1f-130">-ResourceId</span></span>
<span data-ttu-id="b8c1f-131">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b8c1f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c1f-132">-WhatIf</span></span>
<span data-ttu-id="b8c1f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c1f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c1f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c1f-135">CommonParameters</span></span>
<span data-ttu-id="b8c1f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8c1f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c1f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c1f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c1f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8c1f-138">INPUTS</span></span>

### <span data-ttu-id="b8c1f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b8c1f-139">System.String</span></span>

## <span data-ttu-id="b8c1f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8c1f-140">OUTPUTS</span></span>

### <span data-ttu-id="b8c1f-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="b8c1f-141">System.Object</span></span>

## <span data-ttu-id="b8c1f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8c1f-142">NOTES</span></span>

## <span data-ttu-id="b8c1f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8c1f-143">RELATED LINKS</span></span>

