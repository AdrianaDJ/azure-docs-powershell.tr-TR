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
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855797"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="28ead-103">Azure Stack Modülü 1.7.2</span><span class="sxs-lookup"><span data-stu-id="28ead-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="28ead-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="28ead-104">Requirements:</span></span>

<span data-ttu-id="28ead-105">Desteklenen en düşük Azure Stack sürümü 1904'dir.</span><span class="sxs-lookup"><span data-stu-id="28ead-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="28ead-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="28ead-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="28ead-107">Azure Stack için PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="28ead-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="28ead-108">Yükleme üç adımdan oluşur:</span><span class="sxs-lookup"><span data-stu-id="28ead-108">Installation has three steps:</span></span>

1. <span data-ttu-id="28ead-109">Azure Stack sürümünüze bağlı olarak Azure Stack PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="28ead-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="28ead-110">Ek depolama özelliklerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="28ead-110">Enable additional storage features</span></span>
3. <span data-ttu-id="28ead-111">PowerShell yüklenmesini onaylama</span><span class="sxs-lookup"><span data-stu-id="28ead-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="28ead-112">Azure Stack PowerShell’i yükleme</span><span class="sxs-lookup"><span data-stu-id="28ead-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="28ead-113">Ek depolama özelliklerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="28ead-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="28ead-114">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="28ead-114">Release Notes</span></span>

* <span data-ttu-id="28ead-115">1904 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="28ead-115">Supported with 1904 update</span></span>
* <span data-ttu-id="28ead-116">Bu hataya neden olan değişiklik yayınıdır.</span><span class="sxs-lookup"><span data-stu-id="28ead-116">This a breaking change release.</span></span> <span data-ttu-id="28ead-117">Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="28ead-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="28ead-118">Azs.Backup.Admin Modülü \* Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme.</span><span class="sxs-lookup"><span data-stu-id="28ead-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="28ead-119">Simetrik anahtarlar için destek kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="28ead-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="28ead-120">Azs.Fabric.Admin Module       \* Kullanımdan Kaldırma           \* Get-AzsInfrastructureVolume kullanımdan kaldırıldı, yeni Get-AzsVolume cmdlet'ini sağladık           \* Get-AzsStorageSystem kullanımdan kaldırıldı, yeni Get-AzsStorageSubSystem cmdlet'ini sağladık           \* Get-AzsStoragePool kullanımdan kaldırıldı, StorageSubSystem nesnesine kapasite özelliği bulunuyor</span><span class="sxs-lookup"><span data-stu-id="28ead-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="28ead-121">Azs.Compute.Admin Modülü           \* Hata Düzeltmesi: Add-AzsPlatformImage, Get-AzsPlatformImage : Yalnızca başarı yolunda ConvertTo-PlatformImageObject çağrısı           \* Hata Düzeltmesi: Add-AzsVmExtension, Get-AzsVmExtension: Yalnızca başarı yolunda ConvertTo-VmExtensionObject çağrısı</span><span class="sxs-lookup"><span data-stu-id="28ead-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="28ead-122">Azs.Storage.Admin Modülü           \* Hata düzeltmesi: Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.'</span><span class="sxs-lookup"><span data-stu-id="28ead-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
