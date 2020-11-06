---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E460D108-2BF9-4F57-AF3D-13868DC73EA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleAssignment.md
ms.openlocfilehash: 130f2ff4c65f282ca03f775500400479d16cc79c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588378"
---
# <span data-ttu-id="3ff1b-101">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3ff1b-101">New-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="3ff1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff1b-103">Belirtilen RBAC rolü, belirtilen kapsamda belirtilen sorumluya atar.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ff1b-104">SYNTAX</span></span>

### <span data-ttu-id="3ff1b-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ff1b-105">EmptyParameterSet (Default)</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-106">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="3ff1b-106">ResourceGroupWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-107">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="3ff1b-107">ResourceWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-108">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="3ff1b-108">ScopeWithObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> [-Scope <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-109">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="3ff1b-109">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
New-AzureRmRoleAssignment -ObjectId <Guid> -Scope <String> -RoleDefinitionId <Guid> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-110">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-110">ResourceGroupWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-111">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-111">ResourceWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-112">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-112">ScopeWithSignInNameParameterSet</span></span>
```
New-AzureRmRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-113">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-113">ResourceGroupWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-114">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-114">ResourceWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-AllowDelegation]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff1b-115">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff1b-115">ScopeWithSPNParameterSet</span></span>
```
New-AzureRmRoleAssignment -ApplicationId <String> [-Scope <String>] -RoleDefinitionName <String>
 [-AllowDelegation] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff1b-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ff1b-116">DESCRIPTION</span></span>
<span data-ttu-id="3ff1b-117">Erişim vermek için New-AzureRMRoleAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-117">Use the New-AzureRMRoleAssignment command to grant access.</span></span>
<span data-ttu-id="3ff1b-118">Erişim, doğru kapsamda uygun RBAC rolünü atayarak verilir.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-118">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="3ff1b-119">Tüm aboneliğe erişim vermek için, abonelik kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-119">To grant access to the entire subscription, assign a role at the subscription scope.</span></span>
<span data-ttu-id="3ff1b-120">Bir abonelikteki belirli bir kaynak grubuna erişim izni vermek için, kaynak grubu kapsamında bir rol atayın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-120">To grant access to a specific resource group within a subscription, assign a role at the resource group scope.</span></span>
<span data-ttu-id="3ff1b-121">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-121">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="3ff1b-122">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-122">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="3ff1b-123">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-123">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="3ff1b-124">Bir Azure AD uygulaması belirtmek için, ApplicationId veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-124">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="3ff1b-125">Atanmış olan rolün, RoleDefinitionName parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-125">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="3ff1b-126">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-126">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="3ff1b-127">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-127">It defaults to the selected subscription.</span></span> <span data-ttu-id="3ff1b-128">Atamanın kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-128">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="3ff1b-129">Kapsam-bu,/Subscriptions/b ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="3ff1b-129">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\> b.</span></span>
<span data-ttu-id="3ff1b-130">ResourceGroupName-belirtilen kaynak grubuna erişim izni vermek için.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-130">ResourceGroupName - to grant access to the specified resource group.</span></span>
<span data-ttu-id="3ff1b-131">d.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-131">c.</span></span>
<span data-ttu-id="3ff1b-132">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-erişim izni verecek belirli bir kaynağı belirtmek için.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-132">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - to specify a particular resource within a resource group to grant access to.</span></span>

## <span data-ttu-id="3ff1b-133">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ff1b-133">EXAMPLES</span></span>

### <span data-ttu-id="3ff1b-134">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ff1b-134">Example 1</span></span>
```
PS C:\> New-AzureRmRoleAssignment -ResourceGroupName rg1 -SignInName allen.young@live.com -RoleDefinitionName Reader -AllowDelegation
```

<span data-ttu-id="3ff1b-135">Temsilci olarak kullanılabilir durumda olan bir kaynak grubu kapsamındaki bir kullanıcıya okuyucu rolü erişimi verme</span><span class="sxs-lookup"><span data-stu-id="3ff1b-135">Grant Reader role access to a user at a resource group scope with the Role Assignment being available for delegation</span></span>

