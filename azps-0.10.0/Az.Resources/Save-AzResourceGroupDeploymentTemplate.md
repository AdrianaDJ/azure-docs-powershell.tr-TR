---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936328"
---
# <span data-ttu-id="fa18d-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fa18d-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="fa18d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa18d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa18d-103">Bir dosyaya kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fa18d-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="fa18d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa18d-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa18d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa18d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa18d-106">**Save-AzResourceGroupDeploymentTemplate** cmdlet 'ı bir JSON dosyasına kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fa18d-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="fa18d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa18d-107">EXAMPLES</span></span>

### <span data-ttu-id="fa18d-108">Örnek 1: Dağıtım şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="fa18d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="fa18d-109">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fa18d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="fa18d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa18d-110">PARAMETERS</span></span>

### <span data-ttu-id="fa18d-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="fa18d-111">-ApiVersion</span></span>
<span data-ttu-id="fa18d-112">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fa18d-113">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fa18d-113">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa18d-114">-DefaultProfile</span></span>
<span data-ttu-id="fa18d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa18d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="fa18d-116">-DeploymentName</span></span>
<span data-ttu-id="fa18d-117">Dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa18d-118">-Force</span></span>
<span data-ttu-id="fa18d-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fa18d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa18d-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fa18d-120">-InformationAction</span></span>
<span data-ttu-id="fa18d-121">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="fa18d-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fa18d-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa18d-123">'A</span><span class="sxs-lookup"><span data-stu-id="fa18d-123">Continue</span></span>
- <span data-ttu-id="fa18d-124">Manıza</span><span class="sxs-lookup"><span data-stu-id="fa18d-124">Ignore</span></span>
- <span data-ttu-id="fa18d-125">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fa18d-125">Inquire</span></span>
- <span data-ttu-id="fa18d-126">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fa18d-126">SilentlyContinue</span></span>
- <span data-ttu-id="fa18d-127">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fa18d-127">Stop</span></span>
- <span data-ttu-id="fa18d-128">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fa18d-128">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-129">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fa18d-129">-InformationVariable</span></span>
<span data-ttu-id="fa18d-130">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-130">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="fa18d-131">-Path</span></span>
<span data-ttu-id="fa18d-132">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="fa18d-133">-Pre</span></span>
<span data-ttu-id="fa18d-134">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="fa18d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa18d-135">-ResourceGroupName</span></span>
<span data-ttu-id="fa18d-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa18d-137">-Confirm</span></span>
<span data-ttu-id="fa18d-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa18d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa18d-139">-WhatIf</span></span>
<span data-ttu-id="fa18d-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa18d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa18d-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa18d-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa18d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa18d-142">CommonParameters</span></span>
<span data-ttu-id="fa18d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa18d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa18d-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa18d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa18d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa18d-145">INPUTS</span></span>

## <span data-ttu-id="fa18d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa18d-146">OUTPUTS</span></span>

## <span data-ttu-id="fa18d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa18d-147">NOTES</span></span>

## <span data-ttu-id="fa18d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa18d-148">RELATED LINKS</span></span>
