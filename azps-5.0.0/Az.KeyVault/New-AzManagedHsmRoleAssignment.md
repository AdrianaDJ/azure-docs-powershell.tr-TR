---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275303"
---
# <span data-ttu-id="7520f-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7520f-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="7520f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7520f-102">SYNOPSIS</span></span>
<span data-ttu-id="7520f-103">Belirtilen RBAC rolü, belirtilen kapsamda belirtilen sorumluya atar.</span><span class="sxs-lookup"><span data-stu-id="7520f-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="7520f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7520f-104">SYNTAX</span></span>

### <span data-ttu-id="7520f-105">Definitionnamesignınname (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7520f-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7520f-106">Definitionnameapplicationıd</span><span class="sxs-lookup"><span data-stu-id="7520f-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7520f-107">Definitionnameobjectıd</span><span class="sxs-lookup"><span data-stu-id="7520f-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7520f-108">Definitionıdapplicationıd</span><span class="sxs-lookup"><span data-stu-id="7520f-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7520f-109">Definitionıdobjectid</span><span class="sxs-lookup"><span data-stu-id="7520f-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7520f-110">Definitionıdsignınname</span><span class="sxs-lookup"><span data-stu-id="7520f-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7520f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="7520f-111">DESCRIPTION</span></span>
<span data-ttu-id="7520f-112">Bu `New-AzManagedHsmRoleAssignment` komutu kullanarak erişim sağlayın.</span><span class="sxs-lookup"><span data-stu-id="7520f-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="7520f-113">Erişim, doğru kapsamda uygun RBAC rolünü atayarak verilir.</span><span class="sxs-lookup"><span data-stu-id="7520f-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="7520f-114">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7520f-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7520f-115">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7520f-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7520f-116">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7520f-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7520f-117">Bir Azure AD uygulaması belirtmek için, ApplicationId veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7520f-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="7520f-118">Atanmış olan rolün, RoleDefinitionName PR Roledefinitionıd parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7520f-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="7520f-119">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="7520f-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="7520f-120">Varsayılan olarak seçili aboneliği alır.</span><span class="sxs-lookup"><span data-stu-id="7520f-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="7520f-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7520f-121">EXAMPLES</span></span>

### <span data-ttu-id="7520f-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7520f-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="7520f-123">Bu örnek, "" yönetilen HSM Ilkesi Yöneticisi "kullanıcısına user1@microsoft.com en üst kapsamda rol atar.</span><span class="sxs-lookup"><span data-stu-id="7520f-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="7520f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7520f-124">PARAMETERS</span></span>

### <span data-ttu-id="7520f-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7520f-125">-ApplicationId</span></span>
<span data-ttu-id="7520f-126">Uygulama SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="7520f-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7520f-127">-DefaultProfile</span></span>
<span data-ttu-id="7520f-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7520f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7520f-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7520f-129">-HsmName</span></span>
<span data-ttu-id="7520f-130">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="7520f-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7520f-131">-ObjectId</span></span>
<span data-ttu-id="7520f-132">Kullanıcı veya grup nesnesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="7520f-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-133">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="7520f-133">-RoleDefinitionId</span></span>
<span data-ttu-id="7520f-134">Anaparanın atandığı rol kimliği.</span><span class="sxs-lookup"><span data-stu-id="7520f-134">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7520f-135">-RoleDefinitionName</span></span>
<span data-ttu-id="7520f-136">Anapara atanacak RBAC rolünün adı.</span><span class="sxs-lookup"><span data-stu-id="7520f-136">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-137">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="7520f-137">-Scope</span></span>
<span data-ttu-id="7520f-138">Rol atamasının veya tanımının uygulandığı kapsam; Örneğin, '/' veya '/Keys ' veya '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="7520f-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="7520f-139">'/' gözardı edildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7520f-139">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-140">-Signınname</span><span class="sxs-lookup"><span data-stu-id="7520f-140">-SignInName</span></span>
<span data-ttu-id="7520f-141">Kullanıcı oturumu adı.</span><span class="sxs-lookup"><span data-stu-id="7520f-141">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7520f-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="7520f-142">-Confirm</span></span>
<span data-ttu-id="7520f-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7520f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7520f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7520f-144">-WhatIf</span></span>
<span data-ttu-id="7520f-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7520f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7520f-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7520f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7520f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7520f-147">CommonParameters</span></span>
<span data-ttu-id="7520f-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7520f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7520f-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7520f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7520f-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7520f-150">INPUTS</span></span>

### <span data-ttu-id="7520f-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7520f-151">None</span></span>

## <span data-ttu-id="7520f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7520f-152">OUTPUTS</span></span>

### <span data-ttu-id="7520f-153">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultroleödev</span><span class="sxs-lookup"><span data-stu-id="7520f-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="7520f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7520f-154">NOTES</span></span>

## <span data-ttu-id="7520f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7520f-155">RELATED LINKS</span></span>
