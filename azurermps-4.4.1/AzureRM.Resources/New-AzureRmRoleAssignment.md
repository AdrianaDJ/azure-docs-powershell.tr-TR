---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: c3988727e8afd54dddea9719c348222c41f47503
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590665"
---
# <span data-ttu-id="f3958-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f3958-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="f3958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3958-102">SYNOPSIS</span></span>
<span data-ttu-id="f3958-103">Belirtilen RBAC rolü, belirtilen kapsamda belirtilen sorumluya atar.</span><span class="sxs-lookup"><span data-stu-id="f3958-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3958-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3958-104">SYNTAX</span></span>

### <span data-ttu-id="f3958-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3958-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-106">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="f3958-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-107">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="f3958-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-108">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="f3958-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-109">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="f3958-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 -RoleDefinitionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3958-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3958-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3958-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3958-116">DESCRIPTION</span></span>
<span data-ttu-id="f3958-117">Erişim vermek için New-AzureRMRoleAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3958-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="f3958-118">Erişim, doğru kapsamda uygun RBAC rolünü atayarak verilir.</span><span class="sxs-lookup"><span data-stu-id="f3958-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="f3958-119">Tüm aboneliğe erişim vermek için, abonelik kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="f3958-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="f3958-120">Bir abonelikteki belirli bir kaynak grubuna erişim izni vermek için, kaynak grubu kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="f3958-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>

<span data-ttu-id="f3958-121">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f3958-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="f3958-122">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3958-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="f3958-123">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3958-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="f3958-124">Bir Azure AD uygulaması belirtmek için, ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3958-124">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="f3958-125">Atanmış olan rolün, RoleDefinitionName parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3958-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="f3958-126">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f3958-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="f3958-127">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="f3958-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="f3958-128">Atamanın kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f3958-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="f3958-129">Kapsam-bu,/Subscriptions/b ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="f3958-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="f3958-130">ResourceGroupName-belirtilen kaynak grubuna erişim izni vermek için.</span><span class="sxs-lookup"><span data-stu-id="f3958-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="f3958-131">d.</span><span class="sxs-lookup"><span data-stu-id="f3958-131">c.</span></span>
<span data-ttu-id="f3958-132">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-erişim izni verecek belirli bir kaynağı belirtmek için.</span><span class="sxs-lookup"><span data-stu-id="f3958-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="f3958-133">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3958-133">EXAMPLES</span></span>

### <span data-ttu-id="f3958-134">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3958-134">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader
```

<span data-ttu-id="f3958-135">Kaynak grubu kapsamındaki bir kullanıcıya okuyucu rolü erişimi verme</span><span class="sxs-lookup"><span data-stu-id="f3958-135">Grant Reader role access to a user at a resource group scope</span></span>

### <span data-ttu-id="f3958-136">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3958-136">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           ObjectId
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="f3958-137">Güvenlik grubuna erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="f3958-137">Grant access to a security group</span></span>

### <span data-ttu-id="f3958-138">--------------------------Örnek 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3958-138">--------------------------  Example 3  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="f3958-139">Bir kaynaktaki (Web sitesi) bir kullanıcıya erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="f3958-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="f3958-140">--------------------------Örnek 4--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3958-140">--------------------------  Example 4  --------------------------</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="f3958-141">İç içe bir kaynaktaki (alt ağ) gruba erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="f3958-141">Grant access to a group at a nested resource (subnet)</span></span>

## <span data-ttu-id="f3958-142">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3958-142">PARAMETERS</span></span>

### <span data-ttu-id="f3958-143">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f3958-143">-ObjectId</span></span>
<span data-ttu-id="f3958-144">Kullanıcı, Grup veya hizmet sorumlusunun Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="f3958-144">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-145">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="f3958-145">-ParentResource</span></span>
<span data-ttu-id="f3958-146">Hiyerarşide üst kaynak (ResourceName parametresi kullanılarak belirtilen kaynak).</span><span class="sxs-lookup"><span data-stu-id="f3958-146">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="f3958-147">Yalnızca kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturmak için ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f3958-147">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f3958-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3958-148">-ResourceGroupName</span></span>
<span data-ttu-id="f3958-149">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f3958-149">The resource group name.</span></span>
<span data-ttu-id="f3958-150">Belirtilen kaynak grubunda geçerli olan bir ödev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3958-150">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="f3958-151">ResourceName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanıldığında, komut, kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3958-151">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-152">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3958-152">-ResourceName</span></span>
<span data-ttu-id="f3958-153">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f3958-153">The resource name.</span></span>
<span data-ttu-id="f3958-154">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="f3958-154">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="f3958-155">Yalnızca ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır, bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3958-155">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f3958-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3958-156">-ResourceType</span></span>
<span data-ttu-id="f3958-157">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="f3958-157">The resource type.</span></span>
<span data-ttu-id="f3958-158">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="f3958-158">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="f3958-159">Yalnızca ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır ve bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3958-159">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="f3958-160">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="f3958-160">-RoleDefinitionId</span></span>
<span data-ttu-id="f3958-161">Sorumluya atanması gereken RBAC rolünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="f3958-161">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="f3958-162">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f3958-162">-RoleDefinitionName</span></span>
<span data-ttu-id="f3958-163">Sorumluya atanması gereken RBAC rolünün adı (Reader, katkıda bulunanlar, sanal ağ yöneticisi vb.).</span><span class="sxs-lookup"><span data-stu-id="f3958-163">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-164">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f3958-164">-Scope</span></span>
<span data-ttu-id="f3958-165">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="f3958-165">The Scope of the role assignment.</span></span>
<span data-ttu-id="f3958-166">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="f3958-166">In the format of relative URI.</span></span>
<span data-ttu-id="f3958-167">Örneğin, "/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg".</span><span class="sxs-lookup"><span data-stu-id="f3958-167">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="f3958-168">Belirtilmezse, abone düzeyinde rol ataması oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f3958-168">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="f3958-169">Belirtilmişse "/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f3958-169">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-170">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f3958-170">-ServicePrincipalName</span></span>
<span data-ttu-id="f3958-171">Azure AD uygulaması 'nın ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f3958-171">The ServicePrincipalName of the Azure AD application</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-172">-Signınname</span><span class="sxs-lookup"><span data-stu-id="f3958-172">-SignInName</span></span>
<span data-ttu-id="f3958-173">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="f3958-173">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3958-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3958-174">-DefaultProfile</span></span>
<span data-ttu-id="f3958-175">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3958-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3958-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3958-176">CommonParameters</span></span>
<span data-ttu-id="f3958-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3958-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3958-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3958-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3958-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3958-179">INPUTS</span></span>

## <span data-ttu-id="f3958-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3958-180">OUTPUTS</span></span>

### <span data-ttu-id="f3958-181">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="f3958-181">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f3958-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3958-182">NOTES</span></span>
<span data-ttu-id="f3958-183">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="f3958-183">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f3958-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3958-184">RELATED LINKS</span></span>

[<span data-ttu-id="f3958-185">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="f3958-185">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="f3958-186">Remove-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="f3958-186">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="f3958-187">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f3958-187">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

