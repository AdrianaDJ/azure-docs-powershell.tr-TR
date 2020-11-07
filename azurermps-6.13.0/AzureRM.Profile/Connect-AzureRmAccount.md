---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764601"
---
# <span data-ttu-id="a6ab1-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="a6ab1-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="a6ab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ab1-103">Azure Resource Manager cmdlet istekleriyle kullanmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanın.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6ab1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6ab1-104">SYNTAX</span></span>

### <span data-ttu-id="a6ab1-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6ab1-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ab1-106">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a6ab1-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ab1-107">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a6ab1-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ab1-108">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a6ab1-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ab1-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="a6ab1-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6ab1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6ab1-110">DESCRIPTION</span></span>
<span data-ttu-id="a6ab1-111">Connect-AzureRmAccount cmdlet 'i Azure Resource Manager cmdlet istekleriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="a6ab1-112">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="a6ab1-113">Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="a6ab1-114">Geçerli Kullanıcı için herhangi bir içerik bulunmazsa, bu komut kullanıcının bağlam listesini (ilk 25) aboneliklerinin her biri için bir içerikle doldurur.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="a6ab1-115">Kullanıcı için oluşturulan bağlamlar listesi, "Get-AzureRmContext-ListAvailable" çalıştırılarak bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="a6ab1-116">Bu bağlam popülasyonu atlamak için, bu komutu "-Skipcontextpopülasyonu" anahtar parametresiyle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="a6ab1-117">Bu cmdlet 'i çalıştırdıktan sonra, bağlantısı kesildi-AzureRmAccount kullanarak bir Azure hesabından bağlantınızı kesebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="a6ab1-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6ab1-118">EXAMPLES</span></span>

### <span data-ttu-id="a6ab1-119">Örnek 1: Azure hesabına bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="a6ab1-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a6ab1-120">Bu komut bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="a6ab1-121">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="a6ab1-122">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="a6ab1-123">Örnek 2: kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="a6ab1-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a6ab1-124">İlk komut Kullanıcı kimlik bilgilerini (Kullanıcı adı ve parola) sorar ve sonra bunları $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="a6ab1-125">İkinci komut $Credential depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="a6ab1-126">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="a6ab1-127">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="a6ab1-128">Örnek 3: Azure hizmet sorumlusu hesabına bağlanma</span><span class="sxs-lookup"><span data-stu-id="a6ab1-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a6ab1-129">İlk komut, hizmet sorumlusu kimlik bilgilerini (uygulama kimliği ve hizmet sorumlusu parolası) alır ve bunları $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="a6ab1-130">İkinci komut, belirtilen kiracı için $Credential depolanan hizmet sorumlusu kimlik bilgilerini kullanarak Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="a6ab1-131">ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="a6ab1-132">Örnek 4: belirli bir kiracı ve aboneliğe yönelik bir hesaba bağlanmak için etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="a6ab1-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a6ab1-133">Bu komut bir Azure hesabına bağlanır ve varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için AzureRM PowerShell 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="a6ab1-134">Örnek 5: yönetilen hizmet kimliği oturum kimliğini kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="a6ab1-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a6ab1-135">Bu komut, ana bilgisayar ortamının yönetilen hizmet kimliğini kullanarak bağlanır (örneğin, atanmış yönetilen hizmet kimliğine sahip bir Virtuveren hizmeti</span><span class="sxs-lookup"><span data-stu-id="a6ab1-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="a6ab1-136">Örnek 6: sertifikaları kullanarak hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="a6ab1-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="a6ab1-137">Bu komut, sertifika tabanlı hizmet sorumlusu kimlik doğrulamasını kullanarak bir Azure hesabına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="a6ab1-138">Kimlik doğrulaması için kullanılan hizmet sorumlusu, verilen sertifikayla oluşturulmuş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="a6ab1-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6ab1-139">PARAMETERS</span></span>

### <span data-ttu-id="a6ab1-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="a6ab1-140">-AccessToken</span></span>
<span data-ttu-id="a6ab1-141">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="a6ab1-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="a6ab1-142">-AccountId</span></span>
<span data-ttu-id="a6ab1-143">Erişim belirtecinin hesap kimliği</span><span class="sxs-lookup"><span data-stu-id="a6ab1-143">Account Id for access token</span></span>

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

### <span data-ttu-id="a6ab1-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a6ab1-144">-ApplicationId</span></span>
<span data-ttu-id="a6ab1-145">'SI</span><span class="sxs-lookup"><span data-stu-id="a6ab1-145">SPN</span></span>

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

