---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 6ffc2f928d5131f6ef35e7b8028fbfa9afb35700
ms.sourcegitcommit: 984b401a9d3c09e0178b3108f9e6b810772ae6cf
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/11/2020
ms.locfileid: "93935186"
---
# Connect-AzAccount

## SYNOPSIS
Az PowerShell modüllerinden cmdlet 'ler ile kullanmak için kimliği doğrulanmış bir hesapla Azure 'a bağlanın.

## INDEKI

### Userwithsubscriptionıd (varsayılan)

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>]
 [-ContextName <String>] [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Serviceprincipalwithsubscriptionıd

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> -ServicePrincipal
 -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential

```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Serviceprincipalcertificatewithsubscriptionıd

```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Accesstokenwithsubscriptionıd

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ManagedServiceLogin

```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] -Identity
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>]
 [-ManagedServiceSecret <SecureString>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım

Cmdlet, en `Connect-AzAccount` az PowerShell modüllerinden cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır. Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager istekleriyle kullanabilirsiniz. Hizmet yönetimiyle kullanmak üzere kimliği doğrulanmış bir hesap eklemek için, `Add-AzureAccount` Azure PowerShell modülünden cmdlet 'i kullanın. Geçerli Kullanıcı için içerik bulunmazsa, kullanıcının bağlam listesi ilk 25 aboneliğini içeren bir içerikle doldurulur.
Kullanıcı için oluşturulan bağlamların listesi çalışırken bulunabilir `Get-AzContext -ListAvailable` . Bu bağlam popülasyonu atlamak için **Skipcontextpopülasyon** anahtarı parametresini belirtin. Bu cmdlet 'i yürüttükten sonra, kullanarak Azure hesabından bağlantınızı kesebilirsiniz `Disconnect-AzAccount` .

## ÖRNEKLERDEN

### Örnek 1: Azure hesabına bağlanma

Bu örnek bir Azure hesabına bağlanır. Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgileri sağlamanız gerekir. Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Örnek 2: (yalnızca Windows PowerShell 5,1) kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure 'a bağlanın

Bu senaryo yalnızca Windows PowerShell 5,1 ' de çalışır. İlk komut Kullanıcı kimlik bilgilerini sorar ve bunları `$Credential` değişkende depolar. İkinci komut, uygulamasında depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır `$Credential` . Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure ile kimlik bilgilerini doğrular.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Örnek 3: hizmet sorumlusu hesabını kullanarak Azure 'a bağlanma

İlk komut hizmet sorumlusu kimlik bilgilerini sorar ve bunları `$Credential` değişkende depolar. İstendiğinde Kullanıcı adı ve hizmet sorumlusu parolası için uygulama KIMLIĞINIZI girin. İkinci komut belirtilen Azure kiracısına, değişkende depolanan hizmet sorumlusu kimlik bilgilerini kullanarak bağlanır `$Credential` . **ServicePrincipal** Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Örnek 4: belirli bir kiracıya ve aboneliğe bağlanmak için etkileşimli oturum açma

Bu örnek belirtilen kiracı ve abonelikle bir Azure hesabına bağlanıyor.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Örnek 5: yönetilen hizmet kimliği kullanarak bağlanma

Bu örnekte, ana bilgisayar ortamının yönetilen hizmet kimliği (MSI) kullanılarak bağlantı sağlanır. Örneğin, atanmış MSI 'si olan bir sanal makineden Azure 'da oturum açabilirsiniz.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Örnek 6: yönetilen hizmet kimliği oturum açma ve ClientID kullanarak bağlanma

Bu örnekte **Myuseratanandentity** yönetilen hizmet kimliği kullanılarak bağlantı sağlanır. Kullanıcı tarafından atanan kimliği sanal makineye ekler, ardından Kullanıcı tarafından atanan kimliğin ClientID kullanarak bağlanır. Daha fazla bilgi için, [Azure VM 'de Azure kaynakları için yönetilen kimlikleri yapılandırma](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)bölümüne bakın.

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

### Örnek 7: sertifikaları kullanarak bağlanma

Bu örnek, sertifika tabanlı hizmet sorumlusu kimlik doğrulamasını kullanarak bir Azure hesabına bağlanır.
Kimlik doğrulaması için kullanılan hizmet sorumlusu belirtilen sertifikayla oluşturulmuş olmalıdır. Kendinden imzalanan sertifikalar oluşturma ve onlara izinler atama hakkında daha fazla bilgi için, [sertifika](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

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

## PARAMETRELERINE

### -AccessToken

Bir erişim belirteci belirtir.

> [!CAUTION]
> Erişim belirteçleri bir kimlik bilgisi türüdür. Gizli tutmak için uygun güvenlik önlemleri almalısınız. Access belirteçleri Ayrıca zaman aşımına uğramaz ve çalışmakta olan görevlerin tamamlanmasını önleyebilir.

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

### -AccountId

**Accessstoken** parametre kümesindeki erişim BELIRTECININ hesap kimliği. **Managedservice** parametre kümesindeki yönetilen HIZMETIN hesap kimliği. Yönetilen hizmet kaynak KIMLIĞI veya ilişkili istemci KIMLIĞI olabilir.
Sistem tarafından atanan kimliği kullanmak için bu alanı boş bırakın.

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

### -ApplicationId

Hizmet sorumlusunun uygulama KIMLIĞI.

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

### -CertificateThumbprint

Sertifika karması veya Parmak Izi.

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

### -ContextName

Bu oturum açma için varsayılan Azure bağlamının adı. Azure bağlamları hakkında daha fazla bilgi için, [bkz.](/powershell/azure/context-persistence)

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

### -Credential

**PSCredential** nesnesini belirtir. **PSCredential** nesnesi hakkında daha fazla bilgi için, yazın `Get-Help Get-Credential` . **PSCredential** NESNESI kuruluş kimliği kimlik bilgileri IÇIN Kullanıcı kimliği ve parola veya hizmet sorumlusu kimlik bilgileri IÇIN uygulama kimliği ve gizli 'yi sağlar.

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

### -DefaultProfile

Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Ortam

Azure hesabını içeren ortam.

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

### -Force

Aynı ada sormadan var olan içeriğin üzerine yazın.

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

### -GraphAccessToken

Grafik Hizmeti için AccessToken.

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

### -Kimlik

Yönetilen hizmet kimliği kullanarak oturum açın.

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

### -KeyVaultAccessToken

Keykasa hizmeti için AccessToken.

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

### -Managedserviceanabilgisayaradı

Yönetilen hizmetin ana bilgisayar adı.

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

### -ManagedServicePort

Yönetilen hizmetin bağlantı noktası numarası.

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

### -ManagedServiceSecret

Yönetilen hizmet oturumu simgesi.

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

### -Kapsam

Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.

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

### -ServicePrincipal

Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.

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

### -Skipcontextpopülasyonu

İçerik oluşturmayı atlar.

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

### -SkipValidation

Erişim belirtecinin doğrulanmasını atlayın.

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

### -Abonelik

Abonelik adı veya KIMLIĞI.

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

### -Tenant

İsteğe bağlı kiracı adı veya KIMLIĞI.

> [!NOTE]
> Geçerli API sınırlamaları nedeniyle, işletmeler arası (B2B) bir hesap ile bağlantı oluştururken kiracı adı yerine kiracı KIMLIĞI kullanmalısınız.

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

### -UseDeviceAuthentication

Tarayıcı denetimi yerine cihaz kodu kimlik doğrulaması kullanın. Bu, PowerShell sürüm 6 ve üzeri için varsayılan kimlik doğrulama türüdür.

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

### -Onay

Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf

Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### CommonParameters

Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
