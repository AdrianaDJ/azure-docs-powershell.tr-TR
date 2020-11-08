---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 32a5c4ac20d584c26d95724a3f4ab4630504fb6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098509"
---
# <span data-ttu-id="ac327-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ac327-101">Connect-AzAccount</span></span>

## <span data-ttu-id="ac327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac327-102">SYNOPSIS</span></span>
<span data-ttu-id="ac327-103">Az PowerShell modüllerinden cmdlet 'ler ile kullanmak için kimliği doğrulanmış bir hesapla Azure 'a bağlanın.</span><span class="sxs-lookup"><span data-stu-id="ac327-103">Connect to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span>

## <span data-ttu-id="ac327-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac327-104">SYNTAX</span></span>

### <span data-ttu-id="ac327-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ac327-105">UserWithSubscriptionId (Default)</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac327-106">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="ac327-106">ServicePrincipalWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac327-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="ac327-107">UserWithCredential</span></span>

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac327-108">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="ac327-108">ServicePrincipalCertificateWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac327-109">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="ac327-109">AccessTokenWithSubscriptionId</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac327-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="ac327-110">ManagedServiceLogin</span></span>

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac327-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac327-111">DESCRIPTION</span></span>

<span data-ttu-id="ac327-112">Cmdlet, en `Connect-AzAccount` az PowerShell modüllerinden cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-112">The `Connect-AzAccount` cmdlet connects to Azure with an authenticated account for use with cmdlets from the Az PowerShell modules.</span></span> <span data-ttu-id="ac327-113">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager istekleriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac327-113">You can use this authenticated account only with Azure Resource Manager requests.</span></span> <span data-ttu-id="ac327-114">Hizmet yönetimiyle kullanmak üzere kimliği doğrulanmış bir hesap eklemek için, `Add-AzureAccount` Azure PowerShell modülünden cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac327-114">To add an authenticated account for use with Service Management, use the `Add-AzureAccount` cmdlet from the Azure PowerShell module.</span></span> <span data-ttu-id="ac327-115">Geçerli Kullanıcı için içerik bulunmazsa, kullanıcının bağlam listesi ilk 25 aboneliğini içeren bir içerikle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="ac327-115">If no context is found for the current user, the user's context list is populated with a context for each of their first 25 subscriptions.</span></span>
<span data-ttu-id="ac327-116">Kullanıcı için oluşturulan bağlamların listesi çalışırken bulunabilir `Get-AzContext -ListAvailable` .</span><span class="sxs-lookup"><span data-stu-id="ac327-116">The list of contexts created for the user can be found by running `Get-AzContext -ListAvailable`.</span></span> <span data-ttu-id="ac327-117">Bu bağlam popülasyonu atlamak için **Skipcontextpopülasyon** anahtarı parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac327-117">To skip this context population, specify the **SkipContextPopulation** switch parameter.</span></span> <span data-ttu-id="ac327-118">Bu cmdlet 'i yürüttükten sonra, kullanarak Azure hesabından bağlantınızı kesebilirsiniz `Disconnect-AzAccount` .</span><span class="sxs-lookup"><span data-stu-id="ac327-118">After executing this cmdlet, you can disconnect from an Azure account using `Disconnect-AzAccount`.</span></span>

## <span data-ttu-id="ac327-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac327-119">EXAMPLES</span></span>

### <span data-ttu-id="ac327-120">Örnek 1: Azure hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="ac327-120">Example 1: Connect to an Azure account</span></span>

<span data-ttu-id="ac327-121">Bu örnek bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-121">This example connects to an Azure account.</span></span> <span data-ttu-id="ac327-122">Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgileri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac327-122">You must provide a Microsoft account or organizational ID credentials.</span></span> <span data-ttu-id="ac327-123">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ac327-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-124">Örnek 2: (yalnızca Windows PowerShell 5,1) kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure 'a bağlanın</span><span class="sxs-lookup"><span data-stu-id="ac327-124">Example 2: (Windows PowerShell 5.1 only) Connect to Azure using organizational ID credentials</span></span>

