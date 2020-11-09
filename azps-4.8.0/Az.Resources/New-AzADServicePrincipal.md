---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3c96ab0cdcc25e0e1c9b4a343cd68420654d934c
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326146"
---
# <span data-ttu-id="84f7b-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="84f7b-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="84f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="84f7b-103">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="84f7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84f7b-104">SYNTAX</span></span>

### <span data-ttu-id="84f7b-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84f7b-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84f7b-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84f7b-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f7b-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="84f7b-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84f7b-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="84f7b-120">DESCRIPTION</span></span>

<span data-ttu-id="84f7b-121">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="84f7b-122">Varsayılan parametre kümesi, sağlanmadıysa parametreler için varsayılan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="84f7b-123">Varsayılan değerler hakkında daha fazla bilgi için her parametrenin açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="84f7b-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="84f7b-124">Bu cmdlet, **rol** ve **kapsam** parametreleriyle hizmet sorumlusuna rol atama özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="84f7b-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="84f7b-125">İkisi de atlanırsa, katkıda bulunan rol hizmet sorumlusuna atanır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="84f7b-126">**Rol** ve **kapsam** parametrelerinin varsayılan değerleri geçerli aboneliğin **katkıdır** .</span><span class="sxs-lookup"><span data-stu-id="84f7b-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="84f7b-127">Cmdlet, uygulama oluşturur ve ApplicationId sağlanmazsa özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="84f7b-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="84f7b-128">Uygulamaya özgü parametreleri güncelleştirmek için [Update-AzADApplication](./update-azadapplication.md) cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="84f7b-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="84f7b-129">**Yeni-AzADServicePrincipal** komutunu kullanarak bir hizmet sorumlusu oluşturduğunuzda, çıkış, korumanız gereken kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="84f7b-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="84f7b-130">Kodunuzda bu kimlik bilgilerini eklediğinizden veya kaynak denetiminizin kimlik bilgilerini kontrol ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="84f7b-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="84f7b-131">Alternatif olarak, kimlik bilgilerini kullanma gereğini ortadan kaldırmanız için [Yönetilen kimlikler](/azure/active-directory/managed-identities-azure-resources/overview) kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84f7b-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="84f7b-132">Varsayılan olarak, **New-AzADServicePrincipal** , [katılımcı](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamındaki hizmet sorumlusuna atar.</span><span class="sxs-lookup"><span data-stu-id="84f7b-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="84f7b-133">Güvenliği aşılan hizmet sorumlusunun riskini azaltmak için daha belirli bir rol atayın ve kapsamı kaynak veya kaynak grubuyla daraltın.</span><span class="sxs-lookup"><span data-stu-id="84f7b-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="84f7b-134">Daha fazla bilgi için [rol ataması ekleme adımlarını izleyin](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="84f7b-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="84f7b-135">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84f7b-135">EXAMPLES</span></span>

### <span data-ttu-id="84f7b-136">Örnek 1: basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="84f7b-137">Aşağıdaki örnek, belirtilmeyen parametreler için varsayılan değerleri kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="84f7b-138">Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="84f7b-139">**Rol** veya **kapsam** için değer sağlanmadığı için, oluşturulan hizmet sorumlusuna geçerli aboneliğin **katılımcı** rolü atanır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="84f7b-140">Örnek 2: belirtilen role ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="84f7b-141">Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="84f7b-142">Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="84f7b-143">**Kapsam** parametresi için değer sağlanmadığından, geçerli aboneliğin **okuyucu** izinleriyle hizmet sorumlusu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="84f7b-144">Örnek 3: belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="84f7b-145">Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="84f7b-146">Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="84f7b-147">**Rol** parametresi için değer sağlanmadığından, sağlanan kaynak grubu kapsamının **katılımcı** izinleriyle hizmet sorumlusu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="84f7b-148">Örnek 4: belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="84f7b-149">Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="84f7b-150">Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="84f7b-151">Hizmet sorumlusu, sağlanan kaynak grubu kapsamının **okuyucu** izinleriyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="84f7b-152">Örnek 5: rol atamasıyla uygulama KIMLIĞI 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="84f7b-153">Aşağıdaki örnek, uygulama KIMLIĞI ' 00000000-0000-0000-0000-000000000000 ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="84f7b-154">**Rol** veya **kapsam** için değer sağlanmadığı için, oluşturulan hizmet sorumlusuna geçerli aboneliğin **katılımcı** rolü atanır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="84f7b-155">Örnek 6: boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="84f7b-156">Aşağıdaki örnek, [Get-AzADApplication](./get-azadapplication.md) cmdlet 'ini kullanarak uygulamayı ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile alır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="84f7b-157">Sonuçlar, `New-AzADServicePrincipal` Bu uygulama için yeni BIR ad hizmeti sorumlusu oluşturmak üzere cmdlet 'e verilmez.</span><span class="sxs-lookup"><span data-stu-id="84f7b-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="84f7b-158">Örnek 7: DisplayName ve parola kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="84f7b-159">Aşağıdaki örnek, adı **servicePrincipalName** ve **strongpassworld! 23** adında yeni bir uygulama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="84f7b-160">Oluşturulan uygulama temelinde hizmet sorumlusunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="84f7b-161">Başlangıç tarihi ve bitiş tarihi parola kimlik bilgilerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="84f7b-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="84f7b-162">Örnek 8: DisplayName ve düz anahtar kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="84f7b-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="84f7b-163">Aşağıdaki örnek, **servicePrincipalName** ve sertifika **$CERT** adlı yeni bir uygulama oluşturur. Oluşturulan uygulama temelinde hizmet sorumlusunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="84f7b-164">Bitiş tarihi anahtar kimlik bilgilerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="84f7b-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="84f7b-165">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84f7b-165">PARAMETERS</span></span>

