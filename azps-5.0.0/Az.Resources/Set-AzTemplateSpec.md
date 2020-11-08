---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277038"
---
# <span data-ttu-id="4538c-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="4538c-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="4538c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4538c-102">SYNOPSIS</span></span>
<span data-ttu-id="4538c-103">Şablon belirtiminin değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4538c-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="4538c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4538c-104">SYNTAX</span></span>

### <span data-ttu-id="4538c-105">FromJsonStringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4538c-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4538c-106">Updatebyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4538c-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538c-107">Updateversionbyıdfromjsonfileparameterset</span><span class="sxs-lookup"><span data-stu-id="4538c-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538c-108">Updateversionbyıdfromjsonparameterset</span><span class="sxs-lookup"><span data-stu-id="4538c-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538c-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4538c-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538c-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4538c-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4538c-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="4538c-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4538c-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="4538c-112">DESCRIPTION</span></span>
<span data-ttu-id="4538c-113">Templace spec 'i değiştirir. Belirtilen ad ve/veya belirli bir sürüme sahip şablon belirtimi yoksa, oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4538c-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="4538c-114">Şablon spec sürümünün ARM şablonu içeriğini değiştirirken, içerik ham bir JSON dizesinden ( **Updateversionbynamefromjsonparameterset** parametre kümesi) veya BELIRTILEN bir JSON dosyasından ( **Updateversionbynamefromjsonfileparameterset** parametre kümesi kullanılarak) gelebilir.</span><span class="sxs-lookup"><span data-stu-id="4538c-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="4538c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4538c-115">EXAMPLES</span></span>

### <span data-ttu-id="4538c-116">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="4538c-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="4538c-117">"MyTemplateSpec" adlı şablon belirtiminin "v 1.0" sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4538c-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="4538c-118">Belirtilen sürümün sürümün ARM şablonu içeriği olarak $templateJson olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4538c-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="4538c-119">Kök şablon belirtimi ve/veya sürümü henüz yoksa, oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4538c-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="4538c-120">**Notlarında**</span><span class="sxs-lookup"><span data-stu-id="4538c-120">**Notes:**</span></span> 

* <span data-ttu-id="4538c-121">Örnekteki ARM şablonu hiçbir gerçek kaynak içermediğinden işlem yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="4538c-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="4538c-122">Konum yalnızca şablon belirtimi yoksa gereklidir</span><span class="sxs-lookup"><span data-stu-id="4538c-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="4538c-123">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="4538c-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="4538c-124">"MyTemplateSpec" adlı şablon belirtiminin "v 2.0" sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4538c-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="4538c-125">Belirtilen sürüm, sürümün ARM şablon içeriği olarak "myTemplateContent.jsaçık" yerel dosyasının içeriğine sahip olacak.</span><span class="sxs-lookup"><span data-stu-id="4538c-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="4538c-126">Kök şablon belirtimi ve/veya sürümü henüz yoksa, oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4538c-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="4538c-127">**Not:** Konum yalnızca şablon belirtimi yoksa gereklidir</span><span class="sxs-lookup"><span data-stu-id="4538c-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="4538c-128">Örnek 3:</span><span class="sxs-lookup"><span data-stu-id="4538c-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="4538c-129">"MyRG" kaynak grubundaki "myTemplateSpec" adlı şablon belirtiminin açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4538c-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="4538c-130">Şablon belirtimi henüz yoksa oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4538c-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="4538c-131">**Not:** Konum yalnızca şablon belirtimi yoksa gereklidir</span><span class="sxs-lookup"><span data-stu-id="4538c-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="4538c-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4538c-132">PARAMETERS</span></span>

### <span data-ttu-id="4538c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4538c-133">-DefaultProfile</span></span>
<span data-ttu-id="4538c-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4538c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4538c-135">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="4538c-135">-Description</span></span>
<span data-ttu-id="4538c-136">Şablon belirtiminin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="4538c-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4538c-137">-DisplayName</span></span>
<span data-ttu-id="4538c-138">Şablon belirtiminin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="4538c-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-139">-Konum</span><span class="sxs-lookup"><span data-stu-id="4538c-139">-Location</span></span>
<span data-ttu-id="4538c-140">Şablon belirtiminin konumu. Yalnızca şablon belirtimi yoksa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4538c-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="4538c-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="4538c-141">-Name</span></span>
<span data-ttu-id="4538c-142">Şablon belirtiminin adı.</span><span class="sxs-lookup"><span data-stu-id="4538c-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4538c-143">-ResourceGroupName</span></span>
<span data-ttu-id="4538c-144">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4538c-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4538c-145">-ResourceId</span></span>
<span data-ttu-id="4538c-146">Şablon belirtiminin tam kaynak kimliği. örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="4538c-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4538c-147">-TemplateFile</span></span>
<span data-ttu-id="4538c-148">Yerel Azure Kaynak Yöneticisi şablonu JSON dosyasının dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="4538c-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-149">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="4538c-149">-TemplateJson</span></span>
<span data-ttu-id="4538c-150">Azure Resource Manager şablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="4538c-150">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-151">-Version</span><span class="sxs-lookup"><span data-stu-id="4538c-151">-Version</span></span>
<span data-ttu-id="4538c-152">Şablon belirtiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="4538c-152">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="4538c-153">-VersionDescription</span></span>
<span data-ttu-id="4538c-154">Sürümün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="4538c-154">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4538c-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="4538c-155">-Confirm</span></span>
<span data-ttu-id="4538c-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4538c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4538c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4538c-157">-WhatIf</span></span>
<span data-ttu-id="4538c-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4538c-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4538c-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4538c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4538c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4538c-160">CommonParameters</span></span>
<span data-ttu-id="4538c-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4538c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4538c-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4538c-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4538c-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4538c-163">INPUTS</span></span>

### <span data-ttu-id="4538c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="4538c-164">System.String</span></span>

## <span data-ttu-id="4538c-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4538c-165">OUTPUTS</span></span>

### <span data-ttu-id="4538c-166">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="4538c-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="4538c-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4538c-167">NOTES</span></span>

## <span data-ttu-id="4538c-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4538c-168">RELATED LINKS</span></span>
