---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Betikleri AzureRM modülünden yeni Az modülüne geçirmeye yönelik adımları ve araçları öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062114"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Azure PowerShell'i AzureRM'den Az modülüne geçirme

Az modülünün AzureRM ile özellik eşliği vardır ama daha kısa ve daha tutarlı cmdlet adları kullanır.
AzureRM cmdlet'leri için yazılmış betikler otomatik olarak yeni modülle çalışmayacaktır. Geçişi kolaylaştırmak için, Az mevcut betiklerinizi AzureRM kullanarak çalıştırmanıza olanak tanıyan araçlar sunar. Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale yeni modüle geçişi başlatmanıza yardımcı olacaktır.

AzureRM ile Az arasında hataya neden olan değişikliklerin tam listesini görmek için bkz. [AzureRM'den AZ modülüne tüm değişiklikler](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Mevcut betikleri en son AzureRM sürümüyle çalıştığından emin olun

Geçiş adımlarını uygulamadan önce, sisteminizde hangi AzureRM sürümlerinin yüklü olduğunu denetleyin. Bunu yaparak betiklerin zaten en son sürümde çalıştığından emin olabilir ve AzureRM’nin hangi sürümlerinin kaldırılması gerektiğini anlayabilirsiniz.

AzureRM’nin hangi sürümlerini yüklediğinizi denetlemek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

AzureRM'nin kullanılabilir __en son__ sürümü __6.13.1__'dir. Sizde bu sürüm yüklü değilse, mevcut betiklerinizin Az modülüyle çalışabilmesi için burada ve [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) açıklananların ötesinde ek değişikler yapılması gerekebilir.

Betikleriniz AzureRM 6.13.1 ile çalışmıyorsa, bunları [AzureRM 5.x'ten 6.x'e geçiş kılavuzuna](/powershell/azure/azurerm/migration-guide.6.0.0) göre güncelleştirin.
AzureRM modülünün önceki bir sürümünü kullanıyorsanız, her büyük sürüm için geçiş kılavuzları sağlanır.

## <a name="uninstall-azurerm"></a>AzureRM'yi kaldırma

Az modülünün Windows için PowerShell 5.1 üzerindeki mevcut AzureRM yüklemelerinden herhangi biriyle uyumluluğu garanti edilmez. Az modülünü yüklemeden önce [AzureRM'yi kaldırın](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Sisteminizden AzureRM modülünü kaldırmaya hazır değilseniz, onun yerine [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x veya sonraki sürümleri için Az modülünü yükleyebilirsiniz. PowerShell Core ile Windows için PowerShell 5.1 farklı modül kitaplıklarını kullandığından hiçbir çakışma olmayacaktır. PowerShell Core'da yine [diğer adları etkinleştirebilirsiniz](#enable-azurerm-compatibility-aliases).

## <a name="install-the-azure-powershell-az-module"></a>Azure PowerShell Az modülünü yükleme

İlk adım, platformunuza Az modülünü yüklemektir. Az’yi yüklediğinizde AzureRM’yi kaldırmanız önerilir. Aşağıdaki adımlarda, mevcut betiklerinizi çalıştırmaya devam etmeyi ve eski cmdlet adlarıyla uyumluluğu sağlamayı öğreneceksiniz.

Azure PowerShell Az modülünü yüklemek için [Az modülünü yükleme](install-az-ps.md) yönergelerini izleyin.

> [!NOTE]
> Bu noktada, AzureRM'nin tüm sürümlerinin kaldırıldığından ve çakışmaya neden olmayacağından emin olmak için Az modülünde sağlanan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet'ini çalıştırmak isteyebilirsiniz.

## <a name="enable-azurerm-compatibility-aliases"></a>AzureRM uyumluluk diğer adlarını etkinleştirme

AzureRM kaldırıldıktan ve betiklerinizin en son AzureRM sürümüyle çalıştığından emin olduktan sonra, sıra Az modülü için uyumluluk modunu etkinleştirmeye gelir. Uyumluluk şu komutla etkinleştirilir:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Diğer adlar, Az modülü yüklendiğinde eski cmdlet adlarının kullanılabilmesine olanak tanır. Bu diğer adlar, seçili kapsam için profile yazılır. Profil yoksa, bir profil oluşturulur.
`CurrentUser` kapsamından daha geniş bir `-Scope` kullanırken, ilgili profil dosyasını oluşturmak veya güncelleştirmek için uygun izinler gerekir.

> [!IMPORTANT]
> __Yalnızca__ cmdlet adlarının diğer adları vardır; modül adlarının yoktur! `.psd1` içinde `#Requires`, `Import-Module` bağımlılık listelerini veya tam cmdlet adlarını kullanıyorsanız, bu noktada modül adlarıyla ilgili [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) belirtilen süreci izleyerek bunların geçişini yaptığınızdan emin olun.

> [!WARNING]
>
> Bu komut için farklı bir `-Scope` kullanabilirsiniz, ama bunu yapmanız önerilmez. Diğer adlar seçili kapsam için kullanıcı profiline yazılır, dolayısıyla bunları olabildiğince kısıtlı bir kapsamda etkinleştirilmiş durumda tutun. Diğer adların sistem genelinde etkinleştirilmesi, kendi yerel kapsamlarında AzureRM’yi yüklemiş olan diğer kullanıcılarda sorunlara yol açabilir.

Diğer ad modu etkinleştirildikten sonra, hala beklendiği gibi çalıştıklarını doğrulamak için betiklerinizi bir kez daha çalıştırın.
Az modülünde bazı parametre adları değiştirilmiş, eklenmiş veya gerekli hale getirilmiştir. Cmdlet'lerin çıkış türleri de değiştirilmiş olabilir. Bu değişiklikler [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) ayrıntılı olarak açıklanır.

## <a name="update-cmdlets-modules-and-parameters"></a>Cmdlet'leri, modülleri ve parametreleri güncelleştirme

Güncelleştirilen ve diğer adlarla çalıştırılan betiklerle, zaman ayırıp bunları yeni cmdlet'leri kullanacak şekilde güncelleştirebilir ve yeni özellikler gibi diğer değişikliklerden de yararlanabilirsiniz. Betiklerin çoğunda, [Az modülündeki yeni cmdlet adlandırma düzenine uyarak](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes) cmdlet adlarını güncelleştirmeniz yeterli olacaktır. Betiklerinizin ne yaptığına ve hangi Azure PowerShell özelliklerinden yararlandığına bağlı olarak, betiklerin çalışmasını sağlamak için yapmanız gereken başka bazı değişiklikler olabilir.

Örneğin [Blob Depolama cmdlet'leri](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) yeni zaman uyumsuz modeli kullanacak şekilde tümüyle yeniden tasarlanmıştır; dolayısıyla bunların kullanıldığı betiklerin güncelleştirilmesi, yalnızca cmdlet adlarında uygun değişikliklerin yapılmasından çok daha fazla çalışma gerektirir.

Bu noktaya kadar betiklerinizde yalnızca küçük, basit değişiklikler yapmış olsanız veya diğer adlar etkinleştirildiğinde ek değişikliğe gerek kalmadan bu betikler çalışıyor olsa bile, siz cmdlet adlarını değiştirdikten ve diğer adları geçersiz kıldıktan sonra ortadan kalkacak 'saydam' diğer ad davranışlarına bağımlı olmadıklarından emin olmak için [Az 1.0.0'deki hataya neden olan değişikliklerin tam listesini](migrate-az-1.0.0.md) okuyun.

## <a name="disable-aliases"></a>Diğer adları devre dışı bırakma

Geçişinizi tamamladıktan ve diğer ad davranışlarına güvenerek çalışmayı bıraktıktan sonra, diğer adları devre dışı bırakmanız önerilir. Bu işlem [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) cmdlet'iyle yapılır.

> [!IMPORTANT]
> Bu cmdlet'i çalıştırırken, `Enable-AzureRmAlias` cmdlet'inin çağrıldığı her `-Scope` için çağırdığınızdan __emin olun__; aksi takdirde sisteminizde diğer ad davranışına bağımlı betikler kalabilir.
