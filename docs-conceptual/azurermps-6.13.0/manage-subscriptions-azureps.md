---
title: Azure PowerShell ile Azure aboneliklerini yönetme
description: Azure PowerShell ile Azure aboneliklerini yönetme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 9721baff069d2255481a3c993e82db49ba36d9ac
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387913"
---
# <a name="manage-multiple-azure-subscriptions"></a>Birden çok Azure aboneliğini yönetme

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure'la yeni tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır. Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz. Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.

1. Hesabınızdaki tüm aboneliklerin listesini edinin.

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. Varsayılanı ayarlayın.

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. `Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

Varsayılan aboneliğinizi ayarladığınızda, tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.
