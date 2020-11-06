---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: 017d2122537f6ecc56a714e3e30abb20353df6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589373"
---
# <span data-ttu-id="35874-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35874-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="35874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35874-102">SYNOPSIS</span></span>
<span data-ttu-id="35874-103">Belirtilen kapsamda Azure RBAC rol atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="35874-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="35874-104">Varsayılan olarak, seçilen Azure aboneliğindeki tüm rol atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="35874-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="35874-105">Belirli bir kullanıcıya yönelik atamaları listelemek veya belirli bir kaynak grubundaki veya kaynağındaki atamaları listelemek için ilgili parametreleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35874-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35874-106">SYNTAX</span></span>

### <span data-ttu-id="35874-107">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35874-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="35874-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-109">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="35874-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-110">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="35874-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-111">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="35874-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-112">Roleıdwithscopeandobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="35874-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35874-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35874-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="35874-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35874-124">Tanım</span><span class="sxs-lookup"><span data-stu-id="35874-124">DESCRIPTION</span></span>
<span data-ttu-id="35874-125">Kapsamda etkili olan tüm rol atamalarını listelemek için Get-AzureRMRoleAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="35874-126">Parametre olmadan bu komut, aboneliğin altında yapılan tüm rol atamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="35874-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="35874-127">Bu listeye, sorumlu, rol ve kapsam için filtreleme parametrelerini kullanarak filtre uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="35874-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="35874-128">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="35874-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="35874-129">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="35874-130">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="35874-131">Bir Azure AD uygulaması belirtmek için, ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="35874-132">Atanmış olan rolün, RoleDefinitionName parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="35874-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>
<span data-ttu-id="35874-133">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="35874-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="35874-134">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="35874-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="35874-135">Atamanın kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="35874-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="35874-136">Kapsam-bu,/Subscriptions/ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="35874-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="35874-137">Bu, söz konusu kapsamda geçerli olan atamalara filtre uygulanır Yani, bu kapsamda ve yukarıdaki tüm atamalar.</span><span class="sxs-lookup"><span data-stu-id="35874-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="35874-138">ib.</span><span class="sxs-lookup"><span data-stu-id="35874-138">b.</span></span>
<span data-ttu-id="35874-139">ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="35874-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="35874-140">Bu, atamaların belirtilen c kaynak grubunda geçerli olduğunu filtreedecektir.</span><span class="sxs-lookup"><span data-stu-id="35874-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="35874-141">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar ve bu kaynak kapsamında atamaları geçerli filtreedecektir.</span><span class="sxs-lookup"><span data-stu-id="35874-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>
<span data-ttu-id="35874-142">Belirli bir kullanıcının abonelikteki erişimi belirlemek için, ExpandPrincipalGroups anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="35874-143">Kullanıcıya atanan tüm roller ve kullanıcının üyesi olduğu gruplar listelenir.</span><span class="sxs-lookup"><span data-stu-id="35874-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>
<span data-ttu-id="35874-144">Ayrıca, abonelik yöneticilerini ve ortak yöneticileri de görüntülemek için ıncludeclassıntericadministrators anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="35874-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="35874-145">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35874-145">EXAMPLES</span></span>

### <span data-ttu-id="35874-146">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35874-146">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="35874-147">Abonelikteki tüm rol atamalarını listeleme</span><span class="sxs-lookup"><span data-stu-id="35874-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="35874-148">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="35874-148">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="35874-149">Kullanıcıya yapılan tüm rol atamalarını john.doe@contoso.com ve üye olduğu grupları, testRG kapsamındaki veya üstünde alır.</span><span class="sxs-lookup"><span data-stu-id="35874-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="35874-150">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="35874-150">Example 3</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="35874-151">Belirtilen hizmet sorumlusunun tüm rol atamalarını alır</span><span class="sxs-lookup"><span data-stu-id="35874-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="35874-152">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="35874-152">Example 4</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="35874-153">' Site1 ' Web sitesi kapsamındaki rol atamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="35874-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="35874-154">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35874-154">PARAMETERS</span></span>

