---
title: Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma
description: Azure PowerShell ile uygulamanız veya hizmetiniz için nasıl hizmet sorumlusu oluşturabileceğinizi öğrenin.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342195"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="42356-104">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="42356-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="42356-105">Uygulamanızı veya hizmetinizi Azure PowerShell ile yönetmeyi planlıyorsanız, uygulamanızı kendi kimlik bilgileriniz altında değil bir Azure Active Directory (AAD) hizmet sorumlusu altında çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="42356-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="42356-106">Bu makalede, Azure PowerShell ile bir güvenlik sorumlusu oluşturma işlemi adım adım gösterilir.</span><span class="sxs-lookup"><span data-stu-id="42356-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="42356-107">Hizmet sorumlusu nedir?</span><span class="sxs-lookup"><span data-stu-id="42356-107">What is a service principal?</span></span>

<span data-ttu-id="42356-108">Azure hizmet sorumlusu, kullanıcı tarafından oluşturulan uygulamalar, hizmetler ve otomasyon araçlarının belirli Azure kaynaklarına erişmek için kullandığı bir güvenlik kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="42356-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="42356-109">Hizmet sorumlularına görevlerine özel izinler atanır ve bu sayede güvenlik üzerinde daha iyi denetime sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="42356-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="42356-110">Genellikle her tür değişikliği yapma yetkisine sahip olan genel bir kullanıcı kimliğinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="42356-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="42356-111">Kendi izin düzeyinizi doğrulama</span><span class="sxs-lookup"><span data-stu-id="42356-111">Verify your own permission level</span></span>

<span data-ttu-id="42356-112">Öncelikle hem Azure Active Directory’nizde hem de Azure aboneliğinizde yeterli izinlere sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="42356-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="42356-113">Active Directory’de uygulama oluşturabilmeniz ve hizmet sorumlusuna rol atayabilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="42356-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="42356-114">Hesabınızın doğru izinlere sahip olup olmadığını denetlemenin en kolay yolu portalı kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="42356-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="42356-115">Bkz. [Portalda gerekli izinleri denetleme](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="42356-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="42356-116">Uygulamanız için hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="42356-116">Create a service principal for your app</span></span>

<span data-ttu-id="42356-117">Azure hesabınızda oturum açıldıktan sonra hizmet sorumlusunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42356-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="42356-118">Dağıtılan uygulamanızı tanımlamak için aşağıdaki yollardan birine sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="42356-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="42356-119">Dağıtılan uygulamanızın benzersiz adı (aşağıdaki örneklerde yer alan "MyDemoWebApp" gibi)</span><span class="sxs-lookup"><span data-stu-id="42356-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="42356-120">Uygulama Kimliği, yani dağıtılan uygulama, hizmet veya nesnenizle ilişkili benzersiz GUID</span><span class="sxs-lookup"><span data-stu-id="42356-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="42356-121">Uygulamanız ile ilgili bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="42356-121">Get information about your application</span></span>

<span data-ttu-id="42356-122">Uygulamanızla ilgili bilgileri almak için `Get-AzADApplication` cmdlet’ini kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42356-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="42356-123">Uygulamanız için hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="42356-123">Create a service principal for your application</span></span>

<span data-ttu-id="42356-124">Hizmet sorumlusunu oluşturmak için `New-AzADServicePrincipal` cmdlet’i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="42356-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="42356-125">Bundan sonra, `$servicePrincipal.Secret` özelliğini `Connect-AzAccount` için bir bağımsız değişken olarak doğrudan kullanabilir (bkz. "Hizmet sorumlusunu kullanarak oturum açma") veya `SecureString` dizesini düz metin dizesine dönüştürebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="42356-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="42356-126">Hizmet sorumlusunu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="42356-126">Sign in using the service principal</span></span>

