---
title: Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma
description: Azure PowerShell ile uygulamanız veya hizmetiniz için nasıl hizmet sorumlusu oluşturabileceğinizi öğrenin.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 433a638187f024883c177457e420a759968fed9a
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001448"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="8a786-104">Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a786-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="8a786-105">Uygulamanızı veya hizmetinizi Azure PowerShell ile yönetmeyi planlıyorsanız, uygulamanızı kendi kimlik bilgileriniz altında değil bir Azure Active Directory (AAD) hizmet sorumlusu altında çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="8a786-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="8a786-106">Bu makalede, Azure PowerShell ile bir güvenlik sorumlusu oluşturma işlemi adım adım gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8a786-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="8a786-107">Azure portalı aracılığıyla da hizmet sorumlusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="8a786-108">Daha ayrıntılı bilgi edinmek için [Kaynaklara erişebilen bir Active Directory uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](/azure/azure-resource-manager/resource-group-create-service-principal-portal) konusunu okuyun.</span><span class="sxs-lookup"><span data-stu-id="8a786-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="8a786-109">'Hizmet sorumlusu' nedir?</span><span class="sxs-lookup"><span data-stu-id="8a786-109">What is a 'service principal'?</span></span>

<span data-ttu-id="8a786-110">Azure hizmet sorumlusu, kullanıcı tarafından oluşturulan uygulamalar, hizmetler ve otomasyon araçlarının belirli Azure kaynaklarına erişmek için kullandığı bir güvenlik kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="8a786-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="8a786-111">Bunu belirli bir rolü olan ve izinleri sıkı bir şekilde denetlenen bir "kullanıcı kimliği" (kullanıcı adı ve parola veya sertifika) olarak düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="8a786-112">Genel kullanıcı kimliğinin aksine, hizmet sorumlusunun yalnızca belirli şeyleri yapabilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a786-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="8a786-113">Hizmet sorumlusuna yönetim görevlerini gerçekleştirmesi için gereken en düşük izin düzeyini atamanız, güvenliği geliştirir.</span><span class="sxs-lookup"><span data-stu-id="8a786-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="8a786-114">Kendi izin düzeyinizi doğrulama</span><span class="sxs-lookup"><span data-stu-id="8a786-114">Verify your own permission level</span></span>

<span data-ttu-id="8a786-115">Öncelikle hem Azure Active Directory’nizde hem de Azure aboneliğinizde yeterli izinlere sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a786-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="8a786-116">Active Directory’de uygulama oluşturabilmeniz ve hizmet sorumlusuna rol atayabilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a786-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="8a786-117">Hesabınızın doğru izinlere sahip olup olmadığını denetlemenin en kolay yolu portalı kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="8a786-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="8a786-118">Bkz. [Portalda gerekli izinleri denetleme](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="8a786-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="8a786-119">Uygulamanız için hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a786-119">Create a service principal for your app</span></span>

<span data-ttu-id="8a786-120">Azure hesabınızda oturum açıldıktan sonra hizmet sorumlusunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="8a786-121">Dağıtılan uygulamanızı tanımlamak için aşağıdaki yollardan birine sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="8a786-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="8a786-122">Dağıtılan uygulamanızın benzersiz adı (aşağıdaki örneklerde yer alan "MyDemoWebApp" gibi) veya</span><span class="sxs-lookup"><span data-stu-id="8a786-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="8a786-123">Uygulama Kimliği, yani dağıtılan uygulama, hizmet veya nesnenizle ilişkili benzersiz GUID</span><span class="sxs-lookup"><span data-stu-id="8a786-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="8a786-124">Uygulamanız ile ilgili bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="8a786-124">Get information about your application</span></span>

<span data-ttu-id="8a786-125">Uygulamanızla ilgili bilgileri almak için `Get-AzureRmADApplication` cmdlet’ini kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8a786-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="8a786-126">Uygulamanız için hizmet sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a786-126">Create a service principal for your application</span></span>

<span data-ttu-id="8a786-127">Hizmet sorumlusunu oluşturmak için `New-AzureRmADServicePrincipal` cmdlet’i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8a786-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="8a786-128">Hizmet sorumlusuyla ilgili bilgi edinme</span><span class="sxs-lookup"><span data-stu-id="8a786-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="8a786-129">Hizmet sorumlusunu kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="8a786-129">Sign in using the service principal</span></span>

