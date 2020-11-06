---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571621"
---
# <span data-ttu-id="3f90a-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="3f90a-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="3f90a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f90a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f90a-103">Azure Resource Manager cmdlet isteklerinde kullanılmak üzere kimliği doğrulanmış bir hesap ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="3f90a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f90a-104">SYNTAX</span></span>

### <span data-ttu-id="3f90a-105">Userwithsubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f90a-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f90a-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-107">Serviceprincipalwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3f90a-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f90a-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-109">Serviceprincipalcertificatewithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3f90a-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f90a-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-111">Accesstokenwithsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3f90a-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f90a-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f90a-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f90a-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f90a-113">DESCRIPTION</span></span>
<span data-ttu-id="3f90a-114">Add-AzureRmAcccount cmdlet 'i Azure Resource Manager cmdlet istekleri için kullanılmak üzere kimliği doğrulanmış bir Azure hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="3f90a-115">Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f90a-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="3f90a-116">Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f90a-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="3f90a-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f90a-117">EXAMPLES</span></span>

### <span data-ttu-id="3f90a-118">Örnek 1: etkileşimli oturum açma gerektiren bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="3f90a-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="3f90a-119">Bu komut bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="3f90a-120">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="3f90a-121">Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="3f90a-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="3f90a-122">Örnek 2: kuruluş KIMLIĞI kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="3f90a-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="3f90a-123">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3f90a-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="3f90a-124">İkinci komut $Credential 'daki kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="3f90a-125">Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="3f90a-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="3f90a-126">Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3f90a-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="3f90a-127">Örnek 3: hizmet sorumlusu kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="3f90a-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="3f90a-128">İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3f90a-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="3f90a-129">İkinci komut, belirtilen kiracı için $Credential depolanan kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="3f90a-130">ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="3f90a-131">Örnek 4: belirli bir kiracı ve abonelik için hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="3f90a-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="3f90a-132">Bu komut, varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için bir Azure Kaynak Yöneticisi hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="3f90a-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="3f90a-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f90a-133">PARAMETERS</span></span>

### <span data-ttu-id="3f90a-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="3f90a-134">-AccessToken</span></span>
<span data-ttu-id="3f90a-135">Bir erişim belirteci belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3f90a-136">-AccountId</span></span>
<span data-ttu-id="3f90a-137">Erişim belirtecinin hesap kimliği</span><span class="sxs-lookup"><span data-stu-id="3f90a-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3f90a-138">-ApplicationId</span></span>
<span data-ttu-id="3f90a-139">'SI</span><span class="sxs-lookup"><span data-stu-id="3f90a-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3f90a-140">-CertificateThumbprint</span></span>
<span data-ttu-id="3f90a-141">Sertifika karması (Parmak Izi)</span><span class="sxs-lookup"><span data-stu-id="3f90a-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-142">-Credential</span><span class="sxs-lookup"><span data-stu-id="3f90a-142">-Credential</span></span>
<span data-ttu-id="3f90a-143">PSCredential nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="3f90a-144">PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.</span><span class="sxs-lookup"><span data-stu-id="3f90a-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="3f90a-145">PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3f90a-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-146">-Ortam</span><span class="sxs-lookup"><span data-stu-id="3f90a-146">-Environment</span></span>
<span data-ttu-id="3f90a-147">Oturum açacak hesabı içeren ortam</span><span class="sxs-lookup"><span data-stu-id="3f90a-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="3f90a-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3f90a-148">-ServicePrincipal</span></span>
<span data-ttu-id="3f90a-149">Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-150">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3f90a-150">-SubscriptionId</span></span>
<span data-ttu-id="3f90a-151">Aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="3f90a-152">Bu parametreyi belirtmezseniz, abonelik listesinin ilk aboneliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f90a-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f90a-153">-SubscriptionName</span></span>
<span data-ttu-id="3f90a-154">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="3f90a-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-155">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="3f90a-155">-TenantId</span></span>
<span data-ttu-id="3f90a-156">İsteğe bağlı kiracı adı veya KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3f90a-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f90a-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f90a-157">-Confirm</span></span>
<span data-ttu-id="3f90a-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f90a-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f90a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f90a-159">-WhatIf</span></span>
<span data-ttu-id="3f90a-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f90a-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f90a-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f90a-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f90a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f90a-162">CommonParameters</span></span>
<span data-ttu-id="3f90a-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f90a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f90a-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f90a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f90a-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f90a-165">INPUTS</span></span>

## <span data-ttu-id="3f90a-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f90a-166">OUTPUTS</span></span>

### <span data-ttu-id="3f90a-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3f90a-167">PSAzureProfile</span></span>

## <span data-ttu-id="3f90a-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f90a-168">NOTES</span></span>

## <span data-ttu-id="3f90a-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f90a-169">RELATED LINKS</span></span>

