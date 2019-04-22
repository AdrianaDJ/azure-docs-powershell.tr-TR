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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58808077"
---
# <a name="azure-stack-module-171"></a><span data-ttu-id="f2df6-103">Azure Stack Modülü 1.7.1</span><span class="sxs-lookup"><span data-stu-id="f2df6-103">Azure Stack Module 1.7.1</span></span>

## <a name="requirements"></a><span data-ttu-id="f2df6-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="f2df6-104">Requirements:</span></span>

<span data-ttu-id="f2df6-105">Desteklenen en düşük Azure Stack sürümü 1901'dir.</span><span class="sxs-lookup"><span data-stu-id="f2df6-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="f2df6-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="f2df6-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="f2df6-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="f2df6-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a><span data-ttu-id="f2df6-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="f2df6-108">Release Notes</span></span>

* <span data-ttu-id="f2df6-109">1901 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="f2df6-109">Supported with 1901 update</span></span>
* <span data-ttu-id="f2df6-110">Bu hataya neden olan değişiklik yayınıdır.</span><span class="sxs-lookup"><span data-stu-id="f2df6-110">This a breaking change release.</span></span> <span data-ttu-id="f2df6-111">Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="f2df6-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="f2df6-112">Azs.Backup.Admin Modülü \* Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme.</span><span class="sxs-lookup"><span data-stu-id="f2df6-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="f2df6-113">Simetrik anahtarlar için destek kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="f2df6-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="f2df6-114">Azs.Fabric.Admin Module       \* Kullanımdan Kaldırma           \* Get-AzsInfrastructureVolume kullanımdan kaldırıldı, yeni Get-AzsVolume cmdlet'ini sağladık           \* Get-AzsStorageSystem kullanımdan kaldırıldı, yeni Get-AzsStorageSubSystem cmdlet'ini sağladık           \* Get-AzsStoragePool kullanımdan kaldırıldı, StorageSubSystem nesnesine kapasite özelliği bulunuyor</span><span class="sxs-lookup"><span data-stu-id="f2df6-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="f2df6-115">Azs.Compute.Admin Modülü           \* Hata Düzeltmesi: Add-AzsPlatformImage, Get-AzsPlatformImage : Yalnızca başarı yolunda ConvertTo-PlatformImageObject çağrısı           \* Hata Düzeltmesi: Add-AzsVmExtension, Get-AzsVmExtension: Yalnızca başarı yolunda ConvertTo-VmExtensionObject çağrısı</span><span class="sxs-lookup"><span data-stu-id="f2df6-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="f2df6-116">Azs.Storage.Admin Modülü           \* Hata düzeltmesi: Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.'</span><span class="sxs-lookup"><span data-stu-id="f2df6-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