### <span data-ttu-id="a6ab1-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="a6ab1-146">-CertificateThumbprint</span></span>
<span data-ttu-id="a6ab1-147">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="a6ab1-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="a6ab1-148">-ContextName</span><span class="sxs-lookup"><span data-stu-id="a6ab1-148">-ContextName</span></span>
<span data-ttu-id="a6ab1-149">Bu oturumun varsayılan bağlamının adı.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-149">Name of the default context from this login.</span></span>  <span data-ttu-id="a6ab1-150">Oturum açtıktan sonra bu bağlamı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="a6ab1-151">-Credential</span><span class="sxs-lookup"><span data-stu-id="a6ab1-151">-Credential</span></span>
<span data-ttu-id="a6ab1-152">PSCredential nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="a6ab1-153">PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="a6ab1-154">PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ab1-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ab1-155">-DefaultProfile</span></span>
<span data-ttu-id="a6ab1-156">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6ab1-157">-Ortam</span><span class="sxs-lookup"><span data-stu-id="a6ab1-157">-Environment</span></span>
<span data-ttu-id="a6ab1-158">Oturum açacak hesabı içeren ortam</span><span class="sxs-lookup"><span data-stu-id="a6ab1-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="a6ab1-159">-Force</span><span class="sxs-lookup"><span data-stu-id="a6ab1-159">-Force</span></span>
<span data-ttu-id="a6ab1-160">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="a6ab1-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="a6ab1-161">-GraphAccessToken</span></span>
<span data-ttu-id="a6ab1-162">Grafik Hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="a6ab1-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="a6ab1-163">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="a6ab1-163">-Identity</span></span>
<span data-ttu-id="a6ab1-164">Geçerli ortamdaki yönetilen hizmet kimliğini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="a6ab1-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="a6ab1-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="a6ab1-166">Keykasa hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="a6ab1-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="a6ab1-167">-Managedserviceanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="a6ab1-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="a6ab1-168">Yönetilen hizmet oturumu ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="a6ab1-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="a6ab1-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="a6ab1-169">-ManagedServicePort</span></span>
<span data-ttu-id="a6ab1-170">Yönetilen hizmet oturumu açma bağlantı noktası numarası</span><span class="sxs-lookup"><span data-stu-id="a6ab1-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="a6ab1-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="a6ab1-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="a6ab1-172">Gizli, yönetilen hizmet oturumu türleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="a6ab1-173">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a6ab1-173">-Scope</span></span>
<span data-ttu-id="a6ab1-174">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a6ab1-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a6ab1-175">-ServicePrincipal</span></span>
<span data-ttu-id="a6ab1-176">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="a6ab1-177">-Skipcontextpopülasyonu</span><span class="sxs-lookup"><span data-stu-id="a6ab1-177">-SkipContextPopulation</span></span>
<span data-ttu-id="a6ab1-178">İçerik oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="a6ab1-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="a6ab1-179">-SkipValidation</span></span>
<span data-ttu-id="a6ab1-180">Erişim belirteci için doğrulamayı atlama</span><span class="sxs-lookup"><span data-stu-id="a6ab1-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="a6ab1-181">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="a6ab1-181">-Subscription</span></span>
<span data-ttu-id="a6ab1-182">Abonelik adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="a6ab1-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="a6ab1-183">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a6ab1-183">-TenantId</span></span>
<span data-ttu-id="a6ab1-184">İsteğe bağlı etki alanı adı veya kiracı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="a6ab1-185">Tüm oturum açma durumlarında etki alanı adı çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="a6ab1-186">Bulut çözümü sağlayıcısı (CSP) oturum açma, kiracı KIMLIĞI gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ab1-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6ab1-187">-Confirm</span></span>
<span data-ttu-id="a6ab1-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ab1-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ab1-189">-WhatIf</span></span>
<span data-ttu-id="a6ab1-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6ab1-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ab1-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ab1-192">CommonParameters</span></span>
<span data-ttu-id="a6ab1-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6ab1-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ab1-194">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ab1-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ab1-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6ab1-195">INPUTS</span></span>

### <span data-ttu-id="a6ab1-196">System. String</span><span class="sxs-lookup"><span data-stu-id="a6ab1-196">System.String</span></span>
<span data-ttu-id="a6ab1-197">Parametreler: abonelik (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6ab1-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="a6ab1-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6ab1-198">OUTPUTS</span></span>

### <span data-ttu-id="a6ab1-199">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a6ab1-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="a6ab1-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6ab1-200">NOTES</span></span>

## <span data-ttu-id="a6ab1-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6ab1-201">RELATED LINKS</span></span>
