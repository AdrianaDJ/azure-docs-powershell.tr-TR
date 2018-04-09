---
title: Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell'i macOS ve Linux'ta yükleme ve ilk kez kullanmak üzere yapılandırma.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: eed7a35fcf20a17c83d9e5e3272be4b77fa12c34
ms.sourcegitcommit: 8376e0bc5f862d382d7283ba72990e3707591e7b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/30/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Azure PowerShell'i macOS ve Linux'a yükleme ve yapılandırma

PowerShell Core v6 ve Azure PowerShell artık Windows dışındaki platformlara yüklenebilir.
Azure PowerShell'i macOS ve Linux'a yükleme adımları Windows ile benzerdir, ancak önce PowerShell Core v6'yı yüklemeniz gerekir.

> [!NOTE]

> PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.
> Bu ürünler için sınırlı destek sunulur. Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen bunları GitHub üzerinden bildirin.
>
> * [PowerShell Core v6 ile ilgili sorunlar](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell ile ilgili sorunlar](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>1. Adım: PowerShell Core v6'yı yükleme

PowerShell Core v6'yı yükleme adımları, hedef işletim sistemine göre değişiklik gösterir.
PowerShell Core v6 Windows'a da yüklenebilir, ancak bu makalede macOS ve Linux ele alınmışır. Azure PowerShell'i Windows üzerinde kullanmak isterseniz, Windows'a yönelik [yükleme](./install-azurerm-ps.md) makalesine bakın.

Linux veya macOS’ta **PowerShell Core v6**’yı yükleme adımları, Linux dağıtımına ve işletim sistemi sürümüne göre değişkenlik gösterir.
Şu makalede ayrıntılı yönergeler bulunabilir:

- [macOS ve Linux’ta PowerShell Core’u yükleme](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>2. Adım: .NET Core için Azure PowerShell'i yükleme

PowerShell Core v6, PowerShellGet modülü önceden yüklü biçimde gelir. Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir. Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>3. Adım: AzureRM.Netcore modülünü yükleme

Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir. Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

İçeri aktarma işlemi tamamlandıktan sonra, aşağıdaki komutla Azure oturumu açmayı deneyerek yeni yüklediğiniz modülü test edebilirsiniz:

```powershell
Connect-AzureRmAccount
```

Yukarıdaki komut, `https://aka.ms/devicelogin` adresine gidip verilen kodu girmenizi isteyecektir.

## <a name="available-cmdlets"></a>Kullanılabilen cmdlet'ler

.NET Standard için Azure PowerShell modülleri geliştirme aşamasındadır. Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz. AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:

* Hesap yönetimi
  - Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma
  - Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme
* Ortam
  - Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma
  - Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma
* Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.
  - Sanal Makine
  - App Service (Web siteleri)
  - SQL Database
  - Depolama
  - Ağ

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.
