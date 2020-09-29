---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 98bae70dbd61c74aa92e69cb67afc89ebae23f70
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928618"
---
# <a name="azure-powershell-release-notes"></a>Azure PowerShell sürüm notları

## <a name="470---september-2020"></a>4.7.0 - Eylül 2020
#### <a name="azaccounts"></a>Az.Accounts
* Yaklaşan yeni değişiklik iletileri biçimlendirildi
* Azure.Core 1.4.1 sürümüne güncelleştirildi

#### <a name="azaks"></a>Az.Aks
* 'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi. [#12372]
* 'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi. [#11239]
* Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi. [#11239]
* 'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi. [#12371]
* API sürümü 2020-06-01 olarak güncelleştirildi.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Belirli API’ler için ek yasal koşullar gösterildi.

#### <a name="azcompute"></a>Az.Compute
* 'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi
* Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'
* 'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi
* 'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi
* VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi
* 'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi
* 'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi. Alan, sanal makine örneğinin kaynak kimliğini gösterir
* 'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi 
* 'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi

#### <a name="azeventhub"></a>Az.EventHub
* Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.
* #10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.

#### <a name="azfunctions"></a>Az.Functions
* Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.
* PowerShell 6.2 sürümü kullanımdan kaldırıldı. Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.

#### <a name="azhdinsight"></a>Az.HDInsight
* Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi
    - 'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi
* Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi
    - Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi
    - Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi
    - Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi
    - Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi
    - Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi

#### <a name="azkeyvault"></a>Az.KeyVault
* RBAC yetkilendirmesi desteği eklendi [#10557]
* 'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]

#### <a name="azkusto"></a>Az.Kusto
* 'Az.Kusto' modülü genel kullanıma sunuldu

#### <a name="aznetwork"></a>Az.Network
* [Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi
    - 'New-AzVirtualRouter': 
        - IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi
        - -HostedGateway ve -HostedGatewayId parametreleri silindi
    - 'Get-AzVirtualRouter':
        - Abonelik düzeyi parametre kümesi eklendi
    - 'Remove-AzVirtualRouter'
    - 'Add-AzVirtualRouterPeer'
    - 'Get-AzVirtualRouterPeer'
    - 'Remove-AzVirtualRouterPeer'
* Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi
    - 'New-AzExpressRoutePortLOA'
* VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi
* 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.
* 'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi
* 'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]
* 'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi
* Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.
- 'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.
- 'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.
* Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.
* Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.
* 'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi
    - Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.

#### <a name="azresources"></a>Az.Resources
* Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi
* 'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi
* ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterilecek şekilde güncelleştirildi
* Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:
    - 'New-AzServiceFabricManagedCluster'
    - 'Get-AzServiceFabricManagedCluster'
    - 'Set-AzServiceFabricManagedCluster'
    - 'Remove-AzServiceFabricManagedCluster'
    - 'Add-AzServiceFabricManagedClusterClientCertificate'
    - 'Remove-AzServiceFabricManagedClusterClientCertificate'
    - 'New-AzServiceFabricManagedNodeType'
    - 'Get-AzServiceFabricManagedNodeType'
    - 'Set-AzServiceFabricManagedNodeType'
    - 'Remove-AzServiceFabricManagedNodeType'
    - 'Add-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Add-AzServiceFabricManagedNodeTypeVMSecret'
    - 'Remove-AzServiceFabricManagedNodeTypeVMExtension'
    - 'Restart-AzServiceFabricManagedNodeTyp'
* Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.

#### <a name="azsql"></a>Az.Sql
* 'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi
* 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi
* 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi
* 'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi
* Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi
    - 'Start-AzSqlInstanceDatabaseLogReplay'
    - 'Get-AzSqlInstanceDatabaseLogReplay'
    - 'Complete-AzSqlInstanceDatabaseLogReplay'
    - 'Stop-AzSqlInstanceDatabaseLogReplay'
* 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi
* 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi
* 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi
* Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi
* 'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi
* Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi
* 'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi
* 'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi
* Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi

#### <a name="azstorage"></a>Az.Storage
* Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]
* Belirli Bir Noktaya Geri Yükleme Desteği Eklendi
    - 'Enable-AzStorageBlobRestorePolicy'
    - 'Disable-AzStorageBlobRestorePolicy'
    - 'New-AzStorageBlobRangeToRestore'
    - 'Restore-AzStorageBlobRange'
* get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi 
    - 'Get-AzureRMStorageAccount'
* Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi
    - 'Get-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageContainerStoredAccessPolicy'
    - 'Set-AzStorageAccountManagementPolicy'
    - 'Get-AzStorageAccountManagementPolicy'
    - 'Add-AzStorageAccountManagementPolicyAction'
    - 'New-AzStorageAccountManagementPolicyRule'
* Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi

### <a name="thanks-to-our-community-contributors"></a>Topluluğumuzdan katkıda bulunanlara teşekkür ederiz
* Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911) 
* Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807) 
* Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828) 
* Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833) 
* @jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351) 
* @hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784) 
* Joshua Van Daalen (@greenSacrifice)
  * Özellikten Özelliğe yazımını güncelleştirdi (#12821) 
  * New-AzResourceLock.md örneklerini güncelleştirdi (#12806)
* Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825) 
* @rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)

## <a name="461---august-2020"></a>4.6.1 - Ağustos 2020
#### <a name="azcompute"></a>Az.Compute
* False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]

## <a name="460---august-2020"></a>4.6.0 - Ağustos 2020
#### <a name="azaccounts"></a>Az.Accounts
* Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)
* SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]

#### <a name="azautomation"></a>Az.Automation
* Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi

#### <a name="azcompute"></a>Az.Compute
* 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi
* 'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi
* '-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi
* Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* PSPipelineRun sınıfındaki eksik özellikler eklendi.

#### <a name="azhdinsight"></a>Az.HDInsight
* Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.

#### <a name="azkeyvault"></a>Az.KeyVault
* Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi
* SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi

#### <a name="azmaintenance"></a>Az.Maintenance
* 'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi
* 'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi

#### <a name="azmonitor"></a>Az.Monitor
* Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]
* 'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi

#### <a name="azresources"></a>Az.Resources
* 'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.
* Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu
* Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi
* Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi
* 'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı
* Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi 
* '-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]
* 'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi

#### <a name="azsignalr"></a>Az.SignalR
* 'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi
* 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi

#### <a name="azstorage"></a>Az.Storage
* Blob sorgu hızlandırması desteği eklendi
    -  'Get-AzStorageBlobQueryResult'
    -  'New-AzStorageBlobQueryConfig'
* Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi
    -  “Start-AzStorageBlobCopy”
    -  'Get-AzDataLakeGen2Item'
* İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]
    -  “Get-AzStorageBlobContent”
* Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi
    - 'New-AzStorageObjectReplicationPolicyRule'
    - 'Set-AzStorageObjectReplicationPolicy'
    - 'Get-AzStorageObjectReplicationPolicy'
    - 'Remove-AzStorageObjectReplicationPolicy'
* Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi
    - “Update-AzStorageBlobServiceProperty”

## <a name="450---august-2020"></a>4.5.0 - Ağustos 2020
#### <a name="azaccounts"></a>Az.Accounts
* 'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]
* SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]
* Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi
* Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi
* SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı

#### <a name="azaks"></a>Az.Aks
* 'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].
* 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].

#### <a name="azapimanagement"></a>Az.ApiManagement
* Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.
* Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.
* Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.
* Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.
* Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.
* Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.
* Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.
* Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.
* Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.
* Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.
* Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.
* 'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* 'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]

#### <a name="azhdinsight"></a>Az.HDInsight
* Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.
    - 'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi
    - 'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi
* Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:
    - 'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi
    - 'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi
* 'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü

#### <a name="aznetwork"></a>Az.Network
* 'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi
* Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.
* AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.
* 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi
* Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi
* Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.

#### <a name="azresources"></a>Az.Resources
* 'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi
    - Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir

#### <a name="azsql"></a>Az.Sql
* 'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi
* 'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi

#### <a name="azstorage"></a>Az.Storage
* Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi
    -  “New-AzStorageBlobSASToken”
    -  'New-AzStorageContainerSASToken'
* Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi
    -  'New-AzStorageAccountSASToken'
* Tek dosya paylaşımı kullanımını alma desteği eklendi
    - 'Get-AzRmStorageShare'

## <a name="440---july-2020"></a>4.4.0 - Temmuz 2020
#### <a name="azaccounts"></a>Az.Accounts
* “Invoke-AzRestMethod” adlı yeni cmdlet eklendi
* “Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]

#### <a name="azaks"></a>Az.Aks
* “Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı

#### <a name="azautomation"></a>Az.Automation
* Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* “En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* Data Factory’ye genel parametreler eklendi.

#### <a name="azeventgrid"></a>Az.EventGrid
* 2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.
* Yeni özellikler eklendi:
    - Giriş eşleme
    - Olay Teslim Şeması
    - Özel Bağlantı
    - Bulut Olayı V10 Şeması
    - Hedef Olarak Service Bus Konu Başlığı
    - Hedef Olarak Azure İşlevi
    - Web Kancası Toplu İş
    - Güvenli web kancası (AAD desteği)
    - IpFiltering
