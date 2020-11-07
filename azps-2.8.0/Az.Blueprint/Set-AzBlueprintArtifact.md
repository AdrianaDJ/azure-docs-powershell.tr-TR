---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 6bd05fc372afc6ef04c943906de8b3eb99cc0aa5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753108"
---
# <span data-ttu-id="e7345-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="e7345-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="e7345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7345-102">SYNOPSIS</span></span>
<span data-ttu-id="e7345-103">Şeması tanımında bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e7345-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="e7345-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7345-104">SYNTAX</span></span>


### <span data-ttu-id="e7345-105">UpdateTemplateArtifact (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7345-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7345-106">Updateartifactbygirdidosyası</span><span class="sxs-lookup"><span data-stu-id="e7345-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7345-107">Updateroleatama</span><span class="sxs-lookup"><span data-stu-id="e7345-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7345-108">Updatepolicyassignmentarmaact</span><span class="sxs-lookup"><span data-stu-id="e7345-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7345-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7345-109">DESCRIPTION</span></span>
<span data-ttu-id="e7345-110">Bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e7345-110">Update an artifact.</span></span> <span data-ttu-id="e7345-111">Bir yapıyı güncelleştirmenin iki yolu vardır: giriş dosyası olarak bir yapıt veya yapıt için satır içi parametreler sağlama.</span><span class="sxs-lookup"><span data-stu-id="e7345-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="e7345-112">JSON yöntemi, sağlanan yapıt türünün, satır içi parametre yönteminin sağlanması için kullanıcının, yapıt türü parametre türünü sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7345-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="e7345-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7345-113">EXAMPLES</span></span>

### <span data-ttu-id="e7345-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7345-114">Example 1</span></span>
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

<span data-ttu-id="e7345-115">Bir yapıyı bir yapıt JSON dosyası aracılığıyla güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e7345-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="e7345-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7345-116">Example 2</span></span>
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

<span data-ttu-id="e7345-117">Bir yapıyı satır içi parametreler aracılığıyla güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="e7345-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="e7345-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e7345-118">Example 3</span></span>
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

<span data-ttu-id="e7345-119">ARM şablon dosyası aracılığıyla bir yapıyı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e7345-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="e7345-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7345-120">PARAMETERS</span></span>

### <span data-ttu-id="e7345-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="e7345-121">-ArtifactFile</span></span>
<span data-ttu-id="e7345-122">Disk üzerinde JSON biçiminde yapıt dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="e7345-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e7345-123">-Blueprint</span></span>
<span data-ttu-id="e7345-124">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e7345-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7345-125">-DefaultProfile</span></span>
<span data-ttu-id="e7345-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7345-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-127">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="e7345-127">-DependsOn</span></span>
<span data-ttu-id="e7345-128">Geçerli yapıt yaratılmadan önce oluşturulması gereken yapıların adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="e7345-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e7345-129">-Description</span></span>
<span data-ttu-id="e7345-130">Yapının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e7345-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7345-131">-Name</span></span>
<span data-ttu-id="e7345-132">Yapının adı</span><span class="sxs-lookup"><span data-stu-id="e7345-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-133">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="e7345-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="e7345-134">İlke tanımının tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="e7345-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="e7345-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="e7345-136">İlke tanımı yapısına geçirmek için parametrelerin Hashtable 'ı.</span><span class="sxs-lookup"><span data-stu-id="e7345-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7345-137">-ResourceGroupName</span></span>
<span data-ttu-id="e7345-138">Yapının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e7345-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-139">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="e7345-139">-RoleDefinitionId</span></span>
<span data-ttu-id="e7345-140">Rol tanımı listesi</span><span class="sxs-lookup"><span data-stu-id="e7345-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-141">-Roledefinitionprincipalıd</span><span class="sxs-lookup"><span data-stu-id="e7345-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="e7345-142">Rol tanımı sorumlu kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e7345-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e7345-143">-TemplateFile</span></span>
<span data-ttu-id="e7345-144">Diskteki ARM şablon dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="e7345-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e7345-145">-TemplateParameterFile</span></span>
<span data-ttu-id="e7345-146">Diskteki ARM şablon parametre dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="e7345-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-147">-Tür</span><span class="sxs-lookup"><span data-stu-id="e7345-147">-Type</span></span>
<span data-ttu-id="e7345-148">Yapıt türü.</span><span class="sxs-lookup"><span data-stu-id="e7345-148">Type of the artifact.</span></span>
<span data-ttu-id="e7345-149">Üç tür desteklenmektedir: Roleatamamenüsü, polic, Policyas, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="e7345-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7345-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7345-150">CommonParameters</span></span>
<span data-ttu-id="e7345-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7345-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7345-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7345-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7345-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7345-153">INPUTS</span></span>

### <span data-ttu-id="e7345-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e7345-154">System.String</span></span>

### <span data-ttu-id="e7345-155">Microsoft. Azure. Commands. Blueprint. modeller. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="e7345-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="e7345-156">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e7345-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e7345-157">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e7345-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e7345-158">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7345-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e7345-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="e7345-159">System.String[]</span></span>

## <span data-ttu-id="e7345-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7345-160">OUTPUTS</span></span>

### <span data-ttu-id="e7345-161">Microsoft. Azure. Management. Blueprint. modeller. Artifact</span><span class="sxs-lookup"><span data-stu-id="e7345-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="e7345-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7345-162">NOTES</span></span>

## <span data-ttu-id="e7345-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7345-163">RELATED LINKS</span></span>
