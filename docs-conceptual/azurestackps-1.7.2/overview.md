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
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037678"
---
# <a name="azure-stack-module-172"></a>Azure Stack Modülü 1.7.2

## <a name="requirements"></a>Gereksinimler:

Desteklenen en düşük Azure Stack sürümü 1904'dir.

Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin

## <a name="install"></a>Yükleme

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Sürüm Notları

* 1904 güncelleştirmesiyle desteklenir
* Bu hataya neden olan değişiklik yayınıdır. Hataya neden olan değişikliklerin ayrıntıları için bkz. <https://aka.ms/azspshmigration170>
* Hataya neden olan değişiklik: Sertifika tabanlı şifreleme modundaki değişiklikleri yedekleme. Simetrik anahtarlar için destek kullanım dışı bırakıldı.
* Hataya neden olan değişikliklerin ayrıntıları için bkz. https://aka.ms/azspshmigration170
* Azs.Storage.Admin Modülü 
* Hata düzeltmesi - Yeni Depolama Kotası değer sağlanmadığında varsayılanları kullanıyor.
