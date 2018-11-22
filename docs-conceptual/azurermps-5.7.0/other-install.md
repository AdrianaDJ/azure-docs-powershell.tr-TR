---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet kullanmadan yükleme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f9293d2715b36161c3e6d0d9469b6f18ab35d6c8
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52257508"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>MSI veya Web Platformu Yükleyicisi ile Windows'a Azure PowerShell yükleme

Bu makalede MIS veya Web Platformu Yükleyicisi (WebPI) kullanarak Windows'a Azure PowerShell yükleme işlemi açıklanır.  
Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın. Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir. PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).

Linux veya macOS ortamlarına yüklemek için bkz. [Azure PowerShell'i macOS veya Linux'a yükleme](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme

Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir. Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler. Hem `AzureRM` hem de `Azure` modülleri yüklenir.

> [!NOTE]
> `Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.

Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Web Platformu Yükleyicisi'ni kullanarak Windows'a yükleme veya güncelleştirme

[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın. Azure modüllerinin önceki sürümlerini MSI veya WebPI ile yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. Modüller `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yüklenir. Hem `AzureRM` hem de `Azure` modülleri yüklenir.

> [!NOTE]
> `Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.

Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).
