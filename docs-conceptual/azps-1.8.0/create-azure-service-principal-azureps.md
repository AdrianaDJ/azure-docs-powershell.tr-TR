---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 65cf13200c46a955762f4c92b6822033a3723aa8
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408805"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="59f0d-103">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="59f0d-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="59f0d-104">Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="59f0d-105">Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.</span><span class="sxs-lookup"><span data-stu-id="59f0d-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="59f0d-106">Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="59f0d-107">Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="59f0d-108">Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="59f0d-109">Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

> [!WARNING]
> <span data-ttu-id="59f0d-110">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) komutunu kullanarak hizmet sorumlusu oluşturduğunuzda, çıkışta korumanız gereken kimlik bilgileri yer alır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-110">When you create a service principal using the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="59f0d-111">Bu kimlik bilgilerini kodunuza eklemediğinizden emin olun veya kaynak denetiminizdeki kimlik bilgilerini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="59f0d-111">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="59f0d-112">Alternatif olarak, kimlik bilgilerini kullanma gereksinimini ortadan kaldırmak için [yönetilen kimlikleri](/azure/active-directory/managed-identities-azure-resources/overview) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-112">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="59f0d-113">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) varsayılan olarak [Katkıda bulunan](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamında hizmet sorumlusuna atar.</span><span class="sxs-lookup"><span data-stu-id="59f0d-113">By default, [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="59f0d-114">Güvenliği ihlal edilmiş hizmet sorumlusu riskinizi azaltmak için daha belirli bir rol atayın ve kapsamı kaynağa ya da kaynak grubuna daraltın.</span><span class="sxs-lookup"><span data-stu-id="59f0d-114">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="59f0d-115">Daha fazla bilgi için bkz. [Rol ataması ekleme adımları](/azure/role-based-access-control/role-assignments-steps).</span><span class="sxs-lookup"><span data-stu-id="59f0d-115">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="59f0d-116">Hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="59f0d-116">Create a service principal</span></span>

<span data-ttu-id="59f0d-117">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59f0d-117">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="59f0d-118">Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-118">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="59f0d-119">Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="59f0d-119">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="59f0d-120">Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="59f0d-120">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="59f0d-121">Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="59f0d-121">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="59f0d-122">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="59f0d-122">Password-based authentication</span></span>

<span data-ttu-id="59f0d-123">Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="59f0d-123">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="59f0d-124">Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-124">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="59f0d-125">Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-125">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="59f0d-126">Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="59f0d-126">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="59f0d-127">Değeri, konsol çıkışında __görüntülenmez__.</span><span class="sxs-lookup"><span data-stu-id="59f0d-127">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="59f0d-128">Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="59f0d-128">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="59f0d-129">Aşağıdaki kod, gizli diziyi dışarı aktarmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="59f0d-129">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="59f0d-130">Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-130">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="59f0d-131">Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-131">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="59f0d-132">Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="59f0d-132">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="59f0d-133">Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="59f0d-133">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="59f0d-134">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-134">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="59f0d-135">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-135">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="59f0d-136">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="59f0d-136">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="59f0d-137">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="59f0d-137">Certificate-based authentication</span></span>

<span data-ttu-id="59f0d-138">Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="59f0d-138">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="59f0d-139">Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-139">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="59f0d-140">Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-140">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="59f0d-141">Ortak sertifikanın ikili kodlamaları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="59f0d-141">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="59f0d-142">Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="59f0d-142">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="59f0d-143">`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-143">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="59f0d-144">Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-144">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="59f0d-145">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-145">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="59f0d-146">Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-146">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="59f0d-147">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-147">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="59f0d-148">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="59f0d-148">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="59f0d-149">Mevcut bir hizmet sorumlusunu alma</span><span class="sxs-lookup"><span data-stu-id="59f0d-149">Get an existing service principal</span></span>

<span data-ttu-id="59f0d-150">[Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile şu anda etkin kiracı için hizmet sorumlularının listesini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-150">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="59f0d-151">Varsayılan olarak bu komut, kiracıda yer alan __tüm__ hizmet sorumlularını döndürür. Bu yüzden, büyük kuruluşlar için sonuçların döndürülmesi uzun sürebilir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-151">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="59f0d-152">Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:</span><span class="sxs-lookup"><span data-stu-id="59f0d-152">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="59f0d-153">`-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister.</span><span class="sxs-lookup"><span data-stu-id="59f0d-153">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="59f0d-154">Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-154">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="59f0d-155">`-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.</span><span class="sxs-lookup"><span data-stu-id="59f0d-155">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="59f0d-156">Hizmet sorumlusu rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="59f0d-156">Manage service principal roles</span></span>

<span data-ttu-id="59f0d-157">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:</span><span class="sxs-lookup"><span data-stu-id="59f0d-157">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="59f0d-158">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59f0d-158">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="59f0d-159">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59f0d-159">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="59f0d-160">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59f0d-160">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="59f0d-161">Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan** ’dır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-161">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="59f0d-162">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-162">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="59f0d-163">**Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-163">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="59f0d-164">Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="59f0d-164">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="59f0d-165">Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:</span><span class="sxs-lookup"><span data-stu-id="59f0d-165">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="59f0d-166">Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-166">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="59f0d-167">Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar.</span><span class="sxs-lookup"><span data-stu-id="59f0d-167">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="59f0d-168">Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.</span><span class="sxs-lookup"><span data-stu-id="59f0d-168">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="59f0d-169">Hesabınızın rol atama izni yoksa, hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız. Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="59f0d-169">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="59f0d-170">Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_.</span><span class="sxs-lookup"><span data-stu-id="59f0d-170">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="59f0d-171">Bir hizmet sorumlusunun izinlerini kısıtlarken __Katkıda Bulunan__ rolü kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-171">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="59f0d-172">Atanan roller listelenerek değişiklikler doğrulanabilir:</span><span class="sxs-lookup"><span data-stu-id="59f0d-172">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="59f0d-173">Hizmet sorumlusu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="59f0d-173">Sign in using a service principal</span></span>

<span data-ttu-id="59f0d-174">Oturum açarak yeni hizmet sorumlusunun kimlik bilgilerini ve izinlerini test edin.</span><span class="sxs-lookup"><span data-stu-id="59f0d-174">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="59f0d-175">Hizmet sorumlusu ile oturum açmak için, hizmet sorumlusuyla ilişkilendirilen `applicationId` değeri ve altında oluşturulduğu kiracı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-175">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="59f0d-176">Hizmet sorumlusunda parola kullanarak oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="59f0d-176">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="59f0d-177">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="59f0d-177">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="59f0d-178">Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="59f0d-178">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="59f0d-179">Kimlik bilgilerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="59f0d-179">Reset credentials</span></span>

<span data-ttu-id="59f0d-180">Hizmet sorumlusunun kimlik bilgilerini unutursanız yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın.</span><span class="sxs-lookup"><span data-stu-id="59f0d-180">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="59f0d-181">Bu cmdlet, `New-AzADServicePrincipal` ile aynı kimlik bilgileri bağımsız değişkenlerini ve türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="59f0d-181">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="59f0d-182">Kimlik bilgileri bağımsız değişkenleri olmadan, rastgele parola ile yeni bir `PasswordCredential` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="59f0d-182">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59f0d-183">Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59f0d-183">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="59f0d-184">Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:</span><span class="sxs-lookup"><span data-stu-id="59f0d-184">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
