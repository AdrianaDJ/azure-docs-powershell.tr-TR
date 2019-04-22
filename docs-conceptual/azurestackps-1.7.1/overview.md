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
# <a name="azure-stack-module-171"></a>Azure Stack Modülü 1.7.1

## <a name="requirements"></a>Gereksinimler:

Desteklenen en düşük Azure Stack sürümü 1901'dir.

Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin

## <a name="install"></a>Yükleme

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Sürüm Notları

* 1901 güncelleştirmesiyle desteklenir
* Bu hataya neden olan değişiklik yayınıdır. Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin Modülü * Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme. Simetrik anahtarlar için destek kullanım dışı bırakıldı.
* Azs.Fabric.Admin Module       * Kullanımdan Kaldırma           * Get-AzsInfrastructureVolume kullanımdan kaldırıldı, yeni Get-AzsVolume cmdlet'ini sağladık           * Get-AzsStorageSystem kullanımdan kaldırıldı, yeni Get-AzsStorageSubSystem cmdlet'ini sağladık           * Get-AzsStoragePool kullanımdan kaldırıldı, StorageSubSystem nesnesine kapasite özelliği bulunuyor
* Azs.Compute.Admin Modülü           * Hata Düzeltmesi: Add-AzsPlatformImage, Get-AzsPlatformImage : Yalnızca başarı yolunda ConvertTo-PlatformImageObject çağrısı           * Hata Düzeltmesi: Add-AzsVmExtension, Get-AzsVmExtension: Yalnızca başarı yolunda ConvertTo-VmExtensionObject çağrısı
* Azs.Storage.Admin Modülü           * Hata düzeltmesi: Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.'
