---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277041"
---
# <span data-ttu-id="14d6a-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="14d6a-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="14d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="14d6a-103">Yeni bir şablon belirtimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14d6a-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="14d6a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14d6a-104">SYNTAX</span></span>

### <span data-ttu-id="14d6a-105">FromJsonStringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14d6a-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d6a-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d6a-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d6a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="14d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="14d6a-108">Belirtilen ARM şablon içeriğiyle yeni bir şablon belirtimi sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14d6a-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="14d6a-109">İçerik, ham JSON dizesinden ( **Fromjsonstringparameterset** parametre kümesi kullanılarak) veya BELIRTILEN bir JSON dosyasından ( **Fromjsonfileparameterset** parametre kümesi kullanılarak) gelebilir.</span><span class="sxs-lookup"><span data-stu-id="14d6a-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="14d6a-110">Kök şablon belirtimi yoksa, şablon belirtimi sürümüyle birlikte oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="14d6a-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="14d6a-111">Verilen ada sahip bir şablon belirtimi zaten varsa, bu, belirtilen sürüm güncelleştirilir (var olan diğer sürümler korunacak).</span><span class="sxs-lookup"><span data-stu-id="14d6a-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="14d6a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14d6a-112">EXAMPLES</span></span>

### <span data-ttu-id="14d6a-113">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="14d6a-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="14d6a-114">"MyTemplateSpec" adlı bir şablon belirtiminde yeni bir şablon belirtimi sürümü "v 1.0" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14d6a-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="14d6a-115">Belirtilen sürümün sürümün ARM şablonu içeriği olarak $templateJson olacaktır.</span><span class="sxs-lookup"><span data-stu-id="14d6a-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="14d6a-116">**Not:** Örnekteki ARM şablonu hiçbir gerçek kaynak içermediğinden işlem yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="14d6a-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="14d6a-117">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="14d6a-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="14d6a-118">"MyTemplateSpec" adlı bir şablon belirtiminde yeni bir şablon belirtimi sürümü "v 2.0" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14d6a-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="14d6a-119">Belirtilen sürüm, sürümün ARM şablon içeriği olarak "myTemplateContent.jsaçık" yerel dosyasının içeriğine sahip olacak.</span><span class="sxs-lookup"><span data-stu-id="14d6a-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="14d6a-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14d6a-120">PARAMETERS</span></span>

### <span data-ttu-id="14d6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d6a-121">-DefaultProfile</span></span>
<span data-ttu-id="14d6a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14d6a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d6a-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="14d6a-123">-Description</span></span>
<span data-ttu-id="14d6a-124">Şablon belirtiminin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="14d6a-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="14d6a-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14d6a-125">-DisplayName</span></span>
<span data-ttu-id="14d6a-126">Şablon belirtiminin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="14d6a-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="14d6a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="14d6a-127">-Force</span></span>
<span data-ttu-id="14d6a-128">Var olan bir sürümün üzerine yazarken onay sorma.</span><span class="sxs-lookup"><span data-stu-id="14d6a-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="14d6a-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="14d6a-129">-Location</span></span>
<span data-ttu-id="14d6a-130">Şablon belirtiminin konumu. Yalnızca şablon belirtimi yoksa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="14d6a-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="14d6a-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="14d6a-131">-Name</span></span>
<span data-ttu-id="14d6a-132">Şablon belirtiminin adı.</span><span class="sxs-lookup"><span data-stu-id="14d6a-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d6a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d6a-133">-ResourceGroupName</span></span>
<span data-ttu-id="14d6a-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="14d6a-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d6a-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="14d6a-135">-TemplateFile</span></span>
<span data-ttu-id="14d6a-136">Yerel Azure Kaynak Yöneticisi şablonu JSON dosyasının dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="14d6a-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d6a-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="14d6a-137">-TemplateJson</span></span>
<span data-ttu-id="14d6a-138">Azure Resource Manager şablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="14d6a-138">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d6a-139">-Version</span><span class="sxs-lookup"><span data-stu-id="14d6a-139">-Version</span></span>
<span data-ttu-id="14d6a-140">Şablon belirtiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="14d6a-140">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d6a-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="14d6a-141">-VersionDescription</span></span>
<span data-ttu-id="14d6a-142">Sürümün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="14d6a-142">The description of the version.</span></span>

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

### <span data-ttu-id="14d6a-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="14d6a-143">-Confirm</span></span>
<span data-ttu-id="14d6a-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14d6a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d6a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d6a-145">-WhatIf</span></span>
<span data-ttu-id="14d6a-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14d6a-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14d6a-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14d6a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d6a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d6a-148">CommonParameters</span></span>
<span data-ttu-id="14d6a-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14d6a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d6a-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14d6a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d6a-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14d6a-151">INPUTS</span></span>

### <span data-ttu-id="14d6a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="14d6a-152">System.String</span></span>

## <span data-ttu-id="14d6a-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14d6a-153">OUTPUTS</span></span>

### <span data-ttu-id="14d6a-154">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="14d6a-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="14d6a-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14d6a-155">NOTES</span></span>

## <span data-ttu-id="14d6a-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14d6a-156">RELATED LINKS</span></span>
