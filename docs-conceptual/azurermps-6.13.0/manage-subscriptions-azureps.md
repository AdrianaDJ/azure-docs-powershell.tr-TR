---
title: Azure PowerShell ile Azure aboneliklerini yönetme
description: Azure PowerShell ile Azure aboneliklerini yönetme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: a93461af1dafbf8f2c85ef127ecaefadf3be2f52
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52260032"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="2963c-103">Birden çok Azure aboneliğini yönetme</span><span class="sxs-lookup"><span data-stu-id="2963c-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="2963c-104">Azure'la yeni tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır.</span><span class="sxs-lookup"><span data-stu-id="2963c-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="2963c-105">Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2963c-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="2963c-106">Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2963c-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="2963c-107">Hesabınızdaki tüm aboneliklerin listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="2963c-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="2963c-108">Varsayılanı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2963c-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="2963c-109">`Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2963c-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="2963c-110">Varsayılan aboneliğinizi ayarladığınızda, tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="2963c-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
