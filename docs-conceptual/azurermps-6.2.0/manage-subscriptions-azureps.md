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
ms.openlocfilehash: 4f066118373c9ea7deffe7c6474552f1ce91cb56
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820604"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="5fbfe-104">Birden çok Azure aboneliğini yönetme</span><span class="sxs-lookup"><span data-stu-id="5fbfe-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="5fbfe-105">Azure ile ilk kez tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="5fbfe-106">Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="5fbfe-107">Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="5fbfe-108">Hesabınızdaki tüm aboneliklerin listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="5fbfe-109">Varsayılanı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-109">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="5fbfe-110">`Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="5fbfe-111">Varsayılan aboneliğinizi ayarladığınızda, sonraki tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="5fbfe-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
