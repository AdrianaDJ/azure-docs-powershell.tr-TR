---
title: Azure PowerShell Az modülüne giriş
description: Azure PowerShell'in AzureRM modülünün yerini alan yeni Az modülüne giriş.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276087"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Yeni Azure PowerShell Az modülüne giriş

Kasım 2018'den başlayarak, Azure PowerShell `Az` modülü tam genel önizlemeye sunulmuştur.
Az daha kısa komutlar, gelişmiş kararlılık sunar ve Windows, macOS ve Linux'ı destekler. Ayrıca Az, AzureRM ile özellik eşliği ve AzureRM'den kolay geçiş yolu da sunar.

Az .NET Standard kitaplığını kullanır ve bu da PowerShell 5.x ile PowerShell 6.x üzerinde çalıştığı anlamına gelir.
PowerShell 6.x Linux, macOS ve Windows üzerinde çalışabildiğinden, Az tüm platformlarda kullanılabilir.
.NET Standard'ın kullanılması, Azure PowerShell'in kod tabanını kullanıcıları çok az etkileyerek birleştirmemize olanak tanır.

Az yeni bir modüldür, dolayısıyla sürüm sıfırlanmıştır. İlk kararlı sürüm 1.0 olacaktır, ama Kasım 2018 itibarıyla modülün AzureRm ile özellik eşliği vardır.

## <a name="upgrade-to-az"></a>Az modülüne yükseltme

Kullanıcıların yeni `Az` modülüne yükseltmenizi öneririz. Bunu yapmak için:

* [Azure PowerShell AzureRM modülünü kaldırın](/powershell/azure/uninstall-azurerm-ps)
* [Azure PowerShell Az modülünü yükleyin](/powershell/azure/install-az-ps)
* Yeni komut kümesine alışırken `Enable-AzureRMAlias` ile AzureRM için uyumluluk modunu etkinleştirin.

## <a name="migrate-existing-scripts-to-az"></a>Mevcut betikleri için Az modülüne geçirme

Önemli güncelleştirmeler çok rahat yapılamayabilir. Öte yandan, yeni söz dizimindeki güncelleştirmelerle çalışırken mevcut betikleri de kullanmanıza yardımcı olmak için `Az` modülünün bir uyumluluk modu vardır. `AzureRM` uyumluluk modunu etkinleştirmek için `Enable-AzureRmAlias` cmdlet'ini kullanın. Bu cmdlet, `AzureRM` cmdlet adlarını yeni `Az` cmdlet'lerinin diğer adları olarak tanımlar.

Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır. Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın. Örneğin, eski `New-AzureRmVm` komutu `New-AzVm` komutuna dönüştürülmüştür.

Geçiş işleminin tam açıklaması için bkz. [AzureRM'den Az'ye geçiş](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>AzureRM desteğinin geleceği

Aralık 2018'de `Az` sürüm 1.0 kullanıma sunulduğunda, mevcut `AzureRM` modülü artık yeni cmdlet'ler veya özellikler almayacaktır. Öte yandan, `AzureRM` hala resmi olarak korunmaktadır ve hata düzeltmeleri alacaktır. En son Azure hizmetleri ve özelliklerini yakından izlemek için, `Az` modülüne geçmelisiniz.