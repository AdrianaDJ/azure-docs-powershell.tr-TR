---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 4c47d2bac2c63f13ac0ebbccda3e2eed12cd658f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740023"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="2420a-103">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="2420a-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="2420a-104">Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2420a-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="2420a-105">Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.</span><span class="sxs-lookup"><span data-stu-id="2420a-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="2420a-106">Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir.</span><span class="sxs-lookup"><span data-stu-id="2420a-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="2420a-107">Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="2420a-108">Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="2420a-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="2420a-109">Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2420a-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="2420a-110">Hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="2420a-110">Create a service principal</span></span>

<span data-ttu-id="2420a-111">[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2420a-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="2420a-112">Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="2420a-113">Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür.</span><span class="sxs-lookup"><span data-stu-id="2420a-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="2420a-114">Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="2420a-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="2420a-115">Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.</span><span class="sxs-lookup"><span data-stu-id="2420a-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="2420a-116">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="2420a-116">Password-based authentication</span></span>

<span data-ttu-id="2420a-117">Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2420a-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="2420a-118">Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.</span><span class="sxs-lookup"><span data-stu-id="2420a-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="2420a-119">Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir.</span><span class="sxs-lookup"><span data-stu-id="2420a-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="2420a-120">Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2420a-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="2420a-121">Değeri, konsol çıkışında __görüntülenmez__.</span><span class="sxs-lookup"><span data-stu-id="2420a-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="2420a-122">Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="2420a-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="2420a-123">Aşağıdaki kod, gizli diziyi dışarı aktarmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="2420a-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="2420a-124">Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2420a-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="2420a-125">Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir.</span><span class="sxs-lookup"><span data-stu-id="2420a-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="2420a-126">Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2420a-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="2420a-127">Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="2420a-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="2420a-128">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2420a-129">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="2420a-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="2420a-130">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="2420a-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="2420a-131">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="2420a-131">Certificate-based authentication</span></span>

<span data-ttu-id="2420a-132">Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2420a-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="2420a-133">Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="2420a-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="2420a-134">Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="2420a-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="2420a-135">Ortak sertifikanın ikili kodlamaları desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="2420a-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="2420a-136">Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="2420a-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="2420a-137">`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="2420a-138">Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2420a-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="2420a-139">`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="2420a-140">Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="2420a-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2420a-141">Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir.</span><span class="sxs-lookup"><span data-stu-id="2420a-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="2420a-142">Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="2420a-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="2420a-143">Mevcut bir hizmet sorumlusunu alma</span><span class="sxs-lookup"><span data-stu-id="2420a-143">Get an existing service principal</span></span>

<span data-ttu-id="2420a-144">[Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile şu anda etkin kiracı için hizmet sorumlularının listesini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="2420a-145">Varsayılan olarak bu komut, kiracıda yer alan __tüm__ hizmet sorumlularını döndürür. Bu yüzden, büyük kuruluşlar için sonuçların döndürülmesi uzun sürebilir.</span><span class="sxs-lookup"><span data-stu-id="2420a-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="2420a-146">Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:</span><span class="sxs-lookup"><span data-stu-id="2420a-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="2420a-147">`-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister.</span><span class="sxs-lookup"><span data-stu-id="2420a-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="2420a-148">Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.</span><span class="sxs-lookup"><span data-stu-id="2420a-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="2420a-149">`-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.</span><span class="sxs-lookup"><span data-stu-id="2420a-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="2420a-150">Hizmet sorumlusu rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="2420a-150">Manage service principal roles</span></span>

<span data-ttu-id="2420a-151">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:</span><span class="sxs-lookup"><span data-stu-id="2420a-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="2420a-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2420a-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="2420a-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2420a-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="2420a-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2420a-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="2420a-155">Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan**’dır.</span><span class="sxs-lookup"><span data-stu-id="2420a-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="2420a-156">Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2420a-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="2420a-157">**Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2420a-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="2420a-158">Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="2420a-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="2420a-159">Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:</span><span class="sxs-lookup"><span data-stu-id="2420a-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="2420a-160">Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz.</span><span class="sxs-lookup"><span data-stu-id="2420a-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="2420a-161">Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar.</span><span class="sxs-lookup"><span data-stu-id="2420a-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="2420a-162">Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.</span><span class="sxs-lookup"><span data-stu-id="2420a-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="2420a-163">Hesabınızın rol atama izni yoksa, hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız. Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="2420a-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="2420a-164">Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_.</span><span class="sxs-lookup"><span data-stu-id="2420a-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="2420a-165">Bir hizmet sorumlusunun izinlerini kısıtlarken __Katkıda Bulunan__ rolü kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2420a-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="2420a-166">Atanan roller listelenerek değişiklikler doğrulanabilir:</span><span class="sxs-lookup"><span data-stu-id="2420a-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="2420a-167">Hizmet sorumlusu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="2420a-167">Sign in using a service principal</span></span>

<span data-ttu-id="2420a-168">Oturum açarak yeni hizmet sorumlusunun kimlik bilgilerini ve izinlerini test edin.</span><span class="sxs-lookup"><span data-stu-id="2420a-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="2420a-169">Hizmet sorumlusu ile oturum açmak için, hizmet sorumlusuyla ilişkilendirilen `applicationId` değeri ve altında oluşturulduğu kiracı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2420a-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="2420a-170">Hizmet sorumlusunda parola kullanarak oturum açmak için:</span><span class="sxs-lookup"><span data-stu-id="2420a-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="2420a-171">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2420a-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <tenant ID> -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="2420a-172">Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)</span><span class="sxs-lookup"><span data-stu-id="2420a-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="2420a-173">Kimlik bilgilerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="2420a-173">Reset credentials</span></span>

<span data-ttu-id="2420a-174">Hizmet sorumlusunun kimlik bilgilerini unutursanız yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın.</span><span class="sxs-lookup"><span data-stu-id="2420a-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="2420a-175">Bu cmdlet, `New-AzADServicePrincipal` ile aynı kimlik bilgileri bağımsız değişkenlerini ve türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2420a-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="2420a-176">Kimlik bilgileri bağımsız değişkenleri olmadan, rastgele parola ile yeni bir `PasswordCredential` oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2420a-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2420a-177">Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2420a-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="2420a-178">Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:</span><span class="sxs-lookup"><span data-stu-id="2420a-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
