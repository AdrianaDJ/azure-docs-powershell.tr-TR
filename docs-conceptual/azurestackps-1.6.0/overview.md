---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153917"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="753bd-103">Azure Stack Modülü 1.6.0</span><span class="sxs-lookup"><span data-stu-id="753bd-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="753bd-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="753bd-104">Requirements:</span></span>
<span data-ttu-id="753bd-105">Desteklenen en düşük Azure Stack sürümü 1811'dir.</span><span class="sxs-lookup"><span data-stu-id="753bd-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="753bd-106">Not: Daha önceki bir sürümü kullanıyorsanız 1.6.0 sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="753bd-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="753bd-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="753bd-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="753bd-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="753bd-108">Release Notes</span></span>
* <span data-ttu-id="753bd-109">1811 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="753bd-109">Supported with 1811 update</span></span>
* <span data-ttu-id="753bd-110">Azs.Compute.Admin modülü</span><span class="sxs-lookup"><span data-stu-id="753bd-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="753bd-111">New-DataDiskObject için eksik Azs ön eki düzeltildi ve gelecekte kullanım dışı bırakılabileceğine ilişkin uyarıyı içeren bir diğer ad eklendi.</span><span class="sxs-lookup"><span data-stu-id="753bd-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="753bd-112">Azs.Update.Admin Module</span><span class="sxs-lookup"><span data-stu-id="753bd-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="753bd-113">Install-AzsUpdate'ten önce Test-AzureStack'in çalıştırılmasını öneren bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="753bd-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="753bd-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="753bd-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="753bd-115">Yeni cmdlet (Özellikler Azure Stack 1811+ sürümlerinde destekleniyor)</span><span class="sxs-lookup"><span data-stu-id="753bd-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="753bd-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="753bd-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="753bd-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="753bd-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="753bd-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="753bd-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="753bd-119">Kullanımdan kaldırma</span><span class="sxs-lookup"><span data-stu-id="753bd-119">Deprecation</span></span>
        * <span data-ttu-id="753bd-120">Get-AzsInfrastructureVolume artık Get-AzsVolume cmdlet'in diğer adı</span><span class="sxs-lookup"><span data-stu-id="753bd-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="753bd-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="753bd-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="753bd-122">Yeni Repair-AzsAlert cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="753bd-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="753bd-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="753bd-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="753bd-124">Varsayılan kota değerlerinin kullanılmamasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="753bd-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="753bd-125">Azs.Subscriptions.Admin Module</span><span class="sxs-lookup"><span data-stu-id="753bd-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="753bd-126">New-AddonPlanDefinitionObject için eksik Azs ön eki düzeltildi ve gelecekte kullanım dışı bırakılabileceğine ilişkin uyarıyı içeren bir diğer ad eklendi.</span><span class="sxs-lookup"><span data-stu-id="753bd-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
