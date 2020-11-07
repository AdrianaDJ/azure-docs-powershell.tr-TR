---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 39fa584428d711a65d3f11f39508b7e7f0220c9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763324"
---
# <span data-ttu-id="69de3-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="69de3-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="69de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69de3-102">SYNOPSIS</span></span>
<span data-ttu-id="69de3-103">Belirli bir kapsamda belirli bir role atanmış olan belirtilen sorumluya rol atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69de3-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69de3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69de3-104">SYNTAX</span></span>

### <span data-ttu-id="69de3-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69de3-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-106">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="69de3-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-107">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="69de3-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-108">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="69de3-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-109">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="69de3-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69de3-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="69de3-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69de3-116">Roleatamaparametresi kümesi</span><span class="sxs-lookup"><span data-stu-id="69de3-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69de3-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="69de3-117">DESCRIPTION</span></span>
<span data-ttu-id="69de3-118">Verilen kapsamda ve verilen rolde tüm sorumluya erişimi iptal etmek Remove-AzureRmRoleAssignment Command'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="69de3-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>

<span data-ttu-id="69de3-119">Atamanın (anapara gibi) belirtilmesi gerekır.</span><span class="sxs-lookup"><span data-stu-id="69de3-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="69de3-120">Patron bir Kullanıcı (bir kullanıcıyı tanımlayan Signınname veya ObjectID parametrelerini kullanın), güvenlik grubu (bir grubu belirlemek için ObjectID parametresini kullanma) veya hizmet sorumlusu olabilir (bir ServicePrincipal 'ı belirlemek için ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="69de3-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>

<span data-ttu-id="69de3-121">Anaparanın atandığı rol, RoleDefinitionName parametresi kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="69de3-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="69de3-122">Atamanın kapsamı belirtilebilir ve belirtilmemişse, abonelik kapsamının varsayılan değeri, abonelik kapsamında belirtilen anapara ve role atamayı silmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="69de3-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="69de3-123">Atamanın kapsamı aşağıdaki parametrelerden biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="69de3-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="69de3-124">bir.</span><span class="sxs-lookup"><span data-stu-id="69de3-124">a.</span></span>
<span data-ttu-id="69de3-125">Kapsam-bu,/Subscriptions/b ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="69de3-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="69de3-126">ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69de3-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="69de3-127">d.</span><span class="sxs-lookup"><span data-stu-id="69de3-127">c.</span></span>
<span data-ttu-id="69de3-128">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="69de3-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="69de3-129">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69de3-129">EXAMPLES</span></span>

### <span data-ttu-id="69de3-130">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69de3-130">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="69de3-131">john.doe@contoso.comRG1 resourcegroup kapsamındaki okuyucu rolüne atanmış olan rol atamalarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69de3-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="69de3-132">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="69de3-132">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="69de3-133">Rol atamasını ObjectID tarafından tanımlanan gruba ve okuyucu rolüne atanır.</span><span class="sxs-lookup"><span data-stu-id="69de3-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="69de3-134">Silinecek atamayı bulmak için geçerli aboneliği kapsam olarak kullanma.</span><span class="sxs-lookup"><span data-stu-id="69de3-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="69de3-135">--------------------------Örnek 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="69de3-135">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="69de3-136">Get-AzureRmRoleAssignment komutkonumundan getirilen ilk rol atama nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69de3-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="69de3-137">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69de3-137">PARAMETERS</span></span>

### <span data-ttu-id="69de3-138">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="69de3-138">-ObjectId</span></span>
<span data-ttu-id="69de3-139">Kullanıcı, Grup veya hizmet sorumlusunun Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="69de3-139">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-140">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="69de3-140">-ParentResource</span></span>
<span data-ttu-id="69de3-141">Varsa hiyerarşideki üst kaynak (ResourceName parametresi kullanılarak belirtilen kaynak).</span><span class="sxs-lookup"><span data-stu-id="69de3-141">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="69de3-142">Kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturmak için ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="69de3-142">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="69de3-143">-PassThru</span></span>
<span data-ttu-id="69de3-144">Belirtilmişse, silinmiş rol atamasını görüntüler</span><span class="sxs-lookup"><span data-stu-id="69de3-144">If specified, displays the deleted role assignment</span></span>

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

