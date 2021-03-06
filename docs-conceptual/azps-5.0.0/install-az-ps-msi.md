---
title: MSI ile Azure PowerShell'i yükleme
description: Azure PowerShell'i PowerShellGet olmadan MSI kullanarak yükleme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: de9ac41b86e97c948943d22b2019c8022bdf52e0
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409525"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>MSI ile Windows'a Azure PowerShell yükleme

Bu makalede MSI yükleyicisi kullanarak Azure PowerShell'i Windows'a yükleme adımları açıklanmaktadır. MSI yükleyicisi, PowerShell Galerisi'nin güvenlik duvarı tarafından engelleniyor olabileceği veya çevrimdışı bir yükleyicinin gerektiği ortamlar için sağlanmıştır. Azure PowerShell'i yüklemek için önerilen yöntem PowerShellGet'in kullanılmasıdır. PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-az-ps.md).

## <a name="requirements"></a>Gereksinimler

Windows üzerinde MSI yükleyicisi yalnızca PowerShell 5.1 için Azure PowerShell yüklemek üzere tasarlanmıştır. Windows dışı platformlarda yüklemek veya PowerShell’in sonraki sürümlerini yüklemek için [PowerShellGet ile yükleme](install-az-ps.md) yöntemini kullanın. PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:

```powershell-interactive
$PSVersionTable.PSVersion
```

PowerShell 5.1'de Azure PowerShell'i kullanmak için şunları yapmalısınız:

1. Gerekirse [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin. Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.
2. [.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme

Azure PowerShell için MSI paketini [GitHub](https://github.com/Azure/azure-powershell/releases)’dan edinebilirsiniz:

1. https://github.com/Azure/azure-powershell/releases öğesine gidin.
2. Azure PowerShell için en son Galeri Modülünü arayın. (Bunlar kronolojik olarak listelenir ve genellikle adı olmadan yalnızca "4.7.0" gibi bir yayın sürümüdür).
3. Düzeltme eki notlarının en altına kaydırın ve MSI seçeneklerini göstermek için "Varlıklar" seçeneğinin yanındaki oka tıklayın.
4. İndirmeyi başlatmak için tercih ettiğiniz Az-Cmdlets MSI'ya tıklayın.

Azure PowerShell’in önceki sürümlerini MSI kullanarak yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `${env:ProgramFiles}\WindowsPowerShell\Modules` içine yükler.

Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir. Modülü yapısından dolayı, bu işlem bir dakika kadar sürebilir.

Başlattığınız her yeni PowerShell oturumu için bu adımı tekrarlamanız gerekir. Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="provide-feedback"></a>Geri bildirimde bulunma

Azure PowerShell’de bir hata bulursanız [GitHub’da sorun bildirin](https://github.com/Azure/azure-powershell/issues). Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md). Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).
