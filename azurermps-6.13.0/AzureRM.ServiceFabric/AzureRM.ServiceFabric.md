---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570694"
---
# AzureRM. ServiceFabric modülü
## Tanım
Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.

## AzureRM. ServiceFabric cmdlet 'Leri
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Kümeyi oluşturan sanal makine ölçek kümesine yeni bir sertifika ekleyin. Sertifika, uygulama sertifikası olarak kullanılmak üzere tasarlanmıştır.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Kümeye ikincil küme sertifikası ekleyin.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Kümedeki belirli bir düğüme düğüm ekleme.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Var olan kümeye yeni bir düğüm türü ekleyin.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Küme kaynağı ayrıntılarını edinin.

### [Yeni-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır. Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir. Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Küme güvenliği için kullanılan küme sertifikasını kaldırma.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Belirli düğüm türünden düğümleri kümeden kaldırma.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Bir kümeden tam bir düğüm türü kaldırma.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Kümenin hizmet yapısı yükseltme türünü değiştirin.

### [Güncelleştirme-Azurermservicefabricdayanıklılığı](Update-AzureRmServiceFabricDurability.md)
Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.

### [Güncelleştirme-Azurermservicefabricgüvenirlik](Update-AzureRmServiceFabricReliability.md)
Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.

