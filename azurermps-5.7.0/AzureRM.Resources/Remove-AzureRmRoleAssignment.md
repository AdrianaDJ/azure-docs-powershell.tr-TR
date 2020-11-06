---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleAssignment.md
ms.openlocfilehash: 4ca9b3d731c4b4c0029dafa68a1f7e747c62dedb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593438"
---
# <span data-ttu-id="c3184-101">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c3184-101">Remove-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="c3184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3184-102">SYNOPSIS</span></span>
<span data-ttu-id="c3184-103">Belirli bir kapsamda belirli bir role atanmış olan belirtilen sorumluya rol atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3184-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3184-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3184-104">SYNTAX</span></span>

### <span data-ttu-id="c3184-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3184-105">EmptyParameterSet (Default)</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-106">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c3184-106">ResourceWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-107">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c3184-107">ResourceGroupWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-108">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c3184-108">ScopeWithObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-109">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c3184-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-110">ResourceWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-111">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-111">ResourceGroupWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-112">ScopeWithSignInNameParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-113">ResourceWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-114">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-114">ResourceGroupWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3184-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3184-115">ScopeWithSPNParameterSet</span></span>
```
Remove-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3184-116">Roleatamaparametresi kümesi</span><span class="sxs-lookup"><span data-stu-id="c3184-116">RoleAssignmentParameterSet</span></span>
```
Remove-AzureRmRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3184-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3184-117">DESCRIPTION</span></span>
<span data-ttu-id="c3184-118">Verilen kapsamda ve verilen rolde tüm sorumluya erişimi iptal etmek Remove-AzureRmRoleAssignment Command'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3184-118">Use the Remove-AzureRmRoleAssignment commandlet to revoke access to any principal at given scope and given role.</span></span>

