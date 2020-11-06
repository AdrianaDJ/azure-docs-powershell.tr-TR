---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573385"
---
# <span data-ttu-id="016b9-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="016b9-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="016b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="016b9-102">SYNOPSIS</span></span>
<span data-ttu-id="016b9-103">Azure Resource Manager cmdlet istekleriyle kullanmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanın.</span><span class="sxs-lookup"><span data-stu-id="016b9-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="016b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="016b9-104">SYNTAX</span></span>

### <span data-ttu-id="016b9-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="016b9-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="016b9-106">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="016b9-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="016b9-107">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="016b9-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="016b9-108">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="016b9-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="016b9-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="016b9-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="016b9-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="016b9-110">DESCRIPTION</span></span>
<span data-ttu-id="016b9-111">Connect-AzureRmAccount cmdlet 'i Azure Resource Manager cmdlet istekleriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="016b9-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="016b9-112">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="016b9-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="016b9-113">Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="016b9-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="016b9-114">Bu cmdlet 'i çalıştırdıktan sonra, bağlantısı kesildi-AzureRmAccount kullanarak bir Azure hesabından bağlantınızı kesebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="016b9-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="016b9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="016b9-115">EXAMPLES</span></span>

### <span data-ttu-id="016b9-116">Örnek 1: Azure hesabına bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="016b9-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="016b9-117">Bu komut bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="016b9-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="016b9-118">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="016b9-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="016b9-119">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="016b9-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="016b9-120">Örnek 2: kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="016b9-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="016b9-121">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="016b9-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="016b9-122">İkinci komut $Credential depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="016b9-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="016b9-123">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="016b9-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="016b9-124">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="016b9-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="016b9-125">Örnek 3: Azure hizmet sorumlusu hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="016b9-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="016b9-126">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="016b9-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="016b9-127">İkinci komut, belirtilen kiracı için $Credential depolanan hizmet sorumlusu kimlik bilgilerini kullanarak Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="016b9-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="016b9-128">ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="016b9-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="016b9-129">Örnek 4: belirli bir kiracı ve aboneliğe yönelik bir hesaba bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="016b9-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="016b9-130">Bu komut bir Azure hesabına bağlanır ve varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için AzureRM PowerShell 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="016b9-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="016b9-131">Örnek 5: yönetilen hizmet kimliği oturum kimliğini kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="016b9-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="016b9-132">Bu komut, ana bilgisayar ortamının yönetilen hizmet kimliğini kullanarak oturum açar (örneğin, atanmış yönetilen hizmet kimliğine sahip bir Virtuverme hizmeti</span><span class="sxs-lookup"><span data-stu-id="016b9-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="016b9-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="016b9-133">PARAMETERS</span></span>

### <span data-ttu-id="016b9-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="016b9-134">-AccessToken</span></span>
<span data-ttu-id="016b9-135">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="016b9-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="016b9-136">-AccountId</span></span>
<span data-ttu-id="016b9-137">Erişim belirtecinin hesap kimliği</span><span class="sxs-lookup"><span data-stu-id="016b9-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="016b9-138">-ApplicationId</span></span>
<span data-ttu-id="016b9-139">'SI</span><span class="sxs-lookup"><span data-stu-id="016b9-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="016b9-140">-CertificateThumbprint</span></span>
<span data-ttu-id="016b9-141">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="016b9-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-142">-ContextName</span><span class="sxs-lookup"><span data-stu-id="016b9-142">-ContextName</span></span>
<span data-ttu-id="016b9-143">Bu oturumun varsayılan bağlamının adı.</span><span class="sxs-lookup"><span data-stu-id="016b9-143">Name of the default context from this login.</span></span>  <span data-ttu-id="016b9-144">Oturum açtıktan sonra bu bağlamı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="016b9-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-145">-Credential</span><span class="sxs-lookup"><span data-stu-id="016b9-145">-Credential</span></span>
<span data-ttu-id="016b9-146">PSCredential nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="016b9-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="016b9-147">PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.</span><span class="sxs-lookup"><span data-stu-id="016b9-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="016b9-148">PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="016b9-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016b9-149">-DefaultProfile</span></span>
<span data-ttu-id="016b9-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="016b9-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-151">-Ortam</span><span class="sxs-lookup"><span data-stu-id="016b9-151">-Environment</span></span>
<span data-ttu-id="016b9-152">Oturum açacak hesabı içeren ortam</span><span class="sxs-lookup"><span data-stu-id="016b9-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-153">-Force</span><span class="sxs-lookup"><span data-stu-id="016b9-153">-Force</span></span>
<span data-ttu-id="016b9-154">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="016b9-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="016b9-155">-GraphAccessToken</span></span>
<span data-ttu-id="016b9-156">Grafik Hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="016b9-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-157">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="016b9-157">-Identity</span></span>
<span data-ttu-id="016b9-158">Geçerli ortamdaki yönetilen hizmet kimliğini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="016b9-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="016b9-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="016b9-160">Keykasa hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="016b9-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-161">-Managedserviceanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="016b9-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="016b9-162">Yönetilen hizmet oturumu ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="016b9-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="016b9-163">-ManagedServicePort</span></span>
<span data-ttu-id="016b9-164">Yönetilen hizmet oturumu açma bağlantı noktası numarası</span><span class="sxs-lookup"><span data-stu-id="016b9-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-165">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="016b9-165">-Scope</span></span>
<span data-ttu-id="016b9-166">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="016b9-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="016b9-167">-ServicePrincipal</span></span>
<span data-ttu-id="016b9-168">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="016b9-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="016b9-169">-SkipValidation</span></span>
<span data-ttu-id="016b9-170">Erişim belirteci için doğrulamayı atlama</span><span class="sxs-lookup"><span data-stu-id="016b9-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-171">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="016b9-171">-Subscription</span></span>
<span data-ttu-id="016b9-172">Abonelik adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="016b9-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-173">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="016b9-173">-TenantId</span></span>
<span data-ttu-id="016b9-174">İsteğe bağlı kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="016b9-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="016b9-175">-Confirm</span></span>
<span data-ttu-id="016b9-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="016b9-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="016b9-177">-WhatIf</span></span>
<span data-ttu-id="016b9-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="016b9-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="016b9-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="016b9-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016b9-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016b9-180">CommonParameters</span></span>
<span data-ttu-id="016b9-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="016b9-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016b9-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016b9-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016b9-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="016b9-183">INPUTS</span></span>

### <span data-ttu-id="016b9-184">Dizisi</span><span class="sxs-lookup"><span data-stu-id="016b9-184">String</span></span>
<span data-ttu-id="016b9-185">' SubscriptionID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="016b9-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="016b9-186">Dizisi</span><span class="sxs-lookup"><span data-stu-id="016b9-186">String</span></span>
<span data-ttu-id="016b9-187">' SubscriptionName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="016b9-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="016b9-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="016b9-188">OUTPUTS</span></span>

### <span data-ttu-id="016b9-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="016b9-189">PSAzureProfile</span></span>
<span data-ttu-id="016b9-190">Oturum açan kullanıcının kimlik bilgileri, aboneliği, hesap ve kiracı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="016b9-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="016b9-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="016b9-191">NOTES</span></span>

## <span data-ttu-id="016b9-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="016b9-192">RELATED LINKS</span></span>