### <span data-ttu-id="35874-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35874-155">-DefaultProfile</span></span>
<span data-ttu-id="35874-156">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="35874-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35874-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="35874-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="35874-158">Belirtilmişse, doğrudan kullanıcıya atanan rolleri ve kullanıcının üyesi olduğu grupları döndürür (geçişli).</span><span class="sxs-lookup"><span data-stu-id="35874-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="35874-159">Yalnızca Kullanıcı sorumlusu için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="35874-159">Supported only for a user principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35874-160">-Includeclassıntericadministrators</span><span class="sxs-lookup"><span data-stu-id="35874-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="35874-161">Belirtilmişse, abonelik klasik yöneticileri (ortak yönetici, hizmet yöneticileri vb.) rol atamalarını da listeler.</span><span class="sxs-lookup"><span data-stu-id="35874-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35874-162">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="35874-162">-ObjectId</span></span>
<span data-ttu-id="35874-163">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="35874-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="35874-164">Belirtilen sorumluya yapılan tüm atamalara filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="35874-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="35874-165">-ParentResource</span></span>
<span data-ttu-id="35874-166">ResourceName parametresi kullanılarak belirtilen kaynak hiyerarşisindeki üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="35874-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="35874-167">ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35874-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35874-168">-ResourceGroupName</span></span>
<span data-ttu-id="35874-169">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="35874-169">The resource group name.</span></span>
<span data-ttu-id="35874-170">Belirtilen kaynak grubunda geçerli olan rol atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="35874-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="35874-171">ResourceName, ResourceType ve ParentResource parametreleriyle birlikte kullanıldığında, komut, atamaları kaynak grubundaki kaynaklar için geçerli listeler.</span><span class="sxs-lookup"><span data-stu-id="35874-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="35874-172">-ResourceName</span></span>
<span data-ttu-id="35874-173">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="35874-173">The resource name.</span></span>
<span data-ttu-id="35874-174">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="35874-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="35874-175">ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35874-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="35874-176">-ResourceType</span></span>
<span data-ttu-id="35874-177">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="35874-177">The resource type.</span></span>
<span data-ttu-id="35874-178">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="35874-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="35874-179">ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35874-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-180">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="35874-180">-RoleDefinitionId</span></span>
<span data-ttu-id="35874-181">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="35874-181">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="35874-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="35874-182">-RoleDefinitionName</span></span>
<span data-ttu-id="35874-183">Kullanıcıya atanan rol (Reader, katılımcı, sanal ağ yöneticisi vb.).</span><span class="sxs-lookup"><span data-stu-id="35874-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-184">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="35874-184">-Scope</span></span>
<span data-ttu-id="35874-185">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="35874-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="35874-186">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="35874-186">In the format of relative URI.</span></span>
<span data-ttu-id="35874-187">Örneğin,/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg.</span><span class="sxs-lookup"><span data-stu-id="35874-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="35874-188">"/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="35874-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="35874-189">Komut bu kapsamda geçerli olan tüm atamalara filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="35874-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-190">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="35874-190">-ServicePrincipalName</span></span>
<span data-ttu-id="35874-191">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="35874-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="35874-192">Belirtilen Azure AD uygulamasına yapılan tüm atamalara filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="35874-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-193">-Signınname</span><span class="sxs-lookup"><span data-stu-id="35874-193">-SignInName</span></span>
<span data-ttu-id="35874-194">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="35874-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="35874-195">Belirtilen kullanıcıya yapılan tüm atamalara filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="35874-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35874-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35874-196">CommonParameters</span></span>
<span data-ttu-id="35874-197">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35874-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35874-198">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35874-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35874-199">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35874-199">INPUTS</span></span>

### <span data-ttu-id="35874-200">System. Guid</span><span class="sxs-lookup"><span data-stu-id="35874-200">System.Guid</span></span>

### <span data-ttu-id="35874-201">System. String</span><span class="sxs-lookup"><span data-stu-id="35874-201">System.String</span></span>

## <span data-ttu-id="35874-202">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35874-202">OUTPUTS</span></span>

### <span data-ttu-id="35874-203">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="35874-203">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="35874-204">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35874-204">NOTES</span></span>
<span data-ttu-id="35874-205">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="35874-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="35874-206">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35874-206">RELATED LINKS</span></span>

[<span data-ttu-id="35874-207">Yeni-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="35874-207">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="35874-208">Remove-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="35874-208">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="35874-209">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35874-209">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

