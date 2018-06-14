---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853024"
---
# <a name="release-notes"></a><span data-ttu-id="6d95e-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="6d95e-103">Release notes</span></span>

<span data-ttu-id="6d95e-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6d95e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="6d95e-105">Sürüm 1.2.9</span><span class="sxs-lookup"><span data-stu-id="6d95e-105">Version 1.2.9</span></span>

<span data-ttu-id="6d95e-106">Bu Sürümdeki Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="6d95e-106">Changes This Release</span></span>

* <span data-ttu-id="6d95e-107">AzureRm.AzureStackAdmin Modülü</span><span class="sxs-lookup"><span data-stu-id="6d95e-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="6d95e-108">Add-AzureRmResourceProviderRegistration cmdlet’inde Yönetici Azure resource manager ve kiracı azure resource manager bölünmesini desteklemek üzere değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="6d95e-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="6d95e-109">-ResourceManagerType adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d95e-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="6d95e-110">-AdminUri, -ApiVersion, -SubscriptionId ve -Token parametreleri her bir cmdlet’ten kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6d95e-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="6d95e-111">Bu parametrelerinin kullanımdan kaldırılacağı ile ilgili uyarılar yayınlanmıştı ve şimdi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6d95e-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="6d95e-112">AzureStackStorage modülü</span><span class="sxs-lookup"><span data-stu-id="6d95e-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="6d95e-113">Kapsayıcı geçiş senaryolarını destekleyen yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="6d95e-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="6d95e-114">İç bileşenlere ve temel alınan özelliklere başvuran cmdlet'ler kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6d95e-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="6d95e-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="6d95e-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="6d95e-116">Sürüm profilleri kullanılarak Azure PowerShell cmdlet’lerinin sürümlerini yönetmek için yeni modül oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="6d95e-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>