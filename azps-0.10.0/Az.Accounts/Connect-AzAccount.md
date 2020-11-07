---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935274"
---
# <span data-ttu-id="6fa4a-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6fa4a-101">Connect-AzAccount</span></span>

## <span data-ttu-id="6fa4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa4a-103">Azure Resource Manager cmdlet istekleriyle kullanmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="6fa4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fa4a-104">SYNTAX</span></span>

### <span data-ttu-id="6fa4a-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fa4a-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa4a-106">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="6fa4a-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fa4a-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="6fa4a-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fa4a-108">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="6fa4a-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fa4a-109">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="6fa4a-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fa4a-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="6fa4a-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fa4a-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fa4a-111">DESCRIPTION</span></span>
<span data-ttu-id="6fa4a-112">Connect-AzAccount cmdlet 'i Azure Resource Manager cmdlet istekleriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="6fa4a-113">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="6fa4a-114">Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzAccount veya Import-AzPublishSettingsFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="6fa4a-115">Geçerli Kullanıcı için herhangi bir içerik bulunmazsa, bu komut kullanıcının bağlam listesini (ilk 25) aboneliklerinin her biri için bir içerikle doldurur.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="6fa4a-116">Kullanıcı için oluşturulan bağlamlar listesi, "Get-AzContext-ListAvailable" çalıştırılarak bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="6fa4a-117">Bu bağlam popülasyonu atlamak için, bu komutu "-Skipcontextpopülasyonu" anahtar parametresiyle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="6fa4a-118">Bu cmdlet 'i çalıştırdıktan sonra, bağlantınızı kesmeniz-Azhesap kullanarak Azure hesabından bağlantınızı kesebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="6fa4a-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fa4a-119">EXAMPLES</span></span>

### <span data-ttu-id="6fa4a-120">Örnek 1: Azure hesabına bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="6fa4a-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-121">Bu komut bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="6fa4a-122">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="6fa4a-123">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="6fa4a-124">Örnek 2: (yalnızca Windows PowerShell 5,1) kuruluş KIMLIĞI kimlik bilgilerini kullanarak bir Azure hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="6fa4a-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-125">Bu senaryo yalnızca Windows PowerShell 5,1 ' de çalışır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="6fa4a-126">İlk komut Kullanıcı kimlik bilgilerini (Kullanıcı adı ve parola) sorar ve sonra bunları $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="6fa4a-127">İkinci komut $Credential depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="6fa4a-128">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="6fa4a-129">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="6fa4a-130">Örnek 3: Azure hizmet sorumlusu hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="6fa4a-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-131">İlk komut, hizmet sorumlusu kimlik bilgilerini (uygulama kimliği ve hizmet sorumlusu parolası) alır ve bunları $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="6fa4a-132">İkinci komut, belirtilen kiracı için $Credential depolanan hizmet sorumlusu kimlik bilgilerini kullanarak Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="6fa4a-133">ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="6fa4a-134">Örnek 4: belirli bir kiracı ve aboneliğe yönelik bir hesaba bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="6fa4a-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-135">Bu komut bir Azure hesabına bağlanır ve varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için AzureRM PowerShell 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="6fa4a-136">Örnek 5: yönetilen hizmet kimliği oturum kimliğini kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="6fa4a-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-137">Bu komut, ana bilgisayar ortamının yönetilen hizmet kimliğini kullanarak bağlanır (örneğin, atanmış yönetilen hizmet kimliğine sahip bir Virtuveren hizmeti</span><span class="sxs-lookup"><span data-stu-id="6fa4a-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="6fa4a-138">Örnek 6: yönetilen hizmet kimliği oturum açma ve ClientID kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="6fa4a-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-139">Bu komut, Kullanıcı tarafından atanan kimliği sanal makineye ekleyerek "Myuseratanandentity" yönetilen hizmet kimliğini kullanarak bağlantı kurar ve Kullanıcı tarafından atanan kimliğin ClientID kullanarak bağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="6fa4a-140">Yönetilen kimlikleri yapılandırma hakkında daha fazla bilgi buradan bulunabilir: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="6fa4a-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="6fa4a-141">Örnek 7: yönetilen hizmet kimliği oturum açma ve ClientID kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="6fa4a-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-142">Bu komut, Kullanıcı tarafından atanan kimliği sanal makineye ekleyerek "Myuseratanandentity" yönetilen hizmet kimliğini kullanarak bağlantı kurar ve Kullanıcı tarafından atanan kimliğin kimliğini kullanarak bağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="6fa4a-143">Yönetilen kimlikleri yapılandırma hakkında daha fazla bilgi buradan bulunabilir: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="6fa4a-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="6fa4a-144">Örnek 8: sertifikaları kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="6fa4a-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="6fa4a-145">Bu komut, sertifika tabanlı hizmet sorumlusu kimlik doğrulamasını kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="6fa4a-146">Kimlik doğrulaması için kullanılan hizmet sorumlusu, verilen sertifikayla oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="6fa4a-147">Örnek 9: AccessToken kimlik doğrulamasını kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="6fa4a-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="6fa4a-148">Bu komut, AccessToken ve KeyVaultAccessToken kullanılarak "AccountID" içinde belirtilen bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="6fa4a-149">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fa4a-149">PARAMETERS</span></span>

### <span data-ttu-id="6fa4a-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="6fa4a-150">-AccessToken</span></span>
<span data-ttu-id="6fa4a-151">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-151">Specifies an access token.</span></span>

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

