---
title: Azure PowerShell Az modülüne giriş
description: Azure PowerShell'in AzureRM modülünün yerini alan yeni Az modülüne giriş.
ms.date: 05/20/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 4bf05058f576e7a4844f693384b4fa4aea08a042
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427047"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Yeni Azure PowerShell Az modülüne giriş

Azure PowerShell Az modülü, Aralık 2018’de genel yayın aşamasına ulaşmıştır ve artık Azure ile etkileşim kurmak için kullanılması hedeflenen PowerShell modülüdür. Az tarafından daha kısa komutlar, gelişmiş kararlılık ve platformlar arası destek sunulur. Az ayrıca, AzureRM ile özellik eşliği sayesinde size geçiş için kolay bir yol sunar.

> [!NOTE]
> PowerShell 7.x ve üzeri, tüm platformlarda Azure PowerShell ile kullanılması önerilen PowerShell sürümüdür.

Azure PowerShell en son Az modülü sayesinde Windows, macOS ve Linux dahil tüm platformlarda PowerShell 6.2.4 ve üzeri sürümlerle birlikte kullanılabilir. Ayrıca Windows üzerinde PowerShell 5.1 ile de uyumludur.

Az yeni bir modül olduğundan, sürüm 1.0.0 olarak sıfırlanmıştır.

## <a name="why-a-new-module"></a>Neden yeni bir modül?

Büyük güncelleştirmelerle çalışmak zor olabilir. Bu nedenle PowerShell'den Azure'la etkileşim kurmak için yeni cmdlet'ler içeren yeni bir modül kümesi hazırlama kararımızın nedenlerini size açıklamak istiyoruz.

En büyük ve en önemli değişiklik PowerShell'in .NET Standard kitaplığını temel alan [PowerShell](/powershell/scripting/overview)'in kullanıma sunulmasından bu yana platformlar arası bir ürün olmasıdır.
Tüm platformlara Azure desteği getirmeye kararlı olduğumuzdan, Azure PowerShell modüllerinin .NET Standard kullanacak şekilde güncelleştirilmesi ve PowerShell Core ile uyumlu olması gerekiyordu. Mevcut AzureRM modülünü alıp bu desteği eklemek üzere karmaşık değişiklikler yapmak yerine Az modülü oluşturuldu.

Yeni modül oluşturmak, mühendislerimize cmdlet'lerin ve modüllerin tasarımı ile adlandırmasını tutarlı hale getirme fırsatı da verdi. Artık tüm modüller `Az.` ön ekiyle başlıyor ve cmdlet'lerin tümünde _Fiil_-`Az`_İsim_ biçimi kullanılıyor. Daha önce cmdlet adları hem daha uzundu hem de cmdlet adları arasında tutarsızlıklar vardı.

Modül sayısı da azaltıldı: Aynı hizmetlerle çalışan bazı modüller birlikte kullanıma sunuldu. Yönetim düzlemi ve veri düzlemi cmdlet’leri, şimdi hizmetlerine yönelik tek tek modüller içinde yer alır. Bağımlılıkları ve içeri aktarmaları el ile yönetenleriniz için, bu durum işleri çok daha kolaylaştırıyor.

Yeni bir Azure PowerShell modülü oluşturmayı gerektiren bu önemli değişiklikleri yaparak, takım Azure'ın PowerShell cmdlet'leriyle kullanılmasını daha önce mümkün olandan çok daha fazla platformda ve hiç olmadığı kadar kolaylaştırmaya yönelik kararlılığını gösterdi.

## <a name="upgrade-to-az"></a>Az modülüne yükseltme

PowerShell'de en son Azure özelliklerini izlemek için mümkün olan en kısa zamanda Az modülüne geçmelisiniz. AzureRM yerine Az modülünü yüklemeye hazır değilseniz, Az modülünü denemek için çeşitli seçenekleriniz vardır:

