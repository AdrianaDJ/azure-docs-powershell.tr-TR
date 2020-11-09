---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323545"
---
# <span data-ttu-id="112a6-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="112a6-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="112a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="112a6-102">SYNOPSIS</span></span>
<span data-ttu-id="112a6-103">SYNAPSE Analytics rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="112a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="112a6-104">SYNTAX</span></span>

### <span data-ttu-id="112a6-105">GetByWorkspaceNameAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="112a6-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="112a6-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="112a6-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="112a6-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="112a6-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-110">Getbyıo Nesnetandnameparameterset</span><span class="sxs-lookup"><span data-stu-id="112a6-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-111">Getbyıo Nesnetandidparameterset</span><span class="sxs-lookup"><span data-stu-id="112a6-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-112">Getbyıo Nesnetandroledefinitionıdandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="112a6-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-113">Getbyçalışmanesnetandassignmentivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="112a6-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112a6-114">Getbyı</span><span class="sxs-lookup"><span data-stu-id="112a6-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="112a6-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="112a6-115">DESCRIPTION</span></span>
<span data-ttu-id="112a6-116">**Get-AzSynapseRoleAssignment** cmdlet 'ı bir Azure SYNAPSE Analytics rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="112a6-117">Bir rol tanımı veya Kullanıcı asıl adı belirtmezseniz, bu cmdlet tüm rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="112a6-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="112a6-118">EXAMPLES</span></span>

### <span data-ttu-id="112a6-119">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="112a6-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="112a6-120">Bu komut, çalışma alanı altındaki tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="112a6-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="112a6-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="112a6-122">Bu komut, ContosoRole rol adı ile çalışma alanı Contoso'in altındaki tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="112a6-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="112a6-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="112a6-124">Bu komut, ContosoRole rol adı ile çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="112a6-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="112a6-125">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="112a6-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="112a6-126">Bu komut, ardışık düzen aracılığıyla tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="112a6-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="112a6-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="112a6-127">PARAMETERS</span></span>

### <span data-ttu-id="112a6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112a6-128">-DefaultProfile</span></span>
<span data-ttu-id="112a6-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="112a6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="112a6-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="112a6-130">-ObjectId</span></span>
<span data-ttu-id="112a6-131">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="112a6-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-132">-Roleatamakimliği</span><span class="sxs-lookup"><span data-stu-id="112a6-132">-RoleAssignmentId</span></span>
<span data-ttu-id="112a6-133">Rol atamasının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="112a6-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-134">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="112a6-134">-RoleDefinitionId</span></span>
<span data-ttu-id="112a6-135">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="112a6-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="112a6-136">-RoleDefinitionName</span></span>
<span data-ttu-id="112a6-137">Sorumluya atanmış rolün adı.</span><span class="sxs-lookup"><span data-stu-id="112a6-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="112a6-138">-ServicePrincipalName</span></span>
<span data-ttu-id="112a6-139">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="112a6-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-140">-Signınname</span><span class="sxs-lookup"><span data-stu-id="112a6-140">-SignInName</span></span>
<span data-ttu-id="112a6-141">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="112a6-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-142">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="112a6-142">-WorkspaceName</span></span>
<span data-ttu-id="112a6-143">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="112a6-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-144">-</span><span class="sxs-lookup"><span data-stu-id="112a6-144">-WorkspaceObject</span></span>
<span data-ttu-id="112a6-145">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="112a6-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="112a6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112a6-146">CommonParameters</span></span>
<span data-ttu-id="112a6-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="112a6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112a6-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="112a6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112a6-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="112a6-149">INPUTS</span></span>

### <span data-ttu-id="112a6-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="112a6-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="112a6-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="112a6-151">OUTPUTS</span></span>

### <span data-ttu-id="112a6-152">Microsoft. Azure. Commands. SYNAPSE. modeller. Psroleatamaayrıntıları</span><span class="sxs-lookup"><span data-stu-id="112a6-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="112a6-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="112a6-153">NOTES</span></span>

## <span data-ttu-id="112a6-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="112a6-154">RELATED LINKS</span></span>