* Cmdlet'ler güncelleştirildi:
    - “New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:
        - Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.
        - AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.
        - Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.
        - Teslim şeması için yeni, isteğe bağlı parametre eklendi.
    - “New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:
        - IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.
    - “New-AzEventGridTopic'/'New-AzEventGridDomain”:
        - Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi
* Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi

#### <a name="azhdinsight"></a>Az.HDInsight
* Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.

#### <a name="azmonitor"></a>Az.Monitor
* Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]

#### <a name="aznetwork"></a>Az.Network
* VWan HubVnet bağlantısında değişen parametreler düzeltildi
* Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi
    - “Get-AzVirtualApplianceSite”
    - “New-AzVirtualApplianceSite”
    - “Remove-AzVirtualApplianceSite”
    - “Update-AzVirtualApplianceSite”
    - “New-AzOffice365PolicyProperty”
* Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi
    - “Get-AzNetworkVirtualAppliance”
    - “New-AzNetworkVirtualAppliance”
    - “Remove-AzNetworkVirtualAppliance”
    - “Update-AzNetworkVirtualAppliance”
    - “Get-AzNetworkVirtualApplianceSku”
    - “New-AzVirtualApplianceSkuProperty”
* Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi
* Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi
* Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı
* Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı
* Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.

#### <a name="azresources"></a>Az.Resources
* “Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.
* “Unregister-AzResourceProvider” cmdlet’i eklendi.

#### <a name="azsql"></a>Az.Sql
* “Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi
* Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.
* Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”

#### <a name="azstorage"></a>Az.Storage
* Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.
* MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi
    - “Update-AzStorageBlobServiceProperty”
* Blob sürümlerini içeren destek listesi blobları
    - “Get-AzStorageBlob”
* Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi
    - “Get-AzStorageBlob”
    - “Remove-AzStorageBlob”
* Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi
    - “Get-AzStorageBlobContent”
    - “New-AzStorageBlobSASToken”
    - “Remove-AzStorageBlob”
    - “Set-AzStorageBlobContent”
    - “Start-AzStorageBlobCopy”

#### <a name="azstoragesync"></a>Az.StorageSync
* ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi
* “UpdateStorageSyncService” cmdlet’i eklendi
    - “Set-AzStorageSyncService”
* StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.

#### <a name="azwebsites"></a>Az.Websites
* App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi

## <a name="430---june-2020"></a>4.3.0 - Haziran 2020
#### <a name="azaccounts"></a>Az.Accounts
* Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi
* Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]
* Azure.Core bütünleştirilmiş kodu güncelleştirildi
* 'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]

#### <a name="azaks"></a>Az.Aks
* Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi

#### <a name="azbatch"></a>Az.Batch
* Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi
* BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Hesap özelliklerini görüntüleme desteği eklendi.
* PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.

#### <a name="azcompute"></a>Az.Compute
* Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.
* New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.
* VMCustomScriptExtension için Alt Durumlar eklendi [#11297]
* New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.
* SAP için yeni VM Uzantısı’nın adı düzeltildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi

#### <a name="azeventhub"></a>Az.EventHub
* 'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi

#### <a name="azfunctions"></a>Az.Functions
* PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi

#### <a name="azhdinsight"></a>Az.HDInsight
* HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* SDK sürümü 1.1.0 olarak güncelleştirildi
* Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi

#### <a name="azmonitor"></a>Az.Monitor
* 'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi
* 'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]

#### <a name="aznetwork"></a>Az.Network
* 'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi
* Azure FirewallPolicy için yeni cmdlet’ler eklendi
    - 'New-AzFirewallPolicyDnsSetting'
    - Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği
* Arka uç adres havuzu işlemlerine yönelik destek eklendi
    - 'New-AzLoadBalancerBackendAddressConfig'
    - 'New-AzLoadBalancerBackendAddressPool'
    - 'Set-AzLoadBalancerBackendAddressPool'
    - 'Remove-AzLoadBalancerBackendAddressPool'
    - 'Get-AzLoadBalancerBackendAddressPool'
* 'New-AzIpGroup' için ad doğrulaması eklendi
* Azure FirewallPolicy için yeni cmdlet’ler eklendi
    - 'New-AzFirewallPolicyThreatIntelWhitelist'
* Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.
    - New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.
    - Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.
* 'Update-AzVpnGateway' güncelleştirildi
    - Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.
* Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:
    - 'Reset-AzHubRouter'
* Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi
    - RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi
    - Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi
* [Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.
* [Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.
* [Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.
* [Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.
* Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi
    - 'New-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Get-AzApplicationGatewayPrivateLinkConfiguration'
    - 'New-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Set-AzApplicationGatewayPrivateLinkConfiguration'
    - 'Remove-AzApplicationGatewayPrivateLinkConfiguration'
    - 'New-AzApplicationGatewayPrivateLinkIpConfiguration'
* VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.
    - 'New-AzVHubRoute'
    - 'New-AzVHubRouteTable'
    - 'Get-AzVHubRouteTable'
    - 'Update-AzVHubRouteTable'
    - 'Remove-AzVHubRouteTable'
* Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.
    - 'New-AzExpressRouteConnection'
    - 'Set-AzExpressRouteConnection'
    - ‘New-AzVirtualHubVnetConnection’
    - ‘Update-AzVirtualHubVnetConnection’
    - 'New-AzVpnConnection'
    - 'Update-AzVpnConnection'
    - 'New-AzP2sVpnGateway'
    - 'Update-AzP2sVpnGateway'

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]
* 'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi 
* 'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi
    - 'New-AzOperationalInsightsSavedSearch'
    - 'Set-AzOperationalInsightsSavedSearch'

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Backup’a MAB öğelerini getirme desteği eklendi.
* Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler

#### <a name="azresources"></a>Az.Resources
* 'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]
* 'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]
* 'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi
* 'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi
* 'Test-Az*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi
* deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi

#### <a name="azsql"></a>Az.Sql
* SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi
* Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.
* 'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]

#### <a name="azstorage"></a>Az.Storage
* RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi
    -  'New-AzStorageAccount'
* Azure.Core yükleme mantığı Az.Accounts’a taşındı

#### <a name="azwebsites"></a>Az.Websites
* 'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi
* 'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi
* 'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi
* Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi
* Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi
* Kaynak grupları arasında kopyalama için özel durumlar eklendi

## <a name="420---june-2020"></a>4.2.0 - Haziran 2020
#### <a name="azaccounts"></a>Az.Accounts
* Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azapimanagement"></a>Az.ApiManagement
* Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azbilling"></a>Az.Billing
* Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* PrivateEndpoint ve PublicNetworkAccess denetimini destekler. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azdatashare"></a>Az.DataShare
* ''Az.DataShare'' modülü genel kullanıma sunuldu

#### <a name="azdesktopvirtualization"></a>Az.DesktopVirtualization
* ''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* SDK 0.21.0 sürümüne güncelleştirildi
* İsteğe bağlı aşağıdaki parametreler eklendi 
    - 'New-AzOperationalInsightsSavedSearch'
    - 'Set-AzOperationalInsightsSavedSearch'

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* 'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azprivatedns"></a>Az.PrivateDns
* Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.
* SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azresources"></a>Az.Resources
* Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi
* Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi
* -DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi
* Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.
* Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi
* 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi
* SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi

#### <a name="azstorage"></a>Az.Storage
* Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi

## <a name="410---may-2020"></a>4.1.0 - Mayıs 2020
### <a name="highlights-since-the-last-release"></a>Son sürümden bu yana öne çıkanlar
* Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7
* Az.Functions genel kullanıma sunuldu 
* Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı

#### <a name="azaccounts"></a>Az.Accounts
* 'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi
* Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir

#### <a name="azaks"></a>Az.Aks
* API Sürümü 2019-10-01’e yükseltildi
* Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu
* Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'

#### <a name="azapimanagement"></a>Az.ApiManagement
* 'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı
* 'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]
* 'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı. PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.
* 'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı. PropertyId parametresi NamedValueId olarak yeniden adlandırıldı. 
* 'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı. PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.
* 'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı. PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.
* Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.
* Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.
* Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.
* Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.
* Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.
* Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'
* 'Update-AzApplicationInsights' cmdlet’i oluşturuldu
* Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu

#### <a name="azbatch"></a>Az.Batch
* Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.
* 'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.
* Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.
  - Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir. Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.
* 'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.
* 'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.
  - 'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı. Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.

#### <a name="azcompute"></a>Az.Compute
* 'Update-AzVM' cmdlet’ine HostId parametresi eklendi
* 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.
* Yeni değişiklikler
    - FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.
    - AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.
    - AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.
    - AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.
    - MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.
    - AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.
* 'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi. 

#### <a name="azdatafactory"></a>Az.DataFactory
* Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi
* Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi
* Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.
* Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi

#### <a name="azfunctions"></a>Az.Functions
* ''Az.Functions'' modülü genel kullanıma sunuldu

#### <a name="azhdinsight"></a>Az.HDInsight
* Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor

#### <a name="aziothub"></a>Az.IotHub
* SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.
* 'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]
* IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.
* Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.
* IoT Edge otomatik dağıtımını büyük ölçekte yönetin. Yeni cmdlet’ler şunlardır:
    - 'Add-AzIotHubDeployment'
    - 'Get-AzIotHubDeployment'
    - 'Remove-AzIotHubDeployment'
    - 'Set-AzIotHubDeployment'
* IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.
* Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.

#### <a name="azkeyvault"></a>Az.KeyVault
* İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'
* Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi
* Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir
* Kendi anahtarını getir (BYOK) desteği eklendi
    - 'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler
    - 'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler
* 'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi

#### <a name="azmonitor"></a>Az.Monitor
* 'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]
* Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi
    - 'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi
    - 'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler
* PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]
* PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]
* 'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı

#### <a name="aznetwork"></a>Az.Network
* Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi
    - 'New-AzPublicIpAddress'
    - 'New-AzPublicIpPrefix'
    - 'New-AzLoadBalancerFrontendIpConfig'
* Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzSecurityPartnerProvider
        - Remove-AzSecurityPartnerProvider
        - Get-AzSecurityPartnerProvider
        - Set-AzSecurityPartnerProvider
* 'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi
* New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi
* VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.
    - 'New-AzVirtualWan'
    - 'Update-AzVirtualWan'
* Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi
    - 'New-AzPrivateDnsZoneConfig'
    - 'Get-AzPrivateDnsZoneGroup'
    - 'New-AzPrivateDnsZoneGroup'
    - 'Set-AzPrivateDnsZoneGroup'
    - 'Remove-AzPrivateDnsZoneGroup'
* 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi
* 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi
    - Şu cmdlet güncelleştirildi:
        - New-AzFirewall

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi
* Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler
    - 'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')
    - 'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')
    - 'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')
