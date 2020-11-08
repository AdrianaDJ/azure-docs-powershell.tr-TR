---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 5ee859811ce791f57fc8c4fa08d2584b28bef1dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096474"
---
# <span data-ttu-id="b22d5-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="b22d5-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="b22d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b22d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b22d5-103">Yeni bir yapıt oluşturun ve bunu bir şeması tanımı içinde kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b22d5-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="b22d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b22d5-104">SYNTAX</span></span>

### <span data-ttu-id="b22d5-105">CreateTemplateArtifact (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b22d5-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22d5-106">Createartifactbygirdidosyası</span><span class="sxs-lookup"><span data-stu-id="b22d5-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22d5-107">Createroleatama</span><span class="sxs-lookup"><span data-stu-id="b22d5-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b22d5-108">Createpolicyartıact</span><span class="sxs-lookup"><span data-stu-id="b22d5-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b22d5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b22d5-109">DESCRIPTION</span></span>
<span data-ttu-id="b22d5-110">Yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b22d5-110">Create a new artifact.</span></span> <span data-ttu-id="b22d5-111">Yapı oluşturmak için iki yol vardır: giriş dosyası olarak bir yapıt veya yapıt için satır içi parametreler sağlama.</span><span class="sxs-lookup"><span data-stu-id="b22d5-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="b22d5-112">JSON yöntemi, sağlanan yapıt türünün, satır içi parametre yönteminin sağlanması için kullanıcının, yapıt türü parametre türünü sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b22d5-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="b22d5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b22d5-113">EXAMPLES</span></span>

### <span data-ttu-id="b22d5-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b22d5-114">Example 1</span></span>
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

<span data-ttu-id="b22d5-115">Bir yapıt JSON dosyası aracılığıyla yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b22d5-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="b22d5-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b22d5-116">Example 2</span></span>
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

<span data-ttu-id="b22d5-117">Satır içi parametreler aracılığıyla yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b22d5-117">Create a new artifact through inline parameters.</span></span>


### <span data-ttu-id="b22d5-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b22d5-118">Example 3</span></span>
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

<span data-ttu-id="b22d5-119">ARM şablon dosyası aracılığıyla yeni bir yapı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b22d5-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="b22d5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b22d5-120">PARAMETERS</span></span>

### <span data-ttu-id="b22d5-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="b22d5-121">-ArtifactFile</span></span>
<span data-ttu-id="b22d5-122">Disk üzerinde JSON biçiminde yapıt dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="b22d5-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="b22d5-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="b22d5-123">-Blueprint</span></span>
<span data-ttu-id="b22d5-124">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b22d5-124">Blueprint object.</span></span>

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

### <span data-ttu-id="b22d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22d5-125">-DefaultProfile</span></span>
<span data-ttu-id="b22d5-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b22d5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b22d5-127">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="b22d5-127">-DependsOn</span></span>
<span data-ttu-id="b22d5-128">Geçerli yapıt yaratılmadan önce oluşturulması gereken yapıların adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="b22d5-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="b22d5-129">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b22d5-129">-Description</span></span>
<span data-ttu-id="b22d5-130">Yapının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="b22d5-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="b22d5-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="b22d5-131">-Name</span></span>
<span data-ttu-id="b22d5-132">Yapının adı</span><span class="sxs-lookup"><span data-stu-id="b22d5-132">Name of the artifact</span></span>

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

### <span data-ttu-id="b22d5-133">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="b22d5-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="b22d5-134">İlke tanımının tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="b22d5-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="b22d5-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="b22d5-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="b22d5-136">İlke tanımı yapısına geçirmek için parametrelerin Hashtable 'ı.</span><span class="sxs-lookup"><span data-stu-id="b22d5-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="b22d5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b22d5-137">-ResourceGroupName</span></span>
<span data-ttu-id="b22d5-138">Yapının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b22d5-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="b22d5-139">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="b22d5-139">-RoleDefinitionId</span></span>
<span data-ttu-id="b22d5-140">Rol tanımı listesi</span><span class="sxs-lookup"><span data-stu-id="b22d5-140">List of role definition</span></span>

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

### <span data-ttu-id="b22d5-141">-Roledefinitionprincipalıd</span><span class="sxs-lookup"><span data-stu-id="b22d5-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="b22d5-142">Rol tanımı sorumlu kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="b22d5-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="b22d5-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b22d5-143">-TemplateFile</span></span>
<span data-ttu-id="b22d5-144">Diskteki ARM şablon dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="b22d5-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="b22d5-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b22d5-145">-TemplateParameterFile</span></span>
<span data-ttu-id="b22d5-146">Diskteki ARM şablon parametre dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="b22d5-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="b22d5-147">-Tür</span><span class="sxs-lookup"><span data-stu-id="b22d5-147">-Type</span></span>
<span data-ttu-id="b22d5-148">Yapıt türü.</span><span class="sxs-lookup"><span data-stu-id="b22d5-148">Type of the artifact.</span></span>
<span data-ttu-id="b22d5-149">Üç tür desteklenmektedir: Roleatamamenüsü, polic, Policyas, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="b22d5-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="b22d5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22d5-150">CommonParameters</span></span>
<span data-ttu-id="b22d5-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b22d5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b22d5-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b22d5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22d5-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b22d5-153">INPUTS</span></span>

### <span data-ttu-id="b22d5-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b22d5-154">System.String</span></span>

### <span data-ttu-id="b22d5-155">Microsoft. Azure. Commands. Blueprint. modeller. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="b22d5-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="b22d5-156">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b22d5-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b22d5-157">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b22d5-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b22d5-158">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b22d5-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b22d5-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="b22d5-159">System.String[]</span></span>

## <span data-ttu-id="b22d5-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b22d5-160">OUTPUTS</span></span>

### <span data-ttu-id="b22d5-161">Microsoft. Azure. Management. Blueprint. modeller. Artifact</span><span class="sxs-lookup"><span data-stu-id="b22d5-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="b22d5-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b22d5-162">NOTES</span></span>

## <span data-ttu-id="b22d5-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b22d5-163">RELATED LINKS</span></span>
