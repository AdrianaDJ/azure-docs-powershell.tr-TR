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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240564"
---
# <a name="azure-stack-module-170"></a>Azure Stack Modülü 1.7.0

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1901'dir.

Not: Daha önceki bir sürümü kullanıyorsanız 1.7.0 sürümünü yükleyin

## <a name="install"></a>Yükleme
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a>Sürüm Notları
* 1901 güncelleştirmesiyle desteklenir
* Bu hataya neden olan değişiklik yayınıdır. Hataya neden olan değişikliklerin ayrıntıları için bkz. https://aka.ms/azspshmigration170
* Azs.Backup.Admin Modülü * Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme. Simetrik anahtarlar için destek kullanım dışı bırakıldı.
* Azs.Fabric.Admin Module       * Kullanımdan Kaldırma           * Get-AzsInfrastructureVolume kullanımdan kaldırıldı, yeni Get-AzsVolume cmdlet'ini sağladık           * Get-AzsStorageSystem kullanımdan kaldırıldı, yeni Get-AzsStorageSubSystem cmdlet'ini sağladık           * Get-AzsStoragePool kullanımdan kaldırıldı, StorageSubSystem nesnesine kapasite özelliği bulunuyor
* Azs.Compute.Admin Modülü           * Hata Düzeltmesi: Add-AzsPlatformImage, Get-AzsPlatformImage : Yalnızca başarı yolunda ConvertTo-PlatformImageObject çağrısı           * Hata Düzeltmesi: Add-AzsVmExtension, Get-AzsVmExtension: Yalnızca başarı yolunda ConvertTo-VmExtensionObject çağrısı
* Azs.Storage.Admin Modülü           * Hata düzeltmesi: Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.'

