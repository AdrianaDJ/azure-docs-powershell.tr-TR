---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: e314374eff433d1869378bdaa9a0370c3fd3d8d1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022983"
---
# <a name="azure-stack-module-182"></a><span data-ttu-id="6002d-103">Azure Stack Modülü 1.8.2</span><span class="sxs-lookup"><span data-stu-id="6002d-103">Azure Stack Module 1.8.2</span></span>

## <a name="requirements"></a><span data-ttu-id="6002d-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="6002d-104">Requirements:</span></span>

<span data-ttu-id="6002d-105">Desteklenen en düşük Azure Stack sürümü 1910’dur.</span><span class="sxs-lookup"><span data-stu-id="6002d-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="6002d-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="6002d-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="6002d-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="6002d-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a><span data-ttu-id="6002d-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="6002d-108">Release Notes</span></span>

* <span data-ttu-id="6002d-109">1910 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="6002d-109">Supported with 1910 update</span></span>
