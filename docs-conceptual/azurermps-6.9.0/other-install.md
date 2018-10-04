---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bf66e312557f047a9393e26b9de736c1c55c261
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425406"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>MSI ile Windows'a Azure PowerShell yükleme

Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır.  
Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın. Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir. PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).

> [!NOTE]
> Azure PowerShell 6.x ve üzeri sürümler için Web Platformu Yükleyicisi ile yükleme desteği sunulmamaktadır. Web Platformu Yükleyicisi'ni kullanmanız gerekiyorsa lütfen MSI kullanmayı veya Azure PowerShell'in eski bir sürümünü yüklemeyi deneyin.

Azure PowerShell'i bir Docker kapsayıcısında çalıştırmak için bkz. [Azure PowerShell'i Docker'da çalıştırma](azurerm-ps-in-docker.md).

Linux veya macOS ortamlarına yüklemek için bkz. [Azure PowerShell'i macOS veya Linux'a yükleme](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme

Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir. Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler. Hem `AzureRM` hem de `Azure` modülleri yüklenir.

> [!NOTE]
> `Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.

Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).