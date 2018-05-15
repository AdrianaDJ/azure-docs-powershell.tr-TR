---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="version-380"></a>Sürüm 3.8.0
* İşlem
  - Get-* cmdlet’lerinde birden fazla veri sayfasını (120’den fazla öğe) almaya olanak tanıyan hata düzeltmesi
* DataLakeAnalytics
  - Bazı komutların uygun anlatım ve örnekler içermesine yönelik yardım düzeltildi.
* DataLakeStore
  - `Get-AzureRMDataLakeStoreItemContent` cmdlet’i için tam destek eklendi. Bu değişiklik, ilk N veya son N yeni çizgi ile ayrılmış satırın gösterilmesini sağlar.
* HDInsight
  - RServer küme türü için destek eklendi
    + New-AzureRmHDInsightCluster veya New-AzureRmHDInsightClusterConfig içindeki RServer kümesi için Edgenode VM boyutu belirtilebilir
    + RServer artık Add-AzureRmHDInsightConfigValues içinde bir yapılandırma seçeneğidir. RStudio yüklemesinin yapılması gerektiğini belirtmek üzere R Studio bayrağının ayarlanmasına olanak tanır.
* LogicApp
  - Set-AzureRmIntegrationAccountSchema ve Set-AzureRmIntegrationAccountMap cmdlet’lerinin contentlink sorunu düzeltilmiştir (Hem content hem de contentlink’in ayarlanması güncelleştirme hatasına neden oluyordu).
* Ağ
  - Application Gateway’lere yeni web uygulaması güvenlik duvarı özellikleri için destek eklendi
    + New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig eklendi
    + Get-AzureRmApplicationGatewayAvailableWafRuleSets eklendi (Diğer ad: List-AzureRmApplicationGatewayAvailableWafRuleSets)
    + New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration güncelleştirildi: -RuleSetType -RuleSetVersion ve -DisabledRuleGroups parametresi eklendi
    + Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration güncelleştirildi: -RuleSetType -RuleSetVersion ve -DisabledRuleGroups parametresi eklendi
  - Sanal Ağ Geçidi Bağlantılarına IPSec ilkeleri desteği eklendi
  - New-AzureRmIpsecPolicy eklendi
  - New-AzureRmVirtualNetworkGatewayConnection güncelleştirildi: -IpsecPolicies ve -UsePolicyBasedTrafficSelectors parametresi eklendi
* Profil
  - *Eski*: Save-AzureRmProfile, Save-AzureRmContext olarak yeniden adlandırıldı, eski cmdlet adının diğer adı var ve diğer sonraki sürümde kaldırılacak.
  - *Eski*: Select-AzureRmProfile, Import-AzureRmContext olarak yeniden adlandırıldı, eski cmdlet adının diğer adı var ve diğer sonraki sürümde kaldırılacak.
  - Profil cmdlet’lerinin PSAzureContext ve PSAzureProfile çıktı türleri sonraki sürümde değiştirilecek.
  - Save-AzureRmContext cmdlet’i sonraki sürümde OutputType içermeyecek.
  - Cmdlet ortak kodunda veri karmaları için FIPS ile uyumlu algoritma kullanma hatası düzeltildi: https://github.com/Azure/azure-powershell/issues/3651
* Sql
  - Azure Yük Devretme Grubu Cmdlet’lerinde hata düzeltmeleri
  - İşlem yoklaması için düzeltme
  - FailoverPolicy değeri El ile olarak ayarlanırken GracePeriodWithDataLossHour değeri düzeltildi
* TrafficManager
  - Coğrafi trafik yönlendirme yöntemi desteği
    + New-AzureRmTrafficManagerProfile cmdlet’inin TrafficRoutingMethod parametresi için yeni 'Geographic' değeri
    + New-AzureRmTrafficManagerEndpoint ve Add-AzureRmTrafficManagerEndpointConfig için yeni 'GeoMapping' parametresi
    + Profil koleksiyonu döndürdüğünde Get-AzureRmTrafficManagerProfile kanalları düzeltildi
* ServiceManagement
  - Restart-AzureVM: VM’yi yeniden başlatma sırasında bakım gerçekleştirmeye yönelik InitiateMaintenance parametresi eklendi.
  - Get-AzureVM: Bakım Durumu alanı eklendi.
  - Kurtarma Hizmetleri kasası yükseltmesini destekleyen yeni cmdlet’ler eklendi
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
