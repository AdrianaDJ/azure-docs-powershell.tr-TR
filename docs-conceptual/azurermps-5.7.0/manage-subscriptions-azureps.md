---
title: Azure PowerShell ile Azure aboneliklerini yönetme
description: Azure PowerShell ile Azure aboneliklerini yönetme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 5edfe15a1ed4e321d28422e9e6c32a14b717b93c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145080"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="87430-103">Birden çok Azure aboneliğini yönetme</span><span class="sxs-lookup"><span data-stu-id="87430-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="87430-104">Azure ile ilk kez tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır.</span><span class="sxs-lookup"><span data-stu-id="87430-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="87430-105">Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87430-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="87430-106">Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87430-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="87430-107">Hesabınızdaki tüm aboneliklerin listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="87430-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="87430-108">Varsayılanı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="87430-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="87430-109">`Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="87430-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="87430-110">Varsayılan aboneliğinizi ayarladığınızda, sonraki tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="87430-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
