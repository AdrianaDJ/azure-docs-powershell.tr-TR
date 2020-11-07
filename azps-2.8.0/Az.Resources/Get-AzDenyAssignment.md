---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 745df057c7c111bdca7cc30ac0864e15905ffd6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932604"
---
# <span data-ttu-id="c2dd5-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="c2dd5-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="c2dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2dd5-103">Belirtilen kapsamda Azure RBAC reddetme atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="c2dd5-104">Varsayılan olarak, seçilen Azure aboneliğindeki tüm atamaları engeller.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="c2dd5-105">Belirli bir kullanıcıya yönelik atamaları Reddet veya belirli bir kaynak grubundaki veya kaynağındaki atamaları engelle seçeneğini listelemek için ilgili parametreleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="c2dd5-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2dd5-106">SYNTAX</span></span>

### <span data-ttu-id="c2dd5-107">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2dd5-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-108">Denyassignmentivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c2dd5-108">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-109">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-109">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment -DenyAssignmentName <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-110">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="c2dd5-110">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-111">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c2dd5-111">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-112">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c2dd5-112">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-113">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c2dd5-113">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-114">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-114">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-115">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-115">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-116">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-116">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-117">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-117">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-118">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-118">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-119">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-119">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-120">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-120">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-121">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-121">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-122">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-122">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-123">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-123">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String> [-ParentResource <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dd5-124">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2dd5-124">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2dd5-125">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2dd5-125">DESCRIPTION</span></span>
<span data-ttu-id="c2dd5-126">Kapsamda etkin olan tüm atamaları engellemek için Get-AzDenyAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="c2dd5-127">Parametre olmadan bu komut, aboneliğin altında yapılan tüm kabul atamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="c2dd5-128">Bu liste, anapara için filtreleme parametreleri kullanılarak filtrelenebilir, ödev adını ve kapsamını reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="c2dd5-129">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="c2dd5-130">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="c2dd5-131">Bir Azure AD uygulaması belirtmek için, ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="c2dd5-132">Erişimin reddedildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="c2dd5-133">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="c2dd5-134">Reddet atamasının kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="c2dd5-135">Kapsam-bu,/Subscriptions/SubscriptionID ile başlayan tam nitelikli bir kapsamdır \< \> .</span><span class="sxs-lookup"><span data-stu-id="c2dd5-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="c2dd5-136">Bu, söz konusu kapsamda geçerli olan atamaları Reddet (.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="c2dd5-137">ib.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-137">b.</span></span>
<span data-ttu-id="c2dd5-138">ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="c2dd5-139">Bu, ödevleri belirtilen kaynak grubunda geçerli olacak şekilde filtreedecektir (.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="c2dd5-140">d.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-140">c.</span></span>
<span data-ttu-id="c2dd5-141">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar ve bu kaynak kapsamda Reddet atamalarını etkin olarak süzer.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="c2dd5-142">Abonelikteki belirli bir kullanıcı için erişimin reddedildiğini belirlemek için, ExpandPrincipalGroups anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="c2dd5-143">Bu, kullanıcıya atanan tüm atamaları ve kullanıcının üyesi olduğu grupları listeler.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="c2dd5-144">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2dd5-144">EXAMPLES</span></span>

### <span data-ttu-id="c2dd5-145">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2dd5-145">Example 1</span></span>

<span data-ttu-id="c2dd5-146">Aboneliğin tüm atamalarını listeleme</span><span class="sxs-lookup"><span data-stu-id="c2dd5-146">List all deny assignments in the subscription</span></span>

```
PS C:\> Get-AzDenyAssignment
Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  All Principals
                          ObjectType:   SystemDefined
                          ObjectId:     00000000-0000-0000-0000-000000000000
                          }
ExcludePrincipals       : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="c2dd5-147">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c2dd5-147">Example 2</span></span>

<span data-ttu-id="c2dd5-148">john.doe@contoso.comTestRG ve üst kapsamındaki kullanıcıya yapılan tüm atamaları reddetme.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

```
PS C:\> Get-AzDenyAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com

Id                      : 22704996-fbd0-4ab1-8625-722d897825d2
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  john.doe
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  PowershellTestingApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="c2dd5-149">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c2dd5-149">Example 3</span></span>

<span data-ttu-id="c2dd5-150">Belirtilen hizmet sorumlusunun tüm atamalarını reddetme</span><span class="sxs-lookup"><span data-stu-id="c2dd5-150">Gets all deny assignments of the specified service principal</span></span>

```
PS C:\> Get-AzDenyAssignment -ServicePrincipalName 'http://testapp1.com'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True
```

### <span data-ttu-id="c2dd5-151">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="c2dd5-151">Example 4</span></span>

<span data-ttu-id="c2dd5-152">' Site1 ' Web sitesi kapsamındaki atamaları Reddet 'i alır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-152">Gets deny assignments at the 'site1' website scope.</span></span>

```
PS C:\> Get-AzDenyAssignment -Scope '/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/testRG/providers/Microsoft.Web/sites/site1'

Id                      : 43af7d0c-0bf8-407f-96c0-96a29d076431
DenyAssignmentName      : Test deny assignment 1
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourcegroups/testRG
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

Id                      : 94e3d9da-3700-4113-aab4-15f6c173d794
DenyAssignmentName      : Test deny assignment 2
Description             : Test deny assignment for PS cmdlets
Actions                 : {foo/*}
NotActions              : {foo/*/read}
DataActions             : {foo/*}
NotDataActions          : {}
Scope                   : /subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/testRG/providers/Microsoft.Web/sites/site1
DoNotApplyToChildScopes : False
Principals              : {
                          DisplayName:  testuser
                          ObjectType:   User
                          ObjectId:     f8d526a0-54eb-4941-ae69-ebf4a334d0f0
                          ,
                          DisplayName:  TestApp
                          ObjectType:   ServicePrincipal
                          ObjectId:     f2dc21ac-702a-4bde-a4ce-146edf751d81
                          }
ExcludePrincipals       : {}
IsSystemProtected       : True

```

## <span data-ttu-id="c2dd5-153">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2dd5-153">PARAMETERS</span></span>

### <span data-ttu-id="c2dd5-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2dd5-154">-DefaultProfile</span></span>
<span data-ttu-id="c2dd5-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c2dd5-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2dd5-156">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="c2dd5-156">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="c2dd5-157">Belirtilmişse, doğrudan kullanıcıya atanmış olan ve kullanıcının üye olduğu gruplara (geçişli) izin verme atamalarını getirir.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-157">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="c2dd5-158">Yalnızca Kullanıcı sorumlusu için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-158">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="c2dd5-159">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c2dd5-159">-ObjectId</span></span>
<span data-ttu-id="c2dd5-160">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-160">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="c2dd5-161">Filtreler belirtilen sorumluya yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-161">Filters all deny assignments that are made to the specified principal.</span></span>

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

### <span data-ttu-id="c2dd5-162">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="c2dd5-162">-ParentResource</span></span>
<span data-ttu-id="c2dd5-163">ResourceName parametresi kullanılarak belirtilen kaynak hiyerarşisindeki üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-163">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="c2dd5-164">ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-164">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="c2dd5-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2dd5-165">-ResourceGroupName</span></span>
<span data-ttu-id="c2dd5-166">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-166">The resource group name.</span></span>
<span data-ttu-id="c2dd5-167">Belirtilen kaynak grubunda geçerli olan atamaları Reddet listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-167">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="c2dd5-168">ResourceName, ResourceType ve ParentResource parametreleriyle birlikte kullanıldığında, komut listeleri, kaynak grubundaki kaynaklarda atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-168">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="c2dd5-169">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c2dd5-169">-ResourceName</span></span>
<span data-ttu-id="c2dd5-170">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-170">The resource name.</span></span>
<span data-ttu-id="c2dd5-171">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-171">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="c2dd5-172">ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-172">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="c2dd5-173">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c2dd5-173">-ResourceType</span></span>
<span data-ttu-id="c2dd5-174">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-174">The resource type.</span></span>
<span data-ttu-id="c2dd5-175">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-175">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="c2dd5-176">ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-176">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="c2dd5-177">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c2dd5-177">-Scope</span></span>
<span data-ttu-id="c2dd5-178">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-178">The Scope of the role assignment.</span></span>
<span data-ttu-id="c2dd5-179">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-179">In the format of relative URI.</span></span>
<span data-ttu-id="c2dd5-180">Örneğin,/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-180">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="c2dd5-181">"/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-181">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="c2dd5-182">Komut filtreleri bu kapsamda geçerli olan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-182">The command filters all deny assignments that are effective at that scope.</span></span>

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

### <span data-ttu-id="c2dd5-183">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c2dd5-183">-ServicePrincipalName</span></span>
<span data-ttu-id="c2dd5-184">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-184">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="c2dd5-185">Filtreler belirtilen Azure AD uygulamasına yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-185">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="c2dd5-186">-Signınname</span><span class="sxs-lookup"><span data-stu-id="c2dd5-186">-SignInName</span></span>
<span data-ttu-id="c2dd5-187">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-187">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="c2dd5-188">Filtreler belirtilen kullanıcıya yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-188">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="c2dd5-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2dd5-189">CommonParameters</span></span>
<span data-ttu-id="c2dd5-190">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2dd5-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2dd5-191">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2dd5-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2dd5-192">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2dd5-192">INPUTS</span></span>

### <span data-ttu-id="c2dd5-193">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c2dd5-193">System.Guid</span></span>

### <span data-ttu-id="c2dd5-194">System. String</span><span class="sxs-lookup"><span data-stu-id="c2dd5-194">System.String</span></span>

## <span data-ttu-id="c2dd5-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2dd5-195">OUTPUTS</span></span>

### <span data-ttu-id="c2dd5-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="c2dd5-196">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="c2dd5-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2dd5-197">NOTES</span></span>
<span data-ttu-id="c2dd5-198">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="c2dd5-198">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>