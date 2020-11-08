---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275306"
---
# <span data-ttu-id="a4374-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a4374-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="a4374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4374-102">SYNOPSIS</span></span>
<span data-ttu-id="a4374-103">Yönetilen bir HSM 'deki rol atamalarını alma veya listeleme.</span><span class="sxs-lookup"><span data-stu-id="a4374-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="a4374-104">Belirli bir kullanıcının veya rol tanımının atamalarını listelemek için ilgili parametreleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4374-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="a4374-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4374-105">SYNTAX</span></span>

### <span data-ttu-id="a4374-106">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4374-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4374-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="a4374-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4374-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4374-108">DESCRIPTION</span></span>
<span data-ttu-id="a4374-109">`Get-AzManagedHsmRoleAssignment`Bir kapsam üzerinde etkili olan tüm rol atamalarını listelemek için bu komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4374-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="a4374-110">Parametre olmadan bu komut, yönetilen HSM 'nin altında yapılan tüm rol atamalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4374-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="a4374-111">Bu listeye, sorumlu, rol ve kapsam için filtreleme parametrelerini kullanarak filtre uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="a4374-112">Atamanın konusu belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4374-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="a4374-113">Bir Kullanıcı belirtmek için Signınname veya Azure AD ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4374-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="a4374-114">Güvenlik grubu belirtmek için Azure AD ObjectID parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4374-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="a4374-115">Bir Azure AD uygulaması belirtmek için, ApplicationId veya ObjectID parametrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4374-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="a4374-116">Atanmış olan rolün RoleDefinitionName veya Roledefinitionıd parametresi kullanılarak belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a4374-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="a4374-117">Erişimin verildiği kapsam belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="a4374-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="a4374-118">Varsayılan olarak "/" olur.</span><span class="sxs-lookup"><span data-stu-id="a4374-118">It defaults to "/".</span></span>

## <span data-ttu-id="a4374-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4374-119">EXAMPLES</span></span>

### <span data-ttu-id="a4374-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4374-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="a4374-121">Bu örnekte, tüm kapsamda "myHsm" rol atamalarının tümü listelenir.</span><span class="sxs-lookup"><span data-stu-id="a4374-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="a4374-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a4374-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="a4374-123">Bu örnekte, "myHsm" öğesinin tüm rol atamaları "/Keys" kapsamında listelenir ve sonucu Kullanıcı oturum açma adıyla süzer.</span><span class="sxs-lookup"><span data-stu-id="a4374-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="a4374-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4374-124">PARAMETERS</span></span>

### <span data-ttu-id="a4374-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a4374-125">-ApplicationId</span></span>
<span data-ttu-id="a4374-126">Uygulama SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="a4374-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4374-127">-DefaultProfile</span></span>
<span data-ttu-id="a4374-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4374-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4374-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a4374-129">-HsmName</span></span>
<span data-ttu-id="a4374-130">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="a4374-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="a4374-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a4374-131">-ObjectId</span></span>
<span data-ttu-id="a4374-132">Kullanıcı veya grup nesnesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="a4374-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-133">-Roleatamaadı</span><span class="sxs-lookup"><span data-stu-id="a4374-133">-RoleAssignmentName</span></span>
<span data-ttu-id="a4374-134">Rol atamasının adı.</span><span class="sxs-lookup"><span data-stu-id="a4374-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-135">-Roledefinitionıd</span><span class="sxs-lookup"><span data-stu-id="a4374-135">-RoleDefinitionId</span></span>
<span data-ttu-id="a4374-136">Anaparanın atandığı rol kimliği.</span><span class="sxs-lookup"><span data-stu-id="a4374-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a4374-137">-RoleDefinitionName</span></span>
<span data-ttu-id="a4374-138">Anapara atanacak RBAC rolünün adı.</span><span class="sxs-lookup"><span data-stu-id="a4374-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-139">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a4374-139">-Scope</span></span>
<span data-ttu-id="a4374-140">Rol atamasının veya tanımının uygulandığı kapsam; Örneğin, '/' veya '/Keys ' veya '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="a4374-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="a4374-141">'/' gözardı edildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4374-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="a4374-142">-Signınname</span><span class="sxs-lookup"><span data-stu-id="a4374-142">-SignInName</span></span>
<span data-ttu-id="a4374-143">Kullanıcı oturumu adı.</span><span class="sxs-lookup"><span data-stu-id="a4374-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4374-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4374-144">CommonParameters</span></span>
<span data-ttu-id="a4374-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4374-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4374-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a4374-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4374-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4374-147">INPUTS</span></span>

### <span data-ttu-id="a4374-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a4374-148">None</span></span>

## <span data-ttu-id="a4374-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4374-149">OUTPUTS</span></span>

### <span data-ttu-id="a4374-150">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultroleödev</span><span class="sxs-lookup"><span data-stu-id="a4374-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a4374-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4374-151">NOTES</span></span>

## <span data-ttu-id="a4374-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4374-152">RELATED LINKS</span></span>
