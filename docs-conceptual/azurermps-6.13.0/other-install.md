---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 41edefe96ecebf0a7276cdc3b4510acd7e8098f4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241619"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>MSI ile Windows'a Azure PowerShell yükleme

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır.
Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın. Azure PowerShell'i Windows'a yüklemek için PowerShellGet'i kullanmanız önerilir. PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).

> [!NOTE]
> Azure PowerShell 6.x ve üzeri sürümler için Web Platformu Yükleyicisi ile yükleme desteği sunulmamaktadır. Web Platformu Yükleyicisi'ni kullanmanız gerekiyorsa lütfen MSI kullanmayı veya Azure PowerShell'in eski bir sürümünü yüklemeyi deneyin.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme

Windows PowerShell 5.x için Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir. Azure modüllerinin önceki sürümlerini MSI olarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler. Hem `AzureRM` hem de `Azure` modülleri yüklenir.

> [!NOTE]
> `Azure` modülünü yalnızca Azure klasik dağıtım modeliyle çalışıyorsanız kullanın.

Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module AzureRM` kullanarak modülü el ile içeri aktarmanız gerekir. Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.

Başlattığınız her yeni PowerShell oturumu için bu adımı tekrarlamanız gerekir. Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).
