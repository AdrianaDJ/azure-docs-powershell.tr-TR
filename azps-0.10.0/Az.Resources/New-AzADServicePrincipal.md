---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 96ff12056167adaabcb828e2fedfe0c78d59e963
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326143"
---
# <span data-ttu-id="856e8-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="856e8-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="856e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="856e8-102">SYNOPSIS</span></span>
<span data-ttu-id="856e8-103">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="856e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="856e8-104">SYNTAX</span></span>

### <span data-ttu-id="856e8-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="856e8-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="856e8-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="856e8-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="856e8-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="856e8-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856e8-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="856e8-121">DESCRIPTION</span></span>
<span data-ttu-id="856e8-122">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="856e8-123">Kullanıcı için bir değer sağlayamazsa, varsayılan parametre kümesi parametreler için varsayılan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="856e8-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="856e8-124">Kullanılan varsayılan değerler hakkında daha fazla bilgi için aşağıdaki verilen parametrelerin açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="856e8-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="856e8-125">Bu cmdlet, hizmet sorumlusuna ve parametreleriyle rol atama özelliğine sahiptir `Role` `Scope` ; Bu parametrelerden hiçbiri sağlanmadıysa, hizmet sorumlusuna rol atanmaz.</span><span class="sxs-lookup"><span data-stu-id="856e8-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="856e8-126">`Role`And parametrelerinin varsayılan değerleri `Scope` "katkıda bulunanlar" ve geçerli abonelik, sırasıyla ( _Not_ : yalnızca Kullanıcı iki parametreden biri için bir değer sağlarsa, ancak diğeri yerine bir değer sağlıyorsa kullanılır).</span><span class="sxs-lookup"><span data-stu-id="856e8-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="856e8-127">Cmdlet de örtülü olarak bir uygulama oluşturur ve özelliklerini (ApplicationId sağlanmadıysa) ayarlar.</span><span class="sxs-lookup"><span data-stu-id="856e8-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="856e8-128">Uygulamaya özgü parametreleri güncelleştirmek için lütfen Set-AzADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="856e8-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="856e8-129">**Yeni-AzADServicePrincipal** komutunu kullanarak bir hizmet sorumlusu oluşturduğunuzda, çıkış, korumanız gereken kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="856e8-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="856e8-130">Kodunuzda bu kimlik bilgilerini eklediğinizden veya kaynak denetiminizin kimlik bilgilerini kontrol ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="856e8-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="856e8-131">Alternatif olarak, kimlik bilgilerini kullanma gereğini ortadan kaldırmanız için [Yönetilen kimlikler](/azure/active-directory/managed-identities-azure-resources/overview) kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="856e8-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="856e8-132">Varsayılan olarak, **New-AzADServicePrincipal** , [katılımcı](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamındaki hizmet sorumlusuna atar.</span><span class="sxs-lookup"><span data-stu-id="856e8-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="856e8-133">Güvenliği aşılan hizmet sorumlusunun riskini azaltmak için daha belirli bir rol atayın ve kapsamı kaynak veya kaynak grubuyla daraltın.</span><span class="sxs-lookup"><span data-stu-id="856e8-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="856e8-134">Daha fazla bilgi için [rol ataması ekleme adımlarını izleyin](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="856e8-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="856e8-135">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="856e8-135">EXAMPLES</span></span>

### <span data-ttu-id="856e8-136">Örnek 1-basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="856e8-137">Yukarıdaki komut, parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="856e8-138">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="856e8-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="856e8-139">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="856e8-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="856e8-140">Örnek 2-belirtilen rolle ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="856e8-141">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="856e8-142">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="856e8-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="856e8-143">Hizmet sorumlusu, geçerli aboneliğin "okuyucu" izinleriyle oluşturulmuştur (parametre için değer sağlanmadığından beri `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="856e8-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="856e8-144">Örnek 3-belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="856e8-145">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="856e8-146">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="856e8-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="856e8-147">Hizmet sorumlusu, `Role` sağlanan kaynak grubu kapsamının üzerinde "katkıda bulunanlar" izinleriyle oluşturulmuştur (parametre için değer sağlanmamıştır).</span><span class="sxs-lookup"><span data-stu-id="856e8-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="856e8-148">Örnek 4-belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="856e8-149">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="856e8-150">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="856e8-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="856e8-151">Hizmet sorumlusu, sağlanan kaynak grubu kapsamındaki "okuyucu" izinleriyle oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="856e8-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="856e8-152">Örnek 5-rol atamasıyla uygulama kimliği 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="856e8-153">Uygulama kimliği ' 34a28ad2-dec2:4-4a41-BC3B-vseç22ddf90000e ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="856e8-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="856e8-154">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="856e8-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="856e8-155">Örnek 6-Boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="856e8-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="856e8-156">Nesne kimliği ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile ve bu uygulama için yeni bir AD hizmeti sorumlusu oluşturmak için New-AzADServicePrincipal cmdlet 'ine sahip olan uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="856e8-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="856e8-157">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="856e8-157">PARAMETERS</span></span>

