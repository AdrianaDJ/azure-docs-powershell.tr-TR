---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275288"
---
# <span data-ttu-id="38ed0-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="38ed0-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="38ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="38ed0-103">Belirli bir kapsamda belirli bir role atanmış olan belirtilen sorumluya rol atamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38ed0-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="38ed0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38ed0-104">SYNTAX</span></span>

### <span data-ttu-id="38ed0-105">Definitionnamesignınname (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38ed0-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-106">Definitionnameapplicationıd</span><span class="sxs-lookup"><span data-stu-id="38ed0-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-107">Definitionnameobjectıd</span><span class="sxs-lookup"><span data-stu-id="38ed0-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-108">Definitionıdapplicationıd</span><span class="sxs-lookup"><span data-stu-id="38ed0-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-109">Definitionıdobjectid</span><span class="sxs-lookup"><span data-stu-id="38ed0-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-110">Definitionıdsignınname</span><span class="sxs-lookup"><span data-stu-id="38ed0-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38ed0-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ed0-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="38ed0-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ed0-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="38ed0-113">DESCRIPTION</span></span>
<span data-ttu-id="38ed0-114">`Remove-AzManagedHsmRoleAssignment`Verilen kapsamdaki ve verilen rolün herhangi bir sorumlusuna erişimi iptal etmek için cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="38ed0-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="38ed0-115">Atamanın (anapara gibi) belirtilmesi gerekır.</span><span class="sxs-lookup"><span data-stu-id="38ed0-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="38ed0-116">Patron bir Kullanıcı (bir kullanıcıyı tanımlayan Signınname veya ObjectID parametrelerini kullanın), güvenlik grubu (bir grubu belirlemek için ObjectID parametresini kullanma)</span><span class="sxs-lookup"><span data-stu-id="38ed0-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="38ed0-117">Anaparanın atandığı rol, RoleDefinitionName veya Roledefinitionıd parametresi kullanılarak belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="38ed0-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="38ed0-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38ed0-118">EXAMPLES</span></span>

### <span data-ttu-id="38ed0-119">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="38ed0-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="38ed0-120">Bu örnekte, "" yönetilen HSM Ilke Yöneticisi " user1@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="38ed0-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="38ed0-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="38ed0-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="38ed0-122">Bu örnek tüm kapsamlardaki "" tüm rollerini iptal eder user1@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="38ed0-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="38ed0-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38ed0-123">PARAMETERS</span></span>

### <span data-ttu-id="38ed0-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="38ed0-124">-ApplicationId</span></span>
<span data-ttu-id="38ed0-125">Uygulama SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="38ed0-125">The app SPN.</span></span>

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

### <span data-ttu-id="38ed0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ed0-126">-DefaultProfile</span></span>
<span data-ttu-id="38ed0-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38ed0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ed0-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="38ed0-128">-HsmName</span></span>
<span data-ttu-id="38ed0-129">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="38ed0-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed0-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ed0-130">-InputObject</span></span>
<span data-ttu-id="38ed0-131">Rol atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="38ed0-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ed0-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="38ed0-132">-ObjectId</span></span>
<span data-ttu-id="38ed0-133">Kullanıcı veya grup nesnesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="38ed0-133">The user or group object id.</span></span>

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

### <span data-ttu-id="38ed0-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="38ed0-134">-PassThru</span></span>
<span data-ttu-id="38ed0-135">HSM geri yüklendiğinde doğru döner.</span><span class="sxs-lookup"><span data-stu-id="38ed0-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="38ed0-136">-Roleatamaadı</span><span class="sxs-lookup"><span data-stu-id="38ed0-136">-RoleAssignmentName</span></span>
<span data-ttu-id="38ed0-137">Rol atamasının adı.</span><span class="sxs-lookup"><span data-stu-id="38ed0-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ed0-138">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="38ed0-138">-RoleDefinitionId</span></span>
<span data-ttu-id="38ed0-139">Anaparanın atandığı rol kimliği.</span><span class="sxs-lookup"><span data-stu-id="38ed0-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="38ed0-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="38ed0-140">-RoleDefinitionName</span></span>
<span data-ttu-id="38ed0-141">Anapara atanacak RBAC rolünün adı.</span><span class="sxs-lookup"><span data-stu-id="38ed0-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="38ed0-142">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="38ed0-142">-Scope</span></span>
<span data-ttu-id="38ed0-143">Rol atamasının veya tanımının uygulandığı kapsam; Örneğin, '/' veya '/Keys ' veya '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="38ed0-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="38ed0-144">'/' gözardı edildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38ed0-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="38ed0-145">-Signınname</span><span class="sxs-lookup"><span data-stu-id="38ed0-145">-SignInName</span></span>
<span data-ttu-id="38ed0-146">Kullanıcı oturumu adı.</span><span class="sxs-lookup"><span data-stu-id="38ed0-146">The user SignInName.</span></span>

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

### <span data-ttu-id="38ed0-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="38ed0-147">-Confirm</span></span>
<span data-ttu-id="38ed0-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38ed0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ed0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ed0-149">-WhatIf</span></span>
<span data-ttu-id="38ed0-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38ed0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ed0-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38ed0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ed0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ed0-152">CommonParameters</span></span>
<span data-ttu-id="38ed0-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38ed0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ed0-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="38ed0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ed0-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38ed0-155">INPUTS</span></span>

### <span data-ttu-id="38ed0-156">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultroleödev</span><span class="sxs-lookup"><span data-stu-id="38ed0-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="38ed0-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38ed0-157">OUTPUTS</span></span>

### <span data-ttu-id="38ed0-158">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultroleödev</span><span class="sxs-lookup"><span data-stu-id="38ed0-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="38ed0-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38ed0-159">NOTES</span></span>

## <span data-ttu-id="38ed0-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38ed0-160">RELATED LINKS</span></span>
