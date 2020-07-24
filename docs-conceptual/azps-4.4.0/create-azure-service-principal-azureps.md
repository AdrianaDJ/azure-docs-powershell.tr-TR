---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.openlocfilehash: 9d1f0e3be894a592bdf105c2070e9db0cf882921
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382301"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="03101-103">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="03101-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="03101-104">Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03101-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="03101-105">Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.</span><span class="sxs-lookup"><span data-stu-id="03101-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="03101-106">Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir.</span><span class="sxs-lookup"><span data-stu-id="03101-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="03101-107">Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="03101-108">Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="03101-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="03101-109">Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03101-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="03101-110">Hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="03101-110">Create a service principal</span></span>

<span data-ttu-id="03101-111">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="03101-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="03101-112">Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="03101-113">Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="03101-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="03101-114">Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="03101-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="03101-115">Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="03101-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="03101-116">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="03101-116">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03101-117">Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan**’dır.</span><span class="sxs-lookup"><span data-stu-id="03101-117">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="03101-118">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="03101-118">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="03101-119">Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="03101-119">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="03101-120">Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="03101-120">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="03101-121">Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.</span><span class="sxs-lookup"><span data-stu-id="03101-121">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="03101-122">Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir.</span><span class="sxs-lookup"><span data-stu-id="03101-122">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="03101-123">Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="03101-123">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="03101-124">Değeri, konsol çıkışında _görüntülenmez_.</span><span class="sxs-lookup"><span data-stu-id="03101-124">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="03101-125">Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="03101-125">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="03101-126">Aşağıdaki kod, gizli diziyi dışarı aktarmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="03101-126">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="03101-127">Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="03101-127">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="03101-128">Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir.</span><span class="sxs-lookup"><span data-stu-id="03101-128">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="03101-129">Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="03101-129">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="03101-130">Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="03101-130">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="03101-131">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-131">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03101-132">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="03101-132">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="03101-133">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="03101-133">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="03101-134">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="03101-134">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03101-135">Sertifika tabanlı kimlik doğrulaması hizmet sorumlusu oluşturulurken atanan varsayılan bir rol yoktur.</span><span class="sxs-lookup"><span data-stu-id="03101-135">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="03101-136">Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="03101-136">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="03101-137">Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="03101-137">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="03101-138">Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="03101-138">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="03101-139">Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="03101-139">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="03101-140">Ortak sertifikanın ikili kodlamaları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="03101-140">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="03101-141">Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="03101-141">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="03101-142">`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-142">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="03101-143">Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03101-143">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="03101-144">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-144">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="03101-145">Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="03101-145">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03101-146">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="03101-146">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="03101-147">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="03101-147">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="03101-148">Mevcut bir hizmet sorumlusunu alma</span><span class="sxs-lookup"><span data-stu-id="03101-148">Get an existing service principal</span></span>

<span data-ttu-id="03101-149">Etkin kiracı için hizmet sorumlularının listesini [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-149">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="03101-150">Bu komut, varsayılan olarak bir kiracıdaki _tüm_ hizmet sorumlularını döndürür.</span><span class="sxs-lookup"><span data-stu-id="03101-150">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="03101-151">Büyük kuruluşlarda sonuçların döndürülmesi uzun sürebilir.</span><span class="sxs-lookup"><span data-stu-id="03101-151">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="03101-152">Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:</span><span class="sxs-lookup"><span data-stu-id="03101-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="03101-153">`-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister.</span><span class="sxs-lookup"><span data-stu-id="03101-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="03101-154">Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.</span><span class="sxs-lookup"><span data-stu-id="03101-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="03101-155">`-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.</span><span class="sxs-lookup"><span data-stu-id="03101-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="03101-156">Hizmet sorumlusu rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="03101-156">Manage service principal roles</span></span>

<span data-ttu-id="03101-157">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:</span><span class="sxs-lookup"><span data-stu-id="03101-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="03101-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="03101-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="03101-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="03101-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="03101-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="03101-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="03101-161">Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan**’dır.</span><span class="sxs-lookup"><span data-stu-id="03101-161">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="03101-162">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="03101-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="03101-163">**Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="03101-163">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="03101-164">Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="03101-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="03101-165">Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:</span><span class="sxs-lookup"><span data-stu-id="03101-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="03101-166">Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz.</span><span class="sxs-lookup"><span data-stu-id="03101-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="03101-167">Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar.</span><span class="sxs-lookup"><span data-stu-id="03101-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="03101-168">Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.</span><span class="sxs-lookup"><span data-stu-id="03101-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="03101-169">Hesabınızın rol atama izni yoksa hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız.</span><span class="sxs-lookup"><span data-stu-id="03101-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="03101-170">Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="03101-170">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="03101-171">Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_.</span><span class="sxs-lookup"><span data-stu-id="03101-171">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="03101-172">Bir hizmet sorumlusunun izinlerini kısıtlarken **Katkıda Bulunan** rolü kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03101-172">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="03101-173">Atanan roller listelenerek değişiklikler doğrulanabilir:</span><span class="sxs-lookup"><span data-stu-id="03101-173">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="03101-174">Hizmet sorumlusu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="03101-174">Sign in using a service principal</span></span>

<span data-ttu-id="03101-175">Oturum açarak yeni hizmet sorumlusunun kimlik bilgilerini ve izinlerini test edin.</span><span class="sxs-lookup"><span data-stu-id="03101-175">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="03101-176">Hizmet sorumlusu ile oturum açmak için, hizmet sorumlusuyla ilişkilendirilen `applicationId` değeri ve altında oluşturulduğu kiracı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="03101-176">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="03101-177">Hizmet sorumlusunda parola kullanarak oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="03101-177">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="03101-178">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="03101-178">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="03101-179">Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="03101-179">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="03101-180">Kimlik bilgilerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="03101-180">Reset credentials</span></span>

<span data-ttu-id="03101-181">Hizmet sorumlusunun kimlik bilgilerini unutursanız rastgele bir parola ile yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın.</span><span class="sxs-lookup"><span data-stu-id="03101-181">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="03101-182">Bu cmdlet, parola sıfırlanırken kullanıcı tanımlı kimlik bilgilerini desteklemez.</span><span class="sxs-lookup"><span data-stu-id="03101-182">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03101-183">Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="03101-184">Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:</span><span class="sxs-lookup"><span data-stu-id="03101-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="03101-185">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="03101-185">Troubleshooting</span></span>

<span data-ttu-id="03101-186">Şu hatayı alırsanız: _“New-AzADServicePrincipal: identifierUris özelliğine yönelik aynı değere sahip başka bir nesne zaten var.”_ aynı ada sahip başka bir hizmet sorumlusunun zaten mevcut olup olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="03101-186">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_, verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="03101-187">Mevcut hizmet sorumlusu artık gerekmiyorsa bunu aşağıdaki örneği kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-187">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="03101-188">Ayrıca, önceden Azure Active Directory uygulaması için bir hizmet sorumlusu oluşturduysanız bu hatayla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-188">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="03101-189">Hizmet sorumlusunu kaldırsanız da uygulama kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="03101-189">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="03101-190">Bu uygulama, aynı ada sahip başka bir hizmet sorumlusu oluşturmanızı engeller.</span><span class="sxs-lookup"><span data-stu-id="03101-190">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="03101-191">Aynı ada sahip başka bir Azure Active Directory uygulaması olup olmadığını doğrulamak için aşağıdaki örneği kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="03101-191">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="03101-192">Aynı ada sahip başka bir uygulama varsa ve artık bu uygulamaya ihtiyaç duymuyorsanız aşağıdaki örneği kullanarak bunu kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03101-192">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="03101-193">Bu uygulamaya ihtiyaç duyuyorsanız oluşturmayı denediğiniz yeni hizmet sorumlusu için alternatif bir ad seçin.</span><span class="sxs-lookup"><span data-stu-id="03101-193">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>