<span data-ttu-id="c3184-119">Atamanın (anapara gibi) belirtilmesi gerekır.</span><span class="sxs-lookup"><span data-stu-id="c3184-119">The object of the assignment i.e. the principal MUST be specified.</span></span>
<span data-ttu-id="c3184-120">Patron bir Kullanıcı (bir kullanıcıyı tanımlayan Signınname veya ObjectID parametrelerini kullanın), güvenlik grubu (bir grubu belirlemek için ObjectID parametresini kullanma) veya hizmet sorumlusu olabilir (bir ServicePrincipal 'ı belirlemek için ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3184-120">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ServicePrincipalName or ObjectId parameters to identify a ServicePrincipal.</span></span>

<span data-ttu-id="c3184-121">Anaparanın atandığı rol, RoleDefinitionName parametresi kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c3184-121">The role that the principal is assigned to MUST be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="c3184-122">Atamanın kapsamı belirtilebilir ve belirtilmemişse, abonelik kapsamının varsayılan değeri, abonelik kapsamında belirtilen anapara ve role atamayı silmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="c3184-122">The scope of the assignment MAY be specified and if not specified, defaults to the subscription scope i.e. it will try to delete an assignment to the specified principal and role at the subscription scope.</span></span>
<span data-ttu-id="c3184-123">Atamanın kapsamı aşağıdaki parametrelerden biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c3184-123">The scope of the assignment can be specified using one of the following parameters.</span></span>
<span data-ttu-id="c3184-124">bir.</span><span class="sxs-lookup"><span data-stu-id="c3184-124">a.</span></span>
<span data-ttu-id="c3184-125">Kapsam-bu,/Subscriptions/b ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="c3184-125">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="c3184-126">ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3184-126">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="c3184-127">d.</span><span class="sxs-lookup"><span data-stu-id="c3184-127">c.</span></span>
<span data-ttu-id="c3184-128">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c3184-128">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription.</span></span>

## <span data-ttu-id="c3184-129">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3184-129">EXAMPLES</span></span>

### <span data-ttu-id="c3184-130">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c3184-130">Example 1</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

<span data-ttu-id="c3184-131">john.doe@contoso.comRG1 resourcegroup kapsamındaki okuyucu rolüne atanmış olan rol atamalarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3184-131">Removes a role assignment for john.doe@contoso.com who is assigned to the Reader role at the rg1 resourcegroup scope.</span></span>

### <span data-ttu-id="c3184-132">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c3184-132">Example 2</span></span>
```
PS C:\> Remove-AzureRmRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

<span data-ttu-id="c3184-133">Rol atamasını ObjectID tarafından tanımlanan gruba ve okuyucu rolüne atanır.</span><span class="sxs-lookup"><span data-stu-id="c3184-133">Removes the role assignment to the group principal identified by the ObjectId and assigned to the Reader role.</span></span>
<span data-ttu-id="c3184-134">Silinecek atamayı bulmak için geçerli aboneliği kapsam olarak kullanma.</span><span class="sxs-lookup"><span data-stu-id="c3184-134">Defaults to using the current subscription as the scope to find the assignment to be deleted.</span></span>

### <span data-ttu-id="c3184-135">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c3184-135">Example 3</span></span>
```
PS C:\> $roleassignment = Get-AzureRmRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzureRmRoleAssignment -InputObject $roleassignment
```

<span data-ttu-id="c3184-136">Get-AzureRmRoleAssignment komutkonumundan getirilen ilk rol atama nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3184-136">Removes the first role assignment object which is fetched from the Get-AzureRmRoleAssignment commandlet.</span></span>

## <span data-ttu-id="c3184-137">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3184-137">PARAMETERS</span></span>

### <span data-ttu-id="c3184-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3184-138">-DefaultProfile</span></span>
<span data-ttu-id="c3184-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3184-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3184-140">-InputObject</span></span>
<span data-ttu-id="c3184-141">Rol atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c3184-141">Role Assignment object.</span></span>

```yaml
Type: PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-142">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c3184-142">-ObjectId</span></span>
<span data-ttu-id="c3184-143">Kullanıcı, Grup veya hizmet sorumlusunun Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="c3184-143">Azure AD ObjectId of the user, group or service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-144">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="c3184-144">-ParentResource</span></span>
<span data-ttu-id="c3184-145">Varsa hiyerarşideki üst kaynak (ResourceName parametresi kullanılarak belirtilen kaynak).</span><span class="sxs-lookup"><span data-stu-id="c3184-145">The parent resource in the hierarchy(of the resource specified using ResourceName parameter), if any.</span></span>
<span data-ttu-id="c3184-146">Kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturmak için ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3184-146">Must be used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-147">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c3184-147">-PassThru</span></span>
<span data-ttu-id="c3184-148">Belirtilmişse, silinmiş rol atamasını görüntüler</span><span class="sxs-lookup"><span data-stu-id="c3184-148">If specified, displays the deleted role assignment</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3184-149">-ResourceGroupName</span></span>
<span data-ttu-id="c3184-150">Rolün atandığı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c3184-150">The resource group name that the role is assigned to.</span></span>
<span data-ttu-id="c3184-151">Belirtilen kaynak grubu kapsamındaki bir atamayı silmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="c3184-151">Attempts to delete an assignment at the specified resource group scope.</span></span>
<span data-ttu-id="c3184-152">ResourceName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanıldığında, komut, kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3184-152">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c3184-153">-ResourceName</span></span>
<span data-ttu-id="c3184-154">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c3184-154">The resource name.</span></span>
<span data-ttu-id="c3184-155">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="c3184-155">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="c3184-156">ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanarak, kaynağı tanımlayan ve bu kapsamda bir atamayı silebileceğini göreli bir URI biçiminde hiyerarşik bir kapsam oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3184-156">Must be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters, to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c3184-157">-ResourceType</span></span>
<span data-ttu-id="c3184-158">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="c3184-158">The resource type.</span></span>
<span data-ttu-id="c3184-159">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="c3184-159">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="c3184-160">ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte, kaynağı tanımlayan ve söz konusu kaynak kapsamından bir atamayı tanımlayan göreli bir URI biçiminde bir hiyerarşik kapsam oluşturmak için kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3184-160">Must be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a relative URI that identifies the resource and delete an assignment at that resource scope.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-161">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="c3184-161">-RoleDefinitionId</span></span>
<span data-ttu-id="c3184-162">Atamanın silinmesi gereken RBAC rolünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="c3184-162">Id of the RBAC role for which the assignment needs to be deleted.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-163">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c3184-163">-RoleDefinitionName</span></span>
<span data-ttu-id="c3184-164">Atamanın silinmesi gereken RBAC rolünün adı; örneğin, okuyucu, katılımcı, sanal ağ yöneticisi vb.</span><span class="sxs-lookup"><span data-stu-id="c3184-164">Name of the RBAC role for which the assignment needs to be deleted i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-165">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c3184-165">-Scope</span></span>
<span data-ttu-id="c3184-166">Silinecek rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="c3184-166">The Scope of the role assignment to be deleted.</span></span>
<span data-ttu-id="c3184-167">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="c3184-167">In the format of relative URI.</span></span>
<span data-ttu-id="c3184-168">Örneğin, "/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg".</span><span class="sxs-lookup"><span data-stu-id="c3184-168">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="c3184-169">Belirtilmemişse, aboneliği abonelik düzeyinde silmeye çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="c3184-169">If not specified, will attempt to delete the role at subscription level.</span></span>
<span data-ttu-id="c3184-170">Belirtilmişse "/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3184-170">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-171">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c3184-171">-ServicePrincipalName</span></span>
<span data-ttu-id="c3184-172">Azure AD uygulaması 'nın ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c3184-172">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-173">-Signınname</span><span class="sxs-lookup"><span data-stu-id="c3184-173">-SignInName</span></span>
<span data-ttu-id="c3184-174">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="c3184-174">The email address or the user principal name of the user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3184-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3184-175">-Confirm</span></span>
<span data-ttu-id="c3184-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3184-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3184-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3184-177">-WhatIf</span></span>
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

### <span data-ttu-id="c3184-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3184-178">CommonParameters</span></span>
<span data-ttu-id="c3184-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3184-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3184-180">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3184-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3184-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3184-181">INPUTS</span></span>

### <span data-ttu-id="c3184-182">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c3184-182">None</span></span>
<span data-ttu-id="c3184-183">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c3184-183">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3184-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3184-184">OUTPUTS</span></span>

### <span data-ttu-id="c3184-185">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev]</span><span class="sxs-lookup"><span data-stu-id="c3184-185">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="c3184-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3184-186">NOTES</span></span>
<span data-ttu-id="c3184-187">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="c3184-187">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c3184-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3184-188">RELATED LINKS</span></span>

[<span data-ttu-id="c3184-189">Yeni-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="c3184-189">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="c3184-190">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="c3184-190">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="c3184-191">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c3184-191">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