<span data-ttu-id="8a786-130">Artık sağladığınız *appId* ve *parola* ile uygulamanızın yeni hizmet sorumlusu olarak oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="8a786-131">Hizmet sorumlusu için Kiracı Kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="8a786-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="8a786-132">Kiracı Kimliğiniz, Azure’da kişisel kimlik bilgilerinizle oturum açtığınızda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8a786-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="8a786-133">Hizmet sorumlusuyla oturum açmak için aşağıdaki komutları kullanın:</span><span class="sxs-lookup"><span data-stu-id="8a786-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="8a786-134">Başarılı bir oturum açma işleminden sonra şöyle bir çıkış görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="8a786-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="8a786-135">Tebrikler!</span><span class="sxs-lookup"><span data-stu-id="8a786-135">Congratulations!</span></span> <span data-ttu-id="8a786-136">Uygulamanızı çalıştırmak için bu kimlik bilgilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="8a786-137">Ardından, hizmet sorumlusunun izinlerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8a786-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="8a786-138">Rolleri yönetme</span><span class="sxs-lookup"><span data-stu-id="8a786-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="8a786-139">Azure Rol Tabanlı Erişim Denetimi (RBAC), kullanıcı ve hizmet sorumlularının rollerini tanımlama ve yönetmeye yönelik bir modeldir.</span><span class="sxs-lookup"><span data-stu-id="8a786-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="8a786-140">Rollerin kendileriyle ilişkili izin kümeleri vardır ve bir sorumlunun okuyabileceği, erişebileceği, yazabileceği ya da yönetebileceği kaynakları bunlar belirler.</span><span class="sxs-lookup"><span data-stu-id="8a786-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="8a786-141">RBAC ve roller hakkında daha fazla bilgi edinmek için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="8a786-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="8a786-142">Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri sunar:</span><span class="sxs-lookup"><span data-stu-id="8a786-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="8a786-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8a786-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="8a786-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8a786-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="8a786-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8a786-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="8a786-146">Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan**’dır.</span><span class="sxs-lookup"><span data-stu-id="8a786-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="8a786-147">Geniş izinleri göz önünde bulundurulduğunda, uygulamanızın Azure hizmetleriyle gerçekleştirdiği etkileşimlerin kapsamına bağlı olarak, doğru bir seçim olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="8a786-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="8a786-148">**Okuyucu** rolü daha kısıtlayıcıdır ve salt okunur uygulamalar için iyi bir seçim olabilir.</span><span class="sxs-lookup"><span data-stu-id="8a786-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="8a786-149">Azure portalı aracılığıyla role özel izinlerin ayrıntılarını görüntüleyebilir veya özel roller oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="8a786-150">Bu örnekte, bir önceki örneğimize **Okuyucu** rolünü ekleyip **Katkıda Bulunan** rolünü siliyoruz:</span><span class="sxs-lookup"><span data-stu-id="8a786-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="8a786-151">Şu anda atanmış olan rolleri görüntülemek için:</span><span class="sxs-lookup"><span data-stu-id="8a786-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="8a786-152">Rol yönetimi için diğer Azure PowerShell cmdlet’leri:</span><span class="sxs-lookup"><span data-stu-id="8a786-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="8a786-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8a786-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="8a786-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8a786-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="8a786-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8a786-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="8a786-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8a786-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="8a786-157">Güvenlik sorumlusunun kimlik bilgilerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="8a786-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="8a786-158">Düzenli aralıklarla izinleri gözden geçirmek ve parolayı güncelleştirmek, güvenlik açısından iyi bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="8a786-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="8a786-159">Uygulamanız değiştikçe güvenlik kimlik bilgilerini yönetmek ve değiştirmek de isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a786-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="8a786-160">Örneğin, yeni bir parola oluşturup eskisini kaldırarak hizmet sorumlusunun parolasını değiştirebiliriz.</span><span class="sxs-lookup"><span data-stu-id="8a786-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="8a786-161">Hizmet sorumlusu için yeni parola ekleme</span><span class="sxs-lookup"><span data-stu-id="8a786-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8a786-162">Hizmet sorumlusunun kimlik bilgilerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="8a786-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="8a786-163">Hizmet sorumlusundan eski parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8a786-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="8a786-164">Hizmet sorumlusunun kimlik bilgileri listesini doğrulama</span><span class="sxs-lookup"><span data-stu-id="8a786-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```