### <span data-ttu-id="856e8-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="856e8-158">-ApplicationId</span></span>
<span data-ttu-id="856e8-159">Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="856e8-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="856e8-160">Bu özellik, oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="856e8-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="856e8-161">Uygulama kimliği belirtilmezse, bir tane oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="856e8-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="856e8-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="856e8-162">-ApplicationObject</span></span>
<span data-ttu-id="856e8-163">Hizmet sorumlusu 'nın oluşturulduğu uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="856e8-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="856e8-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="856e8-164">-CertValue</span></span>
<span data-ttu-id="856e8-165">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="856e8-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="856e8-166">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="856e8-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="856e8-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856e8-167">-DefaultProfile</span></span>
<span data-ttu-id="856e8-168">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="856e8-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="856e8-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="856e8-169">-DisplayName</span></span>
<span data-ttu-id="856e8-170">Hizmet sorumlusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="856e8-170">The friendly name of the service principal.</span></span> <span data-ttu-id="856e8-171">Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak ' Azure-PowerShell-dd-dd-YYYY-SS-mm-ss ' olarak ayarlanır; burada sonek, uygulama oluşturma zamanı olur.</span><span class="sxs-lookup"><span data-stu-id="856e8-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="856e8-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="856e8-172">-EndDate</span></span>
<span data-ttu-id="856e8-173">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="856e8-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="856e8-174">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="856e8-174">The default end date value is one year from today.</span></span> <span data-ttu-id="856e8-175">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="856e8-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="856e8-176">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="856e8-176">-KeyCredential</span></span>
<span data-ttu-id="856e8-177">Uygulamayla ilişkili anahtar kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="856e8-177">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="856e8-178">-Parola</span><span class="sxs-lookup"><span data-stu-id="856e8-178">-Password</span></span>
<span data-ttu-id="856e8-179">Hizmet sorumlusu ile ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="856e8-179">The password to be associated with the service principal.</span></span> <span data-ttu-id="856e8-180">Parola sağlanmadıysa, rastgele bir GUID oluşturulur ve parola olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="856e8-180">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="856e8-181">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="856e8-181">-PasswordCredential</span></span>
<span data-ttu-id="856e8-182">Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="856e8-182">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="856e8-183">-Role</span><span class="sxs-lookup"><span data-stu-id="856e8-183">-Role</span></span>
<span data-ttu-id="856e8-184">Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol.</span><span class="sxs-lookup"><span data-stu-id="856e8-184">The role that the service principal has over the scope.</span></span> <span data-ttu-id="856e8-185">Bir değer `Scope` sağlanmışsa ancak hiçbir değer sağlanmazsa `Role` , `Role` Varsayılan olarak ' katılımcı ' rolü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="856e8-185">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="856e8-186">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="856e8-186">-Scope</span></span>
<span data-ttu-id="856e8-187">Hizmet sorumlusunun izinleri olan kapsam.</span><span class="sxs-lookup"><span data-stu-id="856e8-187">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="856e8-188">Bir değer `Role` sağlanmışsa ancak hiçbir değer sağlanmazsa `Scope` , `Scope` Varsayılan olarak geçerli abonelik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="856e8-188">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="856e8-189">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="856e8-189">-SkipAssignment</span></span>
<span data-ttu-id="856e8-190">Ayarlıysa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="856e8-190">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="856e8-191">-StartDate</span><span class="sxs-lookup"><span data-stu-id="856e8-191">-StartDate</span></span>
<span data-ttu-id="856e8-192">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="856e8-192">The effective start date of the credential usage.</span></span>
<span data-ttu-id="856e8-193">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="856e8-193">The default start date value is today.</span></span> <span data-ttu-id="856e8-194">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="856e8-194">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="856e8-195">-Onay</span><span class="sxs-lookup"><span data-stu-id="856e8-195">-Confirm</span></span>
<span data-ttu-id="856e8-196">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="856e8-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856e8-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856e8-197">-WhatIf</span></span>
<span data-ttu-id="856e8-198">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="856e8-198">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856e8-199">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="856e8-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856e8-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856e8-200">CommonParameters</span></span>
<span data-ttu-id="856e8-201">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="856e8-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856e8-202">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856e8-202">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856e8-203">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="856e8-203">INPUTS</span></span>

### <span data-ttu-id="856e8-204">System. Guid</span><span class="sxs-lookup"><span data-stu-id="856e8-204">System.Guid</span></span>

### <span data-ttu-id="856e8-205">System. String</span><span class="sxs-lookup"><span data-stu-id="856e8-205">System.String</span></span>

### <span data-ttu-id="856e8-206">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="856e8-206">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="856e8-207">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="856e8-207">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="856e8-208">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="856e8-208">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="856e8-209">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="856e8-209">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="856e8-210">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="856e8-210">System.Security.SecureString</span></span>

### <span data-ttu-id="856e8-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="856e8-211">System.DateTime</span></span>

## <span data-ttu-id="856e8-212">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="856e8-212">OUTPUTS</span></span>

### <span data-ttu-id="856e8-213">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="856e8-213">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="856e8-214">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="856e8-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="856e8-215">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="856e8-215">NOTES</span></span>
<span data-ttu-id="856e8-216">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="856e8-216">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="856e8-217">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="856e8-217">RELATED LINKS</span></span>

[<span data-ttu-id="856e8-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="856e8-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="856e8-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="856e8-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="856e8-220">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="856e8-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="856e8-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="856e8-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="856e8-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="856e8-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="856e8-223">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="856e8-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="856e8-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="856e8-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