* 'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi
* Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu
* Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.
* Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.
* Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.
* Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.
* Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.

#### <a name="azresources"></a>Az.Resources
* Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi
* Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi
* 'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]
* 'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]
* Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'
* Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'
   - Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'
* 'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı
* Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi
* Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi
* Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi
* Dağıtım betiği çıkışına 'error' özelliği eklendi
* NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi
* DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı
* SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi
* Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi
    - 'New-AzDeployment'
    - 'New-AzManagementGroupDeployment'
    - 'New-AzResourceGroupDeployment'
    - 'New-AzTenantDeployment'

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi

#### <a name="azsql"></a>Az.Sql
* Şunların performansı iyileştirildi:
    - 'Set-AzSqlDatabaseSensitivityClassification'
    - 'Set-AzSqlInstanceDatabaseSensitivityClassification'
    - 'Remove-AzSqlDatabaseSensitivityClassification'
    - 'Remove-AzSqlInstanceDatabaseSensitivityClassification'
    - 'Enable-AzSqlDatabaseSensitivityRecommendation'
    - 'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'
    - 'Disable-AzSqlDatabaseSensitivityRecommendation'
    - 'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'
* 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı
* Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* 'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi
* Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi
    - 'Set-AzStorageAccount'
* İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi
    - 'Remove-AzStorageDirectory'
* Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.
    - 'Update-AzStorageAccountNetworkRuleSet'
    - 'Get-AzStorageAccountNetworkRuleSet'
* Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla
    - 'Add-AzStorageAccountNetworkRule'
* Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi
* DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,
    - 'Get-AzDataLakeGen2ChildItem'
* Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi
    -  'New-AzStorageAccount'
    -  'Set-AzStorageAccount'
* Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi
    -  'New-AzStorageAccountKey'
    -  'Get-AzStorageAccountKey'
* Yük devretme Depolama hesabı desteği eklendi
    - 'Invoke-AzStorageAccountFailover'
* 'Get-AzStorageBlobCopyState' yardımı güncelleştirildi
* 'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi
* Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi
* CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak
    - 'Get-AzStorageFile'
    - 'Remove-AzStorageFile'
    - 'Get-AzStorageFileContent'
    - 'Set-AzStorageFileContent'
    - 'Start-AzStorageFileCopy'
* CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak
    - 'New-AzStorageDirectory'
    - 'Remove-AzStorageDirectory'
* CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak
    - 'Get-AzStorageShare'
    - 'New-AzStorageShare'
    - 'Remove-AzStorageShare'
* FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak
    - 'Set-AzStorageShareQuota'

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* 'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* 'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.

## <a name="380---april-2020"></a>3.8.0 - Nisan 2020
### <a name="highlights-since-the-last-release"></a>Son sürümden bu yana öne çıkanlar
* Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7

#### <a name="azaccounts"></a>Az.Accounts
* 'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]

#### <a name="azapimanagement"></a>Az.ApiManagement
* Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi
* 'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi

#### <a name="azcdn"></a>Az.Cdn
* ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı

#### <a name="azcompute"></a>Az.Compute
* 'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.
* -InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.

#### <a name="aziothub"></a>Az.IotHub
* IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:
    - 'Get-AzIotHubDeviceTwin'
    - 'Update-AzIotHubDeviceTwin'
* IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.
* IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:
    - 'Get-AzIotHubModuleTwin'
    - 'Update-AzIotHubModuleTwin'
* Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin. Yeni cmdlet’ler şunlardır:
    - 'Add-AzIotHubConfiguration'
    - 'Get-AzIotHubConfiguration'
    - 'Remove-AzIotHubConfiguration'
    - 'Set-AzIotHubConfiguration'
* Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.

#### <a name="azkeyvault"></a>Az.KeyVault
* Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi
* Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]
* 'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]
* Özel uç noktaya destek eklendi

#### <a name="azmaintenance"></a>Az.Maintenance
* GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor

#### <a name="azmonitor"></a>Az.Monitor
* Özel bağlantı kapsamı için cmdlet’ler eklendi
    - 'Get-AzInsightsPrivateLinkScope'
    - 'Remove-AzInsightsPrivateLinkScope'
    - 'New-AzInsightsPrivateLinkScope'
    - 'Update-AzInsightsPrivateLinkScope'
    - 'Get-AzInsightsPrivateLinkScopedResource'
    - 'New-AzInsightsPrivateLinkScopedResource'
    - 'Remove-AzInsightsPrivateLinkScopedResource'

#### <a name="aznetwork"></a>Az.Network
* Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.
    - 'New-AzVirtualNetworkGateway'
    - 'Set-AzVirtualNetworkGateway'
    - 'New-AzVirtualNetworkGatewayConnection'
    - 'Set-AzVirtualNetworkGatewayConnection'
* FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi
    - 'New-AzLocalNetworkGateway'
    - 'New-AzVpnSiteLink'
* ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi
    - 'Set-AzExpressRouteCircuitConnectionConfig' eklendi
        - IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar
    - 'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi
        - Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi
* Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.
    - New-AzVirtualNetworkGatewayConnection
    - Set-AzVirtualNetworkGatewayConnection

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi
* 'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi

#### <a name="azsql"></a>Az.Sql
* 'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi
* Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.

#### <a name="azstorage"></a>Az.Storage
* Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi
* Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi
    - 'New-AzStorageAccount'
    - 'Set-AzStorageAccount'
* DataLake Gen2 desteklendi
    - 'New-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ChildItem'
    - 'Move-AzDataLakeGen2Item'
    - 'Set-AzDataLakeGen2ItemAclObject'
    - 'Update-AzDataLakeGen2Item'
    - 'Get-AzDataLakeGen2ItemContent'
    - 'Remove-AzDataLakeGen2Item'

## <a name="0100-preview---april-2020"></a>0.10.0-preview - Nisan 2020
### <a name="general"></a>Genel
* Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir. Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar. Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz
* Az modülleri profil 2019-03-01-hybrid’i destekliyor:
  - Az.Billing
  - Az.Compute
  - Az.DataBoxEdge
  - Az.EventHub
  - Az.IotHub
  - Az.KeyVault
  - Az.Monitor
  - Az.Network
  - Az.Resources
  - Az.Storage
  - Az.Websites
* Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu
* Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır
* Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir

## <a name="370---march-2020"></a>3.7.0 - Mart 2020
#### <a name="azaccounts"></a>Az.Accounts
* Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]

#### <a name="azcompute"></a>Az.Compute
* ‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:
    - DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference
* Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.
* ‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi. [#11354]
* Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi
    - ‘Set-AzVMAEMExtension’
    - ‘Get-AzVMAEMExtension’
    - ‘Remove-AzVMAEMExtension’
    - ‘Update-AzVMAEMExtension’
* Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi
* VM PowerState için tam dize değeri tablo biçiminde gösterildi.
* ‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi [#11257]

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi
* Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi
* ‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi

#### <a name="azhdinsight"></a>Az.HDInsight
* Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi

#### <a name="aziothub"></a>Az.IotHub
* Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi. Yeni Cmdlet’ler şunlardır:
    - ‘Get-AzIotHubDistributedTracing’
    - ‘Set-AzIotHubDistributedTracing’

#### <a name="azkeyvault"></a>Az.KeyVault
* ‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi

#### <a name="azmonitor"></a>Az.Monitor
* ‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi
    - ‘New-AzVirtualHubVnetConnection’
    - ‘Update-AzVirtualHubVnetConnection’
    - ‘New-AzVirtualHub’
    - ‘Update-AzVirtualHub’
* SQL Yönetim SDK’sı bağımlılığı kaldırıldı

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Hata iletileri iyileştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.
* Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi
* Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.
* Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.
* AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi
* IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi

#### <a name="azresources"></a>Az.Resources
* ‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]
* Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi
* ‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı. Örnek eklendi.
* ‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]
* Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)

#### <a name="azsql"></a>Az.Sql
* ‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi
* ‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi
* Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.

#### <a name="azsupport"></a>Az.Support
* ‘Az.Support’ modülü genel kullanıma sunuldu

#### <a name="azwebsites"></a>Az.Websites
* Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.
    - ‘Get-AzWebAppTrafficRouting’
    - ‘Update-AzWebAppTrafficRouting’
    - ‘Add-AzWebAppTrafficRouting’
    - ‘Remove-AzWebAppTrafficRouting’

## <a name="361---march-2020"></a>3.6.1 - Mart 2020
#### <a name="azaccounts"></a>Az.Accounts
* 'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]
* 'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]
* UserAgent’ta Az sürümü eklendi

#### <a name="azapimanagement"></a>Az.ApiManagement
* DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]
* 'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]
* 'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi
* 'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.

#### <a name="aziothub"></a>Az.IotHub
* Iot Hub’daki cihazları yönetmek için destek eklendi. Yeni Cmdlet’ler şunlardır:
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'
* IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi. Yeni Cmdlet’ler şunlardır:
    - 'Add-AzIotHubModule'
    - 'Get-AzIotHubModule'
    - 'Remove-AzIotHubModule'
    - 'Set-AzIotHubModule'
* Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.
* Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.
* IoT cihazının üst cihazını almak/ayarlamak için destek eklendi. Yeni Cmdlet’ler şunlardır:
    - 'Get-AzIotHubDeviceParent'
    - 'Set-AzIotHubDeviceParent'
* Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.

#### <a name="azmonitor"></a>Az.Monitor
* 'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]

#### <a name="aznetwork"></a>Az.Network
* SQL Yönetim SDK’sı güncelleştirildi.
* PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.
    - ActionsRequired alanı ActionRequired alanına eşleniyor.
* 'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi

#### <a name="azresources"></a>Az.Resources
* 'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi
* '-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]
* 'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]
* 'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]
* GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi
* İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi
* 'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi
* Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi
    - Get-AzTag -ResourceId
    - New-AzTag -ResourceId
    - Remove-AzTag -ResourceId
* Yeni Tag cmdlet’i eklendi
    - Update-AzTag -ResourceId
* SDK 3.3.0 sürümünden ScopedDeployment getirildi

#### <a name="azsql"></a>Az.Sql
* 'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi
* Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi
    - Yönetilen bir veritabanında LTR ilkesini alma/ayarlama
    - Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma
    - Bir LTR yedeklemesini kaldırma
    - Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme
* New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi
* New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi
* Az.Network için SQL SDK sürümü artırıldı

#### <a name="azstorage"></a>Az.Storage
* ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi
    - 'Set-AzRmStorageContainerImmutabilityPolicy'
* Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi
    - 'New-AzStorageTable'
    - 'Get-AzStorageTable'

#### <a name="azwebsites"></a>Az.Websites
* 'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi
* Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur
* App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi
* Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı
* WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi

## <a name="350---february-2020"></a>3.5.0 - Şubat 2020
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* İstemci tarafı telemetri güncelleştirildi.
* Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.
* Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.

#### <a name="azaccounts"></a>Az.Accounts
* İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi

#### <a name="azautomation"></a>Az.Automation
* 'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* SDK 7.0 olarak güncelleştirildi
* Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi

#### <a name="azcompute"></a>Az.Compute
* Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi

#### <a name="azfrontdoor"></a>Az.FrontDoor
* WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi

#### <a name="aziothub"></a>Az.IotHub
* Iot Hub’daki cihazları yönetmek için destek eklendi. Yeni Cmdlet’ler şunlardır:
    - 'Add-AzIotHubDevice'
    - 'Get-AzIotHubDevice'
    - 'Remove-AzIotHubDevice'
    - 'Set-AzIotHubDevice'

#### <a name="azkeyvault"></a>Az.KeyVault
* Add-AzKeyVaultKey.md için yinelenen metin düzeltildi

#### <a name="azmonitor"></a>Az.Monitor
* Get-AzLog cmdlet’inin açıklaması düzeltildi.
* 'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.
    - Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.

#### <a name="aznetwork"></a>Az.Network
* 'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.
* Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.
* Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.
* Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı
    - Yeni cmdlet eklenmedi. Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.

#### <a name="azresources"></a>Az.Resources
* Şablon dağıtım cmdlet’leri yeniden düzenlendi
    - Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: *-AzManagementGroupDeployment
    - Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: *-AzTenantDeployment
    - *-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi
    - *-AzDeployment cmdlet’leri için *-AzSubscriptionDeployment diğer adları oluşturuldu
* 'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi
* AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.
* Yardım dosyaları yeniden oluşturuldu

#### <a name="azsql"></a>Az.Sql
* Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.
* Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi
* 'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi

#### <a name="azstoragesync"></a>Az.StorageSync
* 'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.

## <a name="340---february-2020"></a>3.4.0 - Şubat 2020
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* Az.CosmosDB ilk sürüm 0.1.0 yayınlandı
* Az.Network ConnectionMonitor V2 desteği eklendi

#### <a name="azaccounts"></a>Az.Accounts
* AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma
* Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** ve **Set-AzApiManagementProduct**
  - https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi
* **Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi

#### <a name="azcompute"></a>Az.Compute
* Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.
* Update-AzDiskEncryptionSet cmdlet’i eklendi
* Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 4.7.0’a güncelleştirildi

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Kaynaklara yönelik LIST işlemlerini ekler
* Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler

#### <a name="azhdinsight"></a>Az.HDInsight
* New-AzHDInsightCluster’ın belge hatası düzeltildi.

#### <a name="azkeyvault"></a>Az.KeyVault
* Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.

#### <a name="aznetwork"></a>Az.Network
* Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.
* Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak
    - New-AzFirewall cmdlet'i güncelleştirildi:
        - Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi
        - Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir
* Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.
* Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.
* Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi
        - New-AzApplicationGatewayRewriteRuleActionSet
* NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu
    - Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi
* İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi
* API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.
* Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.

#### <a name="azresources"></a>Az.Resources
* Varsayılanı bağlam aboneliği olan *-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı
* Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi

#### <a name="azsql"></a>Az.Sql
DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek
    - New-AzStorageAccount
* StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi
* Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState
* Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi

## <a name="330---january-2020"></a>3.3.0 - Ocak 2020
#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi

#### <a name="azcdn"></a>Az.Cdn
* New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme

#### <a name="azcompute"></a>Az.Compute
* İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* 'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi
  - Edge Depolama Kapsayıcısını edinme
* 'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi
  - Yeni Edge Depolama Kapsayıcısı oluşturma
* 'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi
  - Edge Depolama Kapsayıcısını kaldırma
* 'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi
  - Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma
* 'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi
  - Edge Depolama Hesabını edinme
* 'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi
  - Yeni Edge Depolama Hesabını oluşturma
* 'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi
  - Edge Depolama Hesabını kaldırma
* 'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma
  - Paylaşımdaki verileri yenilemek için eylem çağırma
* 'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi
  - Az databoxedge depolama hesabı kimlik bilgilerini ayarlama

#### <a name="azdatafactory"></a>Az.DataFactory
* Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi
* ADF .Net SDK sürümü 4.6.0’a güncelleştirildi
* Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı

#### <a name="azeventhub"></a>Az.EventHub
* Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi

#### <a name="azhdinsight"></a>Az.HDInsight
* Invoke-AzHDInsightHiveJob.md hatası düzeltildi.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* 1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.
* Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.
* Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.
* HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.

#### <a name="azresources"></a>Az.Resources
* 'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.

#### <a name="azsql"></a>Az.Sql
* Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.
* SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Yeni geçerli Lisans türü olarak DR eklendi

#### <a name="azstorage"></a>Az.Storage
* Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi
    - Update-AzStorageAccountNetworkRuleSet
* Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 - Aralık 2019

### <a name="general"></a>Genel
* .psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi

#### <a name="azaccounts"></a>Az.Accounts
* Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı
* Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor

#### <a name="azbatch"></a>Az.Batch
* **New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 4.5.0’a güncelleştirildi

#### <a name="azfrontdoor"></a>Az.FrontDoor
* WAF tarafından yönetilen kuralları dışlama desteği eklendi
* Otomatik tamamlamaya SocketAddr eklendi

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Özel Durum İşleme

#### <a name="azkeyvault"></a>Az.KeyVault
* Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi
* Eliptik Eğri Şifrelemesi Sertifika Yönetimi
    - Sertifika İlkeleri için Eğri belirtme desteği eklendi

#### <a name="azmonitor"></a>Az.Monitor
* Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi. Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni

#### <a name="aznetwork"></a>Az.Network
* AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.

#### <a name="azresources"></a>Az.Resources
* Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.
* İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.

#### <a name="azsql"></a>Az.Sql
* Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi

#### <a name="azstorage"></a>Az.Storage
* OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği
    - Revoke-AzStorageAccountUserDelegationKeys
* Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.
* Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* 'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi
    - Set-AzStorageShareQuota
* Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 - Kasım 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* Az.DataBoxEdge 1.0.0 yayımlandı
* Az.SqlVirtualMachine 1.0.0 yayımlandı

#### <a name="azcompute"></a>Az.Compute
* VM Reapply özelliği
    - Set-AzVM cmdlet’ine Reapply parametresi ekleme
* VM Ölçek Kümesi AutomaticRepairs özelliği:
    - EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss
* New-AzVM için kiracılar arası galeri görüntüsü desteği
* New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.
* Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi
* New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi
* New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi
* New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi
* New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* `Get-AzDataBoxEdgeOrder` cmdlet’i eklendi
    - Sırayı Al
* `New-AzDataBoxEdgeOrder` cmdlet’i eklendi
    - Yeni Sıra oluştur
* `Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi
    - Sırayı kaldır
* `New-AzDataBoxEdgeShare` cmdlet’inde değiştir
    - Yerel Paylaşım’ı oluşturur
* `Set-AzDataBoxEdgeRole` cmdlet’i eklendi
    - IotRole artık Paylaş ile eşlenebilir
* `Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi
    - Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin
* `Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi
    - Tetikleyicilere ilişkin bilgileri alır
* `New-AzDataBoxEdgeTrigger` cmdlet’i eklendi
    - Yeni Tetikleyiciler oluştur
* `Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi
    - Tetikleyicileri kaldır

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 4.4.0’a güncelleştirildi
* Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi

#### <a name="azeventhub"></a>Az.EventHub
* #10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi
* New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi
* BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* ‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.

#### <a name="azprivatedns"></a>Az.PrivateDns
* PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.
* Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.
* Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.

#### <a name="azrediscache"></a>Az.RedisCache
* ‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi. ‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.
* ‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.

#### <a name="azresources"></a>Az.Resources
- İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.
- İlke tanımı oluştur yardım örneği güncelleştirildi
- Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.
- Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.
- Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.

#### <a name="azsql"></a>Az.Sql
* ReadReplicaCount veritabanı için destek eklendi.
* Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi

## <a name="300---november-2019"></a>3.0.0 - Kasım 2019
### <a name="general"></a>Genel
* Az.PrivateDns 1.0.0 yayınlandı

#### <a name="azaccounts"></a>Az.Accounts
* 'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.

#### <a name="azadvisor"></a>Az.Advisor
* Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.

#### <a name="azbatch"></a>Az.Batch
* `BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı. Ayrıca yeni bir `LowPriorityCoreQuota` var.
  - Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.
* **New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.
* `PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i. Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.
  - Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:
    - `AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.
    - `StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.
* **Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.
  - Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir. Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.
  - `ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.
* `PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.
* `PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.
* `PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.
* `PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.
* **Set-AzBatchPoolOSVersion** kaldırıldı. Bu işlem artık desteklenmiyor.
* `PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.
* `PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.
* `PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.
* **Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.
  - **Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.
  - Artık yeni doğrulanmamış resimler de döndürülüyor. Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.
* **New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.
* Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor. Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.
* Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor. Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.
* Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi. Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.
* Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).
* Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).

#### <a name="azcdn"></a>Az.Cdn
* RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.
* New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* Disk Şifreleme Kümesi özelliği
    - Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk
    - Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig
* New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi
* Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı
* New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi
* Yeni değişiklikler
    - CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor
    - GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 4.3.0’a güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor
* Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.
* adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma
* badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme
* Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme
* Birleştirme Hatasını Düzeltme

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Modüllerde çeşitli yazım hataları düzeltildi

#### <a name="azhdinsight"></a>Az.HDInsight
* ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.
* Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.
* Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi
* Beş cmdlet kaldırıldı:
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Üç cmdlet eklendi:
    - Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).
    - Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).
    - Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).
* Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.
* Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.
* Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.
* Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:
*  - Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.
*  - Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.
*  - Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.
* Bazı senaryo test çalışmaları eklendi.
* Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.

#### <a name="aziothub"></a>Az.IotHub
* Hataya neden olan değişiklikler:
    - 'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.
    - 'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.
    - 'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.
    - 'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.
    - 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.
    - 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.
    - 'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.
    - 'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.
    - 'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.
    - 'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.
    - 'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.
    - 'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.
* Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.
* Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.
* Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.
* Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.
* Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.
* Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.
* Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.
* VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi

#### <a name="azresources"></a>Az.Resources
* Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.
    - Şu cmdlet güncelleştirildi:
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.
    - Yeni cmdlet:
        - Get-AzPrivateLinkResource
* Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.
    - PrivateLinkService'e EnableProxyProtocol özelliği eklendi
    - PrivateEndpointConnection'a LinkIdentifier özelliği eklendi
    - New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.
* 'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi
* Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi
* VirtualHub'ın RouteTables alt kaynağı için destek eklendi
    - Yeni cmdlet'ler eklendi:
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi
    - Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:
        - New-AzVirtualHub : Sku parametresi eklendi
        - Update-AzVirtualHub : Sku parametresi eklendi
        - New-AzVirtualWan : VirtualWANType parametresi eklendi
        - Update-AzVirtualWan : VirtualWANType parametresi eklendi
* HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi
    - Yeni cmdlet'ler eklendi:
        - Update-AzureRmVirtualHubVnetConnection
    - Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:
        - New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi
        - New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi
        - Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi
        - New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi
        - Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi
* TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:
        - New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi
* CustomRule'da Geo-Match işleci için destek eklendi
    - FirewallCondition'da işlece GeoMatch eklendi
* perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi
    - Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:
        - New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi
        - New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi
* 'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi
* Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek
* IpGroup'un RouteTables üst düzey kaynağı için destek eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.

#### <a name="azsql"></a>Az.Sql
* Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.
* Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.
* Kullanım dışı bırakılan diğer adlar kaldırıldı:
* Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)
* Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)
* Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı
* Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı
* Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı
* Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle

## <a name="280---october-2019"></a>2.8.0 - Ekim 2019
### <a name="general"></a>Genel
* Az.HealthcareApis 1.0.0 sürümü

#### <a name="azaccounts"></a>Az.Accounts
* Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi
    - [https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi

#### <a name="azautomation"></a>Az.Automation
* Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.

#### <a name="azbatch"></a>Az.Batch
* Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.

#### <a name="azcompute"></a>Az.Compute
* New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi
* Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi
* Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.
* Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.
* ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.
* ADF .Net SDK sürümü 4.2.0’a güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* PowerShell sürümü 1.0.0 olarak güncelleştirildi
* SDK sürümü 1.0.2 olarak güncelleştirildi
* Yeni SDK sürümüne başvurmaları için testler güncelleştirildi
* İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.

#### <a name="aziothub"></a>Az.IotHub
* Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents
* Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor

#### <a name="azmonitor"></a>Az.Monitor
* Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi
* Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın. Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir
* Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.

#### <a name="aznetwork"></a>Az.Network
* Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.
* Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzureRmTrafficSelectorPolicy
    - Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection
* Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi
    - Cmdlet'ler güncelleştirildi:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi
* VirtualNetworkGateways için yeni Nesiller ve SKU’lar
  - VirtualNetworkGateways için yeni Nesiller sunuldu.
  - VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.

#### <a name="azrediscache"></a>Az.RedisCache
* ‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi

#### <a name="azstorage"></a>Az.Storage
* Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi
* Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek
    -  Get-AzRmStorageContainer
* Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.

#### <a name="azwebsites"></a>Az.Websites
* Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor

## <a name="270---september-2019"></a>2.7.0 - Eylül 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* 'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi
* Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı. Bunun yerine 'Set-AzApiManagement' kullanın.

#### <a name="azautomation"></a>Az.Automation
* 'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi
* Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi
* -Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi
* New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi
* Düşük öncelikli sanal makine özelliği eklendi:
    - New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.
    - New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.
* Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.
* Get-AzRemoteDesktopFile için null özel durumu düzeltildi.
* Sona göre konum için VHD Seek yöntemi düzeltildi.
* New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus
* ADF .Net SDK sürümü 4.1.3’e güncelleştirildi

#### <a name="azhdinsight"></a>Az.HDInsight
* Son değişiklikler duyurusu

#### <a name="aziothub"></a>Az.IotHub
* Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.
* IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi. Yeni cmdlet’ler şunlardır:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder
   - Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler. Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.
   - **ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu. Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.
   - **EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi. Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı. **NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.
   - **Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi. Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.
   - **AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi. Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.
* Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi
    - New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur
    - Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder
* Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler
 - Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder
 - 'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı
 - İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi
 - Yardım dosyaları genel olarak geliştirildi
* 'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi

#### <a name="aznetwork"></a>Az.Network
* 'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi
* 'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi
* 'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi
* Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi
* Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi
* Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi
* Özel IP özelliği için ağ arabirimine özellikler eklendi
    - 'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi
    - 'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi
    - Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi
* Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi
* Sanal WAN’da çoklu bağlantı desteği
    - Yeni cmdlet’ler
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Şu cmdlet güncelleştirildi:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi
* VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi

#### <a name="azresources"></a>Az.Resources
* New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi
* Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.

#### <a name="azsignalr"></a>Az.SignalR
* Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi

#### <a name="azsql"></a>Az.Sql
* 'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi
* Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.
* Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı
* Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.
* Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* 'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi
* Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.
    -  Set-AzStorageBlobContent
* Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor
* Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor
* 'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi

## <a name="260---august-2019"></a>2.6.0 - Ağustos 2019
#### <a name="general"></a>Genel
* Çok sayıda modülde çeşitli yazım hataları düzeltildi

#### <a name="azaccounts"></a>Az.Accounts
* Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)

