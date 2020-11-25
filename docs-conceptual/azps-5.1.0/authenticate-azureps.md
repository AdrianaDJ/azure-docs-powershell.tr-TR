---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 46e5e84b6718cc7a700ef2df4e82647e8cb60941
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515118"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler. Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır. Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz. Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır. Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.

Birden fazla aboneliğe erişiminiz varsa başlangıçta Azure’ın ilk döndürdüğü abonelikte oturumunuz açılır. Komutlar varsayılan olarak bu abonelikte çalıştırılır. Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın. Etkin aboneliğinizi değiştirmek ve aynı sistemde oturum değiştirdiğinizde bu değişikliğin geçerliliğini korumasını sağlamak için [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet’ini kullanın.

> [!IMPORTANT]
> Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.
> Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.

## <a name="sign-in-interactively"></a>Etkileşimli olarak oturum açma

Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.

```azurepowershell-interactive
Connect-AzAccount
```

Bu cmdlet, Az PowerShell modülü sürüm 5.0.0’dan itibaren varsayılan olarak, etkileşimli tarayıcı tabanlı bir oturum açma istemi sunar. Daha önce PowerShell sürümü 6 ve üzeri için varsayılan olan bir belirteç dizesi almak üzere `UseDeviceAuthentication` parametresini belirtebilirsiniz.

> [!IMPORTANT]
> Active Directory yetkilendirme uygulamalarında yapılan değişiklikler ve güvenlik kaygıları nedeniyle, kullanıcı adı/parola kimlik bilgisi yetkilendirmesi Azure PowerShell’den kaldırıldı. Kimlik bilgisi yetkilendirmesini otomasyon amacıyla kullanıyorsanız, bunun yerine [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).

Kiracı kimliğinizi bu makalenin sonraki iki bölümünde kullanılacak bir değişkende depolamak için [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet’ini kullanın.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma <a name="sp-signin"/>

Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır. Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir. Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.

Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).

Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın. Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır. Hizmet sorumlusu ile nasıl oturum açacağınız, parola tabanlı veya sertifika tabanlı kimlik doğrulaması yöntemlerinden hangisini kullandığına bağlıdır.

### <a name="password-based-authentication"></a>Parola tabanlı kimlik doğrulaması

Bu bölümdeki örneklerde kullanılmak üzere bir hizmet sorumlusu oluşturun. Hizmet sorumluları oluşturma hakkında daha fazla bilgi için bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın. Bu cmdlet bir kullanıcı adı ve parola için istem gösterir. Kullanıcı adı için hizmet sorumlusunun `applicationID` kimliğini kullanın ve parola için `secret` gizli dizisini düz metne dönüştürün.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Otomasyon senaryoları için, hizmet sorumlusunun `applicationId` kimliğinden ve `secret` gizli dizisinden kimlik bilgileri oluşturmanız gerekir:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Hizmet sorumlusu bağlantılarını otomatikleştirirken, iyi parola depolama yöntemlerini kullandığınızdan emin olun.

### <a name="certificate-based-authentication"></a>Sertifika tabanlı kimlik doğrulaması

Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Kayıtlı uygulama yerine hizmet sorumlusu kullanırken `-ServicePrincipal` bağımsız değişkenini ekleyin ve `-ApplicationId` parametresinin değeri olarak hizmet sorumlusunun Uygulama kimliğini sağlayın.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

PowerShell 5.1'de, sertifika deposu [PKI](/powershell/module/pkiclient) modülü ile yönetilebilir ve denetlenebilir. PowerShell Core 6.x ve sonraki sürümleri için işlem daha karmaşıktır. Aşağıdaki betikler, mevcut sertifikayı PowerShell tarafından erişilebilir sertifika deposuna nasıl aktarabileceğinizi gösterir.

#### <a name="import-a-certificate-in-powershell-51"></a>PowerShell 5.1'de sertifikayı içeri aktarma

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>PowerShell Core 6.x ve sonraki sürümlerinde sertifikayı içeri aktarma

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Yönetilen kimlik kullanarak oturum açma

Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir. Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır. Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz. Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.

Bu örnekte, barındırma ortamının yönetilen kimliği kullanılarak bağlanılır. Örneğin, atanmış bir Yönetilen Hizmet Kimliğine sahip bir Sanal Makine üzerinde yürütülürse, kodun bu atanmış kimliği kullanarak oturum açmasını sağlar.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma

Hesabınız birden fazla kiracıyla ilişkilendirildiyse bağlantı kurarken oturum açmak için `-Tenant` parametresinin belirtilmesi gerekir. Bu parametre tüm oturum açma yöntemleriyle çalışır. Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.

[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), `-Tenant` değerin kiracı kimliği olması **gerekir**.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Başka bir bulut oturumu açma

Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar. Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın. Bu parametre tüm oturum açma yöntemleriyle çalışır. Örneğin, hesabınız Çin bulutundaysa:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Aşağıdaki komut, kullanılabilir ortamların listesini alır:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
