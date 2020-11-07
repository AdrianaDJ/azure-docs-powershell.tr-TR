---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleAssignment.md
ms.openlocfilehash: d1fe464078c41d07f0d40024c06c4d5f88358470
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932561"
---
# <span data-ttu-id="44b19-101">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="44b19-101">New-AzRoleAssignment</span></span>

## <span data-ttu-id="44b19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b19-102">SYNOPSIS</span></span>
<span data-ttu-id="44b19-103">Belirtilen RBAC rolü, belirtilen kapsamda belirtilen sorumluya atar.</span><span class="sxs-lookup"><span data-stu-id="44b19-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="44b19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44b19-104">SYNTAX</span></span>

### <span data-ttu-id="44b19-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44b19-105">EmptyParameterSet (Default)</span></span>
```
New-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-106">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="44b19-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-107">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="44b19-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-108">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="44b19-108">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzRoleAssignment -ObjectId <String> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-109">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-109">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-110">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-110">ResourceWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-111">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-111">ScopeWithSignInNameParameterSet</span></span>
```
New-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-112">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-112">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-113">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-113">ResourceWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44b19-114">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b19-114">ScopeWithSPNParameterSet</span></span>
```
New-AzRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44b19-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="44b19-115">DESCRIPTION</span></span>
<span data-ttu-id="44b19-116">Erişim vermek için New-AzRoleAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="44b19-116">Use the New-AzRoleAssignment command to grant access.</span></span>
<span data-ttu-id="44b19-117">Erişim, doğru kapsamda uygun RBAC rolünü atayarak verilir.</span><span class="sxs-lookup"><span data-stu-id="44b19-117">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="44b19-118">Tüm aboneliğe erişim vermek için, abonelik kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="44b19-118">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="44b19-119">Bir abonelikteki belirli bir kaynak grubuna erişim izni vermek için, kaynak grubu kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="44b19-119">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="44b19-120">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="44b19-120">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="44b19-121">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="44b19-121">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="44b19-122">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="44b19-122">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="44b19-123">Bir Azure AD uygulaması belirtmek için, ApplicationId veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="44b19-123">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="44b19-124">Atanmış olan rolün, RoleDefinitionName parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="44b19-124">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="44b19-125">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="44b19-125">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="44b19-126">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="44b19-126">It defaults to the selected subscription.</span></span> <span data-ttu-id="44b19-127">Atamanın kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="44b19-127">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="44b19-128">Kapsam-bu,/Subscriptions/SubscriptionID b ile başlayan tam nitelikli bir kapsamdır \< \> .</span><span class="sxs-lookup"><span data-stu-id="44b19-128">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="44b19-129">ResourceGroupName-belirtilen kaynak grubuna erişim izni vermek için.</span><span class="sxs-lookup"><span data-stu-id="44b19-129">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="44b19-130">d.</span><span class="sxs-lookup"><span data-stu-id="44b19-130">c.</span></span>
<span data-ttu-id="44b19-131">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-erişim izni verecek belirli bir kaynağı belirtmek için.</span><span class="sxs-lookup"><span data-stu-id="44b19-131">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="44b19-132">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44b19-132">EXAMPLES</span></span>

### <span data-ttu-id="44b19-133">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44b19-133">Example 1</span></span>
```
PS C:\> New-AzRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="44b19-134">Temsilci olarak kullanılabilir durumda olan bir kaynak grubu kapsamındaki bir kullanıcıya okuyucu rolü erişimi verme</span><span class="sxs-lookup"><span data-stu-id="44b19-134">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="44b19-135">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="44b19-135">Example 2</span></span>
```
PS C:\> Get-AzADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="44b19-136">Güvenlik grubuna erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="44b19-136">Grant access to a security group</span></span>

### <span data-ttu-id="44b19-137">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="44b19-137">Example 3</span></span>
```
PS C:\> New-AzRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="44b19-138">Bir kaynaktaki (Web sitesi) bir kullanıcıya erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="44b19-138">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="44b19-139">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="44b19-139">Example 4</span></span>
```
PS C:\> New-AzRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="44b19-140">İç içe bir kaynaktaki (alt ağ) gruba erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="44b19-140">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="44b19-141">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="44b19-141">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="44b19-142">Hizmet sorumlusuna okuyucu erişimi verme</span><span class="sxs-lookup"><span data-stu-id="44b19-142">Grant reader access to a service principal</span></span>

## <span data-ttu-id="44b19-143">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44b19-143">PARAMETERS</span></span>

### <span data-ttu-id="44b19-144">-Allowtemsilci</span><span class="sxs-lookup"><span data-stu-id="44b19-144">-AllowDelegation</span></span>
<span data-ttu-id="44b19-145">Rol ataması oluştururken temsilci bayrağı.</span><span class="sxs-lookup"><span data-stu-id="44b19-145">The delegation flag while creating a Role assignment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b19-146">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="44b19-146">-ApplicationId</span></span>
<span data-ttu-id="44b19-147">ServicePrincipal 'un uygulama KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="44b19-147">The Application ID of the ServicePrincipal</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b19-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b19-148">-DefaultProfile</span></span>
<span data-ttu-id="44b19-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="44b19-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44b19-150">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="44b19-150">-ObjectId</span></span>
<span data-ttu-id="44b19-151">Kullanıcı, Grup veya hizmet sorumlusunun Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="44b19-151">Azure AD Objectid of the user, group or service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b19-152">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="44b19-152">-ParentResource</span></span>
<span data-ttu-id="44b19-153">Hiyerarşide üst kaynak (ResourceName parametresi kullanılarak belirtilen kaynak).</span><span class="sxs-lookup"><span data-stu-id="44b19-153">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="44b19-154">Yalnızca kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturmak için ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="44b19-154">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="44b19-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b19-155">-ResourceGroupName</span></span>
<span data-ttu-id="44b19-156">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="44b19-156">The resource group name.</span></span>
<span data-ttu-id="44b19-157">Belirtilen kaynak grubunda geçerli olan bir ödev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b19-157">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="44b19-158">ResourceName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanıldığında, komut, kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b19-158">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="44b19-159">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44b19-159">-ResourceName</span></span>
<span data-ttu-id="44b19-160">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="44b19-160">The resource name.</span></span>
<span data-ttu-id="44b19-161">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="44b19-161">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="44b19-162">Yalnızca ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır, bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b19-162">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="44b19-163">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="44b19-163">-ResourceType</span></span>
<span data-ttu-id="44b19-164">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="44b19-164">The resource type.</span></span>
<span data-ttu-id="44b19-165">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="44b19-165">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="44b19-166">Yalnızca ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır ve bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44b19-166">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="44b19-167">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="44b19-167">-RoleDefinitionId</span></span>
<span data-ttu-id="44b19-168">Sorumluya atanması gereken RBAC rolünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="44b19-168">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="44b19-169">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="44b19-169">-RoleDefinitionName</span></span>
<span data-ttu-id="44b19-170">Sorumluya atanması gereken RBAC rolünün adı (Reader, katkıda bulunanlar, sanal ağ yöneticisi vb.).</span><span class="sxs-lookup"><span data-stu-id="44b19-170">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b19-171">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="44b19-171">-Scope</span></span>
<span data-ttu-id="44b19-172">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="44b19-172">The Scope of the role assignment.</span></span>
<span data-ttu-id="44b19-173">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="44b19-173">In the format of relative URI.</span></span>
<span data-ttu-id="44b19-174">Örneğin, "/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg".</span><span class="sxs-lookup"><span data-stu-id="44b19-174">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="44b19-175">Belirtilmezse, abone düzeyinde rol ataması oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="44b19-175">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="44b19-176">Belirtilmişse "/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="44b19-176">If specified, it should start with "/subscriptions/{id}".</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44b19-177">-Signınname</span><span class="sxs-lookup"><span data-stu-id="44b19-177">-SignInName</span></span>
<span data-ttu-id="44b19-178">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="44b19-178">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="44b19-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b19-179">CommonParameters</span></span>
<span data-ttu-id="44b19-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44b19-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b19-181">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="44b19-181">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b19-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44b19-182">INPUTS</span></span>

### <span data-ttu-id="44b19-183">System. String</span><span class="sxs-lookup"><span data-stu-id="44b19-183">System.String</span></span>

### <span data-ttu-id="44b19-184">System. Guid</span><span class="sxs-lookup"><span data-stu-id="44b19-184">System.Guid</span></span>

## <span data-ttu-id="44b19-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44b19-185">OUTPUTS</span></span>

### <span data-ttu-id="44b19-186">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="44b19-186">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="44b19-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44b19-187">NOTES</span></span>
<span data-ttu-id="44b19-188">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="44b19-188">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="44b19-189">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44b19-189">RELATED LINKS</span></span>

[<span data-ttu-id="44b19-190">Get-Azrol ataması</span><span class="sxs-lookup"><span data-stu-id="44b19-190">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="44b19-191">Remove-Azroleödev</span><span class="sxs-lookup"><span data-stu-id="44b19-191">Remove-AzRoleAssignment</span></span>](./Remove-AzRoleAssignment.md)

[<span data-ttu-id="44b19-192">Get-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="44b19-192">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)
