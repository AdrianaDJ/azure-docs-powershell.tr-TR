---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571165"
---
# AzureRM. Öngörüler modülü
## Tanım
Bu konuda, Azure Insights cmdlet 'Lerinin yardım konularını görüntüler.

## AzureRM. Öngörüler cmdlet 'Leri
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Otomatik ölçeklendirme ayarı oluşturur.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Günlük uyarısı kuralı ekler veya değiştirir.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Yeni etkinlik günlüğü profili oluşturur. Bu profil, etkinlik günlüğünü bir Azure depolama hesabına arşivlemek veya aynı abonelikteki bir Azure Olay Hub 'ına aktarmak için kullanılır. 

- **Depolama hesabı** -yalnızca standart depolama hesabı (Premium depolama hesabı desteklenmiyor) desteklenir. ARM veya klasik türünde olabilir. Depolama hesabına oturum açtıysa, etkinlik günlüğünü depolama maliyeti normal standart depolama tarifeleriyle faturalanır. Abonelik başına yalnızca bir günlük profili olabilir etkinlik günlüğü dışarı aktarmak için abonelik başına yalnızca bir depolama hesabı kullanılabilir. 

- **Olay Hub 'ı** -etkinlik günlüğünü dışarı aktarmak için abonelik başına yalnızca bir olay hub 'ı olabilir. Etkinlik günlüğü bir olay hub 'ına akıtısa, standart Olay Hub fiyatlandırması uygulanır. 

Etkinlik günlüğünde, olaylar bir bölgeye ait olabilir veya "Global" olabilir. Genel aslýnda bu olaylarda, olayların gerçekten bu kategoriye giren çoğunluğunda bölge çoğunluğu ve bölgeden bağımsızdır. Etkinlik günlüğü profili portaldan ayarlanmışsa, Kullanıcı arabiriminde seçili diğer bölgelerin yanına örtülü olarak "genel" ekler. Cmdlet kullanıldığında, "Global" olarak konum, başka herhangi bir bölgeden ayrı olarak bahsedilmelidir. 

**Not** :- **konumlarda "Global" ayarlanamayan Etkinlik günlüğünün büyük bir bölümünü dışarı aktarmaz.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Bir metrik temelinde bir uyarı kuralı ekler veya güncelleştirir.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Bir WebTest uyarı kuralı ekler veya güncelleştirir.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Etkinlik günlüğü uyarısını devre dışı bırakır ve etiketlerini ayarlar.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Etkinlik günlüğü uyarısını verir ve etiketlerini ayarlar.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Eylem gruplarını alır.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Uyarıların geçmişini alır.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Uyarı kurallarını alır.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Otomatik ölçeklendirme geçmişini alır.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Otomatik ölçeklendirme ayarlarını alır.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Günlüğe kaydedilen kategorileri ve zaman grateleri alır.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Olayların günlüğünü alır.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Günlük profili alır.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Kaynağın metrik değerlerini alır.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Metrik tanımları alır.

### [Get-Azurermusın](Get-AzureRmUsage.md)
Kaynağın kullanım ölçümlerini alır.

### [Yeni-AzureRmActionGroup](New-AzureRmActionGroup.md)
Bellekte bir ActionGroup başvuru nesnesi oluşturur.

### [Yeni-Azurermactiongroupahize](New-AzureRmActionGroupReceiver.md)
Yeni bir eylem grubu alıcısı oluşturur.

### [Yeni-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.

### [Yeni-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Uyarı kuralı için e-posta eylemi oluşturur.

### [Yeni-Azurermalertruleweb kancası](New-AzureRmAlertRuleWebhook.md)
Uyarı kuralı Web kancası oluşturur.

### [Yeni-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Otomatik ölçeklendirme e-posta bildirimi oluşturur.

### [Yeni-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Otomatik ölçeklendirme profili oluşturur.

### [Yeni-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Otomatik ölçeklendirme kuralı oluşturur.

### [Yeni-Azurermautoscaleweb kancası](New-AzureRmAutoscaleWebhook.md)
Otomatik ölçeklendirme Web kancası oluşturur.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Eylem grubunu kaldırır.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Etkinlik günlüğü uyarısını kaldırır.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Uyarı kuralını kaldırır.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Otomatik ölçeklendirme ayarını kaldırır.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Günlük profilini kaldırır.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Yeni bir eylem grubunu oluşturur veya güncelleştirir.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Yeni bir etkinlik günlüğü uyarısını oluşturur veya ayarlar.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Kaynağın günlükleri ve ölçümleri ayarlarını belirler.

