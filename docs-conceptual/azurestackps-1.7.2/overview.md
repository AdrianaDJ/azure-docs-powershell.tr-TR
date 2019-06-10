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
# <a name="azure-stack-module-172"></a>Azure Stack Modülü 1.7.2

## <a name="requirements"></a>Gereksinimler:

Desteklenen en düşük Azure Stack sürümü 1904'dir.

Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin

## <a name="install-powershell-for-azure-stack"></a>Azure Stack için PowerShell yükleme

Yükleme üç adımdan oluşur:

1. Azure Stack sürümünüze bağlı olarak Azure Stack PowerShell'i yükleme
2. Ek depolama özelliklerini etkinleştirme
3. PowerShell yüklenmesini onaylama

### <a name="install-azure-stack-powershell"></a>Azure Stack PowerShell’i yükleme

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

### <a name="enable-additional-storage-features"></a>Ek depolama özelliklerini etkinleştirme

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

## <a name="release-notes"></a>Sürüm Notları

* 1904 güncelleştirmesiyle desteklenir
* Bu hataya neden olan değişiklik yayınıdır. Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin Modülü * Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme. Simetrik anahtarlar için destek kullanım dışı bırakıldı.
* Azs.Fabric.Admin Module       * Kullanımdan Kaldırma           * Get-AzsInfrastructureVolume kullanımdan kaldırıldı, yeni Get-AzsVolume cmdlet'ini sağladık           * Get-AzsStorageSystem kullanımdan kaldırıldı, yeni Get-AzsStorageSubSystem cmdlet'ini sağladık           * Get-AzsStoragePool kullanımdan kaldırıldı, StorageSubSystem nesnesine kapasite özelliği bulunuyor
* Azs.Compute.Admin Modülü           * Hata Düzeltmesi: Add-AzsPlatformImage, Get-AzsPlatformImage : Yalnızca başarı yolunda ConvertTo-PlatformImageObject çağrısı           * Hata Düzeltmesi: Add-AzsVmExtension, Get-AzsVmExtension: Yalnızca başarı yolunda ConvertTo-VmExtensionObject çağrısı
* Azs.Storage.Admin Modülü           * Hata düzeltmesi: Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.'
