---
title: Azure Stack Hub Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Hub Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 754038a312a20e0dd87075bdeb51b13a1f1810a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022985"
---
# <a name="azure-stack-hub-module-202"></a>Azure Stack Hub Modülü 2.0.2

## <a name="requirements"></a>Gereksinimler:

Desteklenen en düşük Azure Stack Hub sürümü 2002’dir.

Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin

## <a name="install"></a>Yükleme

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a>Sürüm Notları

* 2002 güncelleştirmesiyle desteklenir.  

  Azure Stack Hub 2.0.0 hataya neden olan bir değişikliktir. Modül AzureRM modülü yerine Az modülünü kullanır. [Azure Stack Hub’da AzureRM’den Azure PowerShell Az’ye geçiş](https://aka.ms/AA7qsji) bölümünde bir geçiş kılavuzu ve hataya neden olan değişikliklerin listesini bulabilirsiniz.