#### <a name="azaks"></a>Az.Aks
* ‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi
    * Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi
    - ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi
* **Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752
* 'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi

#### <a name="azbatch"></a>Az.Batch
* Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi

#### <a name="azcdn"></a>Az.Cdn
* CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi

#### <a name="azcompute"></a>Az.Compute
* New-AzVMConfig cmdlet’ine VmssID eklendi
* New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi
* VM görüntüsü nesnesine HyperVGeneration özelliği eklendi
* Host ve HostGroup özellikleri eklendi
    - Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi
* Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi
* 'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi
* ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi
* Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi
* Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.

#### <a name="azeventhub"></a>Az.EventHub
* #9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası
* #9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması
* Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi
* #9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* ‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi

#### <a name="azmonitor"></a>Az.Monitor
* Yardım belgelerindeki yanlış parametre adı düzeltildi

#### <a name="aznetwork"></a>Az.Network
* New-AzPrivateLinkServiceIpConfig güncelleştirildi
    - Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.
    - Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.
* SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir
* Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.
* Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.
* AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi
    - Örnek eklendi
    - ‘-Name’ parametresi için açıklama güncelleştirildi
* New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi
* New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi

#### <a name="azresources"></a>Az.Resources
* Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi
    - Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi
    - 'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir
* Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi

#### <a name="azservicebus"></a>Az.ServiceBus
* #9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası
* #9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması
* Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Düğüm ekleme türü cmdlet hataları düzeltildi:
    - Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası. Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681
    - virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi. Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407
    - Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı

#### <a name="azsql"></a>Az.Sql
* Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.

#### <a name="azstorage"></a>Az.Storage
* Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi
* Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi

## <a name="250---july-2019"></a>2.5.0 - Temmuz 2019
#### <a name="azaccounts"></a>Az.Accounts
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* 'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi

#### <a name="azautomation"></a>Az.Automation
* Kaynak dizesindeki yazım hatası düzeltildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* NetworkRuleSet desteği eklendi.

#### <a name="azcompute"></a>Az.Compute
* VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi
* 'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi

#### <a name="azeventhub"></a>Az.EventHub
* SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken
* yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi

#### <a name="azkeyvault"></a>Az.KeyVault
* Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme
    - Filtreleme için yeni MapType parametresi eklendi

#### <a name="azmanagedservices"></a>Az.ManagedServices
* API 2019-06-01 sürümü için destek eklendi (GA)

#### <a name="aznetwork"></a>Az.Network
* Özel uç nokta ve özel bağlantı hizmeti için destek eklendi
    - Yeni cmdlet’ler
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı
    - New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi
        - Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.
        - Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.
* AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı
* Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi
    - Cmdlet'ler güncelleştirildi
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi
* LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi
    - Şu cmdlet güncelleştirildi:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi
    - New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi. Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.
* Özel günlük null normal ifade işleme düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi
* 'Get-AzRecoveryServicesVault.md' güncelleştirildi
* 'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi
* 'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi
* 'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi
* Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi
* 'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi

#### <a name="azresources"></a>Az.Resources
- 'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı
- İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken
* yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi

#### <a name="azsql"></a>Az.Sql
* Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi
* E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi
* Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* 'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi

#### <a name="azstoragesync"></a>Az.StorageSync
* Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.
* TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi
* Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi
* New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi

## <a name="240---july-2019"></a>2.4.0 - Temmuz 2019
#### <a name="azaccounts"></a>Az.Accounts
* Profil cmdlet’leri için destek eklendi
* Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi
* Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi

#### <a name="azadvisor"></a>Az.Advisor
* Az.Advisor genel kullanıma sunuldu
* Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur

#### <a name="azapimanagement"></a>Az.ApiManagement
* [https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi
    - **Get-AzApiManagementSubscription**
        - Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi
        - Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')
* [https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme
    - **Import-AzApiManagementApi**
        - API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi

#### <a name="azautomation"></a>Az.Automation
* Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* New-AzImageConfig’e HyperVGeneration parametresi eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.

#### <a name="azeventgrid"></a>Az.EventGrid
* ‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi

#### <a name="aziothub"></a>Az.IotHub
* Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.

#### <a name="aznetwork"></a>Az.Network
* Genel IP etiketlerine ‘RoutingPreference’ eklendi
* ‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Get-AzPolicyState’de boş başvuru sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* IaaSVM’ler için get-policy komutu düzeltmesi

#### <a name="azresources"></a>Az.Resources
    - Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi
    - Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi
    - Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi
    - İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* 4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi

#### <a name="azsql"></a>Az.Sql
* Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi
* Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı

#### <a name="azstorage"></a>Az.Storage
* Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:
    -  Enable-AzStorageStaticWebsite
* Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi
* Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor
* Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur

## <a name="232---june-2019"></a>2.3.2 - Haziran 2019
#### <a name="azaccounts"></a>Az.Accounts
* İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983
* AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.
* 'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi

#### <a name="azdns"></a>Az.Dns
* 'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.

#### <a name="azeventgrid"></a>Az.EventGrid
* 2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.
* Yeni cmdlet’ler:
    - New-AzureRmEventGridDomain
        - Yeni bir Azure Event Grid etki alanı oluşturur.
    - Get-AzureRmEventGridDomain
        - Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.
    - Remove-AzureRmEventGridDomain
        - Bir Azure Event Grid Etki Alanını kaldırır.
    - New-AzureRmEventGridDomainKey
        - Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.
    - Get-AzureRmEventGridDomainKey
        - Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.
    - New-AzureRmEventGridDomainTopic:
        - Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.
    - Get-AzureRmEventGridDomainTopic
        - Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır
    - Remove-AzureRmEventGridDomainTopic:
        - Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.
* Cmdlet'ler güncelleştirildi:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.
        - Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.
        - Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.
        - Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
            - Olay aboneliği bitiş tarihi,
            - Gelişmiş filtreleme parametreleri.
        - Hedef olarak servicebusqueue için yeni sabit listesi ekler.
        - -IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.
    - Remove-AzureRmEventGridSubscription
        - Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.
        - Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler
* New-AzFrontDoorWafManagedRuleObject
    - Yeni otomatik tamamlama değerleri ekler

#### <a name="aznetwork"></a>Az.Network
* Sanal Ağ Geçidi Kaynağı için destek ekler
    - Yeni cmdlet’ler
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* AvailablePrivateEndpointType ekler
    - Yeni cmdlet’ler
        - Get-AzAvailablePrivateEndpointType
* PrivatePrivateLinkService ekler
    - Yeni cmdlet’ler
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* PrivateEndpoint ekler
    - Yeni cmdlet’ler
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı
    - New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.
    - Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.
* ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.
* ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.
* ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi
* AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi
* New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.
* NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi
* Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi
* ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi
* AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi
* Get-AzNetworkServiceTag cmdlet’i eklendi
* Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi
    - New-AzFirewall cmdlet'i güncelleştirildi:
        - Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi
        - Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi
        - Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder
        - Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName
* Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.
    - New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* ‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi

#### <a name="azresources"></a>Az.Resources
* Ek Şablon Dışarı Aktarma seçenekleri için destek
    - Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi
    - Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi
    - Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi

#### <a name="azservicefabric"></a>Az.ServiceFabric
* ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi

#### <a name="azsql"></a>Az.Sql
* Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi
* Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi
* Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek
    - New-AzStorageAccount
* Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir
* Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler

## <a name="220---june-2019"></a>2.2.0 - Haziran 2019
#### <a name="azcdn"></a>Az.Cdn
* Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.

#### <a name="azcompute"></a>Az.Compute
* İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.
    - Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* #9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi
* #9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi

#### <a name="aznetwork"></a>Az.Network
* Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi
    - ResourceId ve InputObject için diğer ad eklendi

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Get-AzPolicyEvent’de Boş referans sorunu düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* #9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi
* Service Fabric komut satırlarındaki eksik karakter düzeltildi

#### <a name="azsql"></a>Az.Sql
* Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.
* Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı
* Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı
* New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi

## <a name="210---may-2019"></a>2.1.0 - Mayıs 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu
    - **Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır
    - **New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur
    - **New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur
    - **New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.
    - **New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur
    - **Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır
    - **Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir
* ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu
    - **Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır
    - **New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur
    - **Remove-AzApiManagementCache** - Önbelleği kaldırır
    - **Update-AzApiManagementCache** - Önbelleği güncelleştirir
* API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu
    - **New-AzApiManagementSchema** - API için yeni Şema oluşturur
    - **Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır
    - **Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır
    - **Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir
* Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.
    - **New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./
* Ağ Durumunu almak için yeni cmdlet oluşturuldu
    - **Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır. ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.
* **New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi
    - Yeni 'Consumption' SKU'su için destek eklendi
    - 'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi
    - Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır. Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.
    - ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.
* **Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi
* Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]
* **Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi
* **Import-AzApiManagementApi** cmdlet'i güncelleştirildi
    - 'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için
    - Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.
    - Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.
* **Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi
* **Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi
* **New-AzApiManagementApi** cmdlet'i güncelleştirildi
    - API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.
    - 'ApiVersionSet' içinde API oluşturmak için
    - 'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.
    - Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.
* **Set-AzApiManagementApi** cmdlet'i güncelleştirildi
    - API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.
    - API'yi 'ApiVersionSet' olarak güncelleştirmek için
    - Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.
* **New-AzApiManagementRevision** cmdlet'i güncelleştirildi
    - 'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için. Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.
    - 'ApiRevisionDescription' sağlamak için
    - API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.
* **New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi
    - 'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için
    - 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için
* **New-AzApiManagementSubscription** cmdlet'i güncelleştirildi
    - 'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için
    - 'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için
    - Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.
* **Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi
    - 'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için
    - 'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için
    - Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.
* Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate'
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.
    - [https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi
    - [https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi
* Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.
    * [https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi
* Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi. Artık yalnızca eşleşen düğüm döndürülüyor.

#### <a name="azcompute"></a>Az.Compute
* Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.
* New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi

#### <a name="azmonitor"></a>Az.Monitor
* Yardım örneklerindeki yanlış parametre adları düzeltildi

#### <a name="aznetwork"></a>Az.Network
* Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi
    - Şu cmdlet güncelleştirildi:
        - Get-AzEffectiveRouteTable
* New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi

#### <a name="azresources"></a>Az.Resources
* Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi

#### <a name="azsql"></a>Az.Sql
* Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor

## <a name="200---may-2019"></a>2.0.0 - Mayıs 2019
#### <a name="azaccounts"></a>Az.Accounts
* Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.
* Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.

#### <a name="azcompute"></a>Az.Compute
* Yakınlık yerleştirme grubu özelliği.
    - Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.
* New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.
* SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi
* Yeni değişiklikler
    - Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.
    - Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü

#### <a name="azdns"></a>Az.Dns
* Otomatik DNS NameServer Temsilcisi
    - Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.
    - Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü
* WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* İki cmdlet kaldırıldı:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi
* Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:
    - Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.
    - hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.

#### <a name="azmonitor"></a>Az.Monitor
* SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi
    - Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Nat Gateway Resource için destek ekleyin
    - Yeni cmdlet’ler
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Cmdlet'ler güncelleştirildi
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.
    - New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* İlke değerlendirme ayrıntılarını sorgulama desteği.
    - Get-AzPolicyState komutuna '-Expand' parametresini ekleyin. '-Expand PolicyEvaluationDetails' öğesini destekleyin.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.
* Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.
* Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.
* Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.
* Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.
* Diğer küçük düzeltmeler.

#### <a name="azrelay"></a>Az.Relay
* Müşteriye dönük iletilerdeki yazım hatalarını düzeltin

#### <a name="azservicebus"></a>Az.ServiceBus
* Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi

#### <a name="azstorage"></a>Az.Storage
* Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)
* Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.
* Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir
    - New-AzStorageAccount
* 'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* 'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır
* Get-AzWebApp*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi

## <a name="180---april-2019"></a>1.8.0 - Nisan 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azaccounts"></a>Az.Accounts
* Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi

#### <a name="azbatch"></a>Az.Batch
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcdn"></a>Az.Cdn
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcompute"></a>Az.Compute
* Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azdatafactory"></a>Az.DataFactory
* Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azeventgrid"></a>Az.EventGrid
* Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.

#### <a name="azeventhub"></a>Az.EventHub
* Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi

#### <a name="azhdinsight"></a>Az.HDInsight
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="aziothub"></a>Az.IotHub
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azkeyvault"></a>Az.KeyVault
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azmedia"></a>Az.Media
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azmonitor"></a>Az.Monitor
  * GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Azure VM'de SQL için güncelleştirilmiş tablo biçimi
* AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi
* SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi

#### <a name="azrediscache"></a>Az.RedisCache
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azresources"></a>Az.Resources
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azsql"></a>Az.Sql
* İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Birden fazla sütun sınıflandırma işlemi geliştirildi.
* Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.
* Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.
* Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Web siteleri SDK'sı güncelleştirildi.
* PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.

## <a name="170---april-2019"></a>1.7.0 - Nisan 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma
* Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma

#### <a name="azautomation"></a>Az.Automation
* Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi. IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.
* Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi

#### <a name="azcompute"></a>Az.Compute
* New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi
* Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi
* Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.

#### <a name="azresources"></a>Az.Resources
* '-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi
* ‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi
    - İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856
* Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Veritabanı Verileri Sınıflandırması Desteği.

#### <a name="azstorage"></a>Az.Storage
* -UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama
    - New-AzStorageContext
* Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - Mart 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azautomation"></a>Az.Automation
* Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:
    * Dinamik gruplandırma
    * Ön-Son betik
    * Yeniden Başlatma Ayarı

#### <a name="azcompute"></a>Az.Compute
* Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü
* İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.

#### <a name="azkeyvault"></a>Az.KeyVault
* KeyVault cmdlet'lerine joker karakter desteği eklendi

#### <a name="aznetwork"></a>Az.Network
* Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi
* Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi
* Kapsayıcı kaydını kaldırmak için kanal desteği eklendi

#### <a name="azresources"></a>Az.Resources
* Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi
* ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* 'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi

## <a name="150---march-2019"></a>1.5.0 - Mart 2019
#### <a name="azaccounts"></a>Az.Accounts
* AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi
* Connect-AzAccount örnekleri güncelleştirildi

#### <a name="azautomation"></a>Az.Automation
* Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi
* Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi. Artık tüm düğümleri döndürür

#### <a name="azcdn"></a>Az.Cdn
* Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı

#### <a name="azcompute"></a>Az.Compute
* Get cmdlet’lerine joker karakter desteği eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 3.0.1'e güncelleştirildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme

#### <a name="aznetwork"></a>Az.Network
* Network cmdlet’lerine joker karakter desteği eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure VM desteğine SQL Server eklendi
* SDK Güncelleştirmesi
* Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı
* Get-ProtectableItem için Name ve ServerName parametreleri eklendi

#### <a name="azresources"></a>Az.Resources
* Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933
* `Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240
* `Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* AuditingEndpointsCommunicator güncelleştiriliyor.
    - Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 - Şubat 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* AddAzureASAccount cmdlet'i kullanım dışı bırakıldı

#### <a name="azautomation"></a>Az.Automation
* Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi
* Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi
* Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.

#### <a name="azcompute"></a>Az.Compute
* Kimlik parametresi kümeleriyle ilgili sorun düzeltildi
* Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi
* Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi
* Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi

#### <a name="azeventhub"></a>Az.EventHub
* EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi

#### <a name="azkeyvault"></a>Az.KeyVault
* Set-AzKeyVaultSecret’daki etiketleme düzeltildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Tümleştirme Hesapları için Temel SKU eklendi
* XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi
* Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Logic Apps SDK sürüm 4.1.0’a güncelleştirildi

#### <a name="azmonitor"></a>Az.Monitor
* Get-AzMetric için yardım güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.
    - Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.
    - Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.

#### <a name="azresources"></a>Az.Resources
* [https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi
* [https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi
* KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi

#### <a name="azsql"></a>Az.Sql
* SQL DB Hiper Ölçek katmanı için destek eklendi
* Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Get-AzWebAppSlotMetrics örneği düzeltildi

## <a name="130---february-2019"></a>1.3.0 - Şubat 2019
#### <a name="azaccounts"></a>Az.Accounts
* En son ClientRuntime sürümüne güncelleştirme

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Az.AnalysisServices modülü için genel kullanılabilirlik.

#### <a name="azcompute"></a>Az.Compute
* AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi
* Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi
* Update-AzImage için yardım açıklaması ve örnek güncelleştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Az.RecoveryServices modülü için genel kullanılabilirlik.

#### <a name="azresources"></a>Az.Resources
* Kaynak grupları için etiketleme düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166
* `Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi
* Get-AzSqlCapability'de null başvuru özel durumu düzeltildi

## <a name="121---january-2019"></a>1.2.1 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Kimlik Doğrulaması'nın doğru yayınını içeren sürümü

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm

## <a name="120---january-2019"></a>1.2.0 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi

#### <a name="azaks"></a>Az.Aks
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azautomation"></a>Az.Automation
* Python 2 runbook'ları için destek eklendi
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azcdn"></a>Az.Cdn
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azcompute"></a>Az.Compute
* Invoke-AzVMReimage cmdlet'i eklendi
* Set-AzVmss'ye TempDisk parametresi eklendi
* New-AzVM'nin uyarı iletisi düzeltildi

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 3.0.0'a güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* MSI kullanırken ADLS uç noktasındaki sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="aziothub"></a>Az.IotHub
* Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.

#### <a name="azkeyvault"></a>Az.KeyVault
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azresources"></a>Az.Resources
* 'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi
* Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi
* Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi
* Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi
* Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi
* 'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932
* Bazı hata iletileri düzeltildi.
* Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.
* Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.

#### <a name="azsignalr"></a>Az.SignalR
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi
* Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi
* Yönetilen örnekte özel harmanlama desteği

#### <a name="azstorage"></a>Az.Storage
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azwebsites"></a>Az.Websites
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.
* SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi

## <a name="110---january-2019"></a>1.1.0 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi

#### <a name="azcompute"></a>Az.Compute
* Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı
* Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.
    - getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi

#### <a name="azeventgrid"></a>Az.EventGrid
* 2019-01-01 API sürümünü kullanmak için güncelleştirildi.
* Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi
    - New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
        - Olay Yaşam Süresi,
        - Olaylar için teslim girişimleri sayısı üst sınırı,
        - Teslim edilemeyen ileti uç noktası.
    - Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
        - Olay Yaşam Süresi,
        - Olaylar için teslim girişimleri sayısı üst sınırı,
        - Teslim edilemeyen ileti uç noktası.
* New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.
* Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.

#### <a name="aziothub"></a>Az.IotHub
* IotHub SDK'sı en son sürümüne güncelleştirildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor

#### <a name="azresources"></a>Az.Resources
* 'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875
* New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi
* New-AzDeployment belgelerindeki yazım hatası düzeltildi
* 'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

#### <a name="azsql"></a>Az.Sql
* Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.

#### <a name="azstorage"></a>Az.Storage
* Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor
    - New-AzStorageContext
* Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* 'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

## <a name="100---december-2018"></a>1.0.0 - Aralık 2018
### <a name="general"></a>Genel

- Az Modülü Genel Kullanıma Sunuldu
- Her modül için çevrimiçi yardım
- Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)
- AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azaccounts"></a>Az.Accounts
- Önceki adı: Az.Profile
- Profil ve bağlam türleri için tablo biçimleri düzeltildi

### <a name="azapimanagement"></a>Az.ApiManagement
- #7002 düzeltmeleri
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azbatch"></a>Az.Batch
- `PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.
- `PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azbilling"></a>Az.Billing
- Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azcognitivservices"></a>Az.CognitivServices
- New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi
- Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- ManagedIdentity desteği eklendi

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azmonitor"></a>Az.Monitor
- Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azkeyvault"></a>Az.KeyVault
- Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı

### <a name="azmachinelearning"></a>Az.MachineLearning
- Az.MachineLearningCompute modülünden cmdlet’ler eklendi

### <a name="azmedia"></a>Az.Media
- New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı

### <a name="aznetwork"></a>Az.Network
Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi
    - Yeni cmdlet'ler eklendi:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.
    - Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azprofile"></a>Az.Profile
- Modül adı Az.Accounts olarak değiştirildi

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azresources"></a>Az.Resources
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Sertifikayı ortak ad ve parmak iziyle belirtme desteği
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azsignalr"></a>Az.SIgnalR
- SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu

### <a name="azsql"></a>Az.Sql
- Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi
- Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azstorage"></a>Az.Storage
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azwebsites"></a>Az.Websites
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

## <a name="070---december-2018"></a>0.7.0 - Aralık 2018

### <a name="general"></a>Genel

* Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler

### <a name="azcompute"></a>Az.Compute

* `New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi

### <a name="azfrontdoor"></a>Az.FrontDoor

* Bazı bozuk bağlantılar düzeltildi
    - New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.
    - New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.
* Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.

### <a name="azresources"></a>Az.Resources

* https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi
    - Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.

### <a name="azsql"></a>Az.Sql

* Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler
* Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi
* SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.

### <a name="azstorage"></a>Az.Storage

* New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi
* -DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi
    - Start-AzureStorageFileCopy
* Statik Web Sitesi yapılandırması için destek eklendi
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp ve Set-AzureRmWebAppSlot
    - Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi. Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.

## <a name="061---november-2018"></a>0.6.1 - Kasım 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azautomation"></a>Az.Automation
* Swagger tabanlı Azure Otomasyon cmdlet'leri
* Güncelleştirme Yönetimi cmdlet'leri eklendi
* Kaynak Denetimi cmdlet'leri eklendi
* Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi
* DSC Kayıt Düğümü komutu düzeltildi

### <a name="azcompute"></a>Az.Compute
* SystemAssigned kimliği için kimlik sorunu düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Market cmdlet'leri için örnekler açıklaması güncelleştirildi

### <a name="aznetwork"></a>Az.Network
* New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi
* Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi
* Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.
* VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.
* İlke saat dilimi büyük harfe dönüştürüldü.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azrelay"></a>Az.Relay
* Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.

### <a name="azresources"></a>Az.Resources
* `New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi
* New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi
* NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi

### <a name="azsql"></a>Az.Sql
* Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.
    - Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.
    - Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi

## <a name="050---november-2018"></a>0.5.0 - Kasım 2018
#### <a name="general"></a>Genel
* Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır

#### <a name="azprofile"></a>Az.Profile
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi
* Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi
* Connect-AzAccount için TenantId açıklaması güncelleştirildi
* Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6936
* Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7453
* MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7462
* Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Get-AzCognitiveServicesAccountSkus işlemi eklendi.

#### <a name="azcompute"></a>Az.Compute
* Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi
* Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor
* SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* DataLake paketi 1.1.10'a güncelleştirildi.
* Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.

#### <a name="azinsights"></a>Az.Insights
* 7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi
    - Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).
* Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi
    - Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor

#### <a name="aznetwork"></a>Az.Network
* Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* İlke düzeltme cmdlet'leri eklendi

#### <a name="azresources"></a>Az.Resources
* https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi
    - 'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı

#### <a name="azservicebus"></a>Az.ServiceBus
* PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Linux Vmss'ye sertifika ekleme sorunu düzeltildi.
* 'Add-AzServiceFabricClusterCertificate' düzeltildi
    - Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).
    - Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).
* 'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.

## <a name="040---october-2018"></a>0.4.0 - Ekim 2018
#### <a name="azprofile"></a>Az.Profile
* CloudShell’de Get-AzSubscription sorunu çözüldü
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azcompute"></a>Az.Compute
* 'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Sanal Ağ Kuralları desteği ekleme
    - Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.
    - Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.
    - Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.

#### <a name="aznetwork"></a>Az.Network
* Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azresources"></a>Az.Resources
* Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi. Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.

## <a name="030---october-2018"></a>0.3.0 - Ekim 2018
#### <a name="azurestorage"></a>Azure Depolama
* Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.
    - Get-AzStorageUsage

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.

#### <a name="azcompute"></a>Az.Compute
* Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi
* New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.
* Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.

#### <a name="aznetwork"></a>Az.Network
* NetworkProfile işlevselliği eklendi. yeni cmdlet'ler eklendi
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Alt Ağ Modeline hizmet ilişki bağlantısı eklendi
* New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi
* Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi

#### <a name="azrediscache"></a>Az.RedisCache
* Bundan sonra Size parametresi olarak her dizeye izin veriliyor. PSArgumentCompleter açılan listesine P5 eklendi

#### <a name="azresources"></a>Az.Resources
* Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi
* Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi

#### <a name="azsql"></a>Az.Sql
* Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor
* Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor

## <a name="020---september-2018"></a>0.2.0 - Eylül 2018
 İlk Yayın
