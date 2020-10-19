---
title: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme
description: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirmeyi öğrenin.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002343"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Hızlı Başlangıç: PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme

Bu makalede, Az.Tools.Migration PowerShell modülünü kullanarak PowerShell betiklerinizi ve betik modüllerinizi AzureRM'den Az PowerShell modülüne otomatik olarak yükseltmeyi öğreneceksiniz.

> [!IMPORTANT]
> Az.Tools.Migration PowerShell modülü şu anda genel önizlemede aşamasındadır. Bu önizleme sürümü bir hizmet düzeyi sözleşmesi olmadan sağlanır. Üretim iş yüklerinde kullanılması önerilmez. Bazı özellikler desteklenmiyor olabileceği gibi özellikleri sınırlandırılmış da olabilir. Daha fazla bilgi için bkz. [Microsoft Azure Önizlemeleri için Ek Kullanım Koşulları](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Az.Tools.Migration PowerShell modülüyle ilgili geri bildirimleri ve sorunları `azure-powershell-migration` deposunda [bir GitHub sorunu](https://github.com/Azure/azure-powershell-migration/issues) yoluyla gönderin.

## <a name="requirements"></a>Gereksinimler

* Mevcut PowerShell betiklerinizi en son [AzureRM PowerShell modülü sürümüne (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) yükseltin.
* Az.Tools.Migration PowerShell modülünü yükleyin.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>1\. Adım: Yükseltme planı oluşturma

Betiklerinizi ve modüllerinizi Az PowerShell modülüne geçirecek bir yükseltme planı oluşturmak için `New-AzUpgradeModulePlan` cmdlet'ini kullanırsınız. Yükseltme planında, AzureRM'den Az PowerShell cmdlet'lerine taşırken değiştirilmesi gereken belirli dosya ve konum noktalarının ayrıntıları yer alır.

> [!NOTE]
> `New-AzUpgradeModulePlan` cmdlet'i planı yürütmez; yalnızca yükseltme adımlarını oluşturur.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Yükseltme planının sonuçlarını gözden geçirin.

```powershell
# Show the entire upgrade plan
$Plan
```

Uyarıları veya hataları olan komutlara göre sonuçları filtrelemek için aşağıdaki komutu çalıştırın. Bu işlem büyük sonuç kümelerinde yükseltmeyi gerçekleştirmeden önce hataları hızla belirlemeye yardımcı olabilir.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>2\. Adım: Yükseltmeyi gerçekleştirme

`Invoke-AzUpgradeModulePlan` cmdlet'ini çalıştırdığınızda yükseltme planı yürütülür. Bu komut, `New-AzUpgradeModulePlan` cmdlet'i tarafından belirlenmiş olan hatalar dışında belirtilen dosya veya klasörlerin yükseltmesini yapar.

Bu komut için, dosyaların yerinde değiştirilmesi mi gerektiğini yoksa özgün dosyalarınızın yanı sıra (özgün dosyaları değiştirmeden bırakarak) yeni dosyaların mı kaydedileceğini belirtmeniz gerekir.

> [!CAUTION]
> İşlem geri alınamaz. Geçirmeye çalıştığınız PowerShell betiklerinizin ve modüllerinizin her zaman bir yedek kopyası olmasına dikkat edin.

> [!WARNING]
> `-FileEditMode ModifyExistingFiles` seçeneği belirtildiğinde `Invoke-AzUpgradeModulePlan` cmdlet'i yıkıcıdır! `New-AzUpgradeModulePlan` cmdlet'i tarafından oluşturulan modül yükseltme planına uygun olarak betiklerinizi ve işlevlerinizi yerinde değiştirir. Yıkıcı olmayan bir seçenek için onun yerine `-FileEditMode SaveChangesToNewFiles` belirtin.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Yükseltme işleminin sonuçlarını gözden geçirin.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Herhangi bir hata döndürülürse, şu komutu kullanarak hata sonuçlarına daha yakından bakabilirsiniz:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Sınırlamalar

* Toplu parametre kümelerinde otomatik parametre adı güncelleştirmesi desteklenmez. Yükseltme planı oluşturma sırasında böyle bir güncelleştirme bulunursa uyarı döndürülür.
* Dosya G/Ç işlemlerinde varsayılan kodlama kullanılır. Olağan dışı dosya kodlama durumları sorunlara neden olabilir.
* Pester birimi sahte test deyimlerine geçirilen AzureRM cmdlet'leri algılanmaz.
* Şu anda hedef olarak yalnızca Az PowerShell modülü sürüm 4.6.1 desteklenir.

## <a name="next-steps"></a>Sonraki adımlar

Az PowerShell modülü hakkında daha fazla bilgi edinmek için [Azure PowerShell belgelerine](https://docs.microsoft.com/powershell/azure/) bakın