---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264419"
---
# <a name="azure-stack-module-180"></a>Azure Stack Modülü 1.8.0

## <a name="requirements"></a>Gereksinimler:

Desteklenen en düşük Azure Stack sürümü 1910’dur.

Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin

## <a name="install"></a>Yükleme

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Sürüm Notları

* 1910 güncelleştirmesiyle desteklenir
* Değişiklikler şunları içerir:

    - **Yeni DRP Yönetici modülü**: Dağıtım Kaynak Sağlayıcısı (DRP), kaynak sağlayıcılarının Azure Stack Hub’a düzenlenmiş olarak dağıtılmasını sağlar. Bu komutlar, DRP ile etkileşimde bulunmak için Azure Resource Manager katmanıyla etkileşime geçer.

    - **BRP**:
        - Azure’ın yığın altyapısı yedeklemesine yönelik tek rolü geri yükleme desteği.
        - R`estore-AzsBackup` cmdlet’ine `RoleName` parametresi eklendi.

    - **FRP**: API sürümü 2019-05-01 ile **Sürücü** ve **Birim** kaynaklana yönelik önemli değişiklikler. Bu özellikler Azure Stack Hub 1910 ve sonraki sürümlerinde desteklenir:
        - Kimlik, `Name`, `HealthStatus`ve `OperationalStatus` değerleri değiştirildi.
        - **Sürücü** kaynakları için yeni `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` ve `StoragePool` özellikleri desteklenir.
        - **Sürücü** kaynakları için `CanPool` ve `CannotPoolReason` özellikleri kullanımdan kaldırıldı. Bunların yerine `OperationalStatus` kullanın.
