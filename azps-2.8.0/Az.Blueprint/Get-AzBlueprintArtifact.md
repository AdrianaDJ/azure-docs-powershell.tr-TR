---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753126"
---
# <span data-ttu-id="668f6-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="668f6-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="668f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668f6-102">SYNOPSIS</span></span>
<span data-ttu-id="668f6-103">Bir şeması tanımından yapıları alın.</span><span class="sxs-lookup"><span data-stu-id="668f6-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="668f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="668f6-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="668f6-105">DESCRIPTION</span></span>
<span data-ttu-id="668f6-106">Bir şeması tanımından yapıları alın.</span><span class="sxs-lookup"><span data-stu-id="668f6-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="668f6-107">Şeması tanım sürümü belirtilmemişse taslak sürümü alınır.</span><span class="sxs-lookup"><span data-stu-id="668f6-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="668f6-108">Taslak sürümü olmadığı durumlarda, yayımlanan en son şeması tanımı döndürülür.</span><span class="sxs-lookup"><span data-stu-id="668f6-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="668f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="668f6-109">EXAMPLES</span></span>

### <span data-ttu-id="668f6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="668f6-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="668f6-111">Bir şeması tanımından yapıları alın..</span><span class="sxs-lookup"><span data-stu-id="668f6-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="668f6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="668f6-112">PARAMETERS</span></span>

### <span data-ttu-id="668f6-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="668f6-113">-ArtifactFile</span></span>
<span data-ttu-id="668f6-114">Disk üzerinde JSON biçiminde yapıt dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="668f6-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="668f6-115">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="668f6-115">-Blueprint</span></span>
<span data-ttu-id="668f6-116">Blueprint nesnesi.</span><span class="sxs-lookup"><span data-stu-id="668f6-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="668f6-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="668f6-117">-BlueprintVersion</span></span>
<span data-ttu-id="668f6-118">Tüm yapıları almak için şeması sürümü.</span><span class="sxs-lookup"><span data-stu-id="668f6-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668f6-119">-DefaultProfile</span></span>
<span data-ttu-id="668f6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="668f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668f6-121">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="668f6-121">-DependsOn</span></span>
<span data-ttu-id="668f6-122">Geçerli yapıt yaratılmadan önce oluşturulması gereken yapıların adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="668f6-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="668f6-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="668f6-123">-Description</span></span>
<span data-ttu-id="668f6-124">Yapının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="668f6-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="668f6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="668f6-125">-Name</span></span>
<span data-ttu-id="668f6-126">Yapının adı</span><span class="sxs-lookup"><span data-stu-id="668f6-126">Name of the artifact</span></span>

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

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668f6-127">-Policydefinitionıd</span><span class="sxs-lookup"><span data-stu-id="668f6-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="668f6-128">İlke tanımının tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="668f6-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="668f6-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="668f6-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="668f6-130">İlke tanımı yapısına geçirmek için parametrelerin Hashtable 'ı.</span><span class="sxs-lookup"><span data-stu-id="668f6-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="668f6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668f6-131">-ResourceGroupName</span></span>
<span data-ttu-id="668f6-132">Yapının altında olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="668f6-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="668f6-133">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="668f6-133">-RoleDefinitionId</span></span>
<span data-ttu-id="668f6-134">Rol tanımı listesi</span><span class="sxs-lookup"><span data-stu-id="668f6-134">List of role definition</span></span>

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

### <span data-ttu-id="668f6-135">-Roledefinitionprincipalıd</span><span class="sxs-lookup"><span data-stu-id="668f6-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="668f6-136">Rol tanımı sorumlu kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="668f6-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="668f6-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="668f6-137">-TemplateFile</span></span>
<span data-ttu-id="668f6-138">Diskteki ARM şablon dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="668f6-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="668f6-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="668f6-139">-TemplateParameterFile</span></span>
<span data-ttu-id="668f6-140">Diskteki ARM şablon parametre dosyasının konumu.</span><span class="sxs-lookup"><span data-stu-id="668f6-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="668f6-141">-Tür</span><span class="sxs-lookup"><span data-stu-id="668f6-141">-Type</span></span>
<span data-ttu-id="668f6-142">Yapıt türü.</span><span class="sxs-lookup"><span data-stu-id="668f6-142">Type of the artifact.</span></span>
<span data-ttu-id="668f6-143">Üç tür desteklenmektedir: Roleatamamenüsü, polic, Policyas, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="668f6-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="668f6-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="668f6-144">-Confirm</span></span>
<span data-ttu-id="668f6-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="668f6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668f6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668f6-146">-WhatIf</span></span>
<span data-ttu-id="668f6-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="668f6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668f6-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="668f6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668f6-149">CommonParameters</span></span>
<span data-ttu-id="668f6-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="668f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="668f6-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668f6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668f6-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="668f6-152">INPUTS</span></span>

### <span data-ttu-id="668f6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="668f6-153">System.String</span></span>

### <span data-ttu-id="668f6-154">Microsoft. Azure. Commands. Blueprint. modeller. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="668f6-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="668f6-155">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="668f6-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="668f6-156">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="668f6-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="668f6-157">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="668f6-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="668f6-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="668f6-158">System.String[]</span></span>

## <span data-ttu-id="668f6-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="668f6-159">OUTPUTS</span></span>

### <span data-ttu-id="668f6-160">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="668f6-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="668f6-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="668f6-161">NOTES</span></span>

## <span data-ttu-id="668f6-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="668f6-162">RELATED LINKS</span></span>