<span data-ttu-id="42356-127">Artık sağladığınız `appId` ve oluşturulan `password` ile uygulamanızın yeni hizmet sorumlusu olarak oturum</span><span class="sxs-lookup"><span data-stu-id="42356-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="42356-128">açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42356-128">generated.</span></span> <span data-ttu-id="42356-129">Hizmet sorumlusu için Kiracı Kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="42356-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="42356-130">Kiracı Kimliğiniz, Azure’da kişisel kimlik bilgilerinizle oturum açtığınızda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="42356-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="42356-131">Hizmet sorumlusuyla oturum açmak için şu komutları kullanın:</span><span class="sxs-lookup"><span data-stu-id="42356-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="42356-132">Başarılı bir oturum açma işleminden sonra şöyle bir çıkış görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="42356-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="42356-133">Tebrikler!</span><span class="sxs-lookup"><span data-stu-id="42356-133">Congratulations!</span></span> <span data-ttu-id="42356-134">Uygulamanızı çalıştırmak için bu kimlik bilgilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42356-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="42356-135">Ardından, hizmet sorumlusunun izinlerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="42356-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="42356-136">Rolleri yönetme</span><span class="sxs-lookup"><span data-stu-id="42356-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="42356-137">Azure Rol Tabanlı Erişim Denetimi (RBAC), kullanıcı ve hizmet sorumlularının rollerini tanımlama ve yönetmeye yönelik bir modeldir.</span><span class="sxs-lookup"><span data-stu-id="42356-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="42356-138">Rollerin kendileriyle ilişkili izin kümeleri vardır ve bir sorumlunun okuyabileceği, erişebileceği, yazabileceği ya da yönetebileceği kaynakları bunlar belirler.</span><span class="sxs-lookup"><span data-stu-id="42356-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="42356-139">RBAC ve roller hakkında daha fazla bilgi edinmek için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="42356-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="42356-140">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri sunar:</span><span class="sxs-lookup"><span data-stu-id="42356-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="42356-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="42356-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="42356-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="42356-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="42356-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="42356-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="42356-144">Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan**’dır.</span><span class="sxs-lookup"><span data-stu-id="42356-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="42356-145">Geniş izinleri göz önünde bulundurulduğunda, uygulamanızın Azure hizmetleriyle gerçekleştirdiği etkileşimlerin kapsamına bağlı olarak, doğru bir seçim olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="42356-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="42356-146">**Okuyucu** rolü daha kısıtlayıcıdır ve salt okunur uygulamalar için iyi bir seçim olabilir.</span><span class="sxs-lookup"><span data-stu-id="42356-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="42356-147">Azure portalı aracılığıyla role özel izinlerin ayrıntılarını görüntüleyebilir veya özel roller oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42356-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="42356-148">Bu örnekte, bir önceki örneğimize **Okuyucu** rolünü ekleyip **Katkıda Bulunan** rolünü siliyoruz:</span><span class="sxs-lookup"><span data-stu-id="42356-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="42356-149">Şu anda atanmış olan rolleri görüntülemek için:</span><span class="sxs-lookup"><span data-stu-id="42356-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="42356-150">Rol yönetimi için diğer Azure PowerShell cmdlet’leri:</span><span class="sxs-lookup"><span data-stu-id="42356-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="42356-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42356-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="42356-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42356-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="42356-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42356-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="42356-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42356-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="42356-155">Güvenlik sorumlusunun kimlik bilgilerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="42356-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="42356-156">Düzenli aralıklarla izinleri gözden geçirmek ve parolayı güncelleştirmek, güvenlik açısından iyi bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="42356-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="42356-157">Uygulamanız değiştikçe güvenlik kimlik bilgilerini yönetmek ve değiştirmek de isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42356-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="42356-158">Örneğin, yeni bir parola oluşturup eskisini kaldırarak hizmet sorumlusunun parolasını değiştirebiliriz.</span><span class="sxs-lookup"><span data-stu-id="42356-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="42356-159">Hizmet sorumlusu için yeni parola ekleme</span><span class="sxs-lookup"><span data-stu-id="42356-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="42356-160">Hizmet sorumlusunun kimlik bilgilerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="42356-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="42356-161">Hizmet sorumlusundan eski parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="42356-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="42356-162">Hizmet sorumlusunun kimlik bilgileri listesini doğrulama</span><span class="sxs-lookup"><span data-stu-id="42356-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="42356-163">Hizmet sorumlusuyla ilgili bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="42356-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
