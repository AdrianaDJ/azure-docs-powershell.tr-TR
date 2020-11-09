---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20a58253e3f9435a9d33c700435f77fbb42df7ea
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365118"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="06001-103">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="06001-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="06001-104">Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="06001-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="06001-105">Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.</span><span class="sxs-lookup"><span data-stu-id="06001-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="06001-106">Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir.</span><span class="sxs-lookup"><span data-stu-id="06001-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="06001-107">Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="06001-108">Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="06001-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="06001-109">Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06001-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="06001-110">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) komutunu kullanarak hizmet sorumlusu oluşturduğunuzda, çıkışta korumanız gereken kimlik bilgileri yer alır.</span><span class="sxs-lookup"><span data-stu-id="06001-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="06001-111">Bu kimlik bilgilerini kodunuza eklemediğinizden emin olun veya kaynak denetiminizdeki kimlik bilgilerini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="06001-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="06001-112">Alternatif olarak, kimlik bilgilerini kullanma gereksinimini ortadan kaldırmak için [yönetilen kimlikleri](/azure/active-directory/managed-identities-azure-resources/overview) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="06001-113">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) varsayılan olarak [Katkıda bulunan](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamında hizmet sorumlusuna atar.</span><span class="sxs-lookup"><span data-stu-id="06001-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="06001-114">Güvenliği ihlal edilmiş hizmet sorumlusu riskinizi azaltmak için daha belirli bir rol atayın ve kapsamı kaynağa ya da kaynak grubuna daraltın.</span><span class="sxs-lookup"><span data-stu-id="06001-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="06001-115">Daha fazla bilgi için bkz. [Rol ataması ekleme adımları](/azure/role-based-access-control/role-assignments-steps).</span><span class="sxs-lookup"><span data-stu-id="06001-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="06001-116">Hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="06001-116">Create a service principal</span></span>

<span data-ttu-id="06001-117">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06001-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="06001-118">Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
> <span data-ttu-id="06001-119">Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="06001-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation".</span></span>
> <span data-ttu-id="06001-120">Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="06001-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="06001-121">Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="06001-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="06001-122">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="06001-122">Password-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06001-123">Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan** ’dır.</span><span class="sxs-lookup"><span data-stu-id="06001-123">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="06001-124">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="06001-124">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="06001-125">Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="06001-125">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="06001-126">Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="06001-126">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="06001-127">Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.</span><span class="sxs-lookup"><span data-stu-id="06001-127">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="06001-128">Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir.</span><span class="sxs-lookup"><span data-stu-id="06001-128">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="06001-129">Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="06001-129">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="06001-130">Değeri, konsol çıkışında _görüntülenmez_.</span><span class="sxs-lookup"><span data-stu-id="06001-130">Its value _won't_ be displayed in the console output.</span></span> <span data-ttu-id="06001-131">Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="06001-131">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="06001-132">Aşağıdaki kod, gizli diziyi dışarı aktarmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="06001-132">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="06001-133">Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="06001-133">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="06001-134">Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir.</span><span class="sxs-lookup"><span data-stu-id="06001-134">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="06001-135">Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="06001-135">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span>
<span data-ttu-id="06001-136">Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="06001-136">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="06001-137">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-137">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06001-138">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="06001-138">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="06001-139">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="06001-139">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a><span data-ttu-id="06001-140">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="06001-140">Certificate-based authentication</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06001-141">Sertifika tabanlı kimlik doğrulaması hizmet sorumlusu oluşturulurken atanan varsayılan bir rol yoktur.</span><span class="sxs-lookup"><span data-stu-id="06001-141">There is no default role assigned when creating a certificate-based authentication service principal.</span></span> <span data-ttu-id="06001-142">Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).</span><span class="sxs-lookup"><span data-stu-id="06001-142">For information on managing role assignments, see [Manage service principal roles](#manage-service-principal-roles).</span></span>

<span data-ttu-id="06001-143">Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="06001-143">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="06001-144">Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="06001-144">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="06001-145">Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="06001-145">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="06001-146">Ortak sertifikanın ikili kodlamaları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="06001-146">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="06001-147">Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="06001-147">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="06001-148">`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-148">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="06001-149">Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="06001-149">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="06001-150">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-150">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="06001-151">Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="06001-151">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06001-152">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="06001-152">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="06001-153">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="06001-153">To get the active tenant when the service principal was created, run the following command _immediately after_ service principal creation:</span></span>

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="06001-154">Mevcut bir hizmet sorumlusunu alma</span><span class="sxs-lookup"><span data-stu-id="06001-154">Get an existing service principal</span></span>

<span data-ttu-id="06001-155">Etkin kiracı için hizmet sorumlularının listesini [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-155">A list of service principals for the active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="06001-156">Bu komut, varsayılan olarak bir kiracıdaki _tüm_ hizmet sorumlularını döndürür.</span><span class="sxs-lookup"><span data-stu-id="06001-156">By default this command returns _all_ service principals in a tenant.</span></span> <span data-ttu-id="06001-157">Büyük kuruluşlarda sonuçların döndürülmesi uzun sürebilir.</span><span class="sxs-lookup"><span data-stu-id="06001-157">For large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="06001-158">Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:</span><span class="sxs-lookup"><span data-stu-id="06001-158">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

- <span data-ttu-id="06001-159">`-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister.</span><span class="sxs-lookup"><span data-stu-id="06001-159">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="06001-160">Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.</span><span class="sxs-lookup"><span data-stu-id="06001-160">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
- <span data-ttu-id="06001-161">`-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.</span><span class="sxs-lookup"><span data-stu-id="06001-161">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="06001-162">Hizmet sorumlusu rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="06001-162">Manage service principal roles</span></span>

<span data-ttu-id="06001-163">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:</span><span class="sxs-lookup"><span data-stu-id="06001-163">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

- [<span data-ttu-id="06001-164">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06001-164">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
- [<span data-ttu-id="06001-165">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06001-165">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
- [<span data-ttu-id="06001-166">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06001-166">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="06001-167">Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan** ’dır.</span><span class="sxs-lookup"><span data-stu-id="06001-167">The default role for a password-based authentication service principal is **Contributor**.</span></span> <span data-ttu-id="06001-168">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="06001-168">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="06001-169">**Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="06001-169">The **Reader** role is more restrictive, with read-only access.</span></span> <span data-ttu-id="06001-170">Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="06001-170">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="06001-171">Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:</span><span class="sxs-lookup"><span data-stu-id="06001-171">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> <span data-ttu-id="06001-172">Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz.</span><span class="sxs-lookup"><span data-stu-id="06001-172">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="06001-173">Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar.</span><span class="sxs-lookup"><span data-stu-id="06001-173">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="06001-174">Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.</span><span class="sxs-lookup"><span data-stu-id="06001-174">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="06001-175">Hesabınızın rol atama izni yoksa hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız.</span><span class="sxs-lookup"><span data-stu-id="06001-175">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'".</span></span> <span data-ttu-id="06001-176">Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="06001-176">Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="06001-177">Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_.</span><span class="sxs-lookup"><span data-stu-id="06001-177">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="06001-178">Bir hizmet sorumlusunun izinlerini kısıtlarken **Katkıda Bulunan** rolü kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="06001-178">When restricting a service principal's permissions, the **Contributor** role should be removed.</span></span>

<span data-ttu-id="06001-179">Atanan roller listelenerek değişiklikler doğrulanabilir:</span><span class="sxs-lookup"><span data-stu-id="06001-179">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="06001-180">Hizmet sorumlusu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="06001-180">Sign in using a service principal</span></span>

<span data-ttu-id="06001-181">Oturum açarak yeni hizmet sorumlusunun kimlik bilgilerini ve izinlerini test edin.</span><span class="sxs-lookup"><span data-stu-id="06001-181">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="06001-182">Hizmet sorumlusu ile oturum açmak için, hizmet sorumlusuyla ilişkilendirilen `applicationId` değeri ve altında oluşturulduğu kiracı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="06001-182">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="06001-183">Hizmet sorumlusunda parola kullanarak oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="06001-183">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

<span data-ttu-id="06001-184">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="06001-184">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

<span data-ttu-id="06001-185">Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="06001-185">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="06001-186">Kimlik bilgilerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="06001-186">Reset credentials</span></span>

<span data-ttu-id="06001-187">Hizmet sorumlusunun kimlik bilgilerini unutursanız rastgele bir parola ile yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın.</span><span class="sxs-lookup"><span data-stu-id="06001-187">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential with a random password.</span></span> <span data-ttu-id="06001-188">Bu cmdlet, parola sıfırlanırken kullanıcı tanımlı kimlik bilgilerini desteklemez.</span><span class="sxs-lookup"><span data-stu-id="06001-188">This cmdlet does not support user-defined credentials when resetting the password.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06001-189">Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-189">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="06001-190">Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:</span><span class="sxs-lookup"><span data-stu-id="06001-190">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a><span data-ttu-id="06001-191">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="06001-191">Troubleshooting</span></span>

<span data-ttu-id="06001-192">Şu hatayı alırsanız: _“New-AzADServicePrincipal: identifierUris özelliğine yönelik aynı değere sahip başka bir nesne zaten var.”_ aynı ada sahip başka bir hizmet sorumlusunun zaten mevcut olup olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="06001-192">If you receive the error: _"New-AzADServicePrincipal: Another object with the same value for property identifierUris already exists."_ , verify that a service principal with the same name doesn't already exist.</span></span>

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="06001-193">Mevcut hizmet sorumlusu artık gerekmiyorsa bunu aşağıdaki örneği kullanarak kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-193">If the existing service principal is no longer needed, you can remove it using the following example.</span></span>

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="06001-194">Ayrıca, önceden Azure Active Directory uygulaması için bir hizmet sorumlusu oluşturduysanız bu hatayla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-194">This error can also occur when you've previously created a service principal for an Azure Active Directory application.</span></span> <span data-ttu-id="06001-195">Hizmet sorumlusunu kaldırsanız da uygulama kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="06001-195">If you remove the service principal, the application is still available.</span></span> <span data-ttu-id="06001-196">Bu uygulama, aynı ada sahip başka bir hizmet sorumlusu oluşturmanızı engeller.</span><span class="sxs-lookup"><span data-stu-id="06001-196">This application prevents you from creating another service principal with the same name.</span></span>

<span data-ttu-id="06001-197">Aynı ada sahip başka bir Azure Active Directory uygulaması olup olmadığını doğrulamak için aşağıdaki örneği kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="06001-197">You can use the following example to verify that an Azure Active Directory application with the same name doesn't exist:</span></span>

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="06001-198">Aynı ada sahip başka bir uygulama varsa ve artık bu uygulamaya ihtiyaç duymuyorsanız aşağıdaki örneği kullanarak bunu kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06001-198">If an application with the same name does exist and is no longer needed, it can be removed using the following example.</span></span>

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

<span data-ttu-id="06001-199">Bu uygulamaya ihtiyaç duyuyorsanız oluşturmayı denediğiniz yeni hizmet sorumlusu için alternatif bir ad seçin.</span><span class="sxs-lookup"><span data-stu-id="06001-199">Otherwise, choose an alternate name for the new service principal that you're attempting to create.</span></span>
