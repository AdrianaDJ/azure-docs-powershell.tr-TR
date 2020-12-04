---
title: Azure PowerShell betiklerini AzureRM'den Az'ye geçirme
description: Azure PowerShell betiklerini AzureRM’den yeni Az PowerShell modülüne geçirmeye ilişkin adımları ve araçları öğrenin.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/1/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: bc37d0b73db0e6df226788795730730c077fcefa
ms.sourcegitcommit: cd243c8f6dc02dbd6234e764b065643dfd31dd8b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2020
ms.locfileid: "96502598"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Azure PowerShell'i AzureRM'den Az modülüne geçirme

AzureRM PowerShell modülünün tüm sürümleri eskidir. [Az PowerShell modülü](install-az-ps.md) şu anda Azure ile etkileşim kurmak için önerilen PowerShell modülüdür.

## <a name="why-a-new-module"></a>Neden yeni bir modül?

En büyük ve en önemli değişiklik, .NET Standard kitaplığını temel alan [PowerShell](/powershell/scripting/overview)'in kullanıma sunulmasından bu yana platformlar arası bir ürün olmasıdır.

PowerShell dilinin yanı sıra Azure desteğini de tüm platformlara getirmek için çalışıyoruz. Bu konudaki yoğun çalışmalarımız, Azure PowerShell modüllerinin .NET Standard kullanacak ve PowerShell Core ile uyumlu olacak şekilde güncelleştirilmesini gerektiriyordu. Mevcut AzureRM modülü üzerinde çalışıp bu desteği eklemek üzere karmaşık değişiklikler yapmak yerine Az modülü oluşturuldu.

Yeni modül oluşturmak, mühendislerimize cmdlet'lerin ve modüllerin tasarımı ile adlandırmasını tutarlı hale getirme fırsatı da verdi. Artık tüm modüller `Az.` ön ekiyle başlıyor ve cmdlet'lerin tümünde `Verb-AzNoun` adlandırma kuralı kullanılıyor. Önceden cmdlet adları daha uzundu ve tutarsızdı.

Modül sayısı da azaltıldı: Aynı hizmetlerle çalışan bazı modüller birleştirildi. Aynı hizmete yönelik yönetim düzlemi ve veri düzlemi cmdlet’leri şimdi tek bir modülde birleştirildi. Bağımlılıkları ve içeri aktarmaları kendileri yönetenler için, bu değişiklik işleri çok daha kolaylaştırır.

Ekibimizi, bu önemli değişiklikleri yaparak Azure'ın PowerShell cmdlet'leriyle kullanılmasını daha önce mümkün olandan çok daha fazla platformda ve hiç olmadığı kadar kolaylaştırmaya yönelik kararlılığını gösterdi.

## <a name="upgrading-to-az-powershell"></a>Az PowerShell’e yükseltme

AzureRM cmdlet'leri için yazılmış betikler otomatik olarak Az ile çalışmayacaktır. Geçişi kolaylaştırmak için [AzureRM - Az geçişi araç seti](https://github.com/Azure/azure-powershell-migration) geliştirilmiştir. Yeni bir komut kümesine geçmek hiçbir zaman rahat bir işlem olmamıştır, ama bu makale Az PowerShell modülüne geçişi başlatmanıza yardımcı olacaktır. Az PowerShell modülünün neden oluşturulduğu hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](new-azureps-module-az.md).

Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır. Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın. Örneğin, eski `New-AzureRMVm` cmdlet’i `New-AzVm` olarak değiştirildi.
Öte yandan, geçiş süreci yalnızca yeni cmdlet adlarına alışmaktan ibaret değildir. Yeniden adlandırılmış modüller, parametreler ve başka önemli değişiklikler vardır.

