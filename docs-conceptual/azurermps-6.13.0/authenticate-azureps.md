---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 464d7efa640f1d1ffd1c34bfbe6cf13cbe5202b6
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "68863231"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler. Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.

## <a name="sign-in-interactively"></a>Etkileşimli olarak oturum açma

Etkileşimli olarak oturum açmak için [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet'ini kullanın.

```azurepowershell-interactive
Connect-AzureRmAccount
```

Bu cmdlet çalıştırıldığında, Azure hesabınızla ilişkilendirilmiş e-posta adresinizle parolanızı soran bir iletişim kutusu açar. Bu kimlik doğrulaması geçerli PowerShell oturumunu süresince kullanılır.

> [!IMPORTANT]
> Azure PowerShell 6.3.0'dan başlayarak, Windows'da oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır. Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.

## <a name="sign-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma

Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır. Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir. Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.

Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).

Hizmet sorumlusuyla oturum açmak için `-ServicePrincipal` cmdlet'iyle `Connect-AzureRmAccount` bağımsız değişkenini kullanın. Hizmet sorumlusunun oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır. Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın. Bu cmdlet, hizmet sorumlusu kimliğini ve parolasını girmeniz için bir iletişim kutusu görüntüler.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Azure Yönetilen Hizmet Kimliği kullanarak oturum açma

Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir. Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz. Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.

Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma

[Bulut Çözümü Sağlayıcısı (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) olarak oturum açmak için `-TenantId` kullanılması gerekir. Normalde bu parametre kiracı kimliği veya etki alanı adı olarak sağlanabilir. Ancak CSP olarak oturum açmak için **kiracı kimliği** sağlanmalıdır.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Başka bir bulut oturumu açma

Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasal düzenlerle uyumlu ortamlar sunar.
Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.
Örneğin, hesabınız Çin bulutundaysa:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Aşağıdaki komut, kullanılabilir ortamların listesini alır:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin

Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).

Rol yönetimi için Azure PowerShell cmdlet'leri:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
