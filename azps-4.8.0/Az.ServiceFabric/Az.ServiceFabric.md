---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110284"
---
# Az. ServiceFabric modülü
## Tanım
Güvenli küme oluşturma, küme sertifikalarını yerine getirme, kümeden düğüm ekleme veya kaldırma gibi son 2 uç işlemleri otomatikleştirmek için kullanabileceğiniz Azure Service Fabric modülü. Tüm işlemlerin tam listesi aşağıda listelenmiştir.

## Az. ServiceFabric cmdlet 'Leri
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
İstemci kimlik doğrulama amaçları için kümeye ortak ad veya parmak izi ekleyin.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Kümeye ikincil küme sertifikası ekleyin.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Kümeye sertifika ortak adı veya parmak izi ekleyin. Bu işlem, sertifikayı istemci kimlik doğrulama amaçları için kümenin içine kaydeder.

### [Add-Azservicefabricmanagednodetypevmexgeri](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Düğüm türüne VM Uzantısı ekleyin.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Düğüm türüne sertifika parolası ekleyin.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Kümedeki belirli bir düğüme düğüm ekleme.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Var olan kümeye yeni bir düğüm türü ekleyin.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Hizmet dokusu uygulama ayrıntılarını edinin.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Hizmet dokusu uygulama türü ayrıntılarını edinin.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Hizmet dokusu uygulama türü sürüm bilgilerini alın.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Küme kaynağı ayrıntılarını edinin.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Yönetilen küme kaynağı ayrıntılarını edinin.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Yönetilen düğüm türü kaynak ayrıntılarını edinin.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Belirtilen uygulama ve kümenin altındaki hizmet Fabric hizmeti ayrıntılarını edinin.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulaması oluşturun.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Belirtilen kaynak grubu ve küme altında yeni hizmet dokusu uygulama türü oluşturun.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Belirtilen kaynak grubu ve küme altında yeni uygulama türü sürümü oluşturun.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Bu komut, yeni bir hizmet yapısı kümesi ayarlamak için sağladığınız sertifikaları veya sistem tarafından oluşturulan otomatik olarak imzalanan sertifikaları kullanır. Varsayılan bir şablonu veya sağladığınız özel bir şablonu kullanabilir. Otomatik olarak imzalanan sertifikaları dışarı aktarmak için bir klasör belirtme seçeneğiniz vardır ve bunları daha sonra anahtar kasasından alabilirsiniz.

### [Yeni-Azhizmetifabricmanagedcluster](New-AzServiceFabricManagedCluster.md)
Yeni yönetilen küme oluşturun.

### [Yeni-Azhizmetifabricmanagednodetype](New-AzServiceFabricManagedNodeType.md)
Yeni düğüm türü kaynağı oluşturun.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Belirtilen uygulama ve küme altında yeni hizmet yapısı hizmeti oluşturun.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Kümeden bir uygulamayı kaldırma. Bu işlem, uygulamanın altındaki tüm hizmetleri kaldırır.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Service Fabric 'ı kümeden bir uygulama türü. Bu, bu kaynağın altındaki tüm tür sürümlerini kaldırır.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Hizmet yapısı 'nı kümeden uygulama türü sürümü.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
İstemci kimlik doğrulaması için kullanılan istemci sertifikasını veya sertifika konu adlarını (s) kümeye kaldırın.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Küme güvenliği için kullanılan küme sertifikasını kaldırma.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Küme kaynağını kaldırma.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Parmak izi veya ortak ada göre remvoe istemci sertifikası.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Düğüm türünü veya düğüm türü içindeki belirli düğümleri kaldırın.

### [Remove-Azservicefabricmanagednodetypevmexgeri](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Düğüm türünden VM uzantısını kaldırın.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Belirli düğüm türünden düğümleri kümeden kaldırma.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Bir kümeden tam bir düğüm türü kaldırma.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Kümeden bir hizmeti kaldırma.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Kümeden bir veya birden çok hizmet dokusu ayarını kaldırın.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Düğüm türünden belirli düğümleri yeniden başlatın.

### [Set-Azhizmetifabricmanagedcluster](Set-AzServiceFabricManagedCluster.md)
Küme kaynağı özelliklerini ayarlayın.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Düğüm türü kaynak özelliklerini ayarlar ya da-Reimage parametresi

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Kümenin hizmet yapısı yükseltme türünü değiştirin.

### [Güncelleştirme-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Hizmet dokusu uygulamasını güncelleştirme. Bu, uygulama parametrelerini güncellemesine ve/veya uygulama yükseltmesini tetikleyecek uygulama türü sürümünü yükseltmesine olanak tanır.

### [Güncelleştirme-Azservicefabricdayanıklılığı](Update-AzServiceFabricDurability.md)
Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.

### [Update-Azservicefabricgüvenirlik](Update-AzServiceFabricReliability.md)
Kümedeki birincil düğümün güvenilirlik katmanını güncelleyin.

