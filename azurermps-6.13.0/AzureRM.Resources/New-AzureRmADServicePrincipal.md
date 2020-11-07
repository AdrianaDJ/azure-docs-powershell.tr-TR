---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 50f4a277461e81e26d1e553ad24f817415d5b267
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762453"
---
# <span data-ttu-id="823cd-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="823cd-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="823cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="823cd-102">SYNOPSIS</span></span>
<span data-ttu-id="823cd-103">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="823cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="823cd-104">SYNTAX</span></span>

### <span data-ttu-id="823cd-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="823cd-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="823cd-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="823cd-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="823cd-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="823cd-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="823cd-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="823cd-121">DESCRIPTION</span></span>
<span data-ttu-id="823cd-122">Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="823cd-123">Kullanıcı için bir değer sağlayamazsa, varsayılan parametre kümesi parametreler için varsayılan değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="823cd-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="823cd-124">Kullanılan varsayılan değerler hakkında daha fazla bilgi için aşağıdaki verilen parametrelerin açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="823cd-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="823cd-125">Bu cmdlet, hizmet sorumlusuna ve parametreleriyle rol atama özelliğine sahiptir `Role` `Scope` ; Bu parametrelerden hiçbiri sağlanmadıysa, hizmet sorumlusuna rol atanmaz.</span><span class="sxs-lookup"><span data-stu-id="823cd-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="823cd-126">`Role`And parametrelerinin varsayılan değerleri `Scope` "katkıda bulunanlar" ve geçerli abonelik, sırasıyla ( _Not_ : yalnızca Kullanıcı iki parametreden biri için bir değer sağlarsa, ancak diğeri yerine bir değer sağlıyorsa kullanılır).</span><span class="sxs-lookup"><span data-stu-id="823cd-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="823cd-127">Cmdlet de örtülü olarak bir uygulama oluşturur ve özelliklerini (ApplicationId sağlanmadıysa) ayarlar.</span><span class="sxs-lookup"><span data-stu-id="823cd-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="823cd-128">Uygulamaya özgü parametreleri güncelleştirmek için lütfen Set-AzureRmADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="823cd-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="823cd-129">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="823cd-129">EXAMPLES</span></span>

### <span data-ttu-id="823cd-130">Örnek 1-basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="823cd-131">Yukarıdaki komut, parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="823cd-132">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="823cd-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="823cd-133">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="823cd-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="823cd-134">Örnek 2-belirtilen rolle ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="823cd-135">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="823cd-136">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="823cd-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="823cd-137">Hizmet sorumlusu, geçerli aboneliğin "okuyucu" izinleriyle oluşturulmuştur (parametre için değer sağlanmadığından beri `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="823cd-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="823cd-138">Örnek 3-belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="823cd-139">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="823cd-140">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="823cd-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="823cd-141">Hizmet sorumlusu, `Role` sağlanan kaynak grubu kapsamının üzerinde "katkıda bulunanlar" izinleriyle oluşturulmuştur (parametre için değer sağlanmamıştır).</span><span class="sxs-lookup"><span data-stu-id="823cd-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="823cd-142">Örnek 4-belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="823cd-143">Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="823cd-144">Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="823cd-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="823cd-145">Hizmet sorumlusu, sağlanan kaynak grubu kapsamındaki "okuyucu" izinleriyle oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="823cd-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="823cd-146">Örnek 5-rol atamasıyla uygulama kimliği 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="823cd-147">Uygulama kimliği ' 34a28ad2-dec2:4-4a41-BC3B-vseç22ddf90000e ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="823cd-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="823cd-148">Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.</span><span class="sxs-lookup"><span data-stu-id="823cd-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="823cd-149">Örnek 6-Boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="823cd-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="823cd-150">Nesne kimliği ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile ve bu uygulama için yeni bir AD hizmeti sorumlusu oluşturmak için New-AzureRmADServicePrincipal cmdlet 'ine sahip olan uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="823cd-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="823cd-151">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="823cd-151">PARAMETERS</span></span>

### <span data-ttu-id="823cd-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="823cd-152">-ApplicationId</span></span>
<span data-ttu-id="823cd-153">Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="823cd-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="823cd-154">Bu özellik, oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="823cd-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="823cd-155">Uygulama kimliği belirtilmezse, bir tane oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="823cd-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="823cd-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="823cd-156">-ApplicationObject</span></span>
<span data-ttu-id="823cd-157">Hizmet sorumlusu 'nın oluşturulduğu uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="823cd-157">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="823cd-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="823cd-158">-CertValue</span></span>
<span data-ttu-id="823cd-159">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="823cd-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="823cd-160">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="823cd-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="823cd-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823cd-161">-DefaultProfile</span></span>
<span data-ttu-id="823cd-162">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="823cd-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823cd-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="823cd-163">-DisplayName</span></span>
<span data-ttu-id="823cd-164">Hizmet sorumlusunun kolay adı.</span><span class="sxs-lookup"><span data-stu-id="823cd-164">The friendly name of the service principal.</span></span> <span data-ttu-id="823cd-165">Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak ' Azure-PowerShell-dd-dd-YYYY-SS-mm-ss ' olarak ayarlanır; burada sonek, uygulama oluşturma zamanı olur.</span><span class="sxs-lookup"><span data-stu-id="823cd-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="823cd-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="823cd-166">-EndDate</span></span>
<span data-ttu-id="823cd-167">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="823cd-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="823cd-168">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="823cd-168">The default end date value is one year from today.</span></span> <span data-ttu-id="823cd-169">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="823cd-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="823cd-170">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="823cd-170">-KeyCredential</span></span>
<span data-ttu-id="823cd-171">Uygulamayla ilişkili anahtar kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="823cd-171">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="823cd-172">-Parola</span><span class="sxs-lookup"><span data-stu-id="823cd-172">-Password</span></span>
<span data-ttu-id="823cd-173">Hizmet sorumlusu ile ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="823cd-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="823cd-174">Parola sağlanmadıysa, rastgele bir GUID oluşturulur ve parola olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="823cd-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

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

### <span data-ttu-id="823cd-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="823cd-175">-PasswordCredential</span></span>
<span data-ttu-id="823cd-176">Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="823cd-176">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="823cd-177">-Role</span><span class="sxs-lookup"><span data-stu-id="823cd-177">-Role</span></span>
<span data-ttu-id="823cd-178">Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol.</span><span class="sxs-lookup"><span data-stu-id="823cd-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="823cd-179">Bir değer `Scope` sağlanmışsa ancak hiçbir değer sağlanmazsa `Role` , `Role` Varsayılan olarak ' katılımcı ' rolü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="823cd-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="823cd-180">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="823cd-180">-Scope</span></span>
<span data-ttu-id="823cd-181">Hizmet sorumlusunun izinleri olan kapsam.</span><span class="sxs-lookup"><span data-stu-id="823cd-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="823cd-182">Bir değer `Role` sağlanmışsa ancak hiçbir değer sağlanmazsa `Scope` , `Scope` Varsayılan olarak geçerli abonelik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="823cd-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="823cd-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="823cd-183">-SkipAssignment</span></span>
<span data-ttu-id="823cd-184">Ayarlıysa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="823cd-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="823cd-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="823cd-185">-StartDate</span></span>
<span data-ttu-id="823cd-186">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="823cd-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="823cd-187">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="823cd-187">The default start date value is today.</span></span> <span data-ttu-id="823cd-188">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="823cd-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="823cd-189">-Onay</span><span class="sxs-lookup"><span data-stu-id="823cd-189">-Confirm</span></span>
<span data-ttu-id="823cd-190">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="823cd-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="823cd-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="823cd-191">-WhatIf</span></span>
<span data-ttu-id="823cd-192">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="823cd-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="823cd-193">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="823cd-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="823cd-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823cd-194">CommonParameters</span></span>
<span data-ttu-id="823cd-195">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="823cd-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823cd-196">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="823cd-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823cd-197">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="823cd-197">INPUTS</span></span>

### <span data-ttu-id="823cd-198">System. Guid</span><span class="sxs-lookup"><span data-stu-id="823cd-198">System.Guid</span></span>

### <span data-ttu-id="823cd-199">System. String</span><span class="sxs-lookup"><span data-stu-id="823cd-199">System.String</span></span>

### <span data-ttu-id="823cd-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="823cd-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="823cd-201">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="823cd-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="823cd-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="823cd-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="823cd-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="823cd-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="823cd-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="823cd-204">System.Security.SecureString</span></span>

### <span data-ttu-id="823cd-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="823cd-205">System.DateTime</span></span>

## <span data-ttu-id="823cd-206">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="823cd-206">OUTPUTS</span></span>

### <span data-ttu-id="823cd-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="823cd-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="823cd-208">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="823cd-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="823cd-209">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="823cd-209">NOTES</span></span>
<span data-ttu-id="823cd-210">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="823cd-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="823cd-211">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="823cd-211">RELATED LINKS</span></span>

[<span data-ttu-id="823cd-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="823cd-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="823cd-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="823cd-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="823cd-214">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="823cd-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="823cd-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="823cd-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="823cd-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="823cd-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="823cd-217">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="823cd-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="823cd-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="823cd-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

