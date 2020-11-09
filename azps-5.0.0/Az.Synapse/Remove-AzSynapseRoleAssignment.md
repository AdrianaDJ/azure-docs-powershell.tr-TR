---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326125"
---
# <span data-ttu-id="9f3c6-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9f3c6-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="9f3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3c6-103">SYNAPSE Analytics rol atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="9f3c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f3c6-104">SYNTAX</span></span>

### <span data-ttu-id="9f3c6-105">RemoveByWorkspaceNameAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f3c6-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3c6-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3c6-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3c6-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f3c6-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-110">Removebyçalışmakonumunda Nesnetandidparameterset</span><span class="sxs-lookup"><span data-stu-id="9f3c6-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-111">Removebyworkspace Objectandnameparameterset</span><span class="sxs-lookup"><span data-stu-id="9f3c6-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-112">Removebyçalışmakonumunda Nesnetandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="9f3c6-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-113">Removebyıç</span><span class="sxs-lookup"><span data-stu-id="9f3c6-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f3c6-114">Removebyçalışmakonumunda Objectandserviceprincipalnameparameterset</span><span class="sxs-lookup"><span data-stu-id="9f3c6-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f3c6-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f3c6-115">DESCRIPTION</span></span>
<span data-ttu-id="9f3c6-116">**Remove-AzSynapseRoleAssignment** cmdlet 'ı bir Azure SYNAPSE Analytics rol atamasını kalıcı olarak siler.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="9f3c6-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f3c6-117">EXAMPLES</span></span>

### <span data-ttu-id="9f3c6-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f3c6-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="9f3c6-119">Bu komut, rol atama kimliği olan bir Azure SYNAPSE Analytics rol atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="9f3c6-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9f3c6-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="9f3c6-121">Bu komut bir rol adı ve Kullanıcı asıl adı içeren bir Azure SYNAPSE Analytics rol atamasını siler.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="9f3c6-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9f3c6-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="9f3c6-123">Bu komut, bir Azure SYNAPSE Analytics rol atamasını ardışık düzen aracılığıyla rol atama kimliğiyle siler.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="9f3c6-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f3c6-124">PARAMETERS</span></span>

### <span data-ttu-id="9f3c6-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="9f3c6-125">-AsJob</span></span>
<span data-ttu-id="9f3c6-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9f3c6-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f3c6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3c6-127">-DefaultProfile</span></span>
<span data-ttu-id="9f3c6-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f3c6-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="9f3c6-129">-ObjectId</span></span>
<span data-ttu-id="9f3c6-130">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9f3c6-131">-PassThru</span></span>
<span data-ttu-id="9f3c6-132">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9f3c6-133">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9f3c6-134">-Roleatamakimliği</span><span class="sxs-lookup"><span data-stu-id="9f3c6-134">-RoleAssignmentId</span></span>
<span data-ttu-id="9f3c6-135">Rol atamasının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-136">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="9f3c6-136">-RoleDefinitionId</span></span>
<span data-ttu-id="9f3c6-137">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9f3c6-138">-RoleDefinitionName</span></span>
<span data-ttu-id="9f3c6-139">Sorumluya atanmış rolün adı.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9f3c6-140">-ServicePrincipalName</span></span>
<span data-ttu-id="9f3c6-141">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-142">-Signınname</span><span class="sxs-lookup"><span data-stu-id="9f3c6-142">-SignInName</span></span>
<span data-ttu-id="9f3c6-143">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-144">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="9f3c6-144">-WorkspaceName</span></span>
<span data-ttu-id="9f3c6-145">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-146">-</span><span class="sxs-lookup"><span data-stu-id="9f3c6-146">-WorkspaceObject</span></span>
<span data-ttu-id="9f3c6-147">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f3c6-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f3c6-148">-Confirm</span></span>
<span data-ttu-id="9f3c6-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f3c6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f3c6-150">-WhatIf</span></span>
<span data-ttu-id="9f3c6-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f3c6-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f3c6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3c6-153">CommonParameters</span></span>
<span data-ttu-id="9f3c6-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3c6-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9f3c6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3c6-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f3c6-156">INPUTS</span></span>

### <span data-ttu-id="9f3c6-157">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f3c6-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9f3c6-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f3c6-158">OUTPUTS</span></span>

### <span data-ttu-id="9f3c6-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f3c6-159">System.Boolean</span></span>

## <span data-ttu-id="9f3c6-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f3c6-160">NOTES</span></span>

## <span data-ttu-id="9f3c6-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f3c6-161">RELATED LINKS</span></span>
