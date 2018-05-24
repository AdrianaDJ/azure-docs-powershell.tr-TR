---
title: Azure PowerShell Service Management modülünü yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 6f0f56dd09913ac535552aaa06c8e4431d78c24a
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Azure PowerShell Service Management modülünü yükleme

Azure PowerShell’in [PowerShell Galerisi](https://www.powershellgallery.com/)’nden yüklenmesi, tercih edilen yükleme yöntemidir.

## <a name="step-1-install-powershellget"></a>1. Adım: PowerShellGet yükleme

PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir. Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun. PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet yüklü değilse bkz. [PowerShellGet’i edinme](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>2. Adım: Azure PowerShell'i yükleme

Yönetici olarak çalıştırılan Windows PowerShell konsolundan aşağıdaki komutu çalıştırın:

```powershell
Install-Module Azure
```

Azure modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür. AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure modülleri PowerShell Galerisi’nden indirilip yüklenir.

Azure Service Management modülünün, Azure PowerShell Resource Manager modülleriyle ortak bağımlılıkları vardır. Azure PowerShell Resource Manager modüllerini yüklediyseniz, yükleme komutuna `-AllowClobber` parametresini eklemeniz gerekir. Bu, mevcut paylaşılan bağımlılıkların güncelleştirilmesine olanak tanır. Bu parametre kullanılmazsa modül yüklenemez.

```powershell
Install-Module Azure -AllowClobber
```

Bu modülü yükledikten sonra aşağıdaki komutu çalıştırarak modülü içeri aktarabilirsiniz:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Cmdlet'leri kullanmak için

Azure Service Management cmdlet’leriyle çalışmaya başlamak için öncelikle Azure hesabınızda oturum açın. Hesabınızda oturum açmak için aşağıdaki komutu çalıştırın:

```powershell
Add-AzureAccount
```

Azure’da oturum açıldıktan sonra, Azure PowerShell ilgili oturum için bir bağlam oluşturur. Bu bağlam, ilgili oturum içindeki tüm cmdlet’ler için kullanılacak Azure PowerShell ortamını, hesabını, kiracısını ve aboneliğini içerir. Artık aşağıdaki modülleri kullanmaya hazırsınız.

## <a name="azure-service-management-cmdlets"></a>Azure Service Management cmdlet’leri

Azure PowerShell modülleri sık sık güncelleştirilir. Çevrimiçi cmdlet yardımının modülünüzde olmayan cmdlet’leri veya parametreleri içerdiğini fark ederseniz, modülün en son sürümünü indirip yükleyin. Modülünüzün sürümün öğrenmek için şunu yazın: `(Get-Module Azure).Version`.

Azure’daki bazı genel görevleri otomatikleştirmenize yardımcı olabilecek örnek betikler için bkz. [Windows Azure Betik Merkezi](http://www.windowsazure.com/documentation/scripts/).

Windows PowerShell’i yükleme, öğrenme, kullanma ve özelleştirme hakkında genel bilgiler için bkz. [Windows PowerShell ile Betik Oluşturma](http://go.microsoft.com/fwlink/p/?linkid=320210).

### <a name="how-to-get-powershellget"></a>PowerShellGet edinme

|İşletim Sistemi Sürümü|Yükleme yönergeleri|
|---|---|
|Bilgisayarımda Windows 10 veya Windows Server 2016 yüklü|İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir|
|PowerShell 5'e yükseltme yapmak istiyorum|[WMF’nin en son sürümünü yükleyin](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Windows’un PowerShell 3 veya PowerShell 4 içeren bir sürümünü çalıştırıyorum|[PackageManagement modüllerini alın](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Azure PowerShell sürümünü denetleme

En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir. Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
