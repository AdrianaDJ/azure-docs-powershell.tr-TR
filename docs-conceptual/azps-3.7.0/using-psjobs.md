---
title: PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma
description: -AsJob ve Start-Job kullanarak Azure PowerShell cmdlet'lerini paralel veya arka plan görevi olarak çalıştırmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440427"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma

Azure PowerShell, Azure bulutuna bağlanmaya ve yanıtları beklemeye dayanır; dolayısıyla bu cmdlet'lerin çoğu buluttan yanıt alana kadar PowerShell oturumunuzu engeller.
Powershell İşleri, tek bir PowerShell oturumunun içinden cmdlet'leri arka planda çalıştırmanıza veya Azure'da aynı anda birden fazla görev gerçekleştirmenize olanak tanır.

Bu makalede Azure PowerShell cmdlet'lerini PowerShell İşleri olarak çalıştırma ve tamamlanıp tamamlanmadığını denetleme konusuna kısa bir genel bakış sağlanır. Komutları Azure PowerShell'de çalıştırmak için Azure PowerShell bağlamları gerekir ve bunlar [Azure bağlamları ve oturum açma bilgileri](context-persistence.md) konusunda ayrıntılı olarak açıklanmıştır.
PowerShell İşleri hakkında daha fazla bilgi edinmek için bkz. [PowerShell İşleri hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>PowerShell işleri ile Azure bağlamları

PowerShell İşleri, ekli bir PowerShell oturumu olmadan ayrı işlemler olarak çalışır, dolayısıyla Azure kimlik bilgilerinizin onlarla paylaşılması gerekir. Kimlik bilgileri Azure bağlam nesneleri olarak şu yöntemlerden biriyle geçirilir:

* Otomatik bağlam kalıcılığı. Bağlam kalıcılığı varsayılan olarak etkinleştirilir ve oturum açma bilgilerinizi birden çok oturum arasında korur. Bağlam kalıcılığı etkinleştirildiğinde geçerli Azure bağlamı yeni işleme geçirilir:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Azure bağlam nesnesi sağlamak için Azure PowerShell cmdlet'leriyle `-AzContext` parametresini kullanın:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Bağlam kalıcılığı devre dışı bırakılırsa `-AzContext` bağımsız değişkeni gereklidir.

* Bazı Azure PowerShell cmdlet'leri tarafından sağlanan `-AsJob` anahtarını kullanın. Bu anahtar cmdlet'i otomatik olarak geçerli etkin Azure bağlamını kullanıp PowerShell İşi olarak başlatır:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Cmdlet'in `-AsJob` anahtarını destekleyip desteklemediğini görmek için başvuru belgelerine bakın. `-AsJob` anahtarı bağlam otomatik kaydetme ayarının etkinleştirilmesini gerektirmez.

Çalışan işin durumunu denetlemek için [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet'ini kullanabilirsiniz. Şimdiye kadar çalışan işten çıkış almak için [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet'ini kullanın.

Azure'da bir işlemin ilerleme durumunu uzaktan denetlemek için, iş tarafından değiştirilmekte olan kaynağın türüyle ilişkilendirilmiş `Get-` cmdlet'lerini kullanın:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Ayrıca Bkz.

* [Azure PowerShell cmdlet'leri](context-persistence.md)
* [PowerShell İşleri hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Get-Job başvurusu](/powershell/module/microsoft.powershell.core/get-job)
* [Receive-Job başvurusu](/powershell/module/microsoft.powershell.core/receive-job)
