---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: 78ad8ee76aeeec4f57e0d2f2a6b2a1f4d9424d97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939048"
---
# <span data-ttu-id="97b04-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="97b04-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="97b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b04-102">SYNOPSIS</span></span>
<span data-ttu-id="97b04-103">Bir dosyaya kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="97b04-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97b04-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97b04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97b04-105">DESCRIPTION</span></span>
<span data-ttu-id="97b04-106">**Save-AzureRmResourceGroupDeploymentTemplate** cmdlet 'ı bir JSON dosyasına kaynak grubu dağıtım şablonunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="97b04-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="97b04-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97b04-107">EXAMPLES</span></span>

### <span data-ttu-id="97b04-108">Örnek 1: Dağıtım şablonunu kaydetme</span><span class="sxs-lookup"><span data-stu-id="97b04-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="97b04-109">Bu komut TestDeployment 'den Dağıtım şablonunu alır ve geçerli dizine JSON dosyası olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="97b04-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="97b04-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97b04-110">PARAMETERS</span></span>

### <span data-ttu-id="97b04-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="97b04-111">-ApiVersion</span></span>
<span data-ttu-id="97b04-112">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="97b04-113">Belirtilmezse, en son API sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97b04-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="97b04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b04-114">-DefaultProfile</span></span>
<span data-ttu-id="97b04-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97b04-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97b04-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="97b04-116">-DeploymentName</span></span>
<span data-ttu-id="97b04-117">Dağıtımın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="97b04-118">-Force</span><span class="sxs-lookup"><span data-stu-id="97b04-118">-Force</span></span>
<span data-ttu-id="97b04-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="97b04-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97b04-120">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="97b04-120">-InformationAction</span></span>
<span data-ttu-id="97b04-121">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="97b04-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97b04-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97b04-123">'A</span><span class="sxs-lookup"><span data-stu-id="97b04-123">Continue</span></span>
- <span data-ttu-id="97b04-124">Manıza</span><span class="sxs-lookup"><span data-stu-id="97b04-124">Ignore</span></span>
- <span data-ttu-id="97b04-125">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="97b04-125">Inquire</span></span>
- <span data-ttu-id="97b04-126">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="97b04-126">SilentlyContinue</span></span>
- <span data-ttu-id="97b04-127">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="97b04-127">Stop</span></span>
- <span data-ttu-id="97b04-128">Biliriz</span><span class="sxs-lookup"><span data-stu-id="97b04-128">Suspend</span></span>

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

### <span data-ttu-id="97b04-129">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="97b04-129">-InformationVariable</span></span>
<span data-ttu-id="97b04-130">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97b04-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="97b04-131">-Path</span></span>
<span data-ttu-id="97b04-132">Şablon dosyasının çıkış yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="97b04-133">-Pre-</span><span class="sxs-lookup"><span data-stu-id="97b04-133">-Pre</span></span>
<span data-ttu-id="97b04-134">Bu cmdlet 'in hangi API sürümünü kullanacağını otomatik olarak belirlerken sürüm öncesi API sürümlerini kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b04-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="97b04-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b04-135">-ResourceGroupName</span></span>
<span data-ttu-id="97b04-136">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b04-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="97b04-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="97b04-137">-Confirm</span></span>
<span data-ttu-id="97b04-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97b04-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b04-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b04-139">-WhatIf</span></span>
<span data-ttu-id="97b04-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b04-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b04-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97b04-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b04-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b04-142">CommonParameters</span></span>
<span data-ttu-id="97b04-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97b04-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b04-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b04-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b04-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97b04-145">INPUTS</span></span>

## <span data-ttu-id="97b04-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97b04-146">OUTPUTS</span></span>

## <span data-ttu-id="97b04-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97b04-147">NOTES</span></span>

## <span data-ttu-id="97b04-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97b04-148">RELATED LINKS</span></span>
