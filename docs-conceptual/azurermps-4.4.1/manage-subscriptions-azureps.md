---
title: Azure PowerShell ile Azure aboneliklerini yönetme | Microsoft Docs
description: Azure PowerShell ile Azure aboneliklerini yönetme
keywords: Azure PowerShell, abonelik
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 99a2d9c9c1d233a6468e904e322e8d846d7d78aa
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534805"
---
# <a name="manage-multiple-azure-subscriptions"></a>Birden çok Azure aboneliğini yönetme

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure ile ilk kez tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır. Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz. Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.

1. Hesabınızdaki tüm aboneliklerin listesini edinin.

    ```powershell-interactive
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

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. `Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.

    ```powershell-interactive
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

Varsayılan aboneliğinizi ayarladığınızda, sonraki tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.