### <span data-ttu-id="3ff1b-136">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3ff1b-136">Example 2</span></span>
```
PS C:\> Get-AzureRMADGroup -SearchString "Christine Koch Team"

          DisplayName                    Type                           Id
          -----------                    ----                           --------
          Christine Koch Team                                           2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb

PS C:\> New-AzureRmRoleAssignment -ObjectId 2f9d4375-cbf1-48e8-83c9-2a0be4cb33fb -RoleDefinitionName Contributor  -ResourceGroupName rg1
```

<span data-ttu-id="3ff1b-137">Güvenlik grubuna erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="3ff1b-137">Grant access to a security group</span></span>

### <span data-ttu-id="3ff1b-138">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3ff1b-138">Example 3</span></span>
```
PS C:\> New-AzureRmRoleAssignment -SignInName john.doe@contoso.com -RoleDefinitionName Owner -Scope "/subscriptions/86f81fc3-b00f-48cd-8218-3879f51ff362/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="3ff1b-139">Bir kaynaktaki (Web sitesi) bir kullanıcıya erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="3ff1b-139">Grant access to a user at a resource (website)</span></span>

### <span data-ttu-id="3ff1b-140">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3ff1b-140">Example 4</span></span>
```
PS C:\> New-AzureRMRoleAssignment -ObjectId 5ac84765-1c8c-4994-94b2-629461bd191b -RoleDefinitionName "Virtual Machine Contributor" -ResourceName Devices-Engineering-ProjectRND -ResourceType Microsoft.Network/virtualNetworks/subnets -ParentResource virtualNetworks/VNET-EASTUS-01 -ResourceGroupName Network
```

<span data-ttu-id="3ff1b-141">İç içe bir kaynaktaki (alt ağ) gruba erişim izni verme</span><span class="sxs-lookup"><span data-stu-id="3ff1b-141">Grant access to a group at a nested resource (subnet)</span></span>

### <span data-ttu-id="3ff1b-142">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="3ff1b-142">Example 5</span></span>
```
PS C:\> $servicePrincipal = New-AzureRmADServicePrincipal -DisplayName "testServiceprincipal"
PS C:\> New-AzureRmRoleAssignment -RoleDefinitionName "Reader" -ApplicationId $servicePrincipal.ApplicationId
```

<span data-ttu-id="3ff1b-143">Hizmet sorumlusuna okuyucu erişimi verme</span><span class="sxs-lookup"><span data-stu-id="3ff1b-143">Grant reader access to a service principal</span></span>

## <span data-ttu-id="3ff1b-144">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ff1b-144">PARAMETERS</span></span>

### <span data-ttu-id="3ff1b-145">-Allowtemsilci</span><span class="sxs-lookup"><span data-stu-id="3ff1b-145">-AllowDelegation</span></span>
<span data-ttu-id="3ff1b-146">Rol ataması oluştururken temsilci bayrağı.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-146">The delegation flag while creating a Role assignment.</span></span>

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

### <span data-ttu-id="3ff1b-147">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3ff1b-147">-ApplicationId</span></span>
<span data-ttu-id="3ff1b-148">ServicePrincipal 'un uygulama KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3ff1b-148">The Application ID of the ServicePrincipal</span></span>

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

### <span data-ttu-id="3ff1b-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff1b-149">-DefaultProfile</span></span>
<span data-ttu-id="3ff1b-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3ff1b-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ff1b-151">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3ff1b-151">-ObjectId</span></span>
<span data-ttu-id="3ff1b-152">Kullanıcı, Grup veya hizmet sorumlusunun Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-152">Azure AD Objectid of the user, group or service principal.</span></span>

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

### <span data-ttu-id="3ff1b-153">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="3ff1b-153">-ParentResource</span></span>
<span data-ttu-id="3ff1b-154">Hiyerarşide üst kaynak (ResourceName parametresi kullanılarak belirtilen kaynak).</span><span class="sxs-lookup"><span data-stu-id="3ff1b-154">The parent resource in the hierarchy(of the resource specified using ResourceName parameter).</span></span>
<span data-ttu-id="3ff1b-155">Yalnızca kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturmak için ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-155">Should only be  used in conjunction with ResourceGroupName, ResourceType and ResourceName parameters to construct a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="3ff1b-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff1b-156">-ResourceGroupName</span></span>
<span data-ttu-id="3ff1b-157">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-157">The resource group name.</span></span>
<span data-ttu-id="3ff1b-158">Belirtilen kaynak grubunda geçerli olan bir ödev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-158">Creates an assignment that is effective at the specified resource group.</span></span>
<span data-ttu-id="3ff1b-159">ResourceName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanıldığında, komut, kaynağı tanımlayan göreli URI biçiminde bir hiyerarşik kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-159">When used in conjunction with ResourceName, ResourceType and (optionally)ParentResource parameters, the command constructs a hierarchical scope in the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="3ff1b-160">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3ff1b-160">-ResourceName</span></span>
<span data-ttu-id="3ff1b-161">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-161">The resource name.</span></span>
<span data-ttu-id="3ff1b-162">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-162">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="3ff1b-163">Yalnızca ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır, bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-163">Should only be used in conjunction with ResourceGroupName, ResourceType and (optionally)ParentResource parameters to construct a hierarchical scope in the form of a  relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="3ff1b-164">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3ff1b-164">-ResourceType</span></span>
<span data-ttu-id="3ff1b-165">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-165">The resource type.</span></span>
<span data-ttu-id="3ff1b-166">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-166">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="3ff1b-167">Yalnızca ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır ve bir kaynağı tanımlayan göreli URI biçiminde hiyerarşik bir kapsam oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-167">Should only be used in conjunction with ResourceGroupName, ResourceName and (optionally)ParentResource parameters to construct a hierarchical scope in  the form of a relative URI that identifies a resource.</span></span>

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

### <span data-ttu-id="3ff1b-168">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="3ff1b-168">-RoleDefinitionId</span></span>
<span data-ttu-id="3ff1b-169">Sorumluya atanması gereken RBAC rolünün kimliği.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-169">Id of the RBAC role that needs to be assigned to the principal.</span></span>

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

### <span data-ttu-id="3ff1b-170">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3ff1b-170">-RoleDefinitionName</span></span>
<span data-ttu-id="3ff1b-171">Sorumluya atanması gereken RBAC rolünün adı (Reader, katkıda bulunanlar, sanal ağ yöneticisi vb.).</span><span class="sxs-lookup"><span data-stu-id="3ff1b-171">Name of the RBAC role that needs to be assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

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

### <span data-ttu-id="3ff1b-172">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="3ff1b-172">-Scope</span></span>
<span data-ttu-id="3ff1b-173">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-173">The Scope of the role assignment.</span></span>
<span data-ttu-id="3ff1b-174">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-174">In the format of relative URI.</span></span>
<span data-ttu-id="3ff1b-175">Örneğin, "/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg".</span><span class="sxs-lookup"><span data-stu-id="3ff1b-175">For e.g. "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".</span></span>
<span data-ttu-id="3ff1b-176">Belirtilmezse, abone düzeyinde rol ataması oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-176">If not specified, will create the role assignment at subscription level.</span></span>
<span data-ttu-id="3ff1b-177">Belirtilmişse "/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-177">If specified, it should start with "/subscriptions/{id}".</span></span>

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

### <span data-ttu-id="3ff1b-178">-Signınname</span><span class="sxs-lookup"><span data-stu-id="3ff1b-178">-SignInName</span></span>
<span data-ttu-id="3ff1b-179">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-179">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="3ff1b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff1b-180">CommonParameters</span></span>
<span data-ttu-id="3ff1b-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ff1b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff1b-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff1b-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff1b-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ff1b-183">INPUTS</span></span>

### <span data-ttu-id="3ff1b-184">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3ff1b-184">System.Guid</span></span>

### <span data-ttu-id="3ff1b-185">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff1b-185">System.String</span></span>

## <span data-ttu-id="3ff1b-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ff1b-186">OUTPUTS</span></span>

### <span data-ttu-id="3ff1b-187">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="3ff1b-187">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="3ff1b-188">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ff1b-188">NOTES</span></span>
<span data-ttu-id="3ff1b-189">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="3ff1b-189">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3ff1b-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ff1b-190">RELATED LINKS</span></span>

[<span data-ttu-id="3ff1b-191">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="3ff1b-191">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="3ff1b-192">Remove-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="3ff1b-192">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="3ff1b-193">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3ff1b-193">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
