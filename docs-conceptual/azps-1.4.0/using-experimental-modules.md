---
title: Deneysel Azure PowerShell modüllerini kullanma
description: Deneysel Azure PowerShell modüllerinin felsefesi ve kullanımı hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837410"
---
# <a name="use-experimental-azure-powershell-modules"></a>Deneysel Azure PowerShell modüllerini kullanma

Azure PowerShell ekibi Azure’da geliştirici araçlarına vurgu yaparak Azure PowerShell deneyiminde çok sayıda geliştirmeyi denemektedir. Bu makalede, Azure PowerShell ile denemelere nasıl katılabileceğiniz ve geliştirme takımına nasıl geri bildirimde bulunabileceğiniz açıklanır.

## <a name="experimentation-methodology"></a>Deneme yöntemi

Denemeyi kolaylaştırmak amacıyla, yeni ve kullanımı daha kolay yöntemlerle mevcut Azure SDK işlevselliğini uygulayan yeni Azure PowerShell modülleri oluşturuyoruz. Çoğu durumda, cmdlet'ler mevcut cmdlet'leri tam olarak yansıtır. Ancak, deneysel cmdlet’ler Azure kaynaklarını oluşturup yönetmeyi kolaylaştıran kısa bir gösterim ve daha akıllı varsayılan değerler sağlar.

Bu modüller mevcut Azure PowerShell modülleri ile yan yana yüklenebilir. Cmdlet adları, daha kısa adlar sağlamak ve deneysel olmayan mevcut cmdlet'lerle ad çakışmalarını önlemek için kısaltılmıştır.

Deneysel modüller şu adlandırma kuralını kullanır: `Az.*.Experiments`. Bu adlandırma kuralı, Önizleme modüllerinin adlandırması ile benzerdir: `Az.*.Preview`. Önizleme modülleri, deneysel modüllerden farklıdır. Önizleme modüller, Azure hizmetlerinin yalnızca Önizleme teklifi olarak kullanılabilen yeni işlevlerini uygular. Önizleme modülleri, mevcut Azure PowerShell modüllerinin yerine geçer ve aynı cmdlet ve parametre adlarını kullanır.

## <a name="how-to-install-an-experimental-module"></a>Deneysel modül yükleme

Deneysel modüller, tıpkı mevcut Azure PowerShell modülleri gibi PowerShell Galerisinde yayımlanır. Deneysel modüllerin listesini görüntülemek için şu komutu çalıştırın:

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

Deneysel modülü yüklemek için `Install-Module` cmdlet’ini kullanın.

### <a name="documentation-and-support"></a>Belgeler ve destek

Belgeler yükleme paketine dahildir ve `Get-Help` cmdlet'i kullanılarak belgelere erişilebilir. Deneysel modüller için resmi bir belge yayımlanmaz.

Bu modülleri test etmenizi öneririz. Görüşleriniz, kullanılabilirliği artırmamıza ve gereksinimlerinizi karşılamamıza olanak tanır. Ancak, deneysel oldukları için, bu modüllere yönelik destek sınırlıdır. GitHub deposunda bir [sorun](https://github.com/Azure/azure-powershell/issues) oluşturularak sorunlar ya da sorun raporları gönderilebilir.

## <a name="experiments-and-areas-of-improvement"></a>Denemeler ve geliştirilecek alanlar

Bu geliştirmeler, rakip ürünlerindeki başlıca ayırt edici özelliklere göre seçilmiştir. Örneğin Azure CLI, komutları _API yüzey alanı_ yerine _senaryolara_ dayandırmaktadır.
Azure CLI, "kullanmaya başlama" senaryolarını son kullanıcılar için kolaylaştıran birkaç akıllı varsayılan değer kullanır.

### <a name="core-improvements"></a>Temel iyileştirmeler

Temel iyileştirmeler, "sağduyu" olarak kabul edilir ve bu güncelleştirmelerin uygulamaya geçirilmesi için az miktarda deneme gerekir.

- Senaryoya Dayalı Cmdlet’ler - **All*- cmdlet’leri Azure REST hizmeti değil, senaryolar çevresinde tasarlanmalıdır.

- Daha Kısa Adları - Cmdlet'lerin adlarını ve parametrelerin adlarını içerir.
  "Eski" cmdlet’lerle uyumluluk için diğer adları kullanın. _Geriye doğru uyumlu_ parametre kümeleri sağlayın.

- Akıllı Varsayılanlar - "Gerekli" bilgileri doldurmak için akıllı varsayılanlar oluşturun. Örnek:
  - Kaynak Grubu
  - Konum
  - Bağımlı kaynaklar

### <a name="experimental-improvements"></a>Deneysel geliştirmeler

Deneysel geliştirmeler, takımın deneme ile doğrulamayı istediği önemli bir değişikliği sunar.

- Basit türler - Oluşturma senaryoları, karmaşık türlerden ve yapılandırma nesnelerinden uzaklaşmalıdır. Yapılandırmayı bir veya iki parametreye kadar basitleştirin.

- "Akıllı Oluştur" - "Akıllı Oluşturma" özelliğini uygulayan oluşturma senaryolarında _hiçbir_ gerekli parametre yoktur: tüm gerekli bilgiler, Azure PowerShell tarafından sabit bir fikirle seçilir.

- Gri Parametreler - Çoğu durumda, bazı parametreler "gri" veya yarı isteğe bağlı olabilir. Parametre belirtilmezse, kullanıcıya parametrenin oluşturulmasını isteyip istemediği sorulur. Ayrıca, gri parametrelerin kullanıcı onayıyla bağlama dayalı bir değer çıkarması anlamlıdır.
  Örneğin, gri parametrenin en son kullanılan değeri kullanması mantıklı olabilir.

- `-Auto` Anahtarı - `-Auto` anahtarı, kullanıcılar için ana yoldaki gerekli parametrelerin bütünlüğünü sürdürürken _her şeyi varsayılan yapmayı_ "kabul etme" seçeneği sunar.

### <a name="feature-specific-switches"></a>Özelliğe özgü anahtarlar

Örneğin, "Web uygulaması oluşturma" senaryosunda mevcut bir git deposuna bir "azure" uzak birimini otomatik olarak ekleyen `-Git` veya `-AddRemote` olabilir.

- Ayarlanabilir Varsayılanlar - Kullanıcıların `-ResourceGroupName` ve `-Location` gibi yaygın parametreler için varsayılan değerleri ayarlayabilmesi gerekir.

- Boyut Varsayılanları - Birçok Kaynak Sağlayıcısı farklı adlar kullandığından, kaynak "boyutları" kafa karıştırıcı olabilir (örneğin, "Standard\_DS1\_v2" veya "S1"). Bununla birlikte, çoğu kullanıcı daha çok maliyetle ilgilenir. Dolayısıyla bir fiyatlandırma zamanlamasına göre "evrensel" boyutlar tanımlamak mantıklıdır. Kullanıcılar belirli bir boyutu seçebilir veya bütçe kaynağına göre _en iyi seçeneği_ Azure PowerShell’in seçmesine izin verebilir.

- Çıkış Biçimi - Azure PowerShell şu anda `PSObject` döndürmektedir ve çok az konsol çıkışı vardır. Azure PowerShell’in kullanılan "akıllı varsayılanlar" hakkındaki bazı bilgileri kullanıcıya göstermesi gerekebilir.
