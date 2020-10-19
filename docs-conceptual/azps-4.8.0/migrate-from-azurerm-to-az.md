---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021100"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Azure PowerShell'i AzureRM'den Az modülüne geçirme

AzureRM PowerShell modülünün tüm sürümleri eskidir, ancak destek dışı değildir. [Az PowerShell modülü](install-az-ps.md) şu anda Azure ile etkileşim kurmak için önerilen PowerShell modülüdür.

AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır. Geçişi kolaylaştırmak için [AzureRM - Az geçişi araç seti](https://github.com/Azure/azure-powershell-migration) geliştirilmiştir. Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale Az PowerShell modülüne geçişi başlatmanıza yardımcı olacaktır. Az PowerShell modülünün neden oluşturulduğu hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](new-azureps-module-az.md).

AzureRM ile Az arasında hataya neden olan değişikliklerin tam listesini görmek için bkz. [AzureRM'den AZ modülüne tüm değişiklikler](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Mevcut betikleri en son AzureRM sürümüyle çalıştığından emin olun

Geçiş adımlarını uygulamadan önce, sisteminizde hangi AzureRM sürümlerinin yüklü olduğunu denetleyin.
Bunu yaparak betiklerin zaten en son sürümde çalıştığından emin olabilir ve AzureRM’nin hangi sürümlerinin kaldırılması gerektiğini anlayabilirsiniz.

AzureRM’nin hangi sürümlerini yüklediğinizi denetlemek için aşağıdaki örneği çalıştırın:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

AzureRM'nin kullanılabilir **en son** sürümü **6.13.1**'dir. Sizde bu sürüm yüklü değilse, mevcut betiklerinizin Az modülüyle çalışabilmesi için bu makalede ve [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) açıklananların ötesinde ek değişikler yapılması gerekebilir.

Betikleriniz AzureRM 6.13.1 ile çalışmıyorsa, bunları [AzureRM 5.x'ten 6.x'e geçiş kılavuzuna](/powershell/azure/azurerm/migration-guide.6.0.0) göre güncelleştirin. AzureRM modülünün önceki bir sürümünü kullanıyorsanız, her büyük sürüm için geçiş kılavuzları sağlanır.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>AzureRM - Az geçişi araç setini yükleme

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>PowerShell betiklerinizi otomatik olarak geçirme

AzureRM - Az geçişi araç setiyle, betiklerinizde değişiklikler yapmadan ve Az PowerShell modülünü yüklemeden önce bu betiklerin nasıl değiştirileceğini belirleyen bir plan oluşturabilirsiniz.

[PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme](quickstart-migrate-azurerm-to-az-automatically.md) hızlı başlangıcı, PowerShell betiklerinizi AzureRM'den Az PowerShell modülüne otomatik olarak güncelleştirme işleminin tamamında size yol gösterir.

## <a name="next-steps"></a>Sonraki adımlar

[Azure PowerShell'i yükleme](install-az-ps.md)
[AzureRM'yi kaldırma](uninstall-az-ps.md#uninstall-the-azurerm-module)