### <span data-ttu-id="6fa4a-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="6fa4a-152">-AccountId</span></span>
<span data-ttu-id="6fa4a-153">Accessstoken parametre kümesindeki erişim belirtecinin hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="6fa4a-154">ManagedService parametre kümesindeki yönetilen hizmetin hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="6fa4a-155">Yönetilen hizmet kaynak kimliği veya ilişkili istemci kimliği olabilir. SystemAssigned kimliğini kullanmak için bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

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

### <span data-ttu-id="6fa4a-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6fa4a-156">-ApplicationId</span></span>
<span data-ttu-id="6fa4a-157">'SI</span><span class="sxs-lookup"><span data-stu-id="6fa4a-157">SPN</span></span>

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

### <span data-ttu-id="6fa4a-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6fa4a-158">-CertificateThumbprint</span></span>
<span data-ttu-id="6fa4a-159">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="6fa4a-159">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="6fa4a-160">-ContextName</span><span class="sxs-lookup"><span data-stu-id="6fa4a-160">-ContextName</span></span>
<span data-ttu-id="6fa4a-161">Bu oturumun varsayılan bağlamının adı.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-161">Name of the default context from this login.</span></span>  <span data-ttu-id="6fa4a-162">Oturum açtıktan sonra bu bağlamı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-162">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="6fa4a-163">-Credential</span><span class="sxs-lookup"><span data-stu-id="6fa4a-163">-Credential</span></span>
<span data-ttu-id="6fa4a-164">PSCredential nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="6fa4a-165">PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="6fa4a-166">PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="6fa4a-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa4a-167">-DefaultProfile</span></span>
<span data-ttu-id="6fa4a-168">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fa4a-169">-Ortam</span><span class="sxs-lookup"><span data-stu-id="6fa4a-169">-Environment</span></span>
<span data-ttu-id="6fa4a-170">Oturum açacak hesabı içeren ortam</span><span class="sxs-lookup"><span data-stu-id="6fa4a-170">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="6fa4a-171">-Force</span><span class="sxs-lookup"><span data-stu-id="6fa4a-171">-Force</span></span>
<span data-ttu-id="6fa4a-172">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-172">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="6fa4a-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="6fa4a-173">-GraphAccessToken</span></span>
<span data-ttu-id="6fa4a-174">Grafik Hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="6fa4a-174">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="6fa4a-175">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="6fa4a-175">-Identity</span></span>
<span data-ttu-id="6fa4a-176">Geçerli ortamdaki yönetilen hizmet kimliğini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-176">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="6fa4a-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="6fa4a-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="6fa4a-178">Keykasa hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="6fa4a-178">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="6fa4a-179">-Managedserviceanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="6fa4a-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="6fa4a-180">Yönetilen hizmet oturumu ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="6fa4a-180">Host name for managed service login</span></span>

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

### <span data-ttu-id="6fa4a-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="6fa4a-181">-ManagedServicePort</span></span>
<span data-ttu-id="6fa4a-182">Yönetilen hizmet oturumu açma bağlantı noktası numarası</span><span class="sxs-lookup"><span data-stu-id="6fa4a-182">Port number for managed service login</span></span>

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

### <span data-ttu-id="6fa4a-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="6fa4a-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="6fa4a-184">Gizli, yönetilen hizmet oturumu türleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-184">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="6fa4a-185">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6fa4a-185">-Scope</span></span>
<span data-ttu-id="6fa4a-186">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="6fa4a-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fa4a-187">-ServicePrincipal</span></span>
<span data-ttu-id="6fa4a-188">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="6fa4a-189">-Skipcontextpopülasyonu</span><span class="sxs-lookup"><span data-stu-id="6fa4a-189">-SkipContextPopulation</span></span>
<span data-ttu-id="6fa4a-190">İçerik oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-190">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="6fa4a-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="6fa4a-191">-SkipValidation</span></span>
<span data-ttu-id="6fa4a-192">Erişim belirteci için doğrulamayı atlama</span><span class="sxs-lookup"><span data-stu-id="6fa4a-192">Skip validation for access token</span></span>

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

### <span data-ttu-id="6fa4a-193">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="6fa4a-193">-Subscription</span></span>
<span data-ttu-id="6fa4a-194">Abonelik adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="6fa4a-194">Subscription Name or ID</span></span>

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

### <span data-ttu-id="6fa4a-195">-Tenant</span><span class="sxs-lookup"><span data-stu-id="6fa4a-195">-Tenant</span></span>
<span data-ttu-id="6fa4a-196">İsteğe bağlı kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="6fa4a-196">Optional tenant name or ID</span></span>

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

### <span data-ttu-id="6fa4a-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="6fa4a-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="6fa4a-198">Tarayıcı denetimi yerine cihaz kodu kimlik doğrulamasını kullanma</span><span class="sxs-lookup"><span data-stu-id="6fa4a-198">Use device code authentication instead of a browser control</span></span>

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

### <span data-ttu-id="6fa4a-199">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fa4a-199">-Confirm</span></span>
<span data-ttu-id="6fa4a-200">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fa4a-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa4a-201">-WhatIf</span></span>
<span data-ttu-id="6fa4a-202">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fa4a-203">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fa4a-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa4a-204">CommonParameters</span></span>
<span data-ttu-id="6fa4a-205">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa4a-206">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fa4a-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa4a-207">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fa4a-207">INPUTS</span></span>

### <span data-ttu-id="6fa4a-208">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa4a-208">System.String</span></span>

## <span data-ttu-id="6fa4a-209">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fa4a-209">OUTPUTS</span></span>

### <span data-ttu-id="6fa4a-210">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="6fa4a-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="6fa4a-211">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fa4a-211">NOTES</span></span>

## <span data-ttu-id="6fa4a-212">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fa4a-212">RELATED LINKS</span></span>
