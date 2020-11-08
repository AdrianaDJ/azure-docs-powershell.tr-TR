---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107481"
---
# <span data-ttu-id="5ade1-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5ade1-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="5ade1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ade1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ade1-103">SYNAPSE Analytics rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="5ade1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ade1-104">SYNTAX</span></span>

### <span data-ttu-id="5ade1-105">GetByWorkspaceNameAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ade1-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ade1-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ade1-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ade1-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ade1-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-110">Getbyıo Nesnetandnameparameterset</span><span class="sxs-lookup"><span data-stu-id="5ade1-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-111">Getbyıo Nesnetandidparameterset</span><span class="sxs-lookup"><span data-stu-id="5ade1-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-112">Getbyıo Nesnetandroledefinitionıdandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="5ade1-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-113">Getbyçalışmanesnetandassignmentivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="5ade1-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ade1-114">Getbyı</span><span class="sxs-lookup"><span data-stu-id="5ade1-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ade1-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ade1-115">DESCRIPTION</span></span>
<span data-ttu-id="5ade1-116">**Get-AzSynapseRoleAssignment** cmdlet 'ı bir Azure SYNAPSE Analytics rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="5ade1-117">Bir rol tanımı veya Kullanıcı asıl adı belirtmezseniz, bu cmdlet tüm rol atamasını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="5ade1-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ade1-118">EXAMPLES</span></span>

### <span data-ttu-id="5ade1-119">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ade1-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5ade1-120">Bu komut, çalışma alanı altındaki tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="5ade1-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5ade1-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="5ade1-122">Bu komut, ContosoRole rol adı ile çalışma alanı Contoso'in altındaki tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="5ade1-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="5ade1-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="5ade1-124">Bu komut, ContosoRole rol adı ile çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="5ade1-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="5ade1-125">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="5ade1-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="5ade1-126">Bu komut, ardışık düzen aracılığıyla tüm rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ade1-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="5ade1-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ade1-127">PARAMETERS</span></span>

### <span data-ttu-id="5ade1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ade1-128">-DefaultProfile</span></span>
<span data-ttu-id="5ade1-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ade1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ade1-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="5ade1-130">-ObjectId</span></span>
<span data-ttu-id="5ade1-131">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="5ade1-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="5ade1-132">-Roleatamakimliği</span><span class="sxs-lookup"><span data-stu-id="5ade1-132">-RoleAssignmentId</span></span>
<span data-ttu-id="5ade1-133">Rol atamasının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5ade1-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="5ade1-134">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="5ade1-134">-RoleDefinitionId</span></span>
<span data-ttu-id="5ade1-135">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="5ade1-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="5ade1-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="5ade1-136">-RoleDefinitionName</span></span>
<span data-ttu-id="5ade1-137">Sorumluya atanmış rolün adı.</span><span class="sxs-lookup"><span data-stu-id="5ade1-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="5ade1-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5ade1-138">-ServicePrincipalName</span></span>
<span data-ttu-id="5ade1-139">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="5ade1-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="5ade1-140">-Signınname</span><span class="sxs-lookup"><span data-stu-id="5ade1-140">-SignInName</span></span>
<span data-ttu-id="5ade1-141">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="5ade1-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="5ade1-142">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5ade1-142">-WorkspaceName</span></span>
<span data-ttu-id="5ade1-143">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="5ade1-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5ade1-144">-</span><span class="sxs-lookup"><span data-stu-id="5ade1-144">-WorkspaceObject</span></span>
<span data-ttu-id="5ade1-145">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5ade1-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ade1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ade1-146">CommonParameters</span></span>
<span data-ttu-id="5ade1-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ade1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ade1-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ade1-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ade1-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ade1-149">INPUTS</span></span>

### <span data-ttu-id="5ade1-150">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ade1-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5ade1-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ade1-151">OUTPUTS</span></span>

### <span data-ttu-id="5ade1-152">Microsoft. Azure. Commands. SYNAPSE. modeller. Psroleatamaayrıntıları</span><span class="sxs-lookup"><span data-stu-id="5ade1-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="5ade1-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ade1-153">NOTES</span></span>

## <span data-ttu-id="5ade1-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ade1-154">RELATED LINKS</span></span>
