---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya MSI kullanarak Azure PowerShell ile oturum açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106819"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

Azure PowerShell, birden fazla kimlik doğrulama yöntemini destekler. Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.

## <a name="sign-in-interactively"></a>Etkileşimli olarak oturum açma

Etkileşimli olarak oturum açmak için [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet'ini kullanın.

```azurepowershell
Connect-AzureRmAccount
```

Bu cmdlet çalıştırıldığında, Azure hesabınızla ilişkilendirilmiş e-posta adresinizle parolanızı soran bir iletişim kutusu açar. Kimlik doğrulaması yaptığınızda, bu bilgiler geçerli PowerShell oturumu için kaydedilir, iletişim kutusu kapatılır ve tüm Azure PowerShell cmdlet'lerine erişim kazanırsınız.

> [!IMPORTANT]
> Azure PowerShell 6.3.0'dan başlayarak, Windows'da oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır. Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.

## <a name="sign-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma

Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar. Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir. Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.

Azure PowerShell'le kullanmak üzere bir hizmet sorumlusu oluşturmanız gerekirse, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).

Hizmet sorumlusuyla oturum açmak için `Connect-AzureRmAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın. Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır. Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın. Bu cmdlet, hizmet sorumlusu kimliğini ve parolasını girmeniz için bir iletişim kutusu görüntüler.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Azure VM Yönetilen Hizmet Kimliği kullanarak oturum açma

Yönetilen Hizmet Kimliği (MSI), Azure Active Directory’nin bir önizleme özelliğidir. Oturum açmak için bir MSI hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci edinebilirsiniz. MSI yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.

MSI hakkında daha fazla bilgi için bkz. [Oturum açma ve belirteç edinme için Azure VM Yönetilen Hizmet Kimliği’ni (MSI) kullanma](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="sign-in-to-another-cloud"></a>Başka bir bulut oturumu açma

Azure Cloud Services, çeşitli bölgelerin veri işleme düzenlemelerine uygun farklı ortamlar sunar. Azure hesabınız bu bölgelerden biriyle ilişkili bir buluttaysa, oturum açarken ortamı belirtmeni gerekir. Örneğin hesabınız Çin bulutundaysa şu komutla oturum açmanız gerekir:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Kullanabileceğiniz ortamların listesine ulaşmak için şu komutu kullanın:

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
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
