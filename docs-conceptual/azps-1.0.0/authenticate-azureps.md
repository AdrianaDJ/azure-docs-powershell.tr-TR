---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: b5635e291cdc324e66c936aa16c5772507fc78e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54055685"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler. Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır. Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz. Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır. Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.

Oturum açtıktan sonra, komutlar varsayılan aboneliğinizde çalıştırılır. Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın. Azure PowerShell'de oturum açarken kullanılan varsayılan aboneliği değiştirmek için [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) kullanın.

> [!IMPORTANT]
>
> Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.
> Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.

## <a name="sign-in-interactively"></a>Etkileşimli olarak oturum açma

Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.

```azurepowershell-interactive
Connect-AzAccount
```

Bu cmdlet çalıştırıldığında bir belirteç dizesi sunar. Oturum açmak için bu dizeyi kopyalayıp bir tarayıcıda https://microsoft.com/devicelogin sayfasına yapıştırın. Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.

## <a name="sign-in-with-credentials"></a>Kimlik bilgileriyle oturum açma

Ayrıca Azure'a bağlanmak için yetkilendirilmiş bir `PSCredential` nesnesiyle de oturum açabilirsiniz.
Kimlik bilgileri nesnesini almanın en kolay yolu [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet'ini kullanmaktır. Bu cmdlet çalıştırıldığında, sizden kullanıcı adı/parola bilgileri çiftini ister.

> [!Note]
> Bu yaklaşım Microsoft hesaplarıyla veya iki faktörlü kimlik doğrulamasını etkinleştirdiğiniz hesaplarla kullanılamaz.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma

Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır. Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir. Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.

Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).

Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın. Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır. Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın. Bu cmdlet, hizmet sorumlusu kullanıcı kimliği ve parolası için bir istem sunar.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Yönetilen kimlik kullanarak oturum açma 

Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir. Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır. Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz. Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.

Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi edinmek için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma

Hesabınız birden fazla kiracıyla ilişkilendirildiyse, bağlantı kurarken oturum açmak için `-TenantId` parametresinin kullanılması gerekir. Bu parametre, diğer tüm oturum açma yöntemiyle çalışır. Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.

[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), `-TenantId` değerin kiracı kimliği olması **gerekir**.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Başka bir bulut oturumu açma

Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar.
Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.
Örneğin, hesabınız Çin bulutundaysa:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Aşağıdaki komut, kullanılabilir ortamların listesini alır:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```