### <span data-ttu-id="84f7b-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="84f7b-166">-ApplicationId</span></span>

<span data-ttu-id="84f7b-167">Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="84f7b-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="84f7b-168">Bu özellik, oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="84f7b-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="84f7b-169">Var olan bir uygulama için bir uygulama KIMLIĞI belirtilmemişse uygulama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="84f7b-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="84f7b-170">-ApplicationObject</span></span>

<span data-ttu-id="84f7b-171">Hizmet sorumlusu 'nın oluşturulduğu uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="84f7b-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="84f7b-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="84f7b-172">-CertValue</span></span>

<span data-ttu-id="84f7b-173">Asimetrik kimlik bilgileri türü değeri.</span><span class="sxs-lookup"><span data-stu-id="84f7b-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="84f7b-174">Base64 Ile kodlanmış sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="84f7b-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="84f7b-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f7b-175">-DefaultProfile</span></span>

<span data-ttu-id="84f7b-176">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84f7b-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84f7b-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="84f7b-177">-DisplayName</span></span>

<span data-ttu-id="84f7b-178">Hizmet sorumlusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="84f7b-178">The friendly name of the service principal.</span></span> <span data-ttu-id="84f7b-179">Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak **Azure-PowerShell-mm-dd-yyyy-ss-dd-ss** değerini alır ve sonek uygulama oluşturma zamanı olur.</span><span class="sxs-lookup"><span data-stu-id="84f7b-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="84f7b-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="84f7b-180">-EndDate</span></span>

<span data-ttu-id="84f7b-181">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="84f7b-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="84f7b-182">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="84f7b-183">Asimetrik tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten önce veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="84f7b-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="84f7b-184">-KeyCredential</span></span>

<span data-ttu-id="84f7b-185">Uygulamayla ilişkili anahtar kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="84f7b-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="84f7b-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="84f7b-186">-PasswordCredential</span></span>

<span data-ttu-id="84f7b-187">Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="84f7b-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="84f7b-188">-Role</span><span class="sxs-lookup"><span data-stu-id="84f7b-188">-Role</span></span>

<span data-ttu-id="84f7b-189">Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol.</span><span class="sxs-lookup"><span data-stu-id="84f7b-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="84f7b-190">Değer sağlanmazsa, **rol** varsayılan olarak **katılımcı** rolüne göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="84f7b-191">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="84f7b-191">-Scope</span></span>

<span data-ttu-id="84f7b-192">Hizmet sorumlusunun izinleri olan kapsam.</span><span class="sxs-lookup"><span data-stu-id="84f7b-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="84f7b-193">Değer sağlanmazsa **, varsayılan olarak** geçerli abonelik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="84f7b-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="84f7b-194">-SkipAssignment</span></span>

<span data-ttu-id="84f7b-195">Ayarlanırsa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlayın.</span><span class="sxs-lookup"><span data-stu-id="84f7b-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="84f7b-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="84f7b-196">-StartDate</span></span>

<span data-ttu-id="84f7b-197">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="84f7b-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="84f7b-198">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="84f7b-198">The default start date value is today.</span></span> <span data-ttu-id="84f7b-199">Asimetrik tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihin üstünde veya sonra olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84f7b-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="84f7b-200">-Onay</span><span class="sxs-lookup"><span data-stu-id="84f7b-200">-Confirm</span></span>

<span data-ttu-id="84f7b-201">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84f7b-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84f7b-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84f7b-202">-WhatIf</span></span>

<span data-ttu-id="84f7b-203">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84f7b-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84f7b-204">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84f7b-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84f7b-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f7b-205">CommonParameters</span></span>
<span data-ttu-id="84f7b-206">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84f7b-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f7b-207">Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.</span><span class="sxs-lookup"><span data-stu-id="84f7b-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="84f7b-208">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84f7b-208">INPUTS</span></span>

### <span data-ttu-id="84f7b-209">System. Guid</span><span class="sxs-lookup"><span data-stu-id="84f7b-209">System.Guid</span></span>

### <span data-ttu-id="84f7b-210">System. String</span><span class="sxs-lookup"><span data-stu-id="84f7b-210">System.String</span></span>

### <span data-ttu-id="84f7b-211">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="84f7b-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="84f7b-212">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="84f7b-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="84f7b-213">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="84f7b-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="84f7b-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="84f7b-214">System.DateTime</span></span>

## <span data-ttu-id="84f7b-215">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84f7b-215">OUTPUTS</span></span>

### <span data-ttu-id="84f7b-216">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="84f7b-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="84f7b-217">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="84f7b-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="84f7b-218">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84f7b-218">NOTES</span></span>

<span data-ttu-id="84f7b-219">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="84f7b-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="84f7b-220">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84f7b-220">RELATED LINKS</span></span>

[<span data-ttu-id="84f7b-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="84f7b-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="84f7b-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="84f7b-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="84f7b-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="84f7b-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="84f7b-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="84f7b-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="84f7b-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84f7b-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="84f7b-226">Yeni-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84f7b-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="84f7b-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84f7b-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)
