---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326137"
---
# <span data-ttu-id="88ac0-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="88ac0-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="88ac0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="88ac0-103">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="88ac0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88ac0-104">SYNTAX</span></span>

### <span data-ttu-id="88ac0-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88ac0-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88ac0-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88ac0-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ac0-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="88ac0-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ac0-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="88ac0-120">DESCRIPTION</span></span>
<span data-ttu-id="88ac0-121">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="88ac0-122">Kullanıcı için bir değer sağlayamazsa, varsayılan parametre kümesi parametreler için varsayılan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="88ac0-123">Kullanılan varsayılan değerler hakkında daha fazla bilgi için aşağıdaki verilen parametrelerin açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="88ac0-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="88ac0-124">Bu cmdlet, hizmet sorumlusuna ve parametreleriyle rol atama özelliğine sahiptir `Role` `Scope` ; Bu parametrelerden hiçbiri sağlanmadıysa, hizmet sorumlusuna rol atanmaz.</span><span class="sxs-lookup"><span data-stu-id="88ac0-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="88ac0-125">`Role`And parametrelerinin varsayılan değerleri `Scope` "katkıda bulunanlar" ve geçerli abonelik, sırasıyla ( _Not_ : yalnızca Kullanıcı iki parametreden biri için bir değer sağlarsa, ancak diğeri yerine bir değer sağlıyorsa kullanılır).</span><span class="sxs-lookup"><span data-stu-id="88ac0-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="88ac0-126">Cmdlet de örtülü olarak bir uygulama oluşturur ve özelliklerini (ApplicationId sağlanmadıysa) ayarlar.</span><span class="sxs-lookup"><span data-stu-id="88ac0-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="88ac0-127">Uygulamaya özgü parametreleri güncelleştirmek için lütfen Set-AzADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="88ac0-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="88ac0-128">**Yeni-AzADServicePrincipal** komutunu kullanarak bir hizmet sorumlusu oluşturduğunuzda, çıkış, korumanız gereken kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="88ac0-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="88ac0-129">Kodunuzda bu kimlik bilgilerini eklediğinizden veya kaynak denetiminizin kimlik bilgilerini kontrol ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="88ac0-129">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="88ac0-130">Alternatif olarak, kimlik bilgilerini kullanma gereğini ortadan kaldırmanız için [Yönetilen kimlikler](/azure/active-directory/managed-identities-azure-resources/overview) kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="88ac0-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="88ac0-131">Varsayılan olarak, **New-AzADServicePrincipal** , [katılımcı](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamındaki hizmet sorumlusuna atar.</span><span class="sxs-lookup"><span data-stu-id="88ac0-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="88ac0-132">Güvenliği aşılan hizmet sorumlusunun riskini azaltmak için daha belirli bir rol atayın ve kapsamı kaynak veya kaynak grubuyla daraltın.</span><span class="sxs-lookup"><span data-stu-id="88ac0-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="88ac0-133">Daha fazla bilgi için [rol ataması ekleme adımlarını izleyin](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="88ac0-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="88ac0-134">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88ac0-134">EXAMPLES</span></span>

### <span data-ttu-id="88ac0-135">Örnek 1-basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="88ac0-136">Yukarıdaki komut, parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="88ac0-137">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="88ac0-138">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="88ac0-139">Örnek 2-belirtilen rolle ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="88ac0-140">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="88ac0-141">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="88ac0-142">Hizmet sorumlusu, geçerli aboneliğin "okuyucu" izinleriyle oluşturulmuştur (parametre için değer sağlanmadığından beri `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="88ac0-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="88ac0-143">Örnek 3-belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="88ac0-144">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="88ac0-145">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="88ac0-146">Hizmet sorumlusu, `Role` sağlanan kaynak grubu kapsamının üzerinde "katkıda bulunanlar" izinleriyle oluşturulmuştur (parametre için değer sağlanmamıştır).</span><span class="sxs-lookup"><span data-stu-id="88ac0-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="88ac0-147">Örnek 4-belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="88ac0-148">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="88ac0-149">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="88ac0-150">Hizmet sorumlusu, sağlanan kaynak grubu kapsamındaki "okuyucu" izinleriyle oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="88ac0-151">Örnek 5-rol atamasıyla uygulama kimliği 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="88ac0-152">Uygulama kimliği ' 34a28ad2-dec2:4-4a41-BC3B-vseç22ddf90000e ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="88ac0-153">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="88ac0-154">Örnek 6-Boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="88ac0-155">Nesne kimliği ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile ve bu uygulama için yeni bir AD hizmeti sorumlusu oluşturmak için New-AzADServicePrincipal cmdlet 'ine sahip olan uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="88ac0-156">Örnek 7-DisplayName ve parola kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-156">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="88ac0-157">Adı "ServicePrincipalName" ve parola "StrongPassworld! 23" olan yeni bir uygulama oluşturur ve hizmet sorumlusunu yeni oluşturulan uygulamaya göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-157">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="88ac0-158">Başlangıç tarihi ve bitiş tarihi, parola kimlik bilgilerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="88ac0-158">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="88ac0-159">Örnek 8-DisplayName ve düz anahtar kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ac0-159">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="88ac0-160">Adı "ServicePrincipalName" ve sertifika "$cert" olan yeni bir uygulama oluşturur ve hizmet sorumlusunu yeni oluşturulan uygulamaya göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-160">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="88ac0-161">Bitiş tarihi anahtar kimlik bilgilerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="88ac0-161">The end date is added to key credential.</span></span>

