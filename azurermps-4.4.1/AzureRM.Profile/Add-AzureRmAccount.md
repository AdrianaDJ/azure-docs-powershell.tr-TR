---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594208"
---
# <span data-ttu-id="eb8e4-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="eb8e4-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="eb8e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8e4-103">Azure Resource Manager cmdlet isteklerinde kullanılmak üzere kimliği doğrulanmış bir hesap ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb8e4-104">SYNTAX</span></span>

### <span data-ttu-id="eb8e4-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb8e4-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8e4-106">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="eb8e4-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8e4-107">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="eb8e4-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb8e4-108">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="eb8e4-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8e4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb8e4-109">DESCRIPTION</span></span>
<span data-ttu-id="eb8e4-110">Add-AzureRmAcccount cmdlet 'i Azure Resource Manager cmdlet istekleri için kullanılmak üzere kimliği doğrulanmış bir Azure hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="eb8e4-111">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="eb8e4-112">Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="eb8e4-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb8e4-113">EXAMPLES</span></span>

### <span data-ttu-id="eb8e4-114">Örnek 1: etkileşimli oturum açma gerektiren bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="eb8e4-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="eb8e4-115">Bu komut bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="eb8e4-116">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="eb8e4-117">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="eb8e4-118">Örnek 2: kuruluş KIMLIĞI kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="eb8e4-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="eb8e4-119">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="eb8e4-120">İkinci komut $Credential 'daki kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="eb8e4-121">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="eb8e4-122">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="eb8e4-123">Örnek 3: hizmet sorumlusu kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="eb8e4-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="eb8e4-124">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="eb8e4-125">İkinci komut, belirtilen kiracı için $Credential depolanan kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="eb8e4-126">ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="eb8e4-127">Örnek 4: belirli bir kiracı ve abonelik için hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="eb8e4-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="eb8e4-128">Bu komut, varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için bir Azure Kaynak Yöneticisi hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="eb8e4-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb8e4-129">PARAMETERS</span></span>

### <span data-ttu-id="eb8e4-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="eb8e4-130">-AccessToken</span></span>
<span data-ttu-id="eb8e4-131">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="eb8e4-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="eb8e4-132">-AccountId</span></span>
<span data-ttu-id="eb8e4-133">Erişim belirtecinin hesap kimliği</span><span class="sxs-lookup"><span data-stu-id="eb8e4-133">Account Id for access token</span></span>

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

### <span data-ttu-id="eb8e4-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eb8e4-134">-ApplicationId</span></span>
<span data-ttu-id="eb8e4-135">'SI</span><span class="sxs-lookup"><span data-stu-id="eb8e4-135">SPN</span></span>

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

### <span data-ttu-id="eb8e4-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="eb8e4-136">-CertificateThumbprint</span></span>
<span data-ttu-id="eb8e4-137">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="eb8e4-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="eb8e4-138">-ContextName</span><span class="sxs-lookup"><span data-stu-id="eb8e4-138">-ContextName</span></span>
<span data-ttu-id="eb8e4-139">Bu oturumun varsayılan bağlamının adı.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-139">Name of the default context from this login.</span></span>  <span data-ttu-id="eb8e4-140">Oturum açtıktan sonra bu bağlamı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="eb8e4-141">-Credential</span><span class="sxs-lookup"><span data-stu-id="eb8e4-141">-Credential</span></span>
<span data-ttu-id="eb8e4-142">PSCredential nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="eb8e4-143">PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="eb8e4-144">PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="eb8e4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8e4-145">-DefaultProfile</span></span>
<span data-ttu-id="eb8e4-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb8e4-147">-Ortam</span><span class="sxs-lookup"><span data-stu-id="eb8e4-147">-Environment</span></span>
<span data-ttu-id="eb8e4-148">Oturum açacak hesabı içeren ortam</span><span class="sxs-lookup"><span data-stu-id="eb8e4-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="eb8e4-149">-Force</span><span class="sxs-lookup"><span data-stu-id="eb8e4-149">-Force</span></span>
<span data-ttu-id="eb8e4-150">Varsa, var olan içeriğin üzerine yazın.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="eb8e4-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="eb8e4-151">-GraphAccessToken</span></span>
<span data-ttu-id="eb8e4-152">Grafik Hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="eb8e4-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="eb8e4-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="eb8e4-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="eb8e4-154">Keykasa hizmeti için AccessToken</span><span class="sxs-lookup"><span data-stu-id="eb8e4-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="eb8e4-155">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="eb8e4-155">-Scope</span></span>
<span data-ttu-id="eb8e4-156">Bağlam değişikliklerinin kapsamını belirler, örneğin, WHEA değişiklikleri yalnızca örnek işleme uygulanır veya bu kullanıcı tarafından başlatılan tüm oturumlar için.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="eb8e4-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="eb8e4-157">-ServicePrincipal</span></span>
<span data-ttu-id="eb8e4-158">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8e4-159">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="eb8e4-159">-Subscription</span></span>
<span data-ttu-id="eb8e4-160">Abonelik adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="eb8e4-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="eb8e4-161">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="eb8e4-161">-TenantId</span></span>
<span data-ttu-id="eb8e4-162">İsteğe bağlı kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="eb8e4-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="eb8e4-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb8e4-163">-Confirm</span></span>
<span data-ttu-id="eb8e4-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8e4-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8e4-165">-WhatIf</span></span>
<span data-ttu-id="eb8e4-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb8e4-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8e4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8e4-168">CommonParameters</span></span>
<span data-ttu-id="eb8e4-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8e4-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8e4-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8e4-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb8e4-171">INPUTS</span></span>

### <span data-ttu-id="eb8e4-172">Dizisi</span><span class="sxs-lookup"><span data-stu-id="eb8e4-172">String</span></span>
<span data-ttu-id="eb8e4-173">' SubscriptionID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="eb8e4-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="eb8e4-174">Dizisi</span><span class="sxs-lookup"><span data-stu-id="eb8e4-174">String</span></span>
<span data-ttu-id="eb8e4-175">' SubscriptionName ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="eb8e4-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="eb8e4-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb8e4-176">OUTPUTS</span></span>

### <span data-ttu-id="eb8e4-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="eb8e4-177">PSAzureProfile</span></span>
<span data-ttu-id="eb8e4-178">Oturum açan kullanıcının kimlik bilgileri, aboneliği, hesap ve kiracı bilgileri.</span><span class="sxs-lookup"><span data-stu-id="eb8e4-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="eb8e4-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb8e4-179">NOTES</span></span>

## <span data-ttu-id="eb8e4-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb8e4-180">RELATED LINKS</span></span>

