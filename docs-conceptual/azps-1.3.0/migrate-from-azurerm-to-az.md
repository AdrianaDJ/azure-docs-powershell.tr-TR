---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145171"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>AzureRM'den Azure PowerShell Az'ye geçirme

Az modülünün AzureRM ile özellik eşliği vardır ama daha kısa ve daha tutarlı cmdlet adları kullanır.
AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır. Geçişi kolaylaştırmak için, Az mevcut betiklerinizi AzureRM kullanarak çalıştırmanıza olanak tanıyan araçlar sunar. Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale yeni modüle geçişi başlatmanıza yardımcı olacaktır.

AzureRM ile Az arasındaki yeni değişikliklerin tam listesini görmek için bkz. [Az 1.0.0 için geçiş kılavuzu](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>AzureRM’nin yüklü sürümlerini denetleme

Az modülü AzureRM modülüyle yan yana yüklenebilir, ancak bu önerilmez. Geçiş adımlarını uygulamadan önce, sisteminizde hangi AzureRM sürümlerinin yüklü olduğunu denetleyin. Bunu yaparak betiklerin zaten en son yayında çalıştığından emin olabilir ve AzureRM’yi kaldırmadan komut diğer adlarını etkinleştirip etkinleştiremeyeceğinizi anlayabilirsiniz.

AzureRM’nin hangi sürümlerini yüklediğinizi denetlemek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Mevcut betiklerinizin en son AzureRM sürümüyle çalıştığından emin olma

En önemli adım budur! Mevcut betiklerinizi çalıştırın ve AzureRM'nin _en son_ sürümüyle (__6.13.1__) çalıştığınızdan emin olun. Betikleriniz çalışmazsa, [AzureRM geçiş kılavuzunu](/powershell/azure/azurerm/migration-guide.6.0.0) mutlaka okuyun.

## <a name="install-the-azure-powershell-az-module"></a>Azure PowerShell Az modülünü yükleme

İlk adım, platformunuza Az modülünü yüklemektir. Az’yi yüklediğinizde AzureRM’yi kaldırmanız önerilir. Aşağıdaki adımlarda, mevcut betiklerinizi çalıştırmaya devam etmeyi ve eski cmdlet adlarıyla uyumluluğu sağlamayı öğreneceksiniz.

Azure PowerShell Az modülünü yüklemek için şu adımları izleyin:

* __ÖNERİLİR__: [AzureRM modülünü kaldırma](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  AzureRM'nin yalnızca en son sürümünü değil _tüm_ yüklü sürümlerini kaldırdığınızdan emin olun.
* [Az modülünü yükleme](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>AzureRM uyumluluk diğer adlarını etkinleştirin 

> [!IMPORTANT]
>
> Uyumluluk modunu yalnızca AzureRM’nin _tüm_ sürümlerini kaldırdıysanız etkinleştirin. AzureRM cmdlet’leri hala kullanılabilir durumdayken uyumluluk modunun etkinleştirilmesi, tahmin edilemeyen davranışlara yol açabilir. AzureRM’yi kaldırmamaya karar verdiyseniz bu adımı atlayın, ancak tüm AzureRM cmdlet’lerinin eski modülleri kullanacağını ve herhangi bir Az cmdlet’ini çağırmayacağını aklınızda bulundurun.

AzureRM kaldırıldıktan ve betiklerinizin en son AzureRM sürümüyle çalıştığından emin olduktan sonra, sıra Az modülü için uyumluluk modunu etkinleştirmeye gelir. Uyumluluk şu komutla etkinleştirilir:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Diğer adlar, Az modülü yüklendiğinde eski cmdlet adlarının kullanılabilmesine olanak tanır. Bu diğer adlar, seçili kapsam için kullanıcı profiline yazılır. Kullanıcı profili yoksa, bir profil oluşturulur.

> [!WARNING]
>
> Bu komut için farklı bir `-Scope` kullanabilirsiniz, ama bunu yapmanız önerilmez. Diğer adlar seçili kapsam için kullanıcı profiline yazılır, dolayısıyla bunları olabildiğince kısıtlı bir kapsamda etkinleştirilmiş durumda tutun. Diğer adların sistem genelinde etkinleştirilmesi, kendi yerel kapsamlarında AzureRM’yi yüklemiş olan diğer kullanıcılarda sorunlara yol açabilir.

Diğer ad modu etkinleştirildikten sonra, hala beklendiği gibi çalıştıklarını doğrulamak için betiklerinizi bir kez daha çalıştırın. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modül içeri aktarmalarını ve cmdlet adlarını değiştirme

Genel olarak, modül adları `AzureRM` ve `Azure` `Az` olacak şekilde değiştirilmiştir ve cmdlet'lerde de aynı durum geçerlidir.
Örneğin, `AzureRM.Compute` modülü `Az.Compute` olarak yeniden adlandırılmıştır. Şimdi `New-AzureRMVM` `New-AzVM` ve `Get-AzureStorageBlob` de `Get-AzStorageBlob` olmuştur.

Bu adlandırma değişikliğinin bilmeniz gereken özel durumları vardır. Bazı modüller yeniden adlandırılmış veya mevcut modüllerle birleştirilmiştir, ancak `AzureRM` veya `Azure` adının `Az` olarak değiştirilmesi dışında modül cmdlet’lerinin son eki bundan etkilenmemiştir. Bunun dışında, cmdlet sonekinin tamamı yeni modül adını yansıtacak şekilde değiştirilmiştir.

| AzureRM modülü | Az modülü | Cmdlet soneki değişti mi? |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Evet |
| AzureRM.Insights | Az.Monitor | Evet |
| AzureRM.DataFactories | Az.DataFactory | Evet |
| AzureRM.DataFactoryV2 | Az.DataFactory | Evet |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | Hayır |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | Hayır |
| AzureRM.Tags | Az.Resources | Hayır |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Hayır |
| AzureRM.UsageAggregates | Az.Billing | Hayır |
| AzureRM.Consumption | Az.Billing | Hayır |

## <a name="summary"></a>Özet

Bu adımları izleyerek mevcut betiklerinizin tümünü yeni modülü kullanacak şekilde güncelleştirebilirsiniz. Bu adımlarla ilgili, geçiş işleminizi zorlaştıran sorularınız veya sorunlarınız varsa lütfen bu makaleye yorum ekleyin. Bu sayede biz de yönergeleri geliştirebiliriz.