<span data-ttu-id="ac327-125">Bu senaryo yalnızca Windows PowerShell 5,1 ' de çalışır.</span><span class="sxs-lookup"><span data-stu-id="ac327-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="ac327-126">İlk komut Kullanıcı kimlik bilgilerini sorar ve bunları `$Credential` değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="ac327-126">The first command prompts for user credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="ac327-127">İkinci komut, uygulamasında depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="ac327-127">The second command connects to an Azure account using the credentials stored in `$Credential`.</span></span> <span data-ttu-id="ac327-128">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="ac327-128">This account authenticates with Azure using organizational ID credentials.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-129">Örnek 3: hizmet sorumlusu hesabını kullanarak Azure 'a bağlanma</span><span class="sxs-lookup"><span data-stu-id="ac327-129">Example 3: Connect to Azure using a service principal account</span></span>

<span data-ttu-id="ac327-130">İlk komut hizmet sorumlusu kimlik bilgilerini sorar ve bunları `$Credential` değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="ac327-130">The first command prompts for service principal credentials and stores them in the `$Credential` variable.</span></span> <span data-ttu-id="ac327-131">İstendiğinde Kullanıcı adı ve hizmet sorumlusu parolası için uygulama KIMLIĞINIZI girin.</span><span class="sxs-lookup"><span data-stu-id="ac327-131">Enter your application ID for the username and service principal secret as the password when prompted.</span></span> <span data-ttu-id="ac327-132">İkinci komut belirtilen Azure kiracısına, değişkende depolanan hizmet sorumlusu kimlik bilgilerini kullanarak bağlanır `$Credential` .</span><span class="sxs-lookup"><span data-stu-id="ac327-132">The second command connects the specified Azure tenant using the service principal credentials stored in the `$Credential` variable.</span></span> <span data-ttu-id="ac327-133">**ServicePrincipal** Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac327-133">The **ServicePrincipal** switch parameter indicates that the account authenticates as a service principal.</span></span>

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-134">Örnek 4: belirli bir kiracıya ve aboneliğe bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="ac327-134">Example 4: Use an interactive login to connect to a specific tenant and subscription</span></span>

<span data-ttu-id="ac327-135">Bu örnek belirtilen kiracı ve abonelikle bir Azure hesabına bağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="ac327-135">This example connects to an Azure account with the specified tenant and subscription.</span></span>

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-136">Örnek 5: yönetilen hizmet kimliği kullanarak bağlanma</span><span class="sxs-lookup"><span data-stu-id="ac327-136">Example 5: Connect using a Managed Service Identity</span></span>

<span data-ttu-id="ac327-137">Bu örnekte, ana bilgisayar ortamının yönetilen hizmet kimliği (MSI) kullanılarak bağlantı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-137">This example connects using the Managed Service Identity (MSI) of the host environment.</span></span> <span data-ttu-id="ac327-138">Örneğin, atanmış MSI 'si olan bir sanal makineden Azure 'da oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac327-138">For example, you sign into Azure from a virtual machine that has an assigned MSI.</span></span>

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-139">Örnek 6: yönetilen hizmet kimliği oturum açma ve ClientID kullanarak bağlanma</span><span class="sxs-lookup"><span data-stu-id="ac327-139">Example 6: Connect using Managed Service Identity login and ClientId</span></span>

