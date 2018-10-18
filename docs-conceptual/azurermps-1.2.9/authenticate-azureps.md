---
title: Azure PowerShell ile oturum açma
description: Azure PowerShell ile oturum açma
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399204"
---
# <a name="log-in-with-azure-powershell"></a>Azure PowerShell ile oturum açma

Azure PowerShell, birden fazla oturum açma yöntemini destekler. Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.

## <a name="interactive-log-in"></a>Etkileşimli oturum açma

1. `Login-AzureRmAccount` yazın. Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır.

2. Hesabınızla ilişkili e-posta adresini ve parolayı yazın. Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.

## <a name="log-in-with-a-service-principal"></a>Hizmet sorumlusu ile oturum açma

Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar. Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir. Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.

1. Zaten bir hizmet sorumlunuz yoksa [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).

2. Hizmet sorumlusu ile oturum açın.

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    TenantId’nizi almak için etkileşimli olarak oturum açın ve aboneliğinizden TenantId’yi edinin.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a>Azure kaynakları için yönetilen kimlikleri kullanarak oturum açma

Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir. Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.

Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="log-in-to-another-cloud"></a>Başka bir bulut oturumu açma

Azure Cloud Services, devletlerin veri işleme düzenlemelerine uygun farklı ortamlar sunar. Azure hesabınız kamu bulutlarından birindeyse oturum açtığınızda ilgili ortamı belirtmeniz gerekir. Örneğin hesabınız Çin bulutundaysa şu komutla oturum açmanız gerekir:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Kullanabileceğiniz ortamların listesine ulaşmak için şu komutu kullanın:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin

Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).

Rol yönetimi için Azure PowerShell cmdlet'leri

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
