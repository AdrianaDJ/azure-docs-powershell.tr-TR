---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdenyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDenyAssignment.md
ms.openlocfilehash: 22acfc03afa4758c44d6c6f02ac1d734c90a806b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266464"
---
# <span data-ttu-id="d914a-101">Get-AzDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="d914a-101">Get-AzDenyAssignment</span></span>

## <span data-ttu-id="d914a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d914a-102">SYNOPSIS</span></span>
<span data-ttu-id="d914a-103">Belirtilen kapsamda Azure RBAC reddetme atamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d914a-103">Lists Azure RBAC deny assignments at the specified scope.</span></span>
<span data-ttu-id="d914a-104">Varsayılan olarak, seçilen Azure aboneliğindeki tüm atamaları engeller.</span><span class="sxs-lookup"><span data-stu-id="d914a-104">By default it lists all deny assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="d914a-105">Belirli bir kullanıcıya yönelik atamaları Reddet veya belirli bir kaynak grubundaki veya kaynağındaki atamaları engelle seçeneğini listelemek için ilgili parametreleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-105">Use respective parameters to list deny assignments to a specific user, or to list deny assignments on a specific resource group or resource.</span></span>

## <span data-ttu-id="d914a-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d914a-106">SYNTAX</span></span>

### <span data-ttu-id="d914a-107">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d914a-107">EmptyParameterSet (Default)</span></span>
```
Get-AzDenyAssignment [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="d914a-108">ObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-109">Resourcegroupwithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="d914a-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-110">Resourcewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="d914a-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-111">Scopewithobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="d914a-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzDenyAssignment -ObjectId <Guid> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-112">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-112">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-113">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-113">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-114">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-114">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-115">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-115">SignInNameParameterSet</span></span>
```
Get-AzDenyAssignment -SignInName <String> [-ExpandPrincipalGroups] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-116">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-116">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-117">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-117">ResourceWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-118">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-118">ScopeWithSPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> -Scope <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-119">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-119">SPNParameterSet</span></span>
```
Get-AzDenyAssignment -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-120">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-120">ResourceGroupParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-121">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-121">ResourceParameterSet</span></span>
```
Get-AzDenyAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-122">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-122">ScopeParameterSet</span></span>
```
Get-AzDenyAssignment -Scope <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d914a-123">Denyassignmentivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="d914a-123">DenyAssignmentIdParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -Id <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d914a-124">DenyAssignmentNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d914a-124">DenyAssignmentNameParameterSet</span></span>
```
Get-AzDenyAssignment [-Scope <String>] -DenyAssignmentName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d914a-125">Tanım</span><span class="sxs-lookup"><span data-stu-id="d914a-125">DESCRIPTION</span></span>
<span data-ttu-id="d914a-126">Kapsamda etkin olan tüm atamaları engellemek için Get-AzDenyAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-126">Use the Get-AzDenyAssignment command to list all deny assignments that are effective on a scope.</span></span>
<span data-ttu-id="d914a-127">Parametre olmadan bu komut, aboneliğin altında yapılan tüm kabul atamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="d914a-127">Without any parameters, this command returns all the deny assignments made under the subscription.</span></span>
<span data-ttu-id="d914a-128">Bu liste, anapara için filtreleme parametreleri kullanılarak filtrelenebilir, ödev adını ve kapsamını reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="d914a-128">This list can  be filtered using filtering parameters for principal, deny assignment name and scope.</span></span>
<span data-ttu-id="d914a-129">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="d914a-130">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="d914a-131">Bir Azure AD uygulaması belirtmek için, ServicePrincipalName veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>
<span data-ttu-id="d914a-132">Erişimin reddedildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="d914a-132">The scope at which access is being denied may be specified.</span></span>
<span data-ttu-id="d914a-133">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="d914a-133">It defaults to the selected subscription.</span></span>
<span data-ttu-id="d914a-134">Reddet atamasının kapsamı, aşağıdaki parametre birleşimlerinin biri kullanılarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="d914a-134">The scope of the deny assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="d914a-135">Kapsam-bu,/Subscriptions/ile başlayan tam nitelikli bir kapsamdır \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="d914a-135">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="d914a-136">Bu, söz konusu kapsamda geçerli olan atamaları Reddet (.</span><span class="sxs-lookup"><span data-stu-id="d914a-136">This will filter deny assignments that are effective at that particular scope i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="d914a-137">ib.</span><span class="sxs-lookup"><span data-stu-id="d914a-137">b.</span></span>
<span data-ttu-id="d914a-138">ResourceGroupName-aboneliğin altındaki herhangi bir kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d914a-138">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="d914a-139">Bu, ödevleri belirtilen kaynak grubunda geçerli olacak şekilde filtreedecektir (.</span><span class="sxs-lookup"><span data-stu-id="d914a-139">This will filter assignments effective at the specified resource group i.e. all deny assignments at that scope and above.</span></span>
<span data-ttu-id="d914a-140">d.</span><span class="sxs-lookup"><span data-stu-id="d914a-140">c.</span></span>
<span data-ttu-id="d914a-141">ResourceName, ResourceType, ResourceGroupName ve (isteğe bağlı) ParentResource-aboneliğin altındaki belirli bir kaynağı tanımlar ve bu kaynak kapsamda Reddet atamalarını etkin olarak süzer.</span><span class="sxs-lookup"><span data-stu-id="d914a-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter deny assignments effective at that resource scope.</span></span>
<span data-ttu-id="d914a-142">Abonelikteki belirli bir kullanıcı için erişimin reddedildiğini belirlemek için, ExpandPrincipalGroups anahtarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d914a-142">To determine what access is denied for a particular user in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="d914a-143">Bu, kullanıcıya atanan tüm atamaları ve kullanıcının üyesi olduğu grupları listeler.</span><span class="sxs-lookup"><span data-stu-id="d914a-143">This will list all deny assignments assigned to the user, and to the groups that the user is member of.</span></span>

## <span data-ttu-id="d914a-144">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d914a-144">EXAMPLES</span></span>

### <span data-ttu-id="d914a-145">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d914a-145">Example 1</span></span>

<span data-ttu-id="d914a-146">Aboneliğin tüm atamalarını listeleme</span><span class="sxs-lookup"><span data-stu-id="d914a-146">List all deny assignments in the subscription</span></span>

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

### <span data-ttu-id="d914a-147">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d914a-147">Example 2</span></span>

<span data-ttu-id="d914a-148">john.doe@contoso.comTestRG ve üst kapsamındaki kullanıcıya yapılan tüm atamaları reddetme.</span><span class="sxs-lookup"><span data-stu-id="d914a-148">Gets all deny assignments made to user john.doe@contoso.com at the scope testRG and above.</span></span>

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

### <span data-ttu-id="d914a-149">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d914a-149">Example 3</span></span>

<span data-ttu-id="d914a-150">Belirtilen hizmet sorumlusunun tüm atamalarını reddetme</span><span class="sxs-lookup"><span data-stu-id="d914a-150">Gets all deny assignments of the specified service principal</span></span>

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

### <span data-ttu-id="d914a-151">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="d914a-151">Example 4</span></span>

<span data-ttu-id="d914a-152">' Site1 ' Web sitesi kapsamındaki atamaları Reddet 'i alır.</span><span class="sxs-lookup"><span data-stu-id="d914a-152">Gets deny assignments at the 'site1' website scope.</span></span>

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

## <span data-ttu-id="d914a-153">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d914a-153">PARAMETERS</span></span>

### <span data-ttu-id="d914a-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d914a-154">-DefaultProfile</span></span>
<span data-ttu-id="d914a-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d914a-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d914a-156">-DenyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d914a-156">-DenyAssignmentName</span></span>
<span data-ttu-id="d914a-157">Reddet atamasının adı.</span><span class="sxs-lookup"><span data-stu-id="d914a-157">Name of the deny assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: DenyAssignmentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d914a-158">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="d914a-158">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="d914a-159">Belirtilmişse, doğrudan kullanıcıya atanmış olan ve kullanıcının üye olduğu gruplara (geçişli) izin verme atamalarını getirir.</span><span class="sxs-lookup"><span data-stu-id="d914a-159">If specified, returns deny assignments directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="d914a-160">Yalnızca Kullanıcı sorumlusu için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d914a-160">Supported only for a user principal.</span></span>

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

### <span data-ttu-id="d914a-161">-ID</span><span class="sxs-lookup"><span data-stu-id="d914a-161">-Id</span></span>
<span data-ttu-id="d914a-162">İzin kimliğini reddedin.</span><span class="sxs-lookup"><span data-stu-id="d914a-162">Deny assignment id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DenyAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d914a-163">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="d914a-163">-ObjectId</span></span>
<span data-ttu-id="d914a-164">Kullanıcının, grubun veya hizmetin Azure AD ObjectID.</span><span class="sxs-lookup"><span data-stu-id="d914a-164">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="d914a-165">Filtreler belirtilen sorumluya yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="d914a-165">Filters all deny assignments that are made to the specified principal.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d914a-166">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="d914a-166">-ParentResource</span></span>
<span data-ttu-id="d914a-167">ResourceName parametresi kullanılarak belirtilen kaynak hiyerarşisindeki üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="d914a-167">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="d914a-168">ResourceGroupName, ResourceType ve ResourceName parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d914a-168">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

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

### <span data-ttu-id="d914a-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d914a-169">-ResourceGroupName</span></span>
<span data-ttu-id="d914a-170">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d914a-170">The resource group name.</span></span>
<span data-ttu-id="d914a-171">Belirtilen kaynak grubunda geçerli olan atamaları Reddet listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="d914a-171">Lists deny assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="d914a-172">ResourceName, ResourceType ve ParentResource parametreleriyle birlikte kullanıldığında, komut listeleri, kaynak grubundaki kaynaklarda atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="d914a-172">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists deny assignments effective at resources within the resource group.</span></span>

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

### <span data-ttu-id="d914a-173">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d914a-173">-ResourceName</span></span>
<span data-ttu-id="d914a-174">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d914a-174">The resource name.</span></span>
<span data-ttu-id="d914a-175">Örneğin, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="d914a-175">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="d914a-176">ResourceGroupName, ResourceType ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d914a-176">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="d914a-177">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d914a-177">-ResourceType</span></span>
<span data-ttu-id="d914a-178">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="d914a-178">The resource type.</span></span>
<span data-ttu-id="d914a-179">Örneğin, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="d914a-179">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="d914a-180">ResourceGroupName, ResourceName ve (isteğe bağlı) ParentResource parametreleriyle birlikte kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d914a-180">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

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

### <span data-ttu-id="d914a-181">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="d914a-181">-Scope</span></span>
<span data-ttu-id="d914a-182">Rol atamasının kapsamı.</span><span class="sxs-lookup"><span data-stu-id="d914a-182">The Scope of the role assignment.</span></span>
<span data-ttu-id="d914a-183">Göreli URI biçiminde.</span><span class="sxs-lookup"><span data-stu-id="d914a-183">In the format of relative URI.</span></span>
<span data-ttu-id="d914a-184">Örneğin,/Subscriptions/9004a9fd-vseç58e-48dc-aeb2-4a4aec58606f/ResourceGroups/testrg.</span><span class="sxs-lookup"><span data-stu-id="d914a-184">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="d914a-185">"/Subscriptions/{id}" ile başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="d914a-185">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="d914a-186">Komut filtreleri bu kapsamda geçerli olan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="d914a-186">The command filters all deny assignments that are effective at that scope.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, DenyAssignmentIdParameterSet, DenyAssignmentNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="d914a-187">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d914a-187">-ServicePrincipalName</span></span>
<span data-ttu-id="d914a-188">Hizmet sorumlusunun ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="d914a-188">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="d914a-189">Filtreler belirtilen Azure AD uygulamasına yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="d914a-189">Filters all deny assignments that are made to the specified Azure AD application.</span></span>

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

### <span data-ttu-id="d914a-190">-Signınname</span><span class="sxs-lookup"><span data-stu-id="d914a-190">-SignInName</span></span>
<span data-ttu-id="d914a-191">Kullanıcının e-posta adresi veya Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="d914a-191">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="d914a-192">Filtreler belirtilen kullanıcıya yapılan tüm atamaları reddeder.</span><span class="sxs-lookup"><span data-stu-id="d914a-192">Filters all deny assignments that are made to the specified user.</span></span>

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

### <span data-ttu-id="d914a-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d914a-193">CommonParameters</span></span>
<span data-ttu-id="d914a-194">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d914a-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d914a-195">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d914a-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d914a-196">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d914a-196">INPUTS</span></span>

### <span data-ttu-id="d914a-197">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d914a-197">System.Guid</span></span>

### <span data-ttu-id="d914a-198">System. String</span><span class="sxs-lookup"><span data-stu-id="d914a-198">System.String</span></span>

## <span data-ttu-id="d914a-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d914a-199">OUTPUTS</span></span>

### <span data-ttu-id="d914a-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span><span class="sxs-lookup"><span data-stu-id="d914a-200">Microsoft.Azure.Commands.Resources.Models.Authorization.PSDenyAssignment</span></span>

## <span data-ttu-id="d914a-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d914a-201">NOTES</span></span>
<span data-ttu-id="d914a-202">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="d914a-202">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d914a-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d914a-203">RELATED LINKS</span></span>
