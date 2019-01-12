---
title: Azure PowerShell Az modülüne giriş
description: Azure PowerShell'in AzureRM modülünün yerini alan yeni Az modülüne giriş.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cff9a6ef64907c7ff493dbc9c83dd20a82f297d9
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53595129"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Yeni Azure PowerShell Az modülüne giriş

Azure PowerShell Az modülü, Aralık 2018’de genel yayın aşamasına ulaşmıştır ve artık Azure ile etkileşim kurmak için kullanılması hedeflenen PowerShell modülüdür. Az tarafından daha kısa komutlar, gelişmiş kararlılık ve platformlar arası destek sunulur. Ayrıca Az, AzureRM ile özellik eşliği ve AzureRM'den kolay geçiş yolu da sunar.

Az .NET Standard kitaplığını kullanır ve bu da PowerShell 5.x ile PowerShell 6.x üzerinde çalıştığı anlamına gelir.
PowerShell 6.x Linux, macOS ve Windows üzerinde çalışabildiğinden, Azure PowerShell artık tüm platformlarda kullanılabilir.
.NET Standard'ın kullanılması, Azure PowerShell'in kod tabanını kullanıcıları çok az etkileyerek birleştirmemize olanak tanır.

Az yeni bir modül olduğundan, sürüm 1.0.0 olarak sıfırlanmıştır.

## <a name="upgrade-to-az"></a>Az modülüne yükseltme

Tüm kullanıcıların yeni Az modülüne yükseltmesi önerilir. Bunu yapmak için:

* __ÖNERİLİR__: [Azure PowerShell AzureRM modülünü kaldırın](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Azure PowerShell Az modülünü yükleyin](/powershell/azure/install-az-ps)
* Yeni komut kümesine alışırken `Enable-AzureRMAlias` ile AzureRM cmdlet’lerine yönelik diğer adları eklemek için uyumluluk modunu etkinleştirin. Diğer adları __yalnızca__ AzureRM yüklü değilse etkinleştirin.

## <a name="migrate-existing-scripts-to-az"></a>Mevcut betikleri için Az modülüne geçirme

Önemli güncelleştirmeler çok rahat yapılamayabilir. Öte yandan, yeni söz dizimindeki güncelleştirmelerle çalışırken mevcut betikleri de kullanmanıza yardımcı olmak için Az modülünün bir uyumluluk modu vardır. AzureRM uyumluluk modunu etkinleştirmek için `Enable-AzureRmAlias` cmdlet'ini kullanın. Bu cmdlet, AzureRM cmdlet adlarını yeni Az cmdlet'lerinin diğer adları olarak tanımlar.

Yeni cmdlet adları kolay öğrenilecek şekilde tasarlanmıştır. Cmdlet adlarında `AzureRm` veya `Azure` kullanmak yerine `Az` kullanın. Örneğin, eski `New-AzureRMVm` komutu `New-AzVm` komutuna dönüştürülmüştür.

Geçiş işleminin tam açıklaması için bkz. [AzureRM'den Az'ye geçiş](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>AzureRM desteğinin geleceği

Mevcut AzureRM modülü için artık yeni cmdlet’ler veya özellikler sağlanmayacaktır. Bununla birlikte, AzureRM hala resmi olarak bakım kapsamındadır ve hata düzeltmeleri sağlanacaktır. En son Azure hizmetlerini ve özelliklerini takip etmek için Az modülüne geçmelisiniz.