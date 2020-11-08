---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266232"
---
# Az. Storagesehd modülü
## Tanım
Depolama eşitleme modülündeki cmdlet 'ler, PowerShell 'de Azure dosya eşitlemesi ile ilgili işlemleri yönetmenizi sağlar.

## Az. Storagesehd cmdlet 'Leri
### [Get-Azstoragesynccloudenvseçpoint](Get-AzStorageSyncCloudEndpoint.md)
Bu komut, verilen eşitleme grubundaki tüm bulut uç noktalarını listeler.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Bu komut, belirli bir depolama eşitleme hizmeti içindeki tüm eşitleme gruplarını listeler.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları listeler.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Bu komut, belirli bir eşitleme grubundaki tüm sunucu uç noktalarını listeler.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Bu komut, belirli bir abonelik/kaynak grubu kapsamındaki tüm depolama eşitleme hizmetlerini listeler.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir. Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir. Maksimum 10.000 değişiklik algılanabilir. Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılamanın hızla ve 10.000 değişiklik sınırının içinde tamamlanabilmesi için

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Bu komut tüm katmanlı dosyaları yerel diske geri çeker.

### [Yeni-Azstoragesynccloudenvseçpoint](New-AzStorageSyncCloudEndpoint.md)
Bu komut, eşitleme grubunda bir Azure dosya eşitlemesi bulut uç noktası oluşturur.

### [Yeni-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.

### [Yeni-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur. Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.

### [Yeni-AzStorageSyncService](New-AzStorageSyncService.md)
Bu komut, kaynak grubunda yeni bir depolama eşitleme hizmeti oluşturur.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Bu komut, kaynak grubunda bir depolama eşitleme hizmeti ayarlar.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Bu komut, bir sunucuyu güven ilişkisi oluşturan bir depolama Eşitleme hizmetine kaydeder. PowerShell veya Azure portalı bu sunucuda eşitleme yapılandırmak için kullanılabilir.

### [Remove-Azstoragesynccloudenvseçpoint](Remove-AzStorageSyncCloudEndpoint.md)
Bu komut, belirtilen bulut uç noktasını bir eşitleme grubundan siler. En az bir bulut uç noktası olmadan, bu eşitleme grubunda başka sunucu uç noktaları eşitlenebilir.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Bu komut, belirtilen eşitleme grubunu silecek.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Bu komut belirtilen sunucu uç noktasını silecek. Bu konuma eşitleme hemen durdurulur.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Bu komut, belirtilen depolama eşitleme hizmeti 'ni silecek.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Yalnızca sorun giderme için kullanın. Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir. Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.

