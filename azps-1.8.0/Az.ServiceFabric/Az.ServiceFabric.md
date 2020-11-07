---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93750891"
---
# Az. ServiceFabric modülü
## Tanım
Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.

## Az. ServiceFabric cmdlet 'Leri
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin. Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Kümeye ikincil küme sertifikası ekleyin.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Kümedeki belirli bir düğüme düğüm ekleme.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Var olan kümeye yeni bir düğüm türü ekleyin.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Küme kaynağı ayrıntılarını edinin.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır. Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir. Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Küme güvenliği için kullanılan küme sertifikasını kaldırma.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Belirli düğüm türünden düğümleri kümeden kaldırma.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Bir kümeden tam bir düğüm türü kaldırma.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Kümenin hizmet yapısı yükseltme türünü değiştirin.

### [Güncelleştirme-Azservicefabricdayanıklılığı](Update-AzServiceFabricDurability.md)
Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.

### [Update-Azservicefabricgüvenirlik](Update-AzServiceFabricReliability.md)
Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.