AzureRM ile Az arasında hataya neden olan değişikliklerin tam listesini görmek için bkz. [AzureRM'den AZ modülüne tüm değişiklikler](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Mevcut betikleri en son AzureRM sürümüyle çalıştığından emin olun

Geçiş adımlarını uygulamadan önce, sisteminizde hangi AzureRM sürümlerinin yüklü olduğunu denetleyin.
Bunu yaparak betiklerin zaten en son sürümde çalıştığından emin olabilir ve AzureRM’nin hangi sürümlerinin kaldırılması gerektiğini anlayabilirsiniz.

AzureRM’nin hangi sürümlerini yüklediğinizi denetlemek için aşağıdaki örneği çalıştırın:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

AzureRM'nin kullanılabilir **en son** sürümü **6.13.1**'dir. Sizde bu sürüm yüklü değilse mevcut betiklerinizin Az modülüyle çalışabilmesi için bu makalede ve [hataya neden olan değişiklikler listesinde](migrate-az-1.0.0.md) açıklananların ötesinde ek değişikler yapılması gerekebilir.

Betikleriniz AzureRM 6.13.1 ile çalışmıyorsa, bunları [AzureRM 5.x'ten 6.x'e geçiş kılavuzuna](/powershell/azure/azurerm/migration-guide.6.0.0) göre güncelleştirin. AzureRM modülünün önceki bir sürümünü kullanıyorsanız, her büyük sürüm için geçiş kılavuzları sağlanır.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>1\. Seçenek (önerilen): PowerShell betiklerinizi otomatik olarak geçirme

Bu önerilen seçenek, AzureRM betiklerini Az’ye geçirmek için gereken çabayı en aza indirir.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>AzureRM - Az geçişi araç setini yükleme

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Betiklerinizi otomatik olarak dönüştürme

AzureRM - Az geçişi araç setiyle, betiklerinizde değişiklikler yapmadan ve Az PowerShell modülünü yüklemeden önce bu betiklerin nasıl değiştirileceğini belirleyen bir plan oluşturabilirsiniz.

[PowerShell betiklerini AzureRM'den Az PowerShell modülüne otomatik olarak geçirme](quickstart-migrate-azurerm-to-az-automatically.md) hızlı başlangıcı, PowerShell betiklerinizi AzureRM'den Az PowerShell modülüne otomatik olarak güncelleştirme işleminin tamamında size yol gösterir.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>2\. Seçenek: Enable-AzureRmAlias ile uyumluluk modunu kullanma

Yeni söz dizimine güncelleştirirken mevcut betikleri de kullanmanıza yardımcı olmak için Az modülünün bir uyumluluk modu vardır. [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet’i, diğer adlar aracılığıyla bir uyumluluk modunu etkinleştirir. Bu mod, Az’ye tam geçiş için çalışırken mevcut betikleri en az değişiklikle kullanmanıza olanak tanır. Varsayılan olarak, `Enable-AzureRmAlias` yalnızca geçerli PowerShell oturumunun uyumluluk diğer adlarını etkinleştirir. Uyumluluk diğer adlarını PowerShell oturumları arasında kalıcı hale getirmek için `Scope` parametresini kullanın. Daha fazla bilgi için bkz. [Enable-AzureRmAlias başvuru belgeleri](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Cmdlet adlarının diğer adları olsa da, Az cmdlet'lerinde yeni (veya yeniden adlandırılmış) parametreler veya değiştirilmiş dönüş değerleri olacaktır. Diğer adları etkinleştirmenin sizin için geçişi gerçekleştirmesini beklemeyin! Betiklerinizin nerede güncelleştirme gerektirdiğini bulmak için, [hataya neden olan değişikliklerin tam listesine](migrate-az-1.0.0.md) bakın.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>3\. Seçenek: Betiklerinizi Visual Studio Code’da Azure PowerShell uzantısıyla geçirme

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Visual Studio Code için Azure PowerShell uzantısını yükleme

[VS Code için Azure PowerShell uzantısını](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools) yükleyin

### <a name="convert-your-scripts-manually"></a>Betiklerinizi kendiniz dönüştürme

1. AzureRM betiğinizi VS Code’da yükleyin
2. Komut paletini `Ctrl+Shift+P` açıp `Migrate Azure PowerShell script` seçeneğini belirleyerek geçişi başlatın
3. Kaynak sürümü olarak `AzureRM` seçeneğini belirleyin
4. Altı çizili her komut veya parametre için önerilen eylemleri izleyin.

## <a name="next-steps"></a>Sonraki adımlar

[AzureRM’yi kaldırma](uninstall-az-ps.md#uninstall-the-azurerm-module)
[Azure PowerShell’i yükleme](install-az-ps.md)
