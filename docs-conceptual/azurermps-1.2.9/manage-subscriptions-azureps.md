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
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258613"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="91bec-104">Birden çok Azure aboneliğini yönetme</span><span class="sxs-lookup"><span data-stu-id="91bec-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="91bec-105">Azure ile ilk kez tanışıyorsanız, muhtemelen yalnızca bir aboneliğiniz vardır.</span><span class="sxs-lookup"><span data-stu-id="91bec-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="91bec-106">Bununla birlikte, Azure’u bir süredir kullanıyorsanız birden çok Azure aboneliği oluşturmuş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91bec-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="91bec-107">Azure PowerShell’i, komutları belirli bir abonelikte yürütecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91bec-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="91bec-108">Hesabınızdaki tüm aboneliklerin listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="91bec-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="91bec-109">Varsayılanı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="91bec-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="91bec-110">`Get-AzureRmContext` cmdlet’ini çalıştırarak değişikliği doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="91bec-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="91bec-111">Varsayılan aboneliğinizi ayarladığınızda, sonraki tüm Azure PowerShell komutları bu aboneliğe göre çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="91bec-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