## <span data-ttu-id="88ac0-162">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88ac0-162">PARAMETERS</span></span>

### <span data-ttu-id="88ac0-163">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="88ac0-163">-ApplicationId</span></span>
<span data-ttu-id="88ac0-164">Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="88ac0-164">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="88ac0-165">Bu özellik, oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="88ac0-165">Once created this property cannot be changed.</span></span>
<span data-ttu-id="88ac0-166">Uygulama kimliği belirtilmezse, bir tane oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-166">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-167">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="88ac0-167">-ApplicationObject</span></span>
<span data-ttu-id="88ac0-168">Hizmet sorumlusu 'nın oluşturulduğu uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="88ac0-168">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-169">-CertValue</span><span class="sxs-lookup"><span data-stu-id="88ac0-169">-CertValue</span></span>
<span data-ttu-id="88ac0-170">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="88ac0-170">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="88ac0-171">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="88ac0-171">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ac0-172">-DefaultProfile</span></span>
<span data-ttu-id="88ac0-173">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="88ac0-173">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88ac0-174">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="88ac0-174">-DisplayName</span></span>
<span data-ttu-id="88ac0-175">Hizmet sorumlusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="88ac0-175">The friendly name of the service principal.</span></span> <span data-ttu-id="88ac0-176">Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak ' Azure-PowerShell-dd-dd-YYYY-SS-mm-ss ' olarak ayarlanır; burada sonek, uygulama oluşturma zamanı olur.</span><span class="sxs-lookup"><span data-stu-id="88ac0-176">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-177">-EndDate</span><span class="sxs-lookup"><span data-stu-id="88ac0-177">-EndDate</span></span>
<span data-ttu-id="88ac0-178">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="88ac0-178">The effective end date of the credential usage.</span></span>
<span data-ttu-id="88ac0-179">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-179">The default end date value is one year from today.</span></span> <span data-ttu-id="88ac0-180">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-180">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-181">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="88ac0-181">-KeyCredential</span></span>
<span data-ttu-id="88ac0-182">Uygulamayla ilişkili anahtar kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-182">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-183">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="88ac0-183">-PasswordCredential</span></span>
<span data-ttu-id="88ac0-184">Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="88ac0-184">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-185">-Role</span><span class="sxs-lookup"><span data-stu-id="88ac0-185">-Role</span></span>
<span data-ttu-id="88ac0-186">Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol.</span><span class="sxs-lookup"><span data-stu-id="88ac0-186">The role that the service principal has over the scope.</span></span> <span data-ttu-id="88ac0-187">Bir değer `Scope` sağlanmışsa ancak hiçbir değer sağlanmazsa `Role` , `Role` Varsayılan olarak ' katılımcı ' rolü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-187">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-188">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="88ac0-188">-Scope</span></span>
<span data-ttu-id="88ac0-189">Hizmet sorumlusunun izinleri olan kapsam.</span><span class="sxs-lookup"><span data-stu-id="88ac0-189">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="88ac0-190">Bir değer `Role` sağlanmışsa ancak hiçbir değer sağlanmazsa `Scope` , `Scope` Varsayılan olarak geçerli abonelik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-190">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-191">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="88ac0-191">-SkipAssignment</span></span>
<span data-ttu-id="88ac0-192">Ayarlıysa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="88ac0-192">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-193">-StartDate</span><span class="sxs-lookup"><span data-stu-id="88ac0-193">-StartDate</span></span>
<span data-ttu-id="88ac0-194">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="88ac0-194">The effective start date of the credential usage.</span></span>
<span data-ttu-id="88ac0-195">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="88ac0-195">The default start date value is today.</span></span> <span data-ttu-id="88ac0-196">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88ac0-196">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ac0-197">-Onay</span><span class="sxs-lookup"><span data-stu-id="88ac0-197">-Confirm</span></span>
<span data-ttu-id="88ac0-198">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88ac0-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88ac0-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ac0-199">-WhatIf</span></span>
<span data-ttu-id="88ac0-200">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88ac0-200">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ac0-201">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88ac0-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88ac0-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ac0-202">CommonParameters</span></span>
<span data-ttu-id="88ac0-203">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88ac0-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ac0-204">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88ac0-204">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ac0-205">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88ac0-205">INPUTS</span></span>

### <span data-ttu-id="88ac0-206">System. Guid</span><span class="sxs-lookup"><span data-stu-id="88ac0-206">System.Guid</span></span>

### <span data-ttu-id="88ac0-207">System. String</span><span class="sxs-lookup"><span data-stu-id="88ac0-207">System.String</span></span>

### <span data-ttu-id="88ac0-208">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="88ac0-208">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="88ac0-209">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="88ac0-209">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="88ac0-210">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="88ac0-210">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="88ac0-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="88ac0-211">System.DateTime</span></span>

## <span data-ttu-id="88ac0-212">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88ac0-212">OUTPUTS</span></span>

### <span data-ttu-id="88ac0-213">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="88ac0-213">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="88ac0-214">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="88ac0-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="88ac0-215">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88ac0-215">NOTES</span></span>
<span data-ttu-id="88ac0-216">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="88ac0-216">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="88ac0-217">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88ac0-217">RELATED LINKS</span></span>

[<span data-ttu-id="88ac0-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="88ac0-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="88ac0-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="88ac0-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="88ac0-220">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="88ac0-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="88ac0-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="88ac0-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="88ac0-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="88ac0-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="88ac0-223">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="88ac0-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="88ac0-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="88ac0-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

