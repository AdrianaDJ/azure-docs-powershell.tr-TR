---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574422"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>AzureRM'den Azure PowerShell Az'ye geçirme

Az modülünün AzureRM ile özellik eşliği vardır ama daha kısa ve daha tutarlı cmdlet adları kullanır.
AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır. Geçişi kolaylaştırmak için, Az mevcut betiklerinizi AzureRM kullanarak çalıştırmanıza olanak tanıyan araçlar sunar. Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale yeni modüle geçişi başlatmanıza yardımcı olacaktır.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Mevcut betiklerinizin en son AzureRM sürümüyle çalıştığından emin olma

En önemli adım budur! Mevcut betiklerinizi çalıştırın ve AzureRM'nin _en son_ sürümüyle (__6.12.0__) çalıştığınızdan emin olun. Betikleriniz çalışmazsa, [AzureRM geçiş kılavuzunu](migration-guide.6.0.0.md) mutlaka okuyun.

## <a name="install-the-azure-powershell-az-module"></a>Azure PowerShell Az modülünü yükleme

İlk adım, platformunuza Az modülünü yüklemektir. Az'yi yüklemek için AzureRM'yi kaldırmanız gerekir.
Aşağıdaki adımlarda, mevcut betiklerinizi çalıştırmaya devam etmeyi ve eski cmdlet adlarıyla uyumluluğu sağlamayı öğreneceksiniz.

Azure PowerShell Az modülünü yüklemek için şu adımları izleyin:

* [AzureRM modülünü kaldırma](uninstall-azurerm-ps.md). AzureRM'nin yalnızca en son sürümünü değil _tüm_ yüklü sürümlerini kaldırdığınızdan emin olun.
* [Az modülünü yükleme](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>AzureRM diğer ad modunu etkinleştirme

AzureRM kaldırıldıktan ve betiklerinizin en son AzureRM sürümüyle çalıştığından emin olduktan sonra, sıra Az modülü için uyumluluk modunu etkinleştirmeye gelir. Uyumluluk şu komutla etkinleştirilir:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Diğer adlar, `Az` modülü yüklendiğinde eski cmdlet adlarının kullanılabilmesine olanak tanır. Bu diğer adlar, seçili kapsam için kullanıcı profiline yazılır. Kullanıcı profili yoksa, bir profil oluşturulur.

> [!WARNING]
>
> Bu komut için farklı bir `-Scope` kullanabilirsiniz, ama bunu yapmanız önerilmez! Diğer adlar seçili kapsam için kullanıcı profiline yazılır, dolayısıyla bunları olabildiğince kısıtlı bir kapsamda etkinleştirilmiş durumda tutun. Diğer adların sistem genelinde etkinleştirilmesi, kendi yerel kapsamlarında `AzureRM` yüklemiş olan diğer kullanıcılarda sorunlara yol açabilir.

Diğer ad modu etkinleştirildikten sonra, hala beklendiği gibi çalıştıklarını doğrulamak için betiklerinizi bir kez daha çalıştırın. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modül içeri aktarmalarını ve cmdlet adlarını değiştirme

Genel olarak, modül adları `AzureRM` ve `Azure` `Az` olacak şekilde değiştirilmiştir ve cmdlet'lerde de aynı durum geçerlidir.
Örneğin, `AzureRM.Compute` modülü `Az.Compute` olarak yeniden adlandırılmıştır. Şimdi `New-AzureRmVM` `New-AzVM` ve `Get-AzureStorageBlob` de `Get-AzStorageBlob` olmuştur.

Bu adlandırma değişikliğinin, herhangi bir yeniden adlandırma işlemi yapmadan önce bilmeniz gereken özel durumları vardır:

| AzureRM modülü | Az modülü |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Özet

Bu adımları izleyerek mevcut betiklerinizin tümünü yeni modülü kullanacak şekilde güncelleştirebilirsiniz. Bu adımlarla ilgili, geçiş işleminizi zorlaştıran sorularınız veya sorunlarınız varsa lütfen bu makaleye yorum ekleyin. Bu sayede biz de yönergeleri geliştirebiliriz.