<span data-ttu-id="ac327-140">Bu örnekte **Myuseratanandentity** yönetilen hizmet kimliği kullanılarak bağlantı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-140">This example connects using the Managed Service Identity of **myUserAssignedIdentity**.</span></span> <span data-ttu-id="ac327-141">Kullanıcı tarafından atanan kimliği sanal makineye ekler, ardından Kullanıcı tarafından atanan kimliğin ClientID kullanarak bağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-141">It adds the user assigned identity to the virtual machine, then connects using the ClientId of the user assigned identity.</span></span> <span data-ttu-id="ac327-142">Daha fazla bilgi için, [Azure VM 'de Azure kaynakları için yönetilen kimlikleri yapılandırma](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="ac327-142">For more information, see [Configure managed identities for Azure resources on an Azure VM](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).</span></span>

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### <span data-ttu-id="ac327-143">Örnek 7: sertifikaları kullanarak bağlanma</span><span class="sxs-lookup"><span data-stu-id="ac327-143">Example 7: Connect using certificates</span></span>

<span data-ttu-id="ac327-144">Bu örnek, sertifika tabanlı hizmet sorumlusu kimlik doğrulamasını kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="ac327-144">This example connects to an Azure account using certificate-based service principal authentication.</span></span>
<span data-ttu-id="ac327-145">Kimlik doğrulaması için kullanılan hizmet sorumlusu belirtilen sertifikayla oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac327-145">The service principal used for authentication must be created with the specified certificate.</span></span> <span data-ttu-id="ac327-146">Kendinden imzalanan sertifikalar oluşturma ve onlara izinler atama hakkında daha fazla bilgi için, [sertifika](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span><span class="sxs-lookup"><span data-stu-id="ac327-146">For more information on creating a self-signed certificates and assigning them permissions, see [Use Azure PowerShell to create a service principal with a certificate](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)</span></span>

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## <span data-ttu-id="ac327-147">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac327-147">PARAMETERS</span></span>

### <span data-ttu-id="ac327-148">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="ac327-148">-AccessToken</span></span>

<span data-ttu-id="ac327-149">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac327-149">Specifies an access token.</span></span>

> [!CAUTION]
> <span data-ttu-id="ac327-150">Erişim belirteçleri bir kimlik bilgisi türüdür.</span><span class="sxs-lookup"><span data-stu-id="ac327-150">Access tokens are a type of credential.</span></span> <span data-ttu-id="ac327-151">Gizli tutmak için uygun güvenlik önlemleri almalısınız.</span><span class="sxs-lookup"><span data-stu-id="ac327-151">You should take the appropriate security precautions to keep them confidential.</span></span> <span data-ttu-id="ac327-152">Access belirteçleri Ayrıca zaman aşımına uğramaz ve çalışmakta olan görevlerin tamamlanmasını önleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ac327-152">Access tokens also timeout and may prevent long running tasks from completing.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-153">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ac327-153">-AccountId</span></span>

<span data-ttu-id="ac327-154">**Accessstoken** parametre kümesindeki erişim BELIRTECININ hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="ac327-154">Account ID for access token in **AccessToken** parameter set.</span></span> <span data-ttu-id="ac327-155">**Managedservice** parametre kümesindeki yönetilen HIZMETIN hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="ac327-155">Account ID for managed service in **ManagedService** parameter set.</span></span> <span data-ttu-id="ac327-156">Yönetilen hizmet kaynak KIMLIĞI veya ilişkili istemci KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac327-156">Can be a managed service resource ID, or the associated client ID.</span></span>
<span data-ttu-id="ac327-157">Sistem tarafından atanan kimliği kullanmak için bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="ac327-157">To use the system assigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ac327-158">-ApplicationId</span></span>

<span data-ttu-id="ac327-159">Hizmet sorumlusunun uygulama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ac327-159">Application ID of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-160">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ac327-160">-CertificateThumbprint</span></span>

<span data-ttu-id="ac327-161">Sertifika karması veya Parmak Izi.</span><span class="sxs-lookup"><span data-stu-id="ac327-161">Certificate Hash or Thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-162">-ContextName</span><span class="sxs-lookup"><span data-stu-id="ac327-162">-ContextName</span></span>

<span data-ttu-id="ac327-163">Bu oturum açma için varsayılan Azure bağlamının adı.</span><span class="sxs-lookup"><span data-stu-id="ac327-163">Name of the default Azure context for this login.</span></span> <span data-ttu-id="ac327-164">Azure bağlamları hakkında daha fazla bilgi için, [bkz.](/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="ac327-164">For more information about Azure contexts, see [Azure PowerShell context objects](/powershell/azure/context-persistence).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-165">-Credential</span><span class="sxs-lookup"><span data-stu-id="ac327-165">-Credential</span></span>

<span data-ttu-id="ac327-166">**PSCredential** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac327-166">Specifies a **PSCredential** object.</span></span> <span data-ttu-id="ac327-167">**PSCredential** nesnesi hakkında daha fazla bilgi için, yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ac327-167">For more information about the **PSCredential** object, type `Get-Help Get-Credential`.</span></span> <span data-ttu-id="ac327-168">**PSCredential** NESNESI kuruluş kimliği kimlik bilgileri IÇIN Kullanıcı kimliği ve parola veya hizmet sorumlusu kimlik bilgileri IÇIN uygulama kimliği ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ac327-168">The **PSCredential** object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac327-169">-DefaultProfile</span></span>

<span data-ttu-id="ac327-170">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac327-170">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac327-171">-Ortam</span><span class="sxs-lookup"><span data-stu-id="ac327-171">-Environment</span></span>

<span data-ttu-id="ac327-172">Azure hesabını içeren ortam.</span><span class="sxs-lookup"><span data-stu-id="ac327-172">Environment containing the Azure account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-173">-Force</span><span class="sxs-lookup"><span data-stu-id="ac327-173">-Force</span></span>

<span data-ttu-id="ac327-174">Aynı ada sormadan var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="ac327-174">Overwrite the existing context with the same name without prompting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-175">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ac327-175">-GraphAccessToken</span></span>

<span data-ttu-id="ac327-176">Grafik Hizmeti için AccessToken.</span><span class="sxs-lookup"><span data-stu-id="ac327-176">AccessToken for Graph Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-177">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="ac327-177">-Identity</span></span>

<span data-ttu-id="ac327-178">Yönetilen hizmet kimliği kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ac327-178">Login using a Managed Service Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-179">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="ac327-179">-KeyVaultAccessToken</span></span>

<span data-ttu-id="ac327-180">Keykasa hizmeti için AccessToken.</span><span class="sxs-lookup"><span data-stu-id="ac327-180">AccessToken for KeyVault Service.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-181">-Managedserviceanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="ac327-181">-ManagedServiceHostName</span></span>

<span data-ttu-id="ac327-182">Yönetilen hizmetin ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="ac327-182">Host name for the managed service.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-183">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="ac327-183">-ManagedServicePort</span></span>

<span data-ttu-id="ac327-184">Yönetilen hizmetin bağlantı noktası numarası.</span><span class="sxs-lookup"><span data-stu-id="ac327-184">Port number for the managed service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-185">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="ac327-185">-ManagedServiceSecret</span></span>

<span data-ttu-id="ac327-186">Yönetilen hizmet oturumu simgesi.</span><span class="sxs-lookup"><span data-stu-id="ac327-186">Token for the managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-187">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="ac327-187">-Scope</span></span>

<span data-ttu-id="ac327-188">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="ac327-188">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-189">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ac327-189">-ServicePrincipal</span></span>

<span data-ttu-id="ac327-190">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac327-190">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-191">-Skipcontextpopülasyonu</span><span class="sxs-lookup"><span data-stu-id="ac327-191">-SkipContextPopulation</span></span>

<span data-ttu-id="ac327-192">İçerik oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="ac327-192">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-193">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="ac327-193">-SkipValidation</span></span>

<span data-ttu-id="ac327-194">Erişim belirtecinin doğrulanmasını atlayın.</span><span class="sxs-lookup"><span data-stu-id="ac327-194">Skip validation for access token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-195">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="ac327-195">-Subscription</span></span>

<span data-ttu-id="ac327-196">Abonelik adı veya KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ac327-196">Subscription Name or ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-197">-Tenant</span><span class="sxs-lookup"><span data-stu-id="ac327-197">-Tenant</span></span>

<span data-ttu-id="ac327-198">İsteğe bağlı kiracı adı veya KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ac327-198">Optional tenant name or ID.</span></span>

> [!NOTE]
> <span data-ttu-id="ac327-199">Geçerli API sınırlamaları nedeniyle, işletmeler arası (B2B) bir hesap ile bağlantı oluştururken kiracı adı yerine kiracı KIMLIĞI kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ac327-199">Due to limitations of the current API, you must use a tenant ID instead of a tenant name when connecting with a business-to-business (B2B) account.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-200">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ac327-200">-UseDeviceAuthentication</span></span>

<span data-ttu-id="ac327-201">Tarayıcı denetimi yerine cihaz kodu kimlik doğrulaması kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac327-201">Use device code authentication instead of a browser control.</span></span> <span data-ttu-id="ac327-202">Bu, PowerShell sürüm 6 ve üzeri için varsayılan kimlik doğrulama türüdür.</span><span class="sxs-lookup"><span data-stu-id="ac327-202">This is the default authentication type for PowerShell version 6 and higher.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-203">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac327-203">-Confirm</span></span>

<span data-ttu-id="ac327-204">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac327-204">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac327-205">-WhatIf</span></span>

<span data-ttu-id="ac327-206">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac327-206">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac327-207">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac327-207">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac327-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac327-208">CommonParameters</span></span>

<span data-ttu-id="ac327-209">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac327-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac327-210">Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.</span><span class="sxs-lookup"><span data-stu-id="ac327-210">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
<span data-ttu-id="ac327-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac327-211">(http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac327-212">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac327-212">INPUTS</span></span>

### <span data-ttu-id="ac327-213">System. String</span><span class="sxs-lookup"><span data-stu-id="ac327-213">System.String</span></span>

## <span data-ttu-id="ac327-214">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac327-214">OUTPUTS</span></span>

### <span data-ttu-id="ac327-215">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ac327-215">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ac327-216">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac327-216">NOTES</span></span>

## <span data-ttu-id="ac327-217">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac327-217">RELATED LINKS</span></span>
