---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f54e982cd65513de4f64634f535cd70a9ec7b8a3
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534556"
---
# <a name="sign-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell, birden fazla kimlik doğrulama yöntemini destekler. Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.

## <a name="sign-in-interactively"></a>Etkileşimli olarak oturum açma

Etkileşimli olarak oturum açmak için [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet'ini kullanın.

```azurepowershell-interactive
Connect-AzureRmAccount
```

Bu cmdlet çalıştırıldığında, Azure hesabınızla ilişkilendirilmiş e-posta adresinizle parolanızı soran bir iletişim kutusu açar. Kimlik doğrulaması yaptığınızda, bu bilgiler geçerli PowerShell oturumu için kaydedilir, iletişim kutusu kapatılır ve tüm Azure PowerShell cmdlet'lerine erişim kazanırsınız.

> [!IMPORTANT]
> Bu oturum açma işlemi _yalnızca_ geçerli PowerShell oturumuna yöneliktir. Kimlik doğrulamasının birden çok oturumda kalıcı olmasını sağlamak için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.

## <a name="sign-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma

Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar. Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir. Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.

Azure PowerShell'le kullanmak üzere bir hizmet sorumlusu oluşturmanız gerekirse, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).

Hizmet sorumlusuyla oturum açmak için `Connect-AzureRmAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın. Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır. Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın. Bu cmdlet, hizmet sorumlusu kimliğini ve parolasını girmeniz için bir iletişim kutusu görüntüler.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Azure kaynakları için yönetilen kimlikleri kullanarak oturum açma

Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir. Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz. Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.

Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

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
