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
ms.openlocfilehash: 5e30e1b4a21f62c00419cfa77e1d875e110eebec
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428001"
---
# <a name="azure-stack-module-182"></a><span data-ttu-id="318b0-103">Azure Stack Modülü 1.8.2</span><span class="sxs-lookup"><span data-stu-id="318b0-103">Azure Stack Module 1.8.2</span></span>

## <a name="requirements"></a><span data-ttu-id="318b0-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="318b0-104">Requirements:</span></span>

<span data-ttu-id="318b0-105">Desteklenen en düşük Azure Stack sürümü 1910’dur.</span><span class="sxs-lookup"><span data-stu-id="318b0-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="318b0-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="318b0-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="318b0-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="318b0-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a><span data-ttu-id="318b0-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="318b0-108">Release Notes</span></span>

* <span data-ttu-id="318b0-109">1910 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="318b0-109">Supported with 1910 update</span></span>