- [Azure Cloud Shell](/azure/cloud-shell/overview) ile bir `PowerShell` ortamı kullanın. Azure Cloud Shell, Az modülü yüklenmiş ve `Enable-AzureRM` uyumluluk diğer adları etkinleştirilmiş olarak gelen tarayıcı tabanlı bir kabuk ortamıdır.
- Windows için PowerShell 5.1 ile AzureRM modülünü yüklü bırakın ancak PowerShell 6.2.4 veya sonraki sürümleri için Az modülünü yükleyin. Windows için PowerShell 5.1 ile PowerShell 6.2.4 ve üzeri, ayrı modül koleksiyonları kullanır. Yönergeleri izleyerek [PowerShell’in en son sürümünü](/powershell/scripting/install/installing-powershell) yükleyin ve ardından PowerShell 6.2.4 veya üzerinden [Az modülünü yükleyin](install-az-ps.md).

Mevcut AzureRM yüklemesinden yükseltmek için:

1. [Azure PowerShell AzureRM modülünü kaldırın](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Azure PowerShell Az modülünü yükleyin](install-az-ps.md)
3. **İSTEĞE BAĞLI**: Yeni komut kümesine alışırken [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) ile AzureRM cmdlet’lerine yönelik diğer adları eklemek için uyumluluk modunu etkinleştirin. Diğer ayrıntılar için sonraki bölüme veya [AzureRM'den Az modülüne geçişi başlatma](migrate-from-azurerm-to-az.md) konusuna bakın.

## <a name="migrate-existing-scripts-to-az"></a>Mevcut betikleri için Az modülüne geçirme

Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır. Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın. Örneğin, eski `New-AzureRMVm` komutu `New-AzVm` komutuna dönüştürülmüştür.
Öte yandan, geçiş süreci yalnızca yeni cmdlet adlarına alışmaktan ibaret değildir. Yeniden adlandırılmış modüller, parametreler ve başka önemli değişiklikler vardır.

AzureRM'den Az modülüne geçiş sürecinizde size yardımcı olmak için bir dizi kaynak sağladık:

- [AzureRM'den Az modülüne geçişi başlatma](migrate-from-azurerm-to-az.md)
- [AzureRM'den Az 1.0.0'a geçişte hataya neden olan değişikliklerin tam listesi](migrate-az-1.0.0.md)
- [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet'i

Yeni söz dizimine güncelleştirirken mevcut betikleri de kullanmanıza yardımcı olmak için Az modülünün bir uyumluluk modu vardır. [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet'i diğer adlar aracılığıyla bir uyumluluk modunu etkinleştirerek, Az modülüne tam geçiş üzerinde çalışırken çok küçük değişikliklerle mevcut betikleri kullanmanıza olanak tanır. Varsayılan olarak, `Enable-AzureRmAlias` yalnızca geçerli PowerShell oturumunun uyumluluk diğer adlarını etkinleştirir. Uyumluluk diğer adlarını PowerShell oturumları arasında kalıcı hale getirmek için `Scope` parametresini kullanın. Daha fazla bilgi için bkz. [Enable-AzureRmAlias başvuru belgeleri](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Cmdlet adlarının diğer adları olsa da, Az cmdlet'lerinde yeni (veya yeniden adlandırılmış) parametreler veya değiştirilmiş dönüş değerleri olacaktır. Diğer adları etkinleştirmenin sizin için geçişi gerçekleştirmesini beklemeyin! Betiklerinizin nerede güncelleştirme gerektirdiğini bulmak için, [hataya neden olan değişikliklerin tam listesine](migrate-az-1.0.0.md) bakın.

## <a name="continued-support-for-azurerm"></a>Devam eden AzureRM desteği

AzureRM için artık yeni cmdlet’ler veya özellikler sağlanmayacaktır. Bununla birlikte, AzureRM modülü hala resmi olarak bakım kapsamındadır ve Aralık 2020’ye kadar hata düzeltmeleri sağlanacaktır.