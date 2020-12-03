---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427386"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="4677d-103">Azure Stack Modülü 1.7.2</span><span class="sxs-lookup"><span data-stu-id="4677d-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="4677d-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="4677d-104">Requirements:</span></span>

<span data-ttu-id="4677d-105">Desteklenen en düşük Azure Stack sürümü 1904'dir.</span><span class="sxs-lookup"><span data-stu-id="4677d-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="4677d-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="4677d-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="4677d-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="4677d-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="4677d-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="4677d-108">Release Notes</span></span>

* <span data-ttu-id="4677d-109">1904 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="4677d-109">Supported with 1904 update</span></span>
* <span data-ttu-id="4677d-110">Bu hataya neden olan değişiklik yayınıdır.</span><span class="sxs-lookup"><span data-stu-id="4677d-110">This a breaking change release.</span></span> <span data-ttu-id="4677d-111">Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="4677d-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="4677d-112">Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme.</span><span class="sxs-lookup"><span data-stu-id="4677d-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="4677d-113">Simetrik anahtarlar için destek kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="4677d-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="4677d-114">Hataya neden olan değişikliklerin ayrıntıları için bkz. https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="4677d-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="4677d-115">Azs.Storage.Admin Modülü</span><span class="sxs-lookup"><span data-stu-id="4677d-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="4677d-116">Hata düzeltmesi - Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="4677d-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>