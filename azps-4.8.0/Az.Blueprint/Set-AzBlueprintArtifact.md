---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110047"
---
# <span data-ttu-id="9764f-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="9764f-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="9764f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9764f-102">SYNOPSIS</span></span>
<span data-ttu-id="9764f-103">Şeması tanımında bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9764f-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="9764f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9764f-104">SYNTAX</span></span>

### <span data-ttu-id="9764f-105">UpdateTemplateArtifact (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9764f-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9764f-106">Updateartifactbygirdidosyası</span><span class="sxs-lookup"><span data-stu-id="9764f-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9764f-107">Updateroleatama</span><span class="sxs-lookup"><span data-stu-id="9764f-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9764f-108">Updatepolicyassignmentarmaact</span><span class="sxs-lookup"><span data-stu-id="9764f-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9764f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9764f-109">DESCRIPTION</span></span>
<span data-ttu-id="9764f-110">Bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9764f-110">Update an artifact.</span></span> <span data-ttu-id="9764f-111">Bir yapıyı güncelleştirmenin iki yolu vardır: giriş dosyası olarak bir yapıt veya yapıt için satır içi parametreler sağlama.</span><span class="sxs-lookup"><span data-stu-id="9764f-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="9764f-112">JSON yöntemi, sağlanan yapıt türünün, satır içi parametre yönteminin sağlanması için kullanıcının, yapıt türü parametre türünü sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9764f-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="9764f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9764f-113">EXAMPLES</span></span>

### <span data-ttu-id="9764f-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9764f-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="9764f-115">Bir yapıyı bir yapıt JSON dosyası aracılığıyla güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9764f-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="9764f-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9764f-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="9764f-117">Bir yapıyı satır içi parametreler aracılığıyla güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="9764f-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="9764f-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9764f-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="9764f-119">ARM şablon dosyası aracılığıyla bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="9764f-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="9764f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9764f-120">PARAMETERS</span></span>

### <span data-ttu-id="9764f-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="9764f-121">-ArtifactFile</span></span>
<span data-ttu-id="9764f-122">Disk üzerinde JSON biçiminde yapıt dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="9764f-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="9764f-123">-Blueprint</span></span>
<span data-ttu-id="9764f-124">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9764f-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9764f-125">-DefaultProfile</span></span>
<span data-ttu-id="9764f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9764f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9764f-127">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="9764f-127">-DependsOn</span></span>
<span data-ttu-id="9764f-128">Geçerli yapıt yaratılmadan önce oluşturulması gereken yapıların adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="9764f-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9764f-129">-Description</span></span>
<span data-ttu-id="9764f-130">Yapının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9764f-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="9764f-131">-Name</span></span>
<span data-ttu-id="9764f-132">Yapının adı</span><span class="sxs-lookup"><span data-stu-id="9764f-132">Name of the artifact</span></span>

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

### <span data-ttu-id="9764f-133">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="9764f-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="9764f-134">İlke tanımının tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="9764f-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="9764f-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="9764f-136">İlke tanımı yapısına geçirmek için parametrelerin Hashtable 'ı.</span><span class="sxs-lookup"><span data-stu-id="9764f-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9764f-137">-ResourceGroupName</span></span>
<span data-ttu-id="9764f-138">Yapının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9764f-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-139">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="9764f-139">-RoleDefinitionId</span></span>
<span data-ttu-id="9764f-140">Rol tanımı listesi</span><span class="sxs-lookup"><span data-stu-id="9764f-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-141">-Roledefinitionprincipalıd</span><span class="sxs-lookup"><span data-stu-id="9764f-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="9764f-142">Rol tanımı sorumlu kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="9764f-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9764f-143">-TemplateFile</span></span>
<span data-ttu-id="9764f-144">Diskteki ARM şablon dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="9764f-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9764f-145">-TemplateParameterFile</span></span>
<span data-ttu-id="9764f-146">Diskteki ARM şablon parametre dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="9764f-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-147">-Tür</span><span class="sxs-lookup"><span data-stu-id="9764f-147">-Type</span></span>
<span data-ttu-id="9764f-148">Yapıt türü.</span><span class="sxs-lookup"><span data-stu-id="9764f-148">Type of the artifact.</span></span>
<span data-ttu-id="9764f-149">Üç tür desteklenmektedir: Roleatamamenüsü, polic, Policyas, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="9764f-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9764f-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="9764f-150">-Confirm</span></span>
<span data-ttu-id="9764f-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9764f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9764f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9764f-152">-WhatIf</span></span>
<span data-ttu-id="9764f-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9764f-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9764f-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9764f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9764f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9764f-155">CommonParameters</span></span>
<span data-ttu-id="9764f-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9764f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9764f-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9764f-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9764f-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9764f-158">INPUTS</span></span>

### <span data-ttu-id="9764f-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9764f-159">System.String</span></span>

### <span data-ttu-id="9764f-160">Microsoft. Azure. Commands. Blueprint. modeller. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="9764f-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="9764f-161">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="9764f-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="9764f-162">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9764f-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9764f-163">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9764f-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9764f-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="9764f-164">System.String[]</span></span>

## <span data-ttu-id="9764f-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9764f-165">OUTPUTS</span></span>

### <span data-ttu-id="9764f-166">Microsoft. Azure. Management. Blueprint. modeller. Artifact</span><span class="sxs-lookup"><span data-stu-id="9764f-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="9764f-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9764f-167">NOTES</span></span>

## <span data-ttu-id="9764f-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9764f-168">RELATED LINKS</span></span>
