---
title: Azure Stack Hub Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Hub Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: fd1f2a3778e348ba41b46acb4bdce19e18a7f4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81524974"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="c1133-103">Azure Stack Hub Modülü 2.0.0</span><span class="sxs-lookup"><span data-stu-id="c1133-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c1133-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="c1133-104">Requirements:</span></span>

<span data-ttu-id="c1133-105">Desteklenen en düşük Azure Stack Hub sürümü 2002’dir.</span><span class="sxs-lookup"><span data-stu-id="c1133-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="c1133-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="c1133-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="c1133-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="c1133-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="c1133-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="c1133-108">Release Notes</span></span>

* <span data-ttu-id="c1133-109">2002 güncelleştirmesiyle desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c1133-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="c1133-110">Azure Stack Hub 2.0.0 hataya neden olan bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="c1133-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="c1133-111">Modül AzureRM modülü yerine Az modülünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c1133-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="c1133-112">[Azure Stack Hub’da AzureRM’den Azure PowerShell Az’ye geçiş](https://aka.ms/AA7qsji) bölümünde bir geçiş kılavuzu ve hataya neden olan değişikliklerin listesini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1133-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
