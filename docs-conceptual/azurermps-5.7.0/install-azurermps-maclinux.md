---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323263"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Azure PowerShell'i macOS veya Linux'a yükleme

Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 üzerinde çalıştırmak mümkündür. Windows için .NET Framework üzerine kurulan standart Azure PowerShell yerine, bu ürün .NET Core için oluşturulmuştur ve .Net Core çalışma zamanını destekleyen tüm platformlarda çalıştırılabilir.

> [!NOTE]
> PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.
> Bu ürünler için sınırlı destek sunulur. Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen GitHub üzerinden bir sorun girin.
>
> * [PowerShell Core v6 ile ilgili sorunlar](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell ile ilgili sorunlar](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>PowerShell Core v6'yı yükleme

Linux veya macOS’ta PowerShell Core v6’yı yükleme adımları, Linux dağıtımına ve işletim sistemi sürümüne göre değişir.
Şu makalelerde ayrıntılı yönergeler bulunabilir:

- [macOS'ta PowerShell Core'u yükleme](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Linux'ta PowerShell Core'u yükleme](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>.NET Core için Azure PowerShell'i yükleme

PowerShell Core v6, PowerShellGet modülü önceden yüklü biçimde gelir. Bu sayede PowerShell Galerisi'nde yayımlanmış olan modüller kolayca yüklenebilir. Azure PowerShell'i yüklemek için yeni bir PowerShell oturumu açın ve aşağıdaki komutu çalıştırın:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>AzureRM.Netcore modülünü yükleme

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
  - SQL Veritabanı
  - Depolama
  - Ağ

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.
