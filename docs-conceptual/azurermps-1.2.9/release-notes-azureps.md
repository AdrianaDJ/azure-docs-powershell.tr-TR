---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="739b3-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="739b3-103">Release notes</span></span>

<span data-ttu-id="739b3-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="739b3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="739b3-105">Sürüm 1.2.9</span><span class="sxs-lookup"><span data-stu-id="739b3-105">Version 1.2.9</span></span>

<span data-ttu-id="739b3-106">Bu Sürümdeki Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="739b3-106">Changes This Release</span></span>

* <span data-ttu-id="739b3-107">AzureRm.AzureStackAdmin Modülü</span><span class="sxs-lookup"><span data-stu-id="739b3-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="739b3-108">Add-AzureRmResourceProviderRegistration cmdlet’inde Yönetici Azure resource manager ve kiracı azure resource manager bölünmesini desteklemek üzere değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="739b3-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="739b3-109">-ResourceManagerType adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="739b3-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="739b3-110">-AdminUri, -ApiVersion, -SubscriptionId ve -Token parametreleri her bir cmdlet’ten kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="739b3-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="739b3-111">Bu parametrelerinin kullanımdan kaldırılacağı ile ilgili uyarılar yayınlanmıştı ve şimdi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="739b3-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="739b3-112">AzureStackStorage modülü</span><span class="sxs-lookup"><span data-stu-id="739b3-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="739b3-113">Kapsayıcı geçiş senaryolarını destekleyen yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="739b3-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="739b3-114">İç bileşenlere ve temel alınan özelliklere başvuran cmdlet'ler kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="739b3-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="739b3-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="739b3-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="739b3-116">Sürüm profilleri kullanılarak Azure PowerShell cmdlet’lerinin sürümlerini yönetmek için yeni modül oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="739b3-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>