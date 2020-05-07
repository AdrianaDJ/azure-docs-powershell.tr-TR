---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053324"
---
# <a name="azure-stack-module-160"></a>Azure Stack Modülü 1.6.0

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1811'dir.

Not: Daha önceki bir sürümü kullanıyorsanız 1.6.0 sürümünü yükleyin

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

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Sürüm Notları
* 1811 güncelleştirmesiyle desteklenir
* Azs.Compute.Admin modülü
    * New-DataDiskObject için eksik Azs ön eki düzeltildi ve gelecekte kullanım dışı bırakılabileceğine ilişkin uyarıyı içeren bir diğer ad eklendi.
* Azs.Update.Admin Module
    * Install-AzsUpdate'ten önce Test-AzureStack'in çalıştırılmasını öneren bir uyarı eklendi
* Azs.Fabric.Admin
    * Yeni cmdlet (Özellikler Azure Stack 1811+ sürümlerinde destekleniyor)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Kullanımdan kaldırma
        * Get-AzsInfrastructureVolume artık Get-AzsVolume cmdlet'in diğer adı
* Azs.InfrastructureInsights.Admin
    *  Yeni Repair-AzsAlert cmdlet'i eklendi
* Azs.Storage.Admin
    * Varsayılan kota değerlerinin kullanılmamasına neden olan hata düzeltildi
* Azs.Subscriptions.Admin Module
    * New-AddonPlanDefinitionObject için eksik Azs ön eki düzeltildi ve gelecekte kullanım dışı bırakılabileceğine ilişkin uyarıyı içeren bir diğer ad eklendi.
