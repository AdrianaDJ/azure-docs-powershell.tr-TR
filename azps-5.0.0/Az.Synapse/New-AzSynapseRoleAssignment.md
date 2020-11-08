---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276317"
---
# <span data-ttu-id="98979-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="98979-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="98979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98979-102">SYNOPSIS</span></span>
<span data-ttu-id="98979-103">SYNAPSE Analytics rol ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98979-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="98979-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98979-104">SYNTAX</span></span>

### <span data-ttu-id="98979-105">NewByWorkspaceNameAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98979-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98979-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98979-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98979-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98979-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98979-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="98979-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98979-109">Newbyworkspace Objectandnameparameterset</span><span class="sxs-lookup"><span data-stu-id="98979-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98979-110">Newbyçalışmakonumunda Nesnetandidparameterset</span><span class="sxs-lookup"><span data-stu-id="98979-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98979-111">Newbyıo Nesnetandroledefinitionıdandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="98979-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98979-112">Newbyworkspace Objectandserviceprincipalnameparameterset</span><span class="sxs-lookup"><span data-stu-id="98979-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98979-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="98979-113">DESCRIPTION</span></span>
<span data-ttu-id="98979-114">**New-AzSynapseRoleAssignment** cmdlet 'ı bir Azure SYNAPSE Analytics rol ataması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98979-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="98979-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98979-115">EXAMPLES</span></span>

### <span data-ttu-id="98979-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98979-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="98979-117">Bu komut, sorumlu adı ContosoName olan kullanıcıya ContosoRole atar.</span><span class="sxs-lookup"><span data-stu-id="98979-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="98979-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98979-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="98979-119">Bu komut, asıl adı ContosoName ile ardışık düzen olan kullanıcıya ContosoRole atar.</span><span class="sxs-lookup"><span data-stu-id="98979-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="98979-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98979-120">PARAMETERS</span></span>

### <span data-ttu-id="98979-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="98979-121">-AsJob</span></span>
<span data-ttu-id="98979-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="98979-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98979-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98979-123">-DefaultProfile</span></span>
<span data-ttu-id="98979-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98979-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98979-125">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="98979-125">-ObjectId</span></span>
<span data-ttu-id="98979-126">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="98979-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-127">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="98979-127">-RoleDefinitionId</span></span>
<span data-ttu-id="98979-128">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="98979-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="98979-129">-RoleDefinitionName</span></span>
<span data-ttu-id="98979-130">Sorumluya atanmış rolün adı.</span><span class="sxs-lookup"><span data-stu-id="98979-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="98979-131">-ServicePrincipalName</span></span>
<span data-ttu-id="98979-132">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="98979-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-133">-Signınname</span><span class="sxs-lookup"><span data-stu-id="98979-133">-SignInName</span></span>
<span data-ttu-id="98979-134">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="98979-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-135">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="98979-135">-WorkspaceName</span></span>
<span data-ttu-id="98979-136">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="98979-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98979-137">-</span><span class="sxs-lookup"><span data-stu-id="98979-137">-WorkspaceObject</span></span>
<span data-ttu-id="98979-138">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="98979-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98979-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="98979-139">-Confirm</span></span>
<span data-ttu-id="98979-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98979-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98979-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98979-141">-WhatIf</span></span>
<span data-ttu-id="98979-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98979-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98979-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98979-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98979-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98979-144">CommonParameters</span></span>
<span data-ttu-id="98979-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98979-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98979-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="98979-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98979-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98979-147">INPUTS</span></span>

### <span data-ttu-id="98979-148">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="98979-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98979-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98979-149">OUTPUTS</span></span>

### <span data-ttu-id="98979-150">Microsoft. Azure. Commands. SYNAPSE. modeller. Psroleatamaayrıntıları</span><span class="sxs-lookup"><span data-stu-id="98979-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="98979-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98979-151">NOTES</span></span>

## <span data-ttu-id="98979-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98979-152">RELATED LINKS</span></span>