### <span data-ttu-id="69de3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69de3-145">-ResourceGroupName</span></span>
<span data-ttu-id="69de3-146">Rolün atandığı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="69de3-146">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="69de3-147">Belirtilen kaynak grubu kapsamındaki bir atamayı silmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="69de3-147">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="69de3-148">ResourceName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanıldığında, komut, kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69de3-148">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="69de3-149">-ResourceName</span></span>
<span data-ttu-id="69de3-150">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="69de3-150">The resource name.</span></span>
<span data-ttu-id="69de3-151">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="69de3-151">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="69de3-152">ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanarak, kaynağı tanımlayan ve bu kapsamda bir atamayı silebileceğini göreli bir URI biçiminde hiyerarşik bir kapsam oluşturun.</span><span class="sxs-lookup"><span data-stu-id="69de3-152">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-153">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="69de3-153">-ResourceType</span></span>
<span data-ttu-id="69de3-154">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="69de3-154">The resource type.</span></span>
<span data-ttu-id="69de3-155">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="69de3-155">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="69de3-156">ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte, kaynağı tanımlayan ve söz konusu kaynak kapsamından bir atamayı tanımlayan göreli bir URI biçiminde bir hiyerarşik kapsam oluşturmak için kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="69de3-156">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-157">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="69de3-157">-RoleDefinitionId</span></span>
<span data-ttu-id="69de3-158">Atamanın silinmesi gereken RBAC rolünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="69de3-158">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-159">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="69de3-159">-RoleDefinitionName</span></span>
<span data-ttu-id="69de3-160">Atamanın silinmesi gereken RBAC rolünün adı; örneğin, okuyucu, katılımcı, sanal ağ yöneticisi vb.</span><span class="sxs-lookup"><span data-stu-id="69de3-160">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-161">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="69de3-161">-Scope</span></span>
<span data-ttu-id="69de3-162">Silinecek rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="69de3-162">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="69de3-163">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="69de3-163">In the format of relative URI.</span></span>
<span data-ttu-id="69de3-164">Örneğin, "/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg".</span><span class="sxs-lookup"><span data-stu-id="69de3-164">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="69de3-165">Belirtilmemişse, aboneliği abonelik düzeyinde silmeye çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="69de3-165">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="69de3-166">Belirtilmişse "/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="69de3-166">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-167">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="69de3-167">-ServicePrincipalName</span></span>
<span data-ttu-id="69de3-168">Azure AD uygulaması 'nın ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="69de3-168">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-169">-Signınname</span><span class="sxs-lookup"><span data-stu-id="69de3-169">-SignInName</span></span>
<span data-ttu-id="69de3-170">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="69de3-170">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-171">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69de3-171">-InputObject</span></span>
<span data-ttu-id="69de3-172">Rol atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="69de3-172">Role Assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-173">-Onay</span><span class="sxs-lookup"><span data-stu-id="69de3-173">-Confirm</span></span>
<span data-ttu-id="69de3-174">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69de3-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69de3-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69de3-175">-WhatIf</span></span>
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

### <span data-ttu-id="69de3-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69de3-176">-DefaultProfile</span></span>
<span data-ttu-id="69de3-177">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69de3-177">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69de3-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69de3-178">CommonParameters</span></span>
<span data-ttu-id="69de3-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69de3-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69de3-180">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69de3-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69de3-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69de3-181">INPUTS</span></span>

## <span data-ttu-id="69de3-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69de3-182">OUTPUTS</span></span>

### <span data-ttu-id="69de3-183">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev]</span><span class="sxs-lookup"><span data-stu-id="69de3-183">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="69de3-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69de3-184">NOTES</span></span>
<span data-ttu-id="69de3-185">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="69de3-185">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="69de3-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69de3-186">RELATED LINKS</span></span>

[<span data-ttu-id="69de3-187">Yeni-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="69de3-187">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="69de3-188">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="69de3-188">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="69de3-189">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="69de3-189">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
