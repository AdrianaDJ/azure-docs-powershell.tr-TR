---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764780"
---
# <span data-ttu-id="b5859-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b5859-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="b5859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5859-102">SYNOPSIS</span></span>
<span data-ttu-id="b5859-103">Bir dosyaya kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b5859-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5859-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5859-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5859-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5859-105">DESCRIPTION</span></span>
<span data-ttu-id="b5859-106">**Save-AzureRmResourceGroupDeploymentTemplate** cmdlet 'ı bir JSON dosyasına kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b5859-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="b5859-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5859-107">EXAMPLES</span></span>

### <span data-ttu-id="b5859-108">Örnek 1: Dağıtım şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="b5859-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="b5859-109">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b5859-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="b5859-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5859-110">PARAMETERS</span></span>

### <span data-ttu-id="b5859-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="b5859-111">-ApiVersion</span></span>
<span data-ttu-id="b5859-112">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b5859-113">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5859-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="b5859-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b5859-114">-DeploymentName</span></span>
<span data-ttu-id="b5859-115">Dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="b5859-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b5859-116">-Force</span></span>
<span data-ttu-id="b5859-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b5859-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5859-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b5859-118">-InformationAction</span></span>
<span data-ttu-id="b5859-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5859-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5859-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5859-121">'A</span><span class="sxs-lookup"><span data-stu-id="b5859-121">Continue</span></span>
- <span data-ttu-id="b5859-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="b5859-122">Ignore</span></span>
- <span data-ttu-id="b5859-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b5859-123">Inquire</span></span>
- <span data-ttu-id="b5859-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b5859-124">SilentlyContinue</span></span>
- <span data-ttu-id="b5859-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b5859-125">Stop</span></span>
- <span data-ttu-id="b5859-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b5859-126">Suspend</span></span>

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

### <span data-ttu-id="b5859-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b5859-127">-InformationVariable</span></span>
<span data-ttu-id="b5859-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5859-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="b5859-129">-Path</span></span>
<span data-ttu-id="b5859-130">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="b5859-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="b5859-131">-Pre</span></span>
<span data-ttu-id="b5859-132">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5859-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="b5859-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5859-133">-ResourceGroupName</span></span>
<span data-ttu-id="b5859-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5859-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b5859-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5859-135">-Confirm</span></span>
<span data-ttu-id="b5859-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5859-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5859-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5859-137">-WhatIf</span></span>
<span data-ttu-id="b5859-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5859-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5859-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5859-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5859-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5859-140">-DefaultProfile</span></span>
<span data-ttu-id="b5859-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5859-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5859-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5859-142">CommonParameters</span></span>
<span data-ttu-id="b5859-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5859-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5859-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5859-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5859-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5859-145">INPUTS</span></span>

## <span data-ttu-id="b5859-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5859-146">OUTPUTS</span></span>

### <span data-ttu-id="b5859-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b5859-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b5859-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5859-148">NOTES</span></span>

## <span data-ttu-id="b5859-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5859-149">RELATED LINKS</span></span>

