---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b37d25f8efb6c0a5e590617a5ba84a5a5bf18660
ms.sourcegitcommit: ec731e58b7de3eb14df6d3bf308df92154125bbb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2020
ms.locfileid: "95005832"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="bdbd4-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="bdbd4-103">Azure PowerShell release notes</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="bdbd4-104">5.1.0 - Kasım 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-104">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-105">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-106">'Connect-AzAccount -DeviceCode' kullanılıyorsa TenantId ile uyum sağlanamamasına neden olan bir sorun düzeltildi [#13477]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-106">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="bdbd4-107">Yeni 'Get-AzAccessToken' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-107">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="bdbd4-108">Kullanıcı profili yoluna erişilemiyorsa hataya neden olan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-108">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="bdbd4-109">Connect-AzAccount komutu sırasında Write-Object hatasına neden olan bir sorun düzeltildi [#13419]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-109">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="bdbd4-110">Şu cmdlet’lere 'ContainerRegistryEndpointSuffix' parametresi eklendi: 'Add-AzEnvironment', 'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-110">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="bdbd4-111"><kbd>CTRL</kbd>+<kbd>C</kbd> tuşlarına basıldığında oturum açma işleminin kesilmesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-111">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="bdbd4-112">'Connect-AzAccount -KeyVaultAccessToken' komutunun çalışmamasına neden olan bir sorun düzeltildi [#13127]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-112">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="bdbd4-113">'Invoke-AzRestMethod' komutundaki büyük/küçük harfe duyarlı olmayan boş referans ve yöntem düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-113">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-114">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-114">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-115">Kullanıcının, yeni bir Kubernetes kümesi oluşturmak için hizmet sorumlusunu kullanamamasına neden olan bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-115">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="bdbd4-116">[#13012]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-116">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="bdbd4-117">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-117">Az.AppConfiguration</span></span>
* <span data-ttu-id="bdbd4-118">'Az.AppConfiguration' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-118">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-119">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-119">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-120">'New-AzDataFactoryV2LinkedServiceEncryptedCredential' komutunun hata iletisi iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-120">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-121">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-121">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-122">ADLS veri düzlemi SDK’sı 1.2.4-alpha sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-122">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="bdbd4-123">Değişiklikler: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="bdbd4-123">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="bdbd4-124">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="bdbd4-124">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="bdbd4-125">Yeni MSIX Paketi cmdlet’leri eklendi ve Applications cmdlet’leri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-125">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-126">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-126">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-127">EventHub kümesine yönelik etiketi olmayan Küme komutları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-127">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="bdbd4-128">AzEventHubGeoDRConfiguration komutlarındaki PartnerNamespace için yardım metni güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-128">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-129">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-129">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-130">Giden geçişi ve özel bağlantı özelliğini desteklemek için 'New-AzHDInsightCluster' cmdlet’ine 'ResourceProviderConnection' ve 'PrivateLink' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-130">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="bdbd4-131">Özel Ambari veritabanı özelliğini desteklemek için 'New-AzHDInsightCluster' cmdlet’ine 'AmbariDatabase' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-131">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="bdbd4-132">'Add-AzHDInsightMetastore' cmdlet’inin 'MetastoreType' parametresine 'AmbariDatabase' kabul değeri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-132">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-133">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-133">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-134">IoT Hub’ı oluşturma cmdlet’inde etiketlere izin verildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-134">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-135">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-136">Anahtar kasası etiketini güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-136">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bdbd4-137">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdbd4-137">Az.LogicApp</span></span>
* <span data-ttu-id="bdbd4-138">Get-AzLogicAppRunHistory’nin sonuçların yalnızca ilk sayfasını getirmesine neden olan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-138">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-139">Az.Network</span></span>
* <span data-ttu-id="bdbd4-140">Aşağıdaki cmdlet güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-140">Updated below cmdlet</span></span> 
    - <span data-ttu-id="bdbd4-141">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-141">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="bdbd4-142">PublicIpAddressPrefix özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-142">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="bdbd4-143">PublicIpAddressPrefixId özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-143">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="bdbd4-144">Genel yük dengelemeye olanak vermek için aşağıdaki cmdlet’lere yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-144">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="bdbd4-145">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-145">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="bdbd4-146">SKU Tier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-146">Added Sku Tier property</span></span>
    - <span data-ttu-id="bdbd4-147">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-147">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="bdbd4-148">SKU Tier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-148">Added Sku Tier property</span></span>
    - <span data-ttu-id="bdbd4-149">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-149">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="bdbd4-150">SKU Tier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-150">Added Sku Tier property</span></span>
    - <span data-ttu-id="bdbd4-151">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-151">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="bdbd4-152">LoadBalancerFrontendIPConfigurationId özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-152">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="bdbd4-153">Şu cmdlet’ler için kullanımdan kaldırma planlamasına yönelik uyarılar güncelleştirildi:   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-153">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="bdbd4-154">Şu cmdlet’ler için 'RouteTable' bağımsız değişkeninin kullanımdan kaldırma planlamasına yönelik uyarılar eklendi:   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-154">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="bdbd4-155">'-MinScaleUnits' ve '-MaxScaleUnits' bağımsız değişkenleri, 'Set-AzExpressRouteGateway' içinde isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-155">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="bdbd4-156">Application Gateway’de Karşılıklı Kimlik Doğrulama ve SSL Profilleri’ni desteklemek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-156">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="bdbd4-157">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-157">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-158">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-158">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-159">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-159">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-160">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-160">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-161">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-161">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="bdbd4-162">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-162">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="bdbd4-163">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-163">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="bdbd4-164">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-164">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="bdbd4-165">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-165">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="bdbd4-166">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-166">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="bdbd4-167">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-167">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="bdbd4-168">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-168">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="bdbd4-169">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-169">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="bdbd4-170">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-170">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="bdbd4-171">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-171">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="bdbd4-172">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-172">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="bdbd4-173">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-173">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-174">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-174">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-175">İlke BackupTime değeri UTC olarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-175">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="bdbd4-176">Get-AzRecoveryServicesBackupJobDetails cmdlet’inde hataya neden olan değişiklik uyarısı değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-176">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="bdbd4-177">Set-AzRecoveryServicesBackupProtectionPolicy cmdlet’i için örnek betik yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-177">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-178">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-179">Etki değerlendirmesinin farklı büyük/küçük harf düzenlerine sahip iki kaynak grubu kapsamı göstermesine neden olan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-179">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="bdbd4-180">'Export-AzResourceGroup' SDK’yı kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-180">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="bdbd4-181">Ayrıştırma yöntemlerine kültür bilgileri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-181">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-182">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-183">Set-AzSqlDatabaseAudit’in Hiper Ölçek veritabanında desteklenmemesine ve veritabanı sürümünün belirlenememesine neden olan sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-183">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="bdbd4-184">'New-AzSqlInstance' ve 'Set-AzSqlInstance' için MaintenanceConfigurationId eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-184">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="bdbd4-185">GetAzureSqlDatabaseReplicationLink.cs içinde PartnerServerName parametresinin anahtar yerine değere göre denetlenmesine neden olan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-185">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-186">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-187">Yeni erişim kısıtlama özellikleri için destek eklendi: ServiceTag, multi-ip ve http-headers</span><span class="sxs-lookup"><span data-stu-id="bdbd4-187">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="bdbd4-188">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="bdbd4-188">Thanks to our community contributors</span></span>
* <span data-ttu-id="bdbd4-189">John Q. Martin (@johnmart82), Güvenlik duvarı önkoşul bilgilerinin eklenmesi (#13385)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-189">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="bdbd4-190">Manikandan Duraisamy (@madurais-msft), PublicSubnetName bağımsız değişkeninin düzeltilmesi (#13417)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-190">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="bdbd4-191">@mahortas, -HostNames parametre değerlerine yönelik güncelleştirme (#13349)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-191">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="bdbd4-192">@MariachiForHire, desteklenen TrafficAnalyticsInterval değerlerinin eklenmesi (#13304)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-192">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="bdbd4-193">Michael James (@mikejwhat), Get-AzLogicAppRunHistory komutunun 30’dan fazla giriş döndürmesinin sağlanması (#13393)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-193">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="bdbd4-194">Shashikant Shakya (@shshakya), Restore-AzSqlInstanceDatabase.md güncelleştirmesi (#13404)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-194">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="bdbd4-195">5.0.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-195">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-196">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-196">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-197">[Yeni Değişiklik] 'Get-AzProfile' ve 'Select-AzProfile' kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-197">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="bdbd4-198">Azure Directory Authentication Library, Microsoft Authentication Library (MSAL) ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-198">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-199">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-199">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-200">[Yeni Değişiklik] 'New-AzAksCluster' ve 'Set-AzAksCluster' cmdlet’indeki 'ClientIdAndSecret' parametre diğer adı kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-200">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="bdbd4-201">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NodeVmSetType' parametresinin 'AvailabilitySet' varsayılan değeri 'VirtualMachineScaleSets' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-201">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="bdbd4-202">[Yeni Değişiklik] 'New-AzAksCluster' cmdlet’indeki 'NetworkPlugin' parametresinin 'None' varsayılan değeri 'azure' olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-202">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="bdbd4-203">[Yeni Değişiklik] Linux’ta yalnızca bir değeri desteklediğinden 'New-AzAksCluster' cmdlet’indeki 'NodeOsType' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-203">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="bdbd4-204">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bdbd4-204">Az.Billing</span></span>
* <span data-ttu-id="bdbd4-205">'Get-AzBillingAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-205">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="bdbd4-206">'Get-AzBillingProfile' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-206">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="bdbd4-207">'Get-AzInvoiceSection' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-207">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="bdbd4-208">'Get-AzBillingInvoice' cmdlet’ine yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-208">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="bdbd4-209">Get-AzBillingInvoice cmdlet’inin yanıtından DownloadUrlExpiry, Type ve BillingPeriodNames özellikleri kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-209">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-210">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-211">Çoklu kaynak ve özel bağlantı işlevini destekleyecek cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-211">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-213">SDK sürümü 7.4.0-preview olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-213">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-214">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-214">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-215">'New-AzVm' cmdlet’ine '-VmssId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-215">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="bdbd4-216">'New-AzVmss' cmdlet’ine 'PlatformFaultDomainCount' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-216">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-217">Yeni 'Get-AzDiskEncryptionSetAssociatedResource' cmdlet’i</span><span class="sxs-lookup"><span data-stu-id="bdbd4-217">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="bdbd4-218">New-AzDiskConfig cmdlet’ine isteğe bağlı 'Tier' ve 'LogicalSectorSize' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-218">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="bdbd4-219">'New-AzDiskUpdateConfig' cmdlet’ine 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' ve 'DiskMBpsReadOnly' eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-219">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="bdbd4-220">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bdbd4-220">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bdbd4-221">[Yeni Değişiklik] API sürümü 2019-05-01 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-221">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="bdbd4-222">[Yeni Değişiklik] 'New-AzContainerRegistry' cmdlet’inden 'Classic' SKU’su ve 'StorageAccountName' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-222">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="bdbd4-223">Yeni cmdlet’ler eklendi: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-223">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="bdbd4-224">'Update-AzContainerRegistry' cmdlet’ine yeni 'NetworkRuleSet' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-224">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="bdbd4-225">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-225">Az.Databricks</span></span>
* <span data-ttu-id="bdbd4-226">`-EncryptionKeyVersion` başarısız olmadan Databricks çalışma alanını güncelleştirmeye neden olabilecek bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-226">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-227">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-228">ADF .NET SDK’sı 4.12.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-228">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="bdbd4-229">ADF şifrelemesi istemci SDK’sı 4.14.7587.7 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-229">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="bdbd4-230">'Stop-AzDataFactoryV2TriggerRun' ve 'Invoke-AzDataFactoryV2TriggerRun' komutları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-230">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="bdbd4-231">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="bdbd4-231">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="bdbd4-232">Üst düzey ARM nesneleri oluşturmak için Location özelliği gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-232">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="bdbd4-233">\* `New-AzWvdApplicationGroup` için `ApplicationGroupType` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-233">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="bdbd4-234">\* `New-AzWvdApplicationGroup` için `HostPoolArmPath` gerekli kılındı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-234">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="bdbd4-235">\* `New-AzWvdHostPool` cmdlet’ine `PreferredAppGroupType` eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-235">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="bdbd4-236">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bdbd4-236">Az.Functions</span></span>
* <span data-ttu-id="bdbd4-237">[Yeni Değişiklik] 'IncludeSlot' anahtar parametresi, 'Get-AzFunctionApp' cmdlet’inin parametre kümelerinden biri hariç tümünden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-237">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="bdbd4-238">Cmdlet, şimdi '-IncludeSlot' belirtildiğinde sonuçlarda dağıtım yuvalarının alınmasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-238">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="bdbd4-239">'New-AzFunctionApp' güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-239">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="bdbd4-240">-DisableApplicationInsights, bu seçenek belirtildiğinde hiçbir Application Insights projesi oluşturulmayacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-240">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="bdbd4-241">[#12728]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-241">[#12728]</span></span>
  - <span data-ttu-id="bdbd4-242">[Yeni Değişiklik] PowerShell 6.2 işlev uygulamaları oluşturma desteği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-242">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="bdbd4-243">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, PowerShell işlev uygulamaları için Windows üzerinde İşlevler sürüm 3’teki varsayılan çalışma zamanı 6.2 sürümünden 7.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-243">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="bdbd4-244">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Node işlev uygulamaları için Windows ve Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 10 sürümünden 12 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-244">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="bdbd4-245">[Yeni Değişiklik] RuntimeVersion parametresi belirtilmediğinde, Python işlev uygulamaları için Linux üzerinde sürüm 3’teki varsayılan çalışma zamanı 3.7 sürümünden 3.8 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-245">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-246">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-246">Az.HDInsight</span></span>
 * <span data-ttu-id="bdbd4-247">New-AzHDInsightCluster cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-247">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="bdbd4-248">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-248">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="bdbd4-249">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-249">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="bdbd4-250">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-250">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="bdbd4-251">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-251">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="bdbd4-252">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-252">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="bdbd4-253">Yeni parametreler eklendi: ADLS 2. Nesil’i desteklemek üzere 'StorageFileSystem' ve 'StorageAccountManagedIdentity' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-253">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="bdbd4-254">HDInsight Kimlik Aracısını desteklemek üzere yeni 'EnableIDBroker' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-254">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="bdbd4-255">Yeni parametreler eklendi: Kafka REST Proxy’yi desteklemek üzere 'KafkaClientGroupId', 'KafkaClientGroupName' ve 'KafkaManagementNodeSize' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-255">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="bdbd4-256">New-AzHDInsightClusterConfig cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-256">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="bdbd4-257">'DefaultStorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-257">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="bdbd4-258">'DefaultStorageAccountKey' parametresi 'StorageAccountKey' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-258">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="bdbd4-259">'DefaultStorageAccountType' parametresi 'StorageAccountType' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-259">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="bdbd4-260">'PublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-260">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="bdbd4-261">'OutboundPublicNetworkAccessType' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-261">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="bdbd4-262">Set-AzHDInsightDefaultStorage cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-262">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="bdbd4-263">'StorageAccountName' parametresi 'StorageAccountResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-263">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="bdbd4-264">Add-AzHDInsightSecurityProfile cmdlet’inde:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-264">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="bdbd4-265">'Domain' parametresi 'DomainResourceId' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-265">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="bdbd4-266">'OrganizationalUnitDN' parametresi için zorunlu gereksinim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-266">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-267">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-267">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-268">[Yeni Değişiklik] 'New-AzKeyVault' cmdlet’indeki DisableSoftDelete ve 'Update-AzKeyVault' cmdlet’indeki EnableSoftDelete parametreleri kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-268">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="bdbd4-269">[Yeni Değişiklik] Doğrudan SecretValue değerinin görüntülenmesini önlemek amacıyla SecretValueText özniteliği kaldırıldı [#12266]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-269">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="bdbd4-270">Şu yeni kaynak türü için destek eklendi: yönetilen HSM</span><span class="sxs-lookup"><span data-stu-id="bdbd4-270">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="bdbd4-271">Yönetilen HSM’deki anahtarları çalıştırmaya yönelik, yönetilen HSM ve cmdlet’lerin CRUD’si</span><span class="sxs-lookup"><span data-stu-id="bdbd4-271">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="bdbd4-272">Tam HSM yedeklemesi/geri yüklemesi, AES anahtarı oluşturma, güvenlik etki alanı yedeklemesi/geri yüklemesi, RBAC</span><span class="sxs-lookup"><span data-stu-id="bdbd4-272">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bdbd4-273">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-273">Az.ManagedServices</span></span>
* <span data-ttu-id="bdbd4-274">[Yeni Değişiklik] Parametrelerin adlandırma kuralları ve ilişkili örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-274">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-275">Az.Network</span></span>
* <span data-ttu-id="bdbd4-276">[Yeni Değişiklik] 'HostedSubnet' parametresi kaldırıldı ve yerine 'Subnet' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-276">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="bdbd4-277">Sanal Yönlendirici Eş Düğüm Yolları için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-277">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="bdbd4-278">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-278">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="bdbd4-279">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-279">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="bdbd4-280">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-280">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="bdbd4-281">'-SkuTier' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-281">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="bdbd4-282">'-SkuName' parametresi eklendi ve bu parametreye yönelik SKU, Diğer Ad haline getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-282">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="bdbd4-283">'-Sku' parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-283">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="bdbd4-284">[Yeni Değişiklik] 'Start-AzVpnConnectionPacketCapture' ve 'Stop-AzVpnConnectionPacketCapture' cmdlet’lerinde 'Connectionlink' bağımsız değişkeni zorunlu kılındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-284">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="bdbd4-285">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndPointObject', '-Filter' parametresi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-285">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="bdbd4-286">[Yeni Değişiklik] 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet’i 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject' ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-286">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="bdbd4-287">'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet’i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-287">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="bdbd4-288">'-Type' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-288">Added parameter '-Type'</span></span>
    - <span data-ttu-id="bdbd4-289">'-CoverageLevel' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-289">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="bdbd4-290">'-Scope' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-290">Added parameter '-Scope'</span></span>
* <span data-ttu-id="bdbd4-291">'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet’i yeni '-DestinationPortBehavior' parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-291">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-292">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-292">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-293">Katkıda bulunan izinleri için İş Yükü Geri Yüklemesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-293">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="bdbd4-294">Restore-AzRecoveryServicesBackupItem cmdlet’ine yeni parametre kümeleri ve doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-294">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-295">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-296">Ayrıştırma hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-296">Fixed parsing bug</span></span>
* <span data-ttu-id="bdbd4-297">ARM şablonu What-If cmdlet’leri, sonuçlardan önizleme iletisi kaldırılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-297">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="bdbd4-298">'-WhatIf' cmdlet’i daha yüksek bir kapsama ayarlandığında, şablon dağıtım cmdlet’lerinin kilitlenmesiyle ilgili bir sorun düzeltildi [#13038]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-298">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="bdbd4-299">Şablon dağıtım cmdlet’lerinin şablon parametrelerindeki büyük/küçük harfi korumamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-299">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="bdbd4-300">'Export-AzResourceGroup' cmdlet’inde kullanılmak üzere varsayılan API sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-300">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="bdbd4-301">Şablon Belirtimlerine yönelik cmdlet’ler ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec') eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-301">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="bdbd4-302">Mevcut dağıtım cmdlet’lerini kullanarak (yeni -TemplateSpecId parametresi aracılığıyla) Şablon Belirtimlerini dağıtma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-302">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="bdbd4-303">'Get-AzResourceGroupDeploymentOperation', SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-303">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="bdbd4-304">'\*-AzDeployment' cmdlet’lerinden '-ApiVersion' parametresi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-304">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-305">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-306">networkIsolation belirtilmediğinde New-AzSqlDatabaseExport cmdlet’inin başarısız olmasıyla ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-306">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="bdbd4-307">New-AzSqlDatabaseExport ve New-AzSqlDatabaseImport cmdlet’lerinin sonuç nesnesinde OperationStatusLink parametresini döndürmemesiyle ilgili sorun düzeltildi [#13097]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-307">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="bdbd4-308">Yedekleme Alanı Yedeklilik Uyarıları’ndaki Azure Eşlenmiş Bölgeler URL’si Güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-308">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-309">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-310">Eski RestorePolicy.LastEnabledTime özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-310">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="bdbd4-311">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-311">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-312">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-312">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-313">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-313">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="bdbd4-314">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-314">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="bdbd4-315">DaysAfterModificationGreaterThan parametresinin türü int yerine int? olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-315">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="bdbd4-316">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-316">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="bdbd4-317">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-317">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="bdbd4-318">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-318">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="bdbd4-319">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-319">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="bdbd4-320">Erişim katmanına sahip dosya paylaşımı oluşturma/güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-320">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="bdbd4-321">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-321">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="bdbd4-322">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-322">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="bdbd4-323">Data Lake 2. Nesil’deki ACL’yi özyinelemeli olarak ayarlama/güncelleştirme/kaldırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-323">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="bdbd4-324">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-324">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="bdbd4-325">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-325">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="bdbd4-326">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-326">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="bdbd4-327">Yeni x,t iznine sahip Kapsayıcı erişim ilkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-327">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="bdbd4-328">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-328">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="bdbd4-329">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-329">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="bdbd4-330">Permission alt özelliğinin türü enum’dan String’e değiştirilerek Kapsayıcı erişim ilkesi cmdlet’ini alma/ayarlama işleminin çıkışı değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-330">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="bdbd4-331">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-331">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="bdbd4-332">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-332">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="bdbd4-333">JSON ile yönetim ilkesi ayarlamayla ilgili örnek betik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-333">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="bdbd4-334">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-334">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-335">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-336">Premium V3 fiyatlandırma katmanı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-336">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="bdbd4-337">WebSites SDK 3.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-337">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="bdbd4-338">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="bdbd4-338">Thanks to our community contributors</span></span>
* <span data-ttu-id="bdbd4-339">@atul-ram, Get-AzDelegation.md güncelleştirildi (#13176)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-339">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="bdbd4-340">@dineshreddy007, Stack HCI kaydının WAC belirtecini kullanması durumunda doğru atanan Uygulama Rolleri alınıyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-340">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="bdbd4-341">(#13249)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-341">(#13249)</span></span>
* <span data-ttu-id="bdbd4-342">@kongou-ae, New-AzOffice365PolicyProperty.md güncelleştirildi (#13217)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-342">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="bdbd4-343">Lohith Chowdary Chilukuri (@Lochiluk), Set-AzApplicationGateway.md güncelleştirildi (#13150)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-343">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="bdbd4-344">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-344">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="bdbd4-345">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13203)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-345">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="bdbd4-346">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13190)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-346">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="bdbd4-347">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13189)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-347">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="bdbd4-348">Başvurulan cmdlet’lere bağlantılar eklendi (#13137)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-348">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="bdbd4-349">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13204)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-349">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="bdbd4-350">Belgede başvurulan PowerShell cmdlet’lerine bağlantılar eklendi (#13205)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-350">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="bdbd4-351">4.8.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-351">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-352">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-353">Ortak kitaplıklardaki DateTime ayrıştırma sorunu düzeltildi [#13045]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-353">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-354">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-354">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-355">'New-AzCognitiveServicesAccountApiProperty' cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-355">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-356">'New-AzCognitiveServicesAccount' ve 'Set-AzCognitiveServicesAccount' için 'ApiProperty' parametresi destekleniyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-356">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-357">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-358">'Update-ASRRecoveryPlan' cmdlet'indeki sorun Yük Devretme Türleri doldurularak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-358">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="bdbd4-359">'Get-AzVmImage' cmdlet'ine isteğe bağlı '-Top' ve '-OrderBy' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-359">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="bdbd4-360">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-360">Az.Databricks</span></span>
* <span data-ttu-id="bdbd4-361">'Az.Databricks' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-361">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="bdbd4-362">Sanal ağ eşlemesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-362">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-363">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-364">Çıkış iletilerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-364">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-365">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-365">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-366">'Set-AzEventHubNetworkRuleSet' cmdlet'ine isteğe bağlı 'TrustedServiceAccessEnabled' anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-366">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-367">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-367">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-368">'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametrelerini kullanımdan kaldırma planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-368">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="bdbd4-369">'DefaultStorageAccountName' parametresini 'StorageAccountResourceId' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-369">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="bdbd4-370">'DefaultStorageAccountKey' parametresini 'StorageAccountKey' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-370">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="bdbd4-371">'DefaultStorageAccountType' parametresini 'StorageAccountType' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-371">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="bdbd4-372">'DefaultStorageContainer' parametresini 'StorageContainer' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-372">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="bdbd4-373">'DefaultStorageRootPath' parametresini 'StorageRootPath' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-373">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-374">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-374">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-375">Cihazların sdk'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-375">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-376">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-376">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-377">SecretValueText özelliğinin kaldırılacağı ayrıntılı tarih sağlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-377">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bdbd4-378">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-378">Az.ManagedServices</span></span>
* <span data-ttu-id="bdbd4-379">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-379">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-380">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-380">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-381">Uyarı iletisinin gizlenememesi hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-381">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="bdbd4-382">[#12889]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-382">[#12889]</span></span>
* <span data-ttu-id="bdbd4-383">Uyarı kuralı ölçütlerinde 'SkipMetricValidation' parametresi destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-383">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="bdbd4-384">Ölçüm doğrulamasının atlanmasına neden olarak henüz yayılmamış özel bir ölçümle ilgili uyarı kuralı oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-384">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-385">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-385">Az.Network</span></span>
* <span data-ttu-id="bdbd4-386">VPNSite Kaynağına Office365 İlkesi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-386">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="bdbd4-387">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-387">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-388">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-389">İş yükü yedeklemesi için kapsayıcı adı doğrulaması eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-389">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bdbd4-390">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdbd4-390">Az.RedisCache</span></span>
* <span data-ttu-id="bdbd4-391">Microsoft.Cache RP kaydıyla ilgili izin sorunundan dolayı 'New-AzRedisCache' ve 'Set-AzRedisCache' cmdlet'lerinin başarısız olmaması sağlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-391">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-392">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-392">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-393">Aşağıdakilere BackupStorageRedundancy eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-393">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="bdbd4-394">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-394">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="bdbd4-395">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-395">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="bdbd4-396">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-396">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="bdbd4-397">Tüm SQL DB başvurularında BackupStorageRedundancy parametresi için büyük/küçük harf duyarlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-397">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="bdbd4-398">BackupStorageRedundancy uyarı iletisi adları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-398">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-399">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-399">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-400">Depolama hesabının dosya hizmetinde paylaşımı etkinleştirme/devre dışı bırakma/alma geçici silme özellikleri destekleniyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-400">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="bdbd4-401">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-401">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="bdbd4-402">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-402">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="bdbd4-403">Desteklenen liste dosya paylaşımları Depolama hesabının silinmiş olan dosyalarını içeriyor ve Tek dosya paylaşımı kullanımı alınıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-403">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="bdbd4-404">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-404">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="bdbd4-405">Silinmiş dosya paylaşımını geri yükleme destekleniyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-405">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="bdbd4-406">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-406">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="bdbd4-407">Blob hizmeti özelliklerini değiştirmeye yönelik cmdlet'ler değiştirildi. Sunucudan ilk özellikler alınmayacak, yalnızca değiştirilen özellikler sunucuya ayarlanacak.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-407">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="bdbd4-408">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-408">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="bdbd4-409">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-409">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="bdbd4-410">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-410">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-411">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-411">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-412">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-412">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="bdbd4-413">New-AzStorageAccount parametresi -Kind varsayılan değeri için yardım sorunu düzeltildi [#12189]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-413">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="bdbd4-414">Blob karşıya yüklemesinde doğru ContentType ayarlama işlemini göstermek için örnek eklenerek sorun düzeltildi [#12989]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-414">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="bdbd4-415">4.7.0 - Eylül 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-415">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-416">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-417">Yaklaşan yeni değişiklik iletileri biçimlendirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-417">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="bdbd4-418">Azure.Core 1.4.1 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-418">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-419">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-419">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-420">'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-420">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="bdbd4-421">[#12372]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-421">[#12372]</span></span>
* <span data-ttu-id="bdbd4-422">'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-422">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="bdbd4-423">[#11239]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-423">[#11239]</span></span>
* <span data-ttu-id="bdbd4-424">Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-424">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="bdbd4-425">[#11239]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-425">[#11239]</span></span>
* <span data-ttu-id="bdbd4-426">'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-426">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="bdbd4-427">[#12371]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-427">[#12371]</span></span>
* <span data-ttu-id="bdbd4-428">API sürümü 2020-06-01 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-428">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-429">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-430">Belirli API’ler için ek yasal koşullar gösterildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-430">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-431">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-432">'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-432">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="bdbd4-433">Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-433">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="bdbd4-434">'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-434">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="bdbd4-435">'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-435">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="bdbd4-436">VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-436">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="bdbd4-437">'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-437">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="bdbd4-438">'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-438">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="bdbd4-439">Alan, sanal makine örneğinin kaynak kimliğini gösterir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-439">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="bdbd4-440">'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-440">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="bdbd4-441">'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-441">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-442">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-443">ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-443">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-444">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-445">Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-445">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="bdbd4-446">#10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-446">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="bdbd4-447">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bdbd4-447">Az.Functions</span></span>
* <span data-ttu-id="bdbd4-448">Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-448">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="bdbd4-449">PowerShell 6.2 sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-449">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="bdbd4-450">Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-450">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-451">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-451">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-452">Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-452">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="bdbd4-453">'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-453">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="bdbd4-454">Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-454">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="bdbd4-455">Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-455">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-456">Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-456">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-457">Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-457">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-458">Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-458">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-459">Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-459">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-460">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-460">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-461">RBAC yetkilendirmesi desteği eklendi [#10557]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-461">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="bdbd4-462">'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-462">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="bdbd4-463">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="bdbd4-463">Az.Kusto</span></span>
* <span data-ttu-id="bdbd4-464">'Az.Kusto' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-464">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-465">Az.Network</span></span>
* <span data-ttu-id="bdbd4-466">[Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-466">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="bdbd4-467">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-467">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="bdbd4-468">IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-468">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="bdbd4-469">-HostedGateway ve -HostedGatewayId parametreleri silindi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-469">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="bdbd4-470">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="bdbd4-470">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="bdbd4-471">Abonelik düzeyi parametre kümesi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-471">Added subscription level parameter set</span></span>
    - <span data-ttu-id="bdbd4-472">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-472">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="bdbd4-473">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-473">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="bdbd4-474">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-474">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="bdbd4-475">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-475">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="bdbd4-476">Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-476">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="bdbd4-477">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-477">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="bdbd4-478">VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-478">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="bdbd4-479">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-479">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="bdbd4-480">'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-480">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="bdbd4-481">'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-481">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="bdbd4-482">'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-482">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="bdbd4-483">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-483">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="bdbd4-484">'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-484">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="bdbd4-485">'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-485">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="bdbd4-486">Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-486">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="bdbd4-487">Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-487">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="bdbd4-488">'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-488">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="bdbd4-489">Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-489">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-491">İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-491">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-492">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-493">Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-493">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="bdbd4-494">'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-494">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="bdbd4-495">ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterilecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-495">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="bdbd4-496">Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-496">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-497">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-498">Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-498">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="bdbd4-499">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-499">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="bdbd4-500">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-500">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="bdbd4-501">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-501">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="bdbd4-502">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-502">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="bdbd4-503">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-503">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="bdbd4-504">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-504">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="bdbd4-505">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-505">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="bdbd4-506">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-506">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="bdbd4-507">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-507">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="bdbd4-508">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-508">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="bdbd4-509">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-509">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="bdbd4-510">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-510">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="bdbd4-511">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-511">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="bdbd4-512">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-512">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="bdbd4-513">Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-513">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-514">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-514">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-515">'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-515">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="bdbd4-516">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-516">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-517">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-517">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-518">'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-518">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="bdbd4-519">Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-519">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="bdbd4-520">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-520">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="bdbd4-521">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-521">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="bdbd4-522">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-522">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="bdbd4-523">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-523">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="bdbd4-524">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-524">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-525">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-525">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-526">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-526">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-527">Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-527">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="bdbd4-528">'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-528">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="bdbd4-529">Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-529">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="bdbd4-530">'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-530">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="bdbd4-531">'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-531">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="bdbd4-532">Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-532">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-533">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-533">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-534">Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-534">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="bdbd4-535">Belirli Bir Noktaya Geri Yükleme Desteği Eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-535">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="bdbd4-536">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-536">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-537">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-537">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="bdbd4-538">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-538">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="bdbd4-539">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-539">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="bdbd4-540">get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-540">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="bdbd4-541">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-541">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-542">Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-542">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="bdbd4-543">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-543">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="bdbd4-544">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-544">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="bdbd4-545">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-545">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="bdbd4-546">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-546">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="bdbd4-547">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-547">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="bdbd4-548">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-548">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="bdbd4-549">Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-549">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="bdbd4-550">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="bdbd4-550">Thanks to our community contributors</span></span>
* <span data-ttu-id="bdbd4-551">Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-551">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="bdbd4-552">Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-552">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="bdbd4-553">Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-553">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="bdbd4-554">Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-554">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="bdbd4-555">@jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-555">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="bdbd4-556">@hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-556">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="bdbd4-557">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-557">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="bdbd4-558">Özellikten Özelliğe yazımını güncelleştirdi (#12821)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-558">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="bdbd4-559">New-AzResourceLock.md örneklerini güncelleştirdi (#12806)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-559">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="bdbd4-560">Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-560">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="bdbd4-561">@rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-561">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="bdbd4-562">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-562">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="bdbd4-563">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-563">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-564">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-564">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="bdbd4-565">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-565">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-566">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-566">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-567">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-567">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="bdbd4-568">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-568">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-569">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-569">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-570">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-570">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-571">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-571">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-572">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-572">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="bdbd4-573">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-573">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="bdbd4-574">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-574">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="bdbd4-575">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-575">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-576">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-576">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-577">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-577">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-578">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-578">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-579">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-579">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-580">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-580">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-581">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-581">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="bdbd4-582">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-582">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="bdbd4-583">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-583">Az.Maintenance</span></span>
* <span data-ttu-id="bdbd4-584">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-584">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="bdbd4-585">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-585">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bdbd4-586">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-586">Az.ManagedServices</span></span>
* <span data-ttu-id="bdbd4-587">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-587">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-588">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-588">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-589">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-589">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="bdbd4-590">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-590">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-591">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-592">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-592">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="bdbd4-593">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-593">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="bdbd4-594">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-594">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="bdbd4-595">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-595">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="bdbd4-596">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-596">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="bdbd4-597">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-597">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="bdbd4-598">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-598">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="bdbd4-599">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-599">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bdbd4-600">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bdbd4-600">Az.SignalR</span></span>
* <span data-ttu-id="bdbd4-601">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-601">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="bdbd4-602">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-602">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-603">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-603">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-604">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-604">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="bdbd4-605">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-605">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="bdbd4-606">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-606">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="bdbd4-607">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-607">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="bdbd4-608">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-608">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="bdbd4-609">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-609">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="bdbd4-610">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-610">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="bdbd4-611">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-611">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="bdbd4-612">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-612">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="bdbd4-613">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-613">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="bdbd4-614">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-614">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="bdbd4-615">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-615">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="bdbd4-616">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-616">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="bdbd4-617">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-617">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="bdbd4-618">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-618">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="bdbd4-619">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-619">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-620">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-620">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-621">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-621">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="bdbd4-622">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-622">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="bdbd4-623">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-623">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="bdbd4-624">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-624">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="bdbd4-625">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-625">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-626">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-626">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-627">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="bdbd4-627">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="bdbd4-628">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="bdbd4-628">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-629">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-629">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-630">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-630">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-631">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-631">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-632">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-632">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-633">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-633">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-634">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-634">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-635">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-635">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-636">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-636">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-637">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-637">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-638">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-638">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-639">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-639">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-640">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-640">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-641">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-641">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-642">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-642">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-643">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-643">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-644">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-644">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-645">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-645">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-646">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-646">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-647">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-647">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="bdbd4-648">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-648">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="bdbd4-649">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-649">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="bdbd4-650">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-650">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="bdbd4-651">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-651">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="bdbd4-652">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-652">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="bdbd4-653">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-653">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-654">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-654">Az.Network</span></span>
* <span data-ttu-id="bdbd4-655">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-655">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="bdbd4-656">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-656">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="bdbd4-657">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-657">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="bdbd4-658">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-658">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-659">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-659">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-660">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-660">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="bdbd4-661">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-661">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="bdbd4-662">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-662">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-663">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-664">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-664">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-665">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-666">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-666">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="bdbd4-667">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-667">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-668">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-669">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-669">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="bdbd4-670">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-670">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-671">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-671">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-672">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-672">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="bdbd4-673">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-673">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="bdbd4-674">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-674">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="bdbd4-675">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-675">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="bdbd4-676">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-676">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="bdbd4-677">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-677">Supported get single file share usage</span></span>
    - <span data-ttu-id="bdbd4-678">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-678">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="bdbd4-679">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-679">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-680">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-680">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-681">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-681">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="bdbd4-682">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-682">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-683">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-683">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-684">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-684">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-685">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-685">Az.AnalysisServices</span></span>
* <span data-ttu-id="bdbd4-686">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-686">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-687">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-688">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-688">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-689">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-689">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-690">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-690">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-691">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-691">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-692">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-692">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bdbd4-693">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdbd4-693">Az.EventGrid</span></span>
* <span data-ttu-id="bdbd4-694">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-694">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="bdbd4-695">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-695">Added new features:</span></span>
    - <span data-ttu-id="bdbd4-696">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-696">Input mapping</span></span>
    - <span data-ttu-id="bdbd4-697">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="bdbd4-697">Event Delivery Schema</span></span>
    - <span data-ttu-id="bdbd4-698">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-698">Private Link</span></span>
    - <span data-ttu-id="bdbd4-699">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="bdbd4-699">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="bdbd4-700">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-700">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="bdbd4-701">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-701">Azure Function As Destination</span></span>
    - <span data-ttu-id="bdbd4-702">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="bdbd4-702">WebHook Batching</span></span>
    - <span data-ttu-id="bdbd4-703">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-703">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="bdbd4-704">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="bdbd4-704">IpFiltering</span></span>
* <span data-ttu-id="bdbd4-705">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-705">Updated cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-706">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-706">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="bdbd4-707">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-707">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="bdbd4-708">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-708">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="bdbd4-709">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-709">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="bdbd4-710">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-710">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="bdbd4-711">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-711">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="bdbd4-712">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-712">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="bdbd4-713">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-713">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="bdbd4-714">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-714">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-715">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-716">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-716">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="bdbd4-717">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-717">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-718">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-718">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-719">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-719">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-720">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-720">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-721">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-721">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-722">Az.Network</span></span>
* <span data-ttu-id="bdbd4-723">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-723">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="bdbd4-724">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-724">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="bdbd4-725">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-725">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="bdbd4-726">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-726">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="bdbd4-727">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-727">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="bdbd4-728">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-728">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="bdbd4-729">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-729">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="bdbd4-730">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-730">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="bdbd4-731">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-731">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="bdbd4-732">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-732">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="bdbd4-733">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-733">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="bdbd4-734">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-734">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="bdbd4-735">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-735">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="bdbd4-736">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-736">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="bdbd4-737">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-737">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="bdbd4-738">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-738">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="bdbd4-739">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-739">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-740">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-740">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-741">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-741">Removed project reference to Authentication</span></span>
* <span data-ttu-id="bdbd4-742">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-742">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="bdbd4-743">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-743">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-744">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-745">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-745">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="bdbd4-746">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-746">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-747">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-747">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-748">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-748">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="bdbd4-749">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-749">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="bdbd4-750">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-750">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-751">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-751">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-752">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-752">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="bdbd4-753">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-753">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="bdbd4-754">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-754">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="bdbd4-755">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-755">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-756">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-756">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="bdbd4-757">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-757">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="bdbd4-758">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="bdbd4-758">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="bdbd4-759">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-759">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="bdbd4-760">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-760">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="bdbd4-761">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-761">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="bdbd4-762">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-762">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="bdbd4-763">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-763">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="bdbd4-764">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-764">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="bdbd4-765">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-765">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="bdbd4-766">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-766">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="bdbd4-767">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-767">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="bdbd4-768">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-768">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bdbd4-769">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bdbd4-769">Az.StorageSync</span></span>
* <span data-ttu-id="bdbd4-770">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-770">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="bdbd4-771">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-771">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="bdbd4-772">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="bdbd4-772">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="bdbd4-773">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-773">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-774">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-774">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-775">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-775">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="bdbd4-776">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-776">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-777">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-777">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-778">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-778">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="bdbd4-779">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-779">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="bdbd4-780">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-780">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="bdbd4-781">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-781">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-782">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-782">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-783">Eski [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-783">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-784">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-784">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-785">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-785">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="bdbd4-786">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-786">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-787">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-787">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-788">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-788">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="bdbd4-789">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-789">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-790">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-791">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-791">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="bdbd4-792">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-792">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="bdbd4-793">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-793">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="bdbd4-794">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-794">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="bdbd4-795">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-795">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-796">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-796">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-797">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-797">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-798">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-798">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-799">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-799">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="bdbd4-800">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bdbd4-800">Az.Functions</span></span>
* <span data-ttu-id="bdbd4-801">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-801">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-802">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-802">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-803">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-803">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bdbd4-804">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bdbd4-804">Az.HealthcareApis</span></span>
* <span data-ttu-id="bdbd4-805">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-805">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="bdbd4-806">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-806">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-807">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-807">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-808">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-808">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="bdbd4-809">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-809">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-810">Az.Network</span></span>
* <span data-ttu-id="bdbd4-811">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-811">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="bdbd4-812">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-812">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="bdbd4-813">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-813">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="bdbd4-814">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-814">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="bdbd4-815">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-815">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="bdbd4-816">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-816">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="bdbd4-817">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-817">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="bdbd4-818">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-818">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="bdbd4-819">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-819">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="bdbd4-820">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-820">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="bdbd4-821">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-821">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="bdbd4-822">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-822">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="bdbd4-823">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-823">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="bdbd4-824">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-824">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="bdbd4-825">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-825">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="bdbd4-826">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-826">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="bdbd4-827">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-827">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="bdbd4-828">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-828">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="bdbd4-829">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-829">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="bdbd4-830">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-830">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="bdbd4-831">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-831">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="bdbd4-832">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-832">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="bdbd4-833">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-833">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="bdbd4-834">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-834">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="bdbd4-835">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-835">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="bdbd4-836">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-836">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="bdbd4-837">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-837">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="bdbd4-838">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-838">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="bdbd4-839">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-839">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-840">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-840">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-841">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-841">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-842">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-842">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-843">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-843">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-844">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-844">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="bdbd4-845">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-845">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="bdbd4-846">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-846">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="bdbd4-847">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-847">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="bdbd4-848">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-848">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="bdbd4-849">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-849">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="bdbd4-850">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-850">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="bdbd4-851">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-851">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="bdbd4-852">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-852">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="bdbd4-853">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-853">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="bdbd4-854">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-854">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="bdbd4-855">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-855">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="bdbd4-856">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-856">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="bdbd4-857">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-857">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="bdbd4-858">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-858">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="bdbd4-859">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-859">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-860">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-860">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-861">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-861">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="bdbd4-862">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-862">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="bdbd4-863">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-863">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="bdbd4-864">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-864">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="bdbd4-865">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-865">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-866">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-866">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-867">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-867">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="bdbd4-868">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-868">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-869">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-869">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-870">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-870">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="bdbd4-871">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-871">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="bdbd4-872">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-872">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="bdbd4-873">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-873">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="bdbd4-874">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-874">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="bdbd4-875">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-875">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-876">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-876">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-877">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-877">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="bdbd4-878">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-878">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="bdbd4-879">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-879">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-880">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-880">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-881">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-881">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="bdbd4-882">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-882">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-883">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-883">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-884">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-885">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-885">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="bdbd4-886">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-886">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="bdbd4-887">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-887">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="bdbd4-888">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-888">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="bdbd4-889">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-889">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="bdbd4-890">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-890">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="bdbd4-891">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-891">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-892">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-893">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-893">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="bdbd4-895">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-895">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-896">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-896">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-897">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-897">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="bdbd4-898">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bdbd4-898">Az.Billing</span></span>
* <span data-ttu-id="bdbd4-899">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-899">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-900">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-900">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-901">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-901">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-902">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-902">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-903">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-903">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="bdbd4-904">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-904">Az.DataShare</span></span>
* <span data-ttu-id="bdbd4-905">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-905">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="bdbd4-906">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="bdbd4-906">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="bdbd4-907">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-907">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-908">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-908">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-909">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-909">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="bdbd4-910">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-910">Added optional parameters to</span></span> 
    - <span data-ttu-id="bdbd4-911">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-911">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="bdbd4-912">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-912">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-913">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-913">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-914">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-914">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="bdbd4-915">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bdbd4-915">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="bdbd4-916">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-916">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="bdbd4-917">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="bdbd4-917">Az.PrivateDns</span></span>
* <span data-ttu-id="bdbd4-918">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-918">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-920">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-920">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="bdbd4-921">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-921">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-922">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-923">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-923">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="bdbd4-924">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-924">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="bdbd4-925">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-925">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="bdbd4-926">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-926">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="bdbd4-927">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-927">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-928">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-929">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-929">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="bdbd4-930">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-930">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="bdbd4-931">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-931">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-932">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-933">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-933">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="bdbd4-934">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-934">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="bdbd4-935">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-935">Highlights since the last release</span></span>
* <span data-ttu-id="bdbd4-936">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="bdbd4-936">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="bdbd4-937">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-937">General availability of Az.Functions</span></span> 
* <span data-ttu-id="bdbd4-938">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-938">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-939">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-940">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-940">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="bdbd4-941">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-941">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-942">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-942">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-943">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-943">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="bdbd4-944">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-944">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="bdbd4-945">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-945">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-946">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-946">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-947">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-947">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="bdbd4-948">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-948">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="bdbd4-949">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-949">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="bdbd4-950">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-950">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="bdbd4-951">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-951">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="bdbd4-952">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-952">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="bdbd4-953">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-953">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="bdbd4-954">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-954">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="bdbd4-955">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-955">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="bdbd4-956">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-956">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="bdbd4-957">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-957">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="bdbd4-958">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-958">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="bdbd4-959">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-959">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="bdbd4-960">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-960">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="bdbd4-961">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-961">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="bdbd4-962">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-962">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="bdbd4-963">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-963">Az.ApplicationInsights</span></span>
* <span data-ttu-id="bdbd4-964">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-964">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="bdbd4-965">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-965">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="bdbd4-966">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-966">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-967">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-967">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-968">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-968">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="bdbd4-969">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-969">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="bdbd4-970">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-970">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="bdbd4-971">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-971">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="bdbd4-972">Örnek: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-972">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="bdbd4-973">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-973">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="bdbd4-974">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-974">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="bdbd4-975">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-975">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="bdbd4-976">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-976">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-977">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-978">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-978">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="bdbd4-979">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-979">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="bdbd4-980">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-980">Breaking changes</span></span>
    - <span data-ttu-id="bdbd4-981">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-981">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="bdbd4-982">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-982">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="bdbd4-983">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-983">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="bdbd4-984">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-984">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="bdbd4-985">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-985">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="bdbd4-986">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-986">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="bdbd4-987">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-987">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-988">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-988">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-989">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-989">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-990">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-990">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-991">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-991">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="bdbd4-992">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-992">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="bdbd4-993">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-993">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="bdbd4-994">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-994">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="bdbd4-995">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="bdbd4-995">Az.Functions</span></span>
* <span data-ttu-id="bdbd4-996">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-996">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-997">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-997">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-998">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-998">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bdbd4-999">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bdbd4-999">Az.HealthcareApis</span></span>
* <span data-ttu-id="bdbd4-1000">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1000">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1001">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1002">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1002">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="bdbd4-1003">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1003">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="bdbd4-1004">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1004">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="bdbd4-1005">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1005">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="bdbd4-1006">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1006">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="bdbd4-1007">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1007">New cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1008">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1008">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1009">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1009">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1010">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1010">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1011">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1011">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="bdbd4-1012">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1012">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="bdbd4-1013">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1013">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1014">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1014">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1015">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1015">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="bdbd4-1016">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1016">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="bdbd4-1017">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1017">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="bdbd4-1018">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1018">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="bdbd4-1019">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1019">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="bdbd4-1020">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1020">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="bdbd4-1021">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1021">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1022">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1022">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1023">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1023">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="bdbd4-1024">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1024">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="bdbd4-1025">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1025">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="bdbd4-1026">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1026">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="bdbd4-1027">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1027">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="bdbd4-1028">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1028">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="bdbd4-1029">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1029">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1030">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1030">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1031">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1031">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="bdbd4-1032">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1032">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="bdbd4-1033">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1033">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="bdbd4-1034">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1034">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="bdbd4-1035">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1035">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="bdbd4-1036">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1036">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1037">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1037">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="bdbd4-1038">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1038">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="bdbd4-1039">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1039">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="bdbd4-1040">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1040">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="bdbd4-1041">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1041">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="bdbd4-1042">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1042">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="bdbd4-1043">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1043">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="bdbd4-1044">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1044">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="bdbd4-1045">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1045">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="bdbd4-1046">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1046">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="bdbd4-1047">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1047">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="bdbd4-1048">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1048">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="bdbd4-1049">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1049">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="bdbd4-1050">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1050">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="bdbd4-1051">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1051">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="bdbd4-1052">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1052">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="bdbd4-1053">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1053">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="bdbd4-1054">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1054">Updated cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-1055">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1055">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-1056">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1056">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-1057">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1057">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="bdbd4-1058">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1058">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="bdbd4-1059">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1059">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="bdbd4-1060">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1060">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="bdbd4-1061">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1061">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="bdbd4-1062">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1062">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="bdbd4-1063">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1063">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="bdbd4-1064">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1064">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1065">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1065">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1066">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1066">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="bdbd4-1067">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1067">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="bdbd4-1068">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1068">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="bdbd4-1069">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1069">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="bdbd4-1070">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1070">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1071">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1072">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1072">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="bdbd4-1073">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1073">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="bdbd4-1074">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1074">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="bdbd4-1075">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1075">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="bdbd4-1076">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1076">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="bdbd4-1077">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1077">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="bdbd4-1078">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1078">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="bdbd4-1079">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1079">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="bdbd4-1080">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1080">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="bdbd4-1081">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1081">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="bdbd4-1082">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1082">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="bdbd4-1083">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1083">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="bdbd4-1084">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1084">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="bdbd4-1085">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1085">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="bdbd4-1086">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1086">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="bdbd4-1087">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1087">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="bdbd4-1088">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1088">'New-AzDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1089">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1089">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1090">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1090">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="bdbd4-1091">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1091">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-1092">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1092">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-1093">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1093">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1094">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1095">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1095">Enhance performance of:</span></span>
    - <span data-ttu-id="bdbd4-1096">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1096">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="bdbd4-1097">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1097">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="bdbd4-1098">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1098">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="bdbd4-1099">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1099">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="bdbd4-1100">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1100">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="bdbd4-1101">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1101">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="bdbd4-1102">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1102">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="bdbd4-1103">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1103">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="bdbd4-1104">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1104">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="bdbd4-1105">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1105">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1106">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1106">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1107">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1107">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-1108">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1108">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="bdbd4-1109">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1109">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-1110">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1110">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="bdbd4-1111">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1111">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="bdbd4-1112">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1112">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="bdbd4-1113">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1113">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="bdbd4-1114">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1114">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="bdbd4-1115">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1115">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="bdbd4-1116">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1116">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="bdbd4-1117">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1117">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="bdbd4-1118">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1118">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="bdbd4-1119">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1119">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="bdbd4-1120">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1120">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="bdbd4-1121">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1121">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="bdbd4-1122">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1122">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-1123">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1123">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="bdbd4-1124">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1124">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="bdbd4-1125">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1125">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="bdbd4-1126">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1126">Supported failover Storage account</span></span>
    - <span data-ttu-id="bdbd4-1127">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1127">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="bdbd4-1128">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1128">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="bdbd4-1129">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1129">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="bdbd4-1130">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1130">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="bdbd4-1131">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1131">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="bdbd4-1132">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1132">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="bdbd4-1133">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1133">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="bdbd4-1134">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1134">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="bdbd4-1135">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1135">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="bdbd4-1136">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1136">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="bdbd4-1137">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1137">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="bdbd4-1138">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1138">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="bdbd4-1139">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1139">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="bdbd4-1140">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1140">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="bdbd4-1141">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1141">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="bdbd4-1142">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1142">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="bdbd4-1143">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1143">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="bdbd4-1144">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1144">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="bdbd4-1145">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1145">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="bdbd4-1146">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1146">Az.TrafficManager</span></span>
* <span data-ttu-id="bdbd4-1147">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1147">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1148">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1149">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1149">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="bdbd4-1150">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1150">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="bdbd4-1151">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1151">Highlights since the last release</span></span>
* <span data-ttu-id="bdbd4-1152">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1152">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1153">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1154">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1154">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-1155">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1155">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-1156">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1156">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="bdbd4-1157">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1157">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-1158">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1158">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-1159">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1159">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-1161">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1161">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1162">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1163">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1163">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1164">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1164">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1165">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1165">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1166">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1166">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1167">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1167">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="bdbd4-1168">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1168">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="bdbd4-1169">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1169">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="bdbd4-1170">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1170">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1171">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1171">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="bdbd4-1172">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1172">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="bdbd4-1173">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1173">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="bdbd4-1174">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1174">New cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1175">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1175">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-1176">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1176">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-1177">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1177">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="bdbd4-1178">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1178">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="bdbd4-1179">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1179">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1180">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1181">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1181">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="bdbd4-1182">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1182">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="bdbd4-1183">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1183">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="bdbd4-1184">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1184">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="bdbd4-1185">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1185">Az.Maintenance</span></span>
* <span data-ttu-id="bdbd4-1186">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1186">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1187">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1187">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1188">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1188">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="bdbd4-1189">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1189">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="bdbd4-1190">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1190">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="bdbd4-1191">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1191">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="bdbd4-1192">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1192">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="bdbd4-1193">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1193">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="bdbd4-1194">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1194">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="bdbd4-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1195">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1196">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1197">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1197">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="bdbd4-1198">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1198">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="bdbd4-1199">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1199">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="bdbd4-1200">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1200">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="bdbd4-1201">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1201">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="bdbd4-1202">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1202">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="bdbd4-1203">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1203">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="bdbd4-1204">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1204">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="bdbd4-1205">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1205">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="bdbd4-1206">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1206">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="bdbd4-1207">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1207">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="bdbd4-1208">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1208">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="bdbd4-1209">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1209">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="bdbd4-1210">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1210">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="bdbd4-1211">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1211">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="bdbd4-1212">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1212">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-1213">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1213">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-1214">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1214">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="bdbd4-1215">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1215">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-1216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1216">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-1217">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1217">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1218">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1218">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1219">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1219">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="bdbd4-1220">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1220">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1221">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1222">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1222">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="bdbd4-1223">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1223">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="bdbd4-1224">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1224">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="bdbd4-1225">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1225">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="bdbd4-1226">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1226">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="bdbd4-1227">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1227">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="bdbd4-1228">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1228">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="bdbd4-1229">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1229">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="bdbd4-1230">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1230">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="bdbd4-1231">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1231">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="bdbd4-1232">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1232">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="bdbd4-1233">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1233">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="bdbd4-1234">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1234">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="bdbd4-1235">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1235">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="bdbd4-1236">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1236">General</span></span>
* <span data-ttu-id="bdbd4-1237">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1237">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="bdbd4-1238">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1238">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="bdbd4-1239">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](/azure-stack/operator/powershell-install-az-module) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1239">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="bdbd4-1240">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1240">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="bdbd4-1241">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1241">Az.Billing</span></span>
  - <span data-ttu-id="bdbd4-1242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1242">Az.Compute</span></span>
  - <span data-ttu-id="bdbd4-1243">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1243">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="bdbd4-1244">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1244">Az.EventHub</span></span>
  - <span data-ttu-id="bdbd4-1245">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1245">Az.IotHub</span></span>
  - <span data-ttu-id="bdbd4-1246">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1246">Az.KeyVault</span></span>
  - <span data-ttu-id="bdbd4-1247">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1247">Az.Monitor</span></span>
  - <span data-ttu-id="bdbd4-1248">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1248">Az.Network</span></span>
  - <span data-ttu-id="bdbd4-1249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1249">Az.Resources</span></span>
  - <span data-ttu-id="bdbd4-1250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1250">Az.Storage</span></span>
  - <span data-ttu-id="bdbd4-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1251">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1252">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1252">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-1253">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1253">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="bdbd4-1254">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](/azure-stack/operator/powershell-install-az-module) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1254">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="bdbd4-1255">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1255">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1256">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1257">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1257">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1258">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1258">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1259">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1259">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="bdbd4-1260">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1260">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="bdbd4-1261">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1261">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1262">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1262">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="bdbd4-1263">[#11354]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1263">[#11354]</span></span>
* <span data-ttu-id="bdbd4-1264">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1264">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="bdbd4-1265">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1265">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="bdbd4-1266">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1266">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="bdbd4-1267">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1267">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="bdbd4-1268">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1268">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="bdbd4-1269">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1269">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="bdbd4-1270">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1270">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="bdbd4-1271">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1271">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="bdbd4-1272">[#11257]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1272">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1273">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1274">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1274">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="bdbd4-1275">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1275">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-1276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1276">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-1277">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1277">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="bdbd4-1278">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1278">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-1279">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1279">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-1280">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1280">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1281">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1281">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1282">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1282">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="bdbd4-1283">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1283">New Cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1284">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1284">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="bdbd4-1285">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1285">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1286">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1287">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1287">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1288">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1289">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1289">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1290">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1291">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1291">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="bdbd4-1292">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1292">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="bdbd4-1293">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1293">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="bdbd4-1294">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1294">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="bdbd4-1295">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1295">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="bdbd4-1296">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1296">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-1297">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1297">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-1298">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1298">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1299">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1299">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1300">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1300">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="bdbd4-1301">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1301">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="bdbd4-1302">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1302">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="bdbd4-1303">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1303">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="bdbd4-1304">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1304">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="bdbd4-1305">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1305">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1306">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1306">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1307">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1307">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="bdbd4-1308">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1308">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="bdbd4-1309">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1309">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="bdbd4-1310">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1310">Added example.</span></span>
* <span data-ttu-id="bdbd4-1311">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1311">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="bdbd4-1312">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1312">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1313">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1313">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1314">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1314">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="bdbd4-1315">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1315">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="bdbd4-1316">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1316">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="bdbd4-1317">Az.Support</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1317">Az.Support</span></span>
* <span data-ttu-id="bdbd4-1318">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1318">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-1319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1319">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1320">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1320">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="bdbd4-1321">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1321">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="bdbd4-1322">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1322">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="bdbd4-1323">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1323">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="bdbd4-1324">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1324">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="bdbd4-1325">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1325">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1326">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1327">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1327">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="bdbd4-1328">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1328">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="bdbd4-1329">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1329">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-1330">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1330">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-1331">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1331">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="bdbd4-1332">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1332">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="bdbd4-1333">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1333">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="bdbd4-1334">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1334">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-1335">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1335">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-1336">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1336">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1337">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1337">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1338">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1338">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="bdbd4-1339">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1339">New Cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1340">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1340">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1341">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1341">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1342">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1342">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1343">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1343">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="bdbd4-1344">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1344">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="bdbd4-1345">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1345">New Cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1346">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1346">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="bdbd4-1347">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1347">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="bdbd4-1348">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1348">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="bdbd4-1349">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1349">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="bdbd4-1350">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1350">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="bdbd4-1351">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1351">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="bdbd4-1352">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1352">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="bdbd4-1353">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1353">New Cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1354">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1354">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="bdbd4-1355">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1355">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="bdbd4-1356">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1356">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1357">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1358">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1358">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1359">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1359">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1360">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1360">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="bdbd4-1361">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1361">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="bdbd4-1362">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1362">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="bdbd4-1363">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1363">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1364">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1364">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1365">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1365">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="bdbd4-1366">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1366">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="bdbd4-1367">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1367">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="bdbd4-1368">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1368">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="bdbd4-1369">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1369">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="bdbd4-1370">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1370">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="bdbd4-1371">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1371">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="bdbd4-1372">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1372">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="bdbd4-1373">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1373">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="bdbd4-1374">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1374">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="bdbd4-1375">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1375">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="bdbd4-1376">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1376">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="bdbd4-1377">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1377">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="bdbd4-1378">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1378">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1379">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1380">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1380">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="bdbd4-1381">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1381">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="bdbd4-1382">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1382">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="bdbd4-1383">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1383">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="bdbd4-1384">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1384">Remove an LTR backup</span></span>
    - <span data-ttu-id="bdbd4-1385">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1385">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="bdbd4-1386">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1386">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="bdbd4-1387">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1387">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="bdbd4-1388">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1388">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1389">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1390">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1390">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="bdbd4-1391">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1391">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="bdbd4-1392">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1392">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="bdbd4-1393">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1393">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="bdbd4-1394">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1394">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-1395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1395">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1396">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1396">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="bdbd4-1397">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1397">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="bdbd4-1398">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1398">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="bdbd4-1399">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1399">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="bdbd4-1400">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1400">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="bdbd4-1401">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1401">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-1402">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1402">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-1403">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1403">Updated client side telemetry.</span></span>
* <span data-ttu-id="bdbd4-1404">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1404">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="bdbd4-1405">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1405">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1406">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1406">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1407">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1407">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-1408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1408">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-1409">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1409">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-1410">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1410">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-1411">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1411">Updated SDK to 7.0</span></span>
* <span data-ttu-id="bdbd4-1412">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1412">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1413">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1413">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1414">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1414">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-1415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1415">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-1416">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1416">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1417">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1417">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1418">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1418">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="bdbd4-1419">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1419">New Cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1420">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1420">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1421">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1421">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1422">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1422">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="bdbd4-1423">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1423">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1424">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1424">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1425">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1425">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1426">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1426">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1427">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1427">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1428">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1428">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="bdbd4-1429">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1429">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1430">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1431">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1431">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1432">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1432">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="bdbd4-1433">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1433">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="bdbd4-1434">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1434">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="bdbd4-1435">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1435">No new cmdlets are added.</span></span> <span data-ttu-id="bdbd4-1436">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1436">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1437">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1437">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1438">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1438">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1439">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1440">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1440">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="bdbd4-1441">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1441">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="bdbd4-1442">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1442">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="bdbd4-1443">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1443">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="bdbd4-1444">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1444">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="bdbd4-1445">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1445">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="bdbd4-1446">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1446">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="bdbd4-1447">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1447">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1448">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1449">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1449">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="bdbd4-1450">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1450">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="bdbd4-1451">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1451">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="bdbd4-1452">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1452">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="bdbd4-1453">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1453">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bdbd4-1454">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1454">Az.StorageSync</span></span>
* <span data-ttu-id="bdbd4-1455">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1455">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="bdbd4-1456">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1456">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-1457">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1457">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-1458">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1458">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="bdbd4-1459">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1459">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1460">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1460">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1461">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1461">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="bdbd4-1462">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1462">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-1463">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1463">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-1464">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1464">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="bdbd4-1465">**New-AzApiManagementProduct** _ ve _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1465">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="bdbd4-1466"> https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1466">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="bdbd4-1467">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1467">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1468">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1468">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1469">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1469">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="bdbd4-1470">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1470">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="bdbd4-1471">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1471">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-1472">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1472">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="bdbd4-1473">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1473">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1474">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1474">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1475">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1475">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="bdbd4-1476">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1476">Az.DeploymentManager</span></span>
* <span data-ttu-id="bdbd4-1477">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1477">Adds LIST operations for resources</span></span>
* <span data-ttu-id="bdbd4-1478">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1478">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-1479">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1479">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-1480">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1480">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1481">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1481">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1482">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1482">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1483">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1484">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1484">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="bdbd4-1485">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1485">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="bdbd4-1486">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1486">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-1487">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1487">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="bdbd4-1488">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1488">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="bdbd4-1489">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1489">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="bdbd4-1490">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1490">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="bdbd4-1491">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1491">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="bdbd4-1492">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1492">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1493">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="bdbd4-1494">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1494">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="bdbd4-1495">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1495">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="bdbd4-1496">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1496">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-1497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1497">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-1498">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1498">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="bdbd4-1499">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1499">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="bdbd4-1500">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1500">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="bdbd4-1501">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1501">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1502">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1503">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1503">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="bdbd4-1504">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1504">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1505">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1506">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1506">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="bdbd4-1507">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1507">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1508">Az.Sql</span></span>
<span data-ttu-id="bdbd4-1509">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1509">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1510">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1511">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1511">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="bdbd4-1512">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1512">New-AzStorageAccount</span></span>
* <span data-ttu-id="bdbd4-1513">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1513">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="bdbd4-1514">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1514">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-1515">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1515">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1516">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1516">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="bdbd4-1517">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1517">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="bdbd4-1518">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1518">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1519">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1520">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1520">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-1521">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1521">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-1522">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1522">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1523">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1524">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1524">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="bdbd4-1525">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1525">Az.ContainerInstance</span></span>
* <span data-ttu-id="bdbd4-1526">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1526">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="bdbd4-1527">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1527">Az.DataBoxEdge</span></span>
* <span data-ttu-id="bdbd4-1528">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1528">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bdbd4-1529">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1529">Get the Edge Storage Container</span></span>
* <span data-ttu-id="bdbd4-1530">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1530">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bdbd4-1531">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1531">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="bdbd4-1532">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1532">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bdbd4-1533">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1533">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="bdbd4-1534">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1534">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="bdbd4-1535">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1535">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="bdbd4-1536">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1536">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bdbd4-1537">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1537">Get the Edge Storage Account</span></span>
* <span data-ttu-id="bdbd4-1538">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1538">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bdbd4-1539">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1539">Create new Edge Storage Account</span></span>
* <span data-ttu-id="bdbd4-1540">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1540">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="bdbd4-1541">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1541">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="bdbd4-1542">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1542">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="bdbd4-1543">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1543">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="bdbd4-1544">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1544">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="bdbd4-1545">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1545">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1546">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1547">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1547">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="bdbd4-1548">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1548">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="bdbd4-1549">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1549">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="bdbd4-1550">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1550">Az.DevTestLabs</span></span>
* <span data-ttu-id="bdbd4-1551">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1551">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-1552">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1552">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-1553">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1553">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-1554">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1554">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-1555">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1555">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bdbd4-1556">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1556">Az.MachineLearning</span></span>
* <span data-ttu-id="bdbd4-1557">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1557">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="bdbd4-1558">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1558">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="bdbd4-1559">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1559">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="bdbd4-1560">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1560">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="bdbd4-1561">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1561">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="bdbd4-1562">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1562">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="bdbd4-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1563">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="bdbd4-1564">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1564">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1565">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1565">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1566">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1566">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1567">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1567">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1568">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1568">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="bdbd4-1569">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1569">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="bdbd4-1570">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1570">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="bdbd4-1571">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1571">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1572">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1573">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1573">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1574">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1575">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1575">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="bdbd4-1576">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1576">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="bdbd4-1577">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1577">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="bdbd4-1578">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1578">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1579">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1580">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1580">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="bdbd4-1581">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1581">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="bdbd4-1582">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1582">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="bdbd4-1583">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1583">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="bdbd4-1584">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1584">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="bdbd4-1585">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1585">General</span></span>
* <span data-ttu-id="bdbd4-1586">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1586">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1587">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1587">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1588">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1588">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="bdbd4-1589">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1589">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-1590">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1590">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-1591">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1591">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1592">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1592">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1593">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1593">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-1594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1594">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-1595">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1595">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="bdbd4-1596">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1596">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bdbd4-1597">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1597">Az.HealthcareApis</span></span>
* <span data-ttu-id="bdbd4-1598">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1598">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-1599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1599">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-1600">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1600">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="bdbd4-1601">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1601">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="bdbd4-1602">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1602">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1603">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1604">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1604">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="bdbd4-1605">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1605">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="bdbd4-1606">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1606">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1607">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1608">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1608">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1609">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1610">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1610">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="bdbd4-1611">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1611">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1612">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1612">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1613">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1613">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1614">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1614">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1615">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1615">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="bdbd4-1616">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1616">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="bdbd4-1617">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1617">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="bdbd4-1618">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1618">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="bdbd4-1619">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1619">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="bdbd4-1620">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1620">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="bdbd4-1621">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1621">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="bdbd4-1622">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1622">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="bdbd4-1623">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1623">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="bdbd4-1624">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1624">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="bdbd4-1625">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1625">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="bdbd4-1626">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1626">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="bdbd4-1627">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1627">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="bdbd4-1628">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1628">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-1629">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1629">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-1630">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1630">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="bdbd4-1631">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1631">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1632">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1632">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1633">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1633">VM Reapply feature</span></span>
    - <span data-ttu-id="bdbd4-1634">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1634">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="bdbd4-1635">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1635">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="bdbd4-1636">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1636">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="bdbd4-1637">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1637">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="bdbd4-1638">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1638">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="bdbd4-1639">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1639">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="bdbd4-1640">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1640">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="bdbd4-1641">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1641">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="bdbd4-1642">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1642">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="bdbd4-1643">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1643">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="bdbd4-1644">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1644">Az.DataBoxEdge</span></span>
* <span data-ttu-id="bdbd4-1645">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1645">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bdbd4-1646">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1646">Get the Order</span></span>
* <span data-ttu-id="bdbd4-1647">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1647">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bdbd4-1648">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1648">Create new Order</span></span>
* <span data-ttu-id="bdbd4-1649">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1649">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="bdbd4-1650">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1650">Remove the Order</span></span>
* <span data-ttu-id="bdbd4-1651">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1651">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="bdbd4-1652">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1652">Now creates Local Share</span></span>
* <span data-ttu-id="bdbd4-1653">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1653">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="bdbd4-1654">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1654">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="bdbd4-1655">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1655">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="bdbd4-1656">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1656">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="bdbd4-1657">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1657">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bdbd4-1658">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1658">Gets the information about Triggers</span></span>
* <span data-ttu-id="bdbd4-1659">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1659">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bdbd4-1660">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1660">Create new Triggers</span></span>
* <span data-ttu-id="bdbd4-1661">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1661">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="bdbd4-1662">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1662">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1663">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1664">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1664">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="bdbd4-1665">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1665">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-1667">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1667">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-1668">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1668">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-1669">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1669">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-1670">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1670">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-1671">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1671">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="bdbd4-1672">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1672">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="bdbd4-1673">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1673">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="bdbd4-1674">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1674">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1675">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1675">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1676">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1676">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="bdbd4-1677">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1677">Az.PrivateDns</span></span>
* <span data-ttu-id="bdbd4-1678">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1678">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1680">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1680">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="bdbd4-1681">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1681">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="bdbd4-1682">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1682">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bdbd4-1683">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1683">Az.RedisCache</span></span>
* <span data-ttu-id="bdbd4-1684">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1684">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="bdbd4-1685">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1685">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1686">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1686">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1687">Az.Resources</span></span>
- <span data-ttu-id="bdbd4-1688">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1688">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="bdbd4-1689">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1689">Updated create policy definition help example</span></span>
- <span data-ttu-id="bdbd4-1690">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1690">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="bdbd4-1691">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1691">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="bdbd4-1692">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1692">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1693">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1694">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1694">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="bdbd4-1695">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1695">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="bdbd4-1696">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1696">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="bdbd4-1697">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1697">General</span></span>
* <span data-ttu-id="bdbd4-1698">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1698">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1699">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1700">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1700">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bdbd4-1701">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1701">Az.Advisor</span></span>
* <span data-ttu-id="bdbd4-1702">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1702">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-1703">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1703">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-1704">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1704">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="bdbd4-1705">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1705">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="bdbd4-1706">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1706">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="bdbd4-1707">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1707">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="bdbd4-1708">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1708">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="bdbd4-1709">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1709">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="bdbd4-1710">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1710">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="bdbd4-1711">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1711">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="bdbd4-1712">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1712">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="bdbd4-1713">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1713">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bdbd4-1714">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1714">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="bdbd4-1715">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1715">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="bdbd4-1716">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1716">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bdbd4-1717">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1717">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="bdbd4-1718">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1718">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="bdbd4-1719">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1719">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="bdbd4-1720">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1720">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="bdbd4-1721">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1721">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="bdbd4-1722">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1722">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="bdbd4-1723">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1723">This operation is no longer supported.</span></span>
* <span data-ttu-id="bdbd4-1724">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1724">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bdbd4-1725">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1725">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bdbd4-1726">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1726">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="bdbd4-1727">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1727">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="bdbd4-1728">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1728">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="bdbd4-1729">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1729">New non-verified images are also now returned.</span></span> <span data-ttu-id="bdbd4-1730">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1730">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="bdbd4-1731">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1731">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="bdbd4-1732">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1732">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="bdbd4-1733">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1733">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="bdbd4-1734">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1734">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="bdbd4-1735">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1735">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="bdbd4-1736">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1736">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="bdbd4-1737">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1737">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="bdbd4-1738">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1738">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="bdbd4-1739">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1739">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-1740">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1740">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-1741">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1741">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="bdbd4-1742">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1742">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1743">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1744">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1744">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="bdbd4-1745">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1745">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="bdbd4-1746">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1746">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="bdbd4-1747">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1747">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bdbd4-1748">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1748">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="bdbd4-1749">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1749">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="bdbd4-1750">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1750">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="bdbd4-1751">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1751">Breaking changes</span></span>
    - <span data-ttu-id="bdbd4-1752">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1752">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="bdbd4-1753">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1753">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1754">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1754">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1755">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1755">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-1756">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1756">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-1757">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1757">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="bdbd4-1758">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1758">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="bdbd4-1759">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1759">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="bdbd4-1760">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1760">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="bdbd4-1761">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1761">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="bdbd4-1762">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1762">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-1763">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1763">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-1764">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1764">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-1765">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1765">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-1766">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1766">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="bdbd4-1767">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1767">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="bdbd4-1768">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1768">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="bdbd4-1769">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1769">Removed five cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-1770">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1770">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bdbd4-1771">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1771">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bdbd4-1772">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1772">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bdbd4-1773">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1773">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="bdbd4-1774">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1774">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="bdbd4-1775">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1775">Added three cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-1776">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1776">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bdbd4-1777">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1777">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bdbd4-1778">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1778">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="bdbd4-1779">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1779">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="bdbd4-1780">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1780">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="bdbd4-1781">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1781">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="bdbd4-1782">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1782">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="bdbd4-1783">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1783">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="bdbd4-1784">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1784">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="bdbd4-1785">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1785">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="bdbd4-1786">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1786">Added some scenario test cases.</span></span>
* <span data-ttu-id="bdbd4-1787">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1787">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1788">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1788">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1789">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1789">Breaking changes:</span></span>
    - <span data-ttu-id="bdbd4-1790">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1790">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bdbd4-1791">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1791">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bdbd4-1792">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1792">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bdbd4-1793">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1793">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bdbd4-1794">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1794">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="bdbd4-1795">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1795">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="bdbd4-1796">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1796">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="bdbd4-1797">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1797">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="bdbd4-1798">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1798">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bdbd4-1799">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1799">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bdbd4-1800">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1800">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bdbd4-1801">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1801">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-1802">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1802">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-1803">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1803">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1804">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1804">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="bdbd4-1805">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1805">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="bdbd4-1806">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1806">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1807">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1807">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1808">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1808">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1809">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1809">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1810">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1810">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-1811">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1811">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1812">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-1813">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1813">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1814">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1814">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1815">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1815">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="bdbd4-1816">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1816">Updated cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-1817">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1817">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-1818">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1818">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-1819">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1819">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-1820">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1820">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-1821">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1821">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bdbd4-1822">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1822">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="bdbd4-1823">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1823">New cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-1824">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1824">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="bdbd4-1825">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1825">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="bdbd4-1826">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1826">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="bdbd4-1827">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1827">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="bdbd4-1828">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1828">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="bdbd4-1829">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1829">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="bdbd4-1830">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1830">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="bdbd4-1831">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1831">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="bdbd4-1832">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1832">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1833">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1833">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="bdbd4-1834">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1834">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bdbd4-1835">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1835">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bdbd4-1836">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1836">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bdbd4-1837">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1837">Set-AzVirtualHub</span></span>
* <span data-ttu-id="bdbd4-1838">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1838">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="bdbd4-1839">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1839">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bdbd4-1840">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1840">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bdbd4-1841">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1841">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bdbd4-1842">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1842">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="bdbd4-1843">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1843">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="bdbd4-1844">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1844">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="bdbd4-1845">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1846">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1846">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="bdbd4-1847">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1847">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bdbd4-1848">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1848">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bdbd4-1849">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1849">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bdbd4-1850">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1850">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bdbd4-1851">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1851">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bdbd4-1852">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1852">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="bdbd4-1853">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1853">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="bdbd4-1854">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1854">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1855">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1855">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="bdbd4-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1856">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="bdbd4-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1857">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="bdbd4-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1858">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="bdbd4-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1859">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="bdbd4-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1860">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="bdbd4-1861">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1861">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bdbd4-1862">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1862">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="bdbd4-1863">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1863">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="bdbd4-1864">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1864">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="bdbd4-1865">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1865">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="bdbd4-1866">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1866">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bdbd4-1867">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1867">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="bdbd4-1868">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1868">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="bdbd4-1869">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1869">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="bdbd4-1870">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1870">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="bdbd4-1871">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1871">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="bdbd4-1872">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1872">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1873">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1873">New-AzIpGroup</span></span>
        - <span data-ttu-id="bdbd4-1874">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1874">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="bdbd4-1875">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1875">Get-AzIpGroup</span></span>
        - <span data-ttu-id="bdbd4-1876">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1876">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-1877">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1877">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-1878">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1878">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1879">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1880">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1880">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="bdbd4-1881">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1881">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="bdbd4-1882">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1882">Removed deprecated aliases:</span></span>
* <span data-ttu-id="bdbd4-1883">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1883">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="bdbd4-1884">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1884">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="bdbd4-1885">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1885">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bdbd4-1886">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1886">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="bdbd4-1887">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1887">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="bdbd4-1888">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1888">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1889">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1889">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1890">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1890">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="bdbd4-1891">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1891">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bdbd4-1892">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1892">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bdbd4-1893">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1893">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="bdbd4-1894">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1894">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="bdbd4-1895">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1895">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="bdbd4-1896">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1896">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="bdbd4-1897">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1897">General</span></span>
* <span data-ttu-id="bdbd4-1898">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1898">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-1899">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1899">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-1900">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1900">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-1901">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1901">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-1902">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1902">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="bdbd4-1903">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1903">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-1904">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1904">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-1905">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1905">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-1906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1906">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-1907">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1907">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1908">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1908">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1909">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1909">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="bdbd4-1910">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1910">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="bdbd4-1911">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1911">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="bdbd4-1912">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1912">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1913">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1913">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1914">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1914">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="bdbd4-1915">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1915">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="bdbd4-1916">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1916">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1917">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-1918">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1918">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bdbd4-1919">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1919">Az.HealthcareApis</span></span>
* <span data-ttu-id="bdbd4-1920">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1920">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="bdbd4-1921">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1921">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="bdbd4-1922">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1922">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="bdbd4-1923">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1923">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1924">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1924">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1925">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1925">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="bdbd4-1926">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1926">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1927">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1928">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1928">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="bdbd4-1929">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1929">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="bdbd4-1930">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1930">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="bdbd4-1931">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1931">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-1932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1932">Az.Network</span></span>
* <span data-ttu-id="bdbd4-1933">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1933">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="bdbd4-1934">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1934">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="bdbd4-1935">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1935">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-1936">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1936">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="bdbd4-1937">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1937">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bdbd4-1938">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1938">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="bdbd4-1939">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1939">Updated cmdlets:</span></span>
        - <span data-ttu-id="bdbd4-1940">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1940">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bdbd4-1941">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1941">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bdbd4-1942">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1942">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bdbd4-1943">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1943">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="bdbd4-1944">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1944">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="bdbd4-1945">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1945">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="bdbd4-1946">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1946">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bdbd4-1947">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1947">Az.RedisCache</span></span>
* <span data-ttu-id="bdbd4-1948">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1948">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-1949">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1949">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-1950">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1950">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-1951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1951">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-1952">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1952">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="bdbd4-1953">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1953">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bdbd4-1954">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1954">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="bdbd4-1955">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1955">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bdbd4-1956">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1956">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bdbd4-1957">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1957">Az.StorageSync</span></span>
* <span data-ttu-id="bdbd4-1958">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1958">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-1959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1959">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-1960">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1960">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="bdbd4-1961">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1961">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-1962">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1962">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-1963">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1963">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="bdbd4-1964">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1964">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="bdbd4-1965">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1965">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-1966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1966">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-1967">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1967">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="bdbd4-1968">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1968">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="bdbd4-1969">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1969">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-1970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1970">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-1971">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1971">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="bdbd4-1972">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1972">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bdbd4-1973">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1973">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="bdbd4-1974">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1974">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="bdbd4-1975">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1975">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="bdbd4-1976">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1976">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="bdbd4-1977">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1977">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="bdbd4-1978">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1978">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="bdbd4-1979">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1979">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-1980">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1980">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-1981">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1981">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="bdbd4-1982">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1982">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-1983">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1983">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-1984">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1984">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-1985">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1985">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-1986">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1986">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="bdbd4-1987">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1987">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="bdbd4-1988">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1988">New cmdlets are:</span></span>
    - <span data-ttu-id="bdbd4-1989">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1989">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bdbd4-1990">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1990">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bdbd4-1991">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1991">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bdbd4-1992">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1992">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-1993">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1993">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-1994">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1994">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="bdbd4-1995">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1995">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="bdbd4-1996">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1996">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="bdbd4-1997">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1997">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="bdbd4-1998">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1998">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="bdbd4-1999">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-1999">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="bdbd4-2000">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2000">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="bdbd4-2001">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2001">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="bdbd4-2002">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2002">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bdbd4-2003">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2003">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="bdbd4-2004">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2004">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bdbd4-2005">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2005">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="bdbd4-2006">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2006">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="bdbd4-2007">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2007">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="bdbd4-2008">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2008">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="bdbd4-2009">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2009">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="bdbd4-2010">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2010">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="bdbd4-2011">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2011">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="bdbd4-2012">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2012">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="bdbd4-2013">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2013">Overall improved help files</span></span>
* <span data-ttu-id="bdbd4-2014">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2014">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2015">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2015">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2016">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2016">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="bdbd4-2017">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2017">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="bdbd4-2018">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2018">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="bdbd4-2019">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2019">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="bdbd4-2020">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2020">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="bdbd4-2021">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2021">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="bdbd4-2022">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2022">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="bdbd4-2023">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2023">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="bdbd4-2024">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2024">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="bdbd4-2025">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2025">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="bdbd4-2026">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2026">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="bdbd4-2027">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2027">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="bdbd4-2028">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2028">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2029">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2029">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="bdbd4-2030">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2030">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="bdbd4-2031">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2031">Updated cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-2032">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2032">New-VpnSite</span></span>
        - <span data-ttu-id="bdbd4-2033">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2033">Update-VpnSite</span></span>
        - <span data-ttu-id="bdbd4-2034">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2034">New-VpnConnection</span></span>
        - <span data-ttu-id="bdbd4-2035">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2035">Update-VpnConnection</span></span>
* <span data-ttu-id="bdbd4-2036">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2036">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2037">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2037">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2038">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2038">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="bdbd4-2039">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2039">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2040">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2040">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2041">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2041">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-2042">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2042">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-2043">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2043">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="bdbd4-2044">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2044">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="bdbd4-2045">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2045">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bdbd4-2046">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2046">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bdbd4-2047">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2047">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bdbd4-2048">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2048">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="bdbd4-2049">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2049">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bdbd4-2050">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2050">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bdbd4-2051">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2051">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bdbd4-2052">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2052">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bdbd4-2053">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2053">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="bdbd4-2054">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2054">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bdbd4-2055">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2055">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bdbd4-2056">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2056">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bdbd4-2057">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2057">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="bdbd4-2058">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2058">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bdbd4-2059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2059">Az.SignalR</span></span>
* <span data-ttu-id="bdbd4-2060">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2060">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2061">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2062">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2062">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="bdbd4-2063">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2063">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="bdbd4-2064">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2064">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="bdbd4-2065">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2065">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="bdbd4-2066">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2066">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2067">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2067">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2068">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2068">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="bdbd4-2069">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2069">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="bdbd4-2070">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2070">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="bdbd4-2071">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2071">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="bdbd4-2072">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2072">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="bdbd4-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2073">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="bdbd4-2074">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2074">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="bdbd4-2075">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2075">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bdbd4-2076">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2076">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bdbd4-2077">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2077">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bdbd4-2078">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2078">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2079">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2079">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2080">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2080">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="bdbd4-2081">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2081">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="bdbd4-2082">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2082">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="bdbd4-2083">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2083">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="bdbd4-2084">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2084">General</span></span>
* <span data-ttu-id="bdbd4-2085">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2085">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2086">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2087">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2087">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-2088">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2088">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-2089">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2089">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="bdbd4-2090">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2090">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-2091">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2091">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-2092">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2092">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="bdbd4-2093">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2093">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="bdbd4-2094">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2094">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="bdbd4-2095">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2095">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="bdbd4-2096">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2096">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-2097">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2097">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-2098">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2098">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-2099">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2099">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-2100">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2100">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2101">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2101">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2102">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2102">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="bdbd4-2103">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2103">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="bdbd4-2104">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2104">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="bdbd4-2105">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2105">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="bdbd4-2106">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2106">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="bdbd4-2107">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2107">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="bdbd4-2108">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2108">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="bdbd4-2109">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2109">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2110">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2111">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2111">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="bdbd4-2112">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2112">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="bdbd4-2113">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2113">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="bdbd4-2114">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2114">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-2115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2115">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-2116">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2116">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-2117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2117">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-2118">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2118">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="bdbd4-2119">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2119">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="bdbd4-2120">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2120">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="bdbd4-2121">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2121">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="bdbd4-2122">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2122">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bdbd4-2123">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2123">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-2124">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2124">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-2125">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2125">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2126">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2127">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2127">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="bdbd4-2128">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2128">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="bdbd4-2129">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2129">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="bdbd4-2130">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2130">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="bdbd4-2131">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2131">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="bdbd4-2132">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2132">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="bdbd4-2133">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2133">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2134">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2134">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2135">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2135">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="bdbd4-2136">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2136">Added example</span></span>
    - <span data-ttu-id="bdbd4-2137">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2137">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="bdbd4-2138">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2138">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="bdbd4-2139">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2139">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2140">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2141">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2141">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2142">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2143">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2143">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="bdbd4-2144">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2144">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="bdbd4-2145">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2145">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="bdbd4-2146">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2146">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-2147">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2147">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-2148">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2148">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="bdbd4-2149">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2149">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="bdbd4-2150">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2150">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-2151">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2151">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-2152">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2152">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="bdbd4-2153">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2153">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="bdbd4-2154">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2154">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="bdbd4-2155">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2155">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="bdbd4-2156">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2156">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="bdbd4-2157">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2157">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2158">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2159">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2159">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2160">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2161">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2161">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="bdbd4-2162">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2162">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="bdbd4-2163">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2163">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="bdbd4-2164">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2164">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="bdbd4-2165">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2165">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="bdbd4-2166">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2166">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2167">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2167">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2168">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2168">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="bdbd4-2169">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2169">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2170">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2171">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2171">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="bdbd4-2172">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2172">Az.ApplicationInsights</span></span>
* <span data-ttu-id="bdbd4-2173">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2173">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2174">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2174">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2175">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2175">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-2176">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2176">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-2177">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2177">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2178">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2178">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2179">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2179">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bdbd4-2180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2180">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bdbd4-2181">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2181">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="bdbd4-2182">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2182">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2183">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2184">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2184">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="bdbd4-2185">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2185">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-2186">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2186">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-2187">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2187">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bdbd4-2188">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2188">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-2189">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2189">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-2190">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2190">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bdbd4-2191">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2191">Az.LogicApp</span></span>
* <span data-ttu-id="bdbd4-2192">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2192">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="bdbd4-2193">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2193">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bdbd4-2194">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2194">Az.ManagedServices</span></span>
* <span data-ttu-id="bdbd4-2195">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2195">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2196">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2197">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2197">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="bdbd4-2198">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2198">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2199">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2199">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bdbd4-2200">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2200">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bdbd4-2201">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2201">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-2202">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2202">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-2203">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2203">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-2204">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2204">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bdbd4-2205">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2205">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="bdbd4-2206">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2206">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="bdbd4-2207">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2207">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="bdbd4-2208">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2208">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="bdbd4-2209">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2209">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="bdbd4-2210">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2210">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="bdbd4-2211">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2211">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="bdbd4-2212">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2212">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="bdbd4-2213">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2213">Updated cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2214">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2214">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bdbd4-2215">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2215">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bdbd4-2216">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2216">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bdbd4-2217">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2217">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bdbd4-2218">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2218">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="bdbd4-2219">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2219">Updated cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-2220">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2220">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bdbd4-2221">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2221">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bdbd4-2222">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2222">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="bdbd4-2223">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2223">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="bdbd4-2224">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2224">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="bdbd4-2225">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2225">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2226">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2227">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2227">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="bdbd4-2228">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2228">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2229">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2229">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2230">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2230">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bdbd4-2231">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2231">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="bdbd4-2232">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2232">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="bdbd4-2233">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2233">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bdbd4-2234">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2234">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="bdbd4-2235">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2235">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bdbd4-2236">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2236">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="bdbd4-2237">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2237">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bdbd4-2238">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2238">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="bdbd4-2239">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2239">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2240">Az.Resources</span></span>
- <span data-ttu-id="bdbd4-2241">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2241">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="bdbd4-2242">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2242">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-2243">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2243">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-2244">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2244">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bdbd4-2245">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2245">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2246">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2247">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2247">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="bdbd4-2248">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2248">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="bdbd4-2249">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2249">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2250">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2250">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2251">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2251">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bdbd4-2252">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2252">Az.StorageSync</span></span>
* <span data-ttu-id="bdbd4-2253">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2253">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="bdbd4-2254">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2254">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2255">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2256">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2256">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="bdbd4-2257">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2257">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="bdbd4-2258">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2258">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="bdbd4-2259">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2259">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2260">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2261">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2261">Add support for profile cmdlets</span></span>
* <span data-ttu-id="bdbd4-2262">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2262">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="bdbd4-2263">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2263">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bdbd4-2264">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2264">Az.Advisor</span></span>
* <span data-ttu-id="bdbd4-2265">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2265">GA release of Az.Advisor</span></span>
* <span data-ttu-id="bdbd4-2266">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2266">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-2267">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2267">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-2268">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2268">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="bdbd4-2269">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2269">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="bdbd4-2270">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2270">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="bdbd4-2271">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2271">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="bdbd4-2272">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2272">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="bdbd4-2273">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2273">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="bdbd4-2274">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2274">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2275">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2276">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2276">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2277">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2278">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2278">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2279">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2279">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2280">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2280">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bdbd4-2281">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2281">Az.EventGrid</span></span>
* <span data-ttu-id="bdbd4-2282">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2282">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-2283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2283">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-2284">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2284">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2285">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2286">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2286">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="bdbd4-2287">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2287">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-2288">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2288">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-2289">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2289">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="bdbd4-2290">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2290">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2291">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2291">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2292">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2292">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2293">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2293">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2294">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2294">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2295">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2295">Az.Resources</span></span>
    - <span data-ttu-id="bdbd4-2296">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2296">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="bdbd4-2297">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2297">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="bdbd4-2298">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2298">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="bdbd4-2299">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2299">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-2300">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2300">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-2301">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2301">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2302">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2303">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2303">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="bdbd4-2304">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2304">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="bdbd4-2305">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2305">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bdbd4-2306">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2306">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bdbd4-2307">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2307">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bdbd4-2308">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2308">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bdbd4-2309">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2309">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bdbd4-2310">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2310">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="bdbd4-2311">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2311">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2312">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2312">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2313">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2313">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="bdbd4-2314">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2314">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="bdbd4-2315">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2315">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="bdbd4-2316">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2316">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="bdbd4-2317">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2317">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="bdbd4-2318">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2318">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bdbd4-2319">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2319">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bdbd4-2320">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2320">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="bdbd4-2321">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2321">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="bdbd4-2322">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2322">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bdbd4-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2323">Az.StorageSync</span></span>
* <span data-ttu-id="bdbd4-2324">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2324">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="bdbd4-2325">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2325">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2326">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2327">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2327">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="bdbd4-2328">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2328">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="bdbd4-2329">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2329">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="bdbd4-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2330">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="bdbd4-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2331">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2332">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2333">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2333">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="bdbd4-2334">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2334">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="bdbd4-2335">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2335">Az.Dns</span></span>
* <span data-ttu-id="bdbd4-2336">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2336">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bdbd4-2337">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2337">Az.EventGrid</span></span>
* <span data-ttu-id="bdbd4-2338">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2338">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="bdbd4-2339">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2339">New cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-2340">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2340">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bdbd4-2341">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2341">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bdbd4-2342">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2342">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bdbd4-2343">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2343">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="bdbd4-2344">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2344">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bdbd4-2345">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2345">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bdbd4-2346">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2346">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bdbd4-2347">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2347">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bdbd4-2348">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2348">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bdbd4-2349">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2349">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="bdbd4-2350">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2350">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bdbd4-2351">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2351">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="bdbd4-2352">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2352">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="bdbd4-2353">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2353">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="bdbd4-2354">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2354">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bdbd4-2355">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2355">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="bdbd4-2356">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2356">Updated cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2357">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="bdbd4-2358">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2358">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bdbd4-2359">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2359">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bdbd4-2360">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2360">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="bdbd4-2361">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2361">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="bdbd4-2362">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2362">Event subscription expiration date,</span></span>
            - <span data-ttu-id="bdbd4-2363">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2363">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="bdbd4-2364">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2364">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="bdbd4-2365">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2365">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="bdbd4-2366">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2366">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="bdbd4-2367">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2367">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="bdbd4-2368">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2368">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="bdbd4-2369">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2369">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="bdbd4-2370">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2370">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-2371">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2371">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-2372">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2372">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="bdbd4-2373">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2373">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="bdbd4-2374">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2374">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="bdbd4-2375">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2375">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2376">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2376">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2377">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2377">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="bdbd4-2378">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2378">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2379">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="bdbd4-2380">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2380">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="bdbd4-2381">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2381">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2382">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2382">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="bdbd4-2383">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2383">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="bdbd4-2384">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2384">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2385">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2385">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bdbd4-2386">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2386">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bdbd4-2387">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2387">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bdbd4-2388">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2388">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="bdbd4-2389">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2389">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bdbd4-2390">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2390">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="bdbd4-2391">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2391">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2392">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2392">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bdbd4-2393">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2393">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bdbd4-2394">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2394">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bdbd4-2395">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2395">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="bdbd4-2396">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2396">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="bdbd4-2397">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2397">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="bdbd4-2398">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2398">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="bdbd4-2399">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2399">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="bdbd4-2400">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2400">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="bdbd4-2401">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2401">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="bdbd4-2402">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2402">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="bdbd4-2403">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2403">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="bdbd4-2404">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2404">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="bdbd4-2405">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2405">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="bdbd4-2406">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2406">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="bdbd4-2407">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2407">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="bdbd4-2408">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2408">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="bdbd4-2409">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2409">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="bdbd4-2410">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2410">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-2411">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2411">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="bdbd4-2412">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2412">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="bdbd4-2413">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2413">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="bdbd4-2414">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2414">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="bdbd4-2415">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2415">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="bdbd4-2416">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2416">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bdbd4-2417">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2417">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bdbd4-2418">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2418">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2419">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2419">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2420">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2420">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2421">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2422">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2422">Support for additional Template Export options</span></span>
    - <span data-ttu-id="bdbd4-2423">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2423">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bdbd4-2424">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2424">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bdbd4-2425">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2425">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-2426">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2426">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-2427">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2427">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2428">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2428">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2429">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2429">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="bdbd4-2430">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2430">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="bdbd4-2431">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2431">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="bdbd4-2432">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2432">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bdbd4-2433">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2433">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bdbd4-2434">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2434">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bdbd4-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2435">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="bdbd4-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2436">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2437">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2437">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2438">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2438">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="bdbd4-2439">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2439">New-AzStorageAccount</span></span>
* <span data-ttu-id="bdbd4-2440">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2440">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="bdbd4-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2441">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2442">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2443">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2443">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="bdbd4-2444">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2444">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="bdbd4-2445">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2445">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="bdbd4-2446">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2446">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-2447">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2447">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2448">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2449">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2449">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="bdbd4-2450">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2450">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-2451">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2451">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-2452">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2452">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="bdbd4-2453">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2453">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2454">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2455">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2455">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="bdbd4-2456">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2456">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-2457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2457">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-2458">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2458">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2459">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2460">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2460">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-2461">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2461">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-2462">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2462">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-2463">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2463">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-2464">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2464">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="bdbd4-2465">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2465">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2466">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2467">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2467">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="bdbd4-2468">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2468">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bdbd4-2469">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2469">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="bdbd4-2470">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2470">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2471">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2471">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2472">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2472">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="bdbd4-2473">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2473">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-2474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2474">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-2475">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2475">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="bdbd4-2476">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2476">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="bdbd4-2477">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2477">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="bdbd4-2478">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2478">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="bdbd4-2479">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2479">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="bdbd4-2480">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2480">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="bdbd4-2481">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2481">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="bdbd4-2482">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2482">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="bdbd4-2483">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2483">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="bdbd4-2484">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2484">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="bdbd4-2485">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2485">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="bdbd4-2486">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2486">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="bdbd4-2487">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2487">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="bdbd4-2488">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2488">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="bdbd4-2489">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2489">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="bdbd4-2490">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2490">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="bdbd4-2491">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2491">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="bdbd4-2492">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2492">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="bdbd4-2493">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2493">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="bdbd4-2494">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2494">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="bdbd4-2495">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2495">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="bdbd4-2496">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2496">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="bdbd4-2497">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2497">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="bdbd4-2498">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2498">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="bdbd4-2499">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2499">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="bdbd4-2500">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2500">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="bdbd4-2501">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2501">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="bdbd4-2502">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2502">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="bdbd4-2503">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2503">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="bdbd4-2504">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2504">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="bdbd4-2505">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2505">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="bdbd4-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2506">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="bdbd4-2507">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2507">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="bdbd4-2508">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2508">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bdbd4-2509">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2509">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="bdbd4-2510">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2510">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="bdbd4-2511">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2511">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="bdbd4-2512">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2512">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="bdbd4-2513">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2513">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="bdbd4-2514">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2514">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bdbd4-2515">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2515">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bdbd4-2516">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2516">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="bdbd4-2517">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2517">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="bdbd4-2518">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2518">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="bdbd4-2519">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2519">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bdbd4-2520">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2520">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bdbd4-2521">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2521">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="bdbd4-2522">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2522">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="bdbd4-2523">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2523">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="bdbd4-2524">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2524">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="bdbd4-2525">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2525">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="bdbd4-2526">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2526">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="bdbd4-2527">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2527">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="bdbd4-2528">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2528">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="bdbd4-2529">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2529">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="bdbd4-2530">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2530">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="bdbd4-2531">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2531">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bdbd4-2532">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2532">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bdbd4-2533">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2533">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bdbd4-2534">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2534">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bdbd4-2535">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2535">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bdbd4-2536">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2536">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bdbd4-2537">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2537">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bdbd4-2538">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2538">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bdbd4-2539">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2539">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="bdbd4-2540">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2540">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="bdbd4-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2541">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="bdbd4-2542">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2542">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="bdbd4-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2543">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="bdbd4-2544">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2544">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="bdbd4-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2545">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="bdbd4-2546">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2546">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="bdbd4-2547">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2547">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="bdbd4-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2548">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="bdbd4-2549">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2549">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="bdbd4-2550">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2550">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="bdbd4-2551">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2551">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2552">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2552">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2553">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2553">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="bdbd4-2554">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2554">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="bdbd4-2555">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2555">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="bdbd4-2556">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2556">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="bdbd4-2557">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2557">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="bdbd4-2558">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2558">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="bdbd4-2559">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2559">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2560">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2561">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2561">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="bdbd4-2562">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2562">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-2563">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2563">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-2564">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2564">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-2565">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2565">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-2566">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2566">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2567">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2568">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2568">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="bdbd4-2569">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2569">Updated cmdlet:</span></span>
        - <span data-ttu-id="bdbd4-2570">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2570">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="bdbd4-2571">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2571">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2572">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2573">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2573">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2574">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2575">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2575">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="bdbd4-2576">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2576">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2577">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2577">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2578">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2578">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-2579">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2579">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-2580">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2580">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="bdbd4-2581">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2581">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2582">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2582">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2583">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2583">Proximity placement group feature.</span></span>
    - <span data-ttu-id="bdbd4-2584">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2584">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="bdbd4-2585">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2585">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="bdbd4-2586">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2586">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="bdbd4-2587">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2587">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="bdbd4-2588">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2588">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="bdbd4-2589">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2589">Breaking changes</span></span>
    - <span data-ttu-id="bdbd4-2590">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2590">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="bdbd4-2591">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2591">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="bdbd4-2592">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2592">Az.DeploymentManager</span></span>
* <span data-ttu-id="bdbd4-2593">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2593">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="bdbd4-2594">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2594">Az.Dns</span></span>
* <span data-ttu-id="bdbd4-2595">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2595">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="bdbd4-2596">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2596">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="bdbd4-2597">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2597">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-2598">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2598">Az.FrontDoor</span></span>
* <span data-ttu-id="bdbd4-2599">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2599">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="bdbd4-2600">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2600">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-2601">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2601">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-2602">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2602">Removed two cmdlets:</span></span>
    - <span data-ttu-id="bdbd4-2603">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2603">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="bdbd4-2604">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2604">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bdbd4-2605">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2605">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bdbd4-2606">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2606">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="bdbd4-2607">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2607">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="bdbd4-2608">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2608">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-2609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2609">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-2610">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2610">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="bdbd4-2611">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2611">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="bdbd4-2612">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2612">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="bdbd4-2613">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2613">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="bdbd4-2614">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2614">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="bdbd4-2615">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2615">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="bdbd4-2616">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2616">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="bdbd4-2617">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2617">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bdbd4-2618">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2618">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bdbd4-2619">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2619">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bdbd4-2620">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2620">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bdbd4-2621">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2621">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bdbd4-2622">SQR API hakkında [daha fazla](/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2622">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="bdbd4-2623">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2623">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2624">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2625">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2625">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="bdbd4-2626">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2626">New cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2627">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2627">New-AzNatGateway</span></span>
        - <span data-ttu-id="bdbd4-2628">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2628">Get-AzNatGateway</span></span>
        - <span data-ttu-id="bdbd4-2629">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2629">Set-AzNatGateway</span></span>
        - <span data-ttu-id="bdbd4-2630">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2630">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="bdbd4-2631">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2631">Updated cmdlets</span></span>
        - <span data-ttu-id="bdbd4-2632">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2632">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="bdbd4-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2633">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="bdbd4-2634">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2634">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="bdbd4-2635">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2635">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="bdbd4-2636">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2636">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-2637">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2637">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-2638">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2638">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="bdbd4-2639">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2639">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="bdbd4-2640">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2640">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2641">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2641">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2642">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2642">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="bdbd4-2643">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2643">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="bdbd4-2644">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2644">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="bdbd4-2645">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2645">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="bdbd4-2646">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2646">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="bdbd4-2647">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2647">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="bdbd4-2648">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2648">Az.Relay</span></span>
* <span data-ttu-id="bdbd4-2649">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2649">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-2650">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2650">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-2651">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2651">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2652">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2652">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2653">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2653">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="bdbd4-2654">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2654">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="bdbd4-2655">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2655">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="bdbd4-2656">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2656">New-AzStorageAccount</span></span>
* <span data-ttu-id="bdbd4-2657">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2657">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="bdbd4-2658">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2658">New-AzStorageAccount</span></span>
    - <span data-ttu-id="bdbd4-2659">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2659">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="bdbd4-2660">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2660">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2661">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2661">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2662">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2662">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="bdbd4-2663">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2663">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="bdbd4-2664">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2664">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-2665">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2665">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-2666">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2666">General availability of `Az` module</span></span>
* <span data-ttu-id="bdbd4-2667">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2667">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bdbd4-2668">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2668">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bdbd4-2669">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2669">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bdbd4-2670">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2670">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bdbd4-2671">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2671">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2672">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2672">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2673">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2674">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2674">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bdbd4-2675">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2675">Az.Batch</span></span>
* <span data-ttu-id="bdbd4-2676">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2676">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-2677">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2677">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-2678">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2678">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-2679">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2679">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-2680">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2680">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2681">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2682">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2682">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="bdbd4-2683">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2683">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2684">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2684">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2685">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2686">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2686">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-2687">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2687">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-2688">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2688">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bdbd4-2689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2689">Az.EventGrid</span></span>
* <span data-ttu-id="bdbd4-2690">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2690">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-2691">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2691">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-2692">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2692">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bdbd4-2693">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2693">Az.HDInsight</span></span>
* <span data-ttu-id="bdbd4-2694">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-2695">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2695">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-2696">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-2697">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2697">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-2698">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2699">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2699">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bdbd4-2700">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2700">Az.MachineLearning</span></span>
* <span data-ttu-id="bdbd4-2701">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="bdbd4-2702">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2702">Az.Media</span></span>
* <span data-ttu-id="bdbd4-2703">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2703">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-2704">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2704">Az.Monitor</span></span>
  * <span data-ttu-id="bdbd4-2705">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2705">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="bdbd4-2706">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2706">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="bdbd4-2707">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2707">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="bdbd4-2708">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2708">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bdbd4-2709">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2709">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bdbd4-2710">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2710">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="bdbd4-2711">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2711">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2712">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2713">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2713">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2714">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2714">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="bdbd4-2715">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2715">Az.NotificationHubs</span></span>
* <span data-ttu-id="bdbd4-2716">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2717">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2717">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2718">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2718">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="bdbd4-2719">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2719">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="bdbd4-2720">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2720">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2721">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2721">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2722">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2722">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2723">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2723">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="bdbd4-2724">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2724">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="bdbd4-2725">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2725">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bdbd4-2726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2726">Az.RedisCache</span></span>
* <span data-ttu-id="bdbd4-2727">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2727">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2728">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2729">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2729">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2730">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2730">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2731">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2731">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="bdbd4-2732">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2732">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2733">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2733">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="bdbd4-2734">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2734">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="bdbd4-2735">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2735">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="bdbd4-2736">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2736">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="bdbd4-2737">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2737">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2738">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2739">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2739">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="bdbd4-2740">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bdbd4-2741">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2741">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="bdbd4-2742">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2742">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="bdbd4-2743">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2743">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-2744">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2744">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-2745">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2745">General availability of `Az` module</span></span>
* <span data-ttu-id="bdbd4-2746">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2746">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bdbd4-2747">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2747">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bdbd4-2748">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2748">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bdbd4-2749">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2749">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bdbd4-2750">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2750">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2751">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2751">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2752">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2752">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2753">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2753">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-2754">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2754">Az.AnalysisServices</span></span>
* <span data-ttu-id="bdbd4-2755">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2755">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="bdbd4-2756">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2756">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2757">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2757">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2758">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2758">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="bdbd4-2759">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2759">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="bdbd4-2760">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2760">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2761">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2761">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2762">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2762">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bdbd4-2763">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2763">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="bdbd4-2764">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2764">Az.ContainerInstance</span></span>
* <span data-ttu-id="bdbd4-2765">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2765">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2766">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2766">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2767">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2767">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="bdbd4-2768">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2768">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2769">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2769">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2770">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2770">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="bdbd4-2771">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2771">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="bdbd4-2772">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2772">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="bdbd4-2773">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2773">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="bdbd4-2774">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2774">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="bdbd4-2775">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2775">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2776">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2777">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2777">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2778">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2778">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2779">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2779">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="bdbd4-2780">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2780">New-AzStorageContext</span></span>
* <span data-ttu-id="bdbd4-2781">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2781">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="bdbd4-2782">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2782">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bdbd4-2783">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2783">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bdbd4-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2784">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="bdbd4-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2785">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="bdbd4-2786">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2786">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="bdbd4-2787">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2787">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bdbd4-2788">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2788">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bdbd4-2789">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2789">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="bdbd4-2790">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2790">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="bdbd4-2791">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2791">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bdbd4-2792">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2792">Highlights since the last major release</span></span>
* <span data-ttu-id="bdbd4-2793">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2793">General availability of `Az` module</span></span>
* <span data-ttu-id="bdbd4-2794">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2794">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bdbd4-2795">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2795">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bdbd4-2796">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2796">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bdbd4-2797">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2797">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bdbd4-2798">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2798">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2799">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2799">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2800">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2800">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2801">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2801">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="bdbd4-2802">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2802">Dynamic grouping</span></span>
    * <span data-ttu-id="bdbd4-2803">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2803">Pre-Post script</span></span>
    * <span data-ttu-id="bdbd4-2804">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2804">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2805">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2806">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2806">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="bdbd4-2807">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2807">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-2808">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2808">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-2809">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2809">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2810">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2810">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2811">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2811">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="bdbd4-2812">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2812">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2813">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2814">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2814">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="bdbd4-2815">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2815">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2816">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2816">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2817">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2817">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="bdbd4-2818">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2818">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2819">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2819">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2820">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2820">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2821">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2822">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2822">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="bdbd4-2823">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2823">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bdbd4-2824">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2824">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bdbd4-2825">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2825">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bdbd4-2826">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2826">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="bdbd4-2827">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2827">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="bdbd4-2828">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2828">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2829">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2830">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2830">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="bdbd4-2831">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2831">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2832">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2832">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2833">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2833">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="bdbd4-2834">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2834">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2835">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2835">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2836">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2836">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="bdbd4-2837">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2837">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="bdbd4-2838">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2838">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-2839">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2839">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-2840">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2840">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2841">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2841">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2842">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2842">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2843">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2843">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2844">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2844">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bdbd4-2845">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2845">Az.LogicApp</span></span>
* <span data-ttu-id="bdbd4-2846">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2846">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2847">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2848">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2848">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2849">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2850">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2850">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="bdbd4-2851">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2851">SDK Update</span></span>
* <span data-ttu-id="bdbd4-2852">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2852">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="bdbd4-2853">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2853">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2854">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2855">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2855">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="bdbd4-2856">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2856">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="bdbd4-2857">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2857">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="bdbd4-2858">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2858">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="bdbd4-2859">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2859">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="bdbd4-2860">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2860">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2861">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2861">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2862">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2862">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="bdbd4-2863">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2863">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2864">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2865">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2865">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="bdbd4-2866">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2866">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-2867">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2867">Az.AnalysisServices</span></span>
* <span data-ttu-id="bdbd4-2868">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2868">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2869">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2869">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2870">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2870">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="bdbd4-2871">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2871">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="bdbd4-2872">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2872">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-2873">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2873">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-2874">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2874">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2875">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2875">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2876">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2876">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="bdbd4-2877">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2877">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="bdbd4-2878">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2878">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="bdbd4-2879">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2879">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-2880">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2880">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-2881">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2881">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bdbd4-2882">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2882">Az.EventHub</span></span>
* <span data-ttu-id="bdbd4-2883">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2883">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-2884">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2884">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-2885">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2885">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bdbd4-2886">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2886">Az.LogicApp</span></span>
* <span data-ttu-id="bdbd4-2887">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2887">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="bdbd4-2888">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2888">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="bdbd4-2889">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2889">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="bdbd4-2890">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2890">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bdbd4-2891">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2891">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bdbd4-2892">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2892">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bdbd4-2893">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2893">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="bdbd4-2894">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2894">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="bdbd4-2895">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2895">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bdbd4-2896">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2896">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bdbd4-2897">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2897">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bdbd4-2898">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2898">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="bdbd4-2899">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2899">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bdbd4-2900">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2900">Az.Monitor</span></span>
* <span data-ttu-id="bdbd4-2901">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2901">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2902">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2902">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2903">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2903">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-2904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2904">Az.OperationalInsights</span></span>
* <span data-ttu-id="bdbd4-2905">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2905">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="bdbd4-2906">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2906">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="bdbd4-2907">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2907">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2908">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2909">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2909">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bdbd4-2910">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2910">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="bdbd4-2911">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2911">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="bdbd4-2912">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2912">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2913">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2914">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2914">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="bdbd4-2915">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2915">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-2916">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2916">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-2917">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2917">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="bdbd4-2918">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2918">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2919">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2919">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2920">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2920">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-2921">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2921">Az.AnalysisServices</span></span>
<span data-ttu-id="bdbd4-2922">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2922">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2923">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2924">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2924">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="bdbd4-2925">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2925">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="bdbd4-2926">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2926">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2927">Az.RecoveryServices</span></span>
<span data-ttu-id="bdbd4-2928">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2928">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2929">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2930">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2930">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="bdbd4-2931">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2931">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bdbd4-2932">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2932">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="bdbd4-2933">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2933">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2934">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2934">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2935">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2935">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="bdbd4-2936">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2936">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="bdbd4-2937">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2937">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="bdbd4-2938">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2938">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2939">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2940">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2940">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bdbd4-2941">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2941">Az.AnalysisServices</span></span>
* <span data-ttu-id="bdbd4-2942">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2942">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-2943">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2943">Az.RecoveryServices</span></span>
* <span data-ttu-id="bdbd4-2944">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2944">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="bdbd4-2945">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2945">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-2946">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2946">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-2947">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2947">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bdbd4-2948">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2948">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bdbd4-2949">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2949">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="bdbd4-2950">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2950">Az.Aks</span></span>
* <span data-ttu-id="bdbd4-2951">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2951">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bdbd4-2952">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2952">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-2953">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2953">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="bdbd4-2954">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2954">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bdbd4-2955">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2955">Az.Cdn</span></span>
* <span data-ttu-id="bdbd4-2956">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2956">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-2957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2957">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-2958">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2958">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="bdbd4-2959">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2959">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="bdbd4-2960">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2960">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bdbd4-2961">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2961">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bdbd4-2962">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2962">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bdbd4-2963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2963">Az.DataFactory</span></span>
* <span data-ttu-id="bdbd4-2964">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2964">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-2965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2965">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-2966">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2966">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="bdbd4-2967">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2967">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="bdbd4-2968">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2968">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-2969">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2969">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-2970">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2970">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-2971">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2971">Az.KeyVault</span></span>
* <span data-ttu-id="bdbd4-2972">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2972">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2973">Az.Network</span></span>
* <span data-ttu-id="bdbd4-2974">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2974">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-2975">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2975">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-2976">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2976">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="bdbd4-2977">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2977">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="bdbd4-2978">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2978">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="bdbd4-2979">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2979">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="bdbd4-2980">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2980">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="bdbd4-2981">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2981">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="bdbd4-2982">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2982">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-2983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2983">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-2984">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2984">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="bdbd4-2985">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2985">Fix some error messages.</span></span>
* <span data-ttu-id="bdbd4-2986">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2986">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="bdbd4-2987">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2987">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bdbd4-2988">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2988">Az.SignalR</span></span>
* <span data-ttu-id="bdbd4-2989">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2989">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-2990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2990">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-2991">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2991">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bdbd4-2992">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2992">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="bdbd4-2993">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2993">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="bdbd4-2994">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2994">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-2995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2995">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-2996">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2996">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bdbd4-2997">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2997">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="bdbd4-2998">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2998">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="bdbd4-2999">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bdbd4-2999">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="bdbd4-3000">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3000">Az.TrafficManager</span></span>
* <span data-ttu-id="bdbd4-3001">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3001">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-3002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3002">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-3003">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3003">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bdbd4-3004">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3004">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="bdbd4-3005">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3005">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="bdbd4-3006">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3006">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bdbd4-3007">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3007">Az.Accounts</span></span>
* <span data-ttu-id="bdbd4-3008">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3008">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-3009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3009">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-3010">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3010">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="bdbd4-3011">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3011">Updated the description of ID in help files</span></span>
* <span data-ttu-id="bdbd4-3012">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3012">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-3013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3013">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-3014">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3014">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="bdbd4-3015">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3015">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bdbd4-3016">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3016">Az.EventGrid</span></span>
* <span data-ttu-id="bdbd4-3017">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3017">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="bdbd4-3018">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3018">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="bdbd4-3019">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3019">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bdbd4-3020">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3020">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bdbd4-3021">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3021">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bdbd4-3022">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3022">Dead letter endpoint.</span></span>
    - <span data-ttu-id="bdbd4-3023">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3023">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bdbd4-3024">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3024">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bdbd4-3025">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3025">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bdbd4-3026">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3026">Dead letter endpoint.</span></span>
* <span data-ttu-id="bdbd4-3027">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3027">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="bdbd4-3028">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3028">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bdbd4-3029">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3029">Az.IotHub</span></span>
* <span data-ttu-id="bdbd4-3030">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3030">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bdbd4-3031">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3031">Az.LogicApp</span></span>
* <span data-ttu-id="bdbd4-3032">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3032">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-3033">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3033">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-3034">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3034">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="bdbd4-3035">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3035">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="bdbd4-3036">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3036">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bdbd4-3037">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3037">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="bdbd4-3038">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3038">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="bdbd4-3039">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3039">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bdbd4-3040">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3040">Az.SignalR</span></span>
* <span data-ttu-id="bdbd4-3041">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3041">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3042">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-3043">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3043">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bdbd4-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3044">Az.Storage</span></span>
* <span data-ttu-id="bdbd4-3045">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3045">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="bdbd4-3046">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3046">New-AzStorageContext</span></span>
* <span data-ttu-id="bdbd4-3047">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3047">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="bdbd4-3048">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3048">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-3049">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3049">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-3050">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3050">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="bdbd4-3051">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3051">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="bdbd4-3052">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3052">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="bdbd4-3053">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3053">General</span></span>

- <span data-ttu-id="bdbd4-3054">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3054">General Availability of Az Module</span></span>
- <span data-ttu-id="bdbd4-3055">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3055">Online help for each module</span></span>
- <span data-ttu-id="bdbd4-3056">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3056">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="bdbd4-3057">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3057">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="bdbd4-3058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3058">Az.Accounts</span></span>
- <span data-ttu-id="bdbd4-3059">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3059">Changed from Az.Profile</span></span>
- <span data-ttu-id="bdbd4-3060">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3060">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-3061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3061">Az.ApiManagement</span></span>
- <span data-ttu-id="bdbd4-3062">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3062">Fixes for #7002</span></span>
- <span data-ttu-id="bdbd4-3063">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="bdbd4-3064">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3064">Az.Batch</span></span>
- <span data-ttu-id="bdbd4-3065">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3065">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="bdbd4-3066">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3066">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="bdbd4-3067">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3067">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="bdbd4-3068">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3068">Az.Billing</span></span>
- <span data-ttu-id="bdbd4-3069">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3069">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="bdbd4-3070">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3070">Az.CognitivServices</span></span>
- <span data-ttu-id="bdbd4-3071">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3071">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="bdbd4-3072">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3072">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bdbd4-3073">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3073">Az.ContainerInstance</span></span>
- <span data-ttu-id="bdbd4-3074">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3074">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="bdbd4-3075">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3075">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="bdbd4-3076">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3076">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-3077">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3077">Az.DataLakeStore</span></span>
- <span data-ttu-id="bdbd4-3078">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3078">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="bdbd4-3079">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3079">Az.Monitor</span></span>
- <span data-ttu-id="bdbd4-3080">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3080">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="bdbd4-3081">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3081">Az.KeyVault</span></span>
- <span data-ttu-id="bdbd4-3082">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3082">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="bdbd4-3083">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3083">Az.MachineLearning</span></span>
- <span data-ttu-id="bdbd4-3084">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3084">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="bdbd4-3085">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3085">Az.Media</span></span>
- <span data-ttu-id="bdbd4-3086">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3086">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bdbd4-3087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3087">Az.Network</span></span>
<span data-ttu-id="bdbd4-3088">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3088">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="bdbd4-3089">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3089">New cmdlets added:</span></span>
        - <span data-ttu-id="bdbd4-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3090">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3091">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3092">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3093">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3094">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3095">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3095">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="bdbd4-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3096">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="bdbd4-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3097">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="bdbd4-3098">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3098">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="bdbd4-3099">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3099">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="bdbd4-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3100">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bdbd4-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bdbd4-3102">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3102">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="bdbd4-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3103">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="bdbd4-3104">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3104">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="bdbd4-3105">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3105">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="bdbd4-3106">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3106">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bdbd4-3107">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3107">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bdbd4-3108">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3108">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="bdbd4-3109">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3109">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="bdbd4-3110">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3110">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="bdbd4-3111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3111">Az.OperationalInsights</span></span>
- <span data-ttu-id="bdbd4-3112">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="bdbd4-3113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3113">Az.Profile</span></span>
- <span data-ttu-id="bdbd4-3114">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3114">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-3115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3115">Az.RecoveryServices</span></span>
- <span data-ttu-id="bdbd4-3116">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="bdbd4-3117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3117">Az.Resources</span></span>
- <span data-ttu-id="bdbd4-3118">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3118">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-3119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3119">Az.ServiceFabric</span></span>
- <span data-ttu-id="bdbd4-3120">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3120">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="bdbd4-3121">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3121">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="bdbd4-3122">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3122">Az.SIgnalR</span></span>
- <span data-ttu-id="bdbd4-3123">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3123">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="bdbd4-3124">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3124">Az.Sql</span></span>
- <span data-ttu-id="bdbd4-3125">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3125">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="bdbd4-3126">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3126">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="bdbd4-3127">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="bdbd4-3128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3128">Az.Storage</span></span>
- <span data-ttu-id="bdbd4-3129">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3129">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bdbd4-3130">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3130">Az.Websites</span></span>
- <span data-ttu-id="bdbd4-3131">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3131">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="bdbd4-3132">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3132">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="bdbd4-3133">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3133">General</span></span>

* <span data-ttu-id="bdbd4-3134">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3134">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="bdbd4-3135">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3135">Az.Compute</span></span>

* <span data-ttu-id="bdbd4-3136">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3136">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-3137">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3137">Az.DataLakeStore</span></span>

* <span data-ttu-id="bdbd4-3138">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3138">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="bdbd4-3139">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3139">Az.FrontDoor</span></span>

* <span data-ttu-id="bdbd4-3140">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3140">Fixed some broken links</span></span>
    - <span data-ttu-id="bdbd4-3141">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3141">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="bdbd4-3142">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3142">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bdbd4-3143">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3143">Az.RecoveryServices</span></span>

* <span data-ttu-id="bdbd4-3144">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3144">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="bdbd4-3145">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3145">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="bdbd4-3146">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3146">Az.Resources</span></span>

* <span data-ttu-id="bdbd4-3147"> https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3147">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="bdbd4-3148">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3148">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="bdbd4-3149">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3149">Az.Sql</span></span>

* <span data-ttu-id="bdbd4-3150">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3150">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="bdbd4-3151">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3151">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="bdbd4-3152">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3152">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="bdbd4-3153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3153">Az.Storage</span></span>

* <span data-ttu-id="bdbd4-3154">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3154">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="bdbd4-3155">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3155">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="bdbd4-3156">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3156">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bdbd4-3157">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3157">Support Static Website configuration</span></span>
    - <span data-ttu-id="bdbd4-3158">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3158">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="bdbd4-3159">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3159">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bdbd4-3160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3160">Az.Websites</span></span>

* <span data-ttu-id="bdbd4-3161">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3161">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="bdbd4-3162">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3162">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="bdbd4-3163">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3163">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="bdbd4-3164">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3164">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bdbd4-3165">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3165">Az.ApiManagement</span></span>
* <span data-ttu-id="bdbd4-3166">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3166">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="bdbd4-3167">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3167">Az.Automation</span></span>
* <span data-ttu-id="bdbd4-3168">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3168">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="bdbd4-3169">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3169">Added Update Management cmdlets</span></span>
* <span data-ttu-id="bdbd4-3170">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3170">Added Source Control cmdlets</span></span>
* <span data-ttu-id="bdbd4-3171">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3171">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="bdbd4-3172">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3172">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="bdbd4-3173">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3173">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-3174">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3174">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="bdbd4-3175">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3175">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bdbd4-3176">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3176">Az.ContainerInstance</span></span>
* <span data-ttu-id="bdbd4-3177">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3177">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="bdbd4-3178">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3178">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bdbd4-3179">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3179">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bdbd4-3180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3180">Az.Network</span></span>
* <span data-ttu-id="bdbd4-3181">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3181">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="bdbd4-3182">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3182">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="bdbd4-3183">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3183">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="bdbd4-3184">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3184">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="bdbd4-3185">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3185">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bdbd4-3186">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3186">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="bdbd4-3187">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3187">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="bdbd4-3188">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3188">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bdbd4-3189">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3189">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="bdbd4-3190">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3190">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="bdbd4-3191">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3191">Az.Relay</span></span>
* <span data-ttu-id="bdbd4-3192">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3192">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="bdbd4-3193">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3193">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-3194">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3194">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="bdbd4-3195">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3195">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="bdbd4-3196">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3196">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-3197">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3197">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-3198">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3198">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="bdbd4-3199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3199">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-3200">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3200">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="bdbd4-3201">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3201">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdbd4-3202">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3202">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdbd4-3203">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3203">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdbd4-3204">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3204">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bdbd4-3205">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3205">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdbd4-3206">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3206">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdbd4-3207">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3207">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bdbd4-3208">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3208">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="bdbd4-3209">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3209">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="bdbd4-3210">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3210">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="bdbd4-3211">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3211">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="bdbd4-3212">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3212">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bdbd4-3213">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3213">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bdbd4-3214">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3214">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="bdbd4-3215">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3215">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="bdbd4-3216">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3216">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="bdbd4-3217">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3217">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bdbd4-3218">Genel</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3218">General</span></span>
* <span data-ttu-id="bdbd4-3219">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3219">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="bdbd4-3220">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3220">Az.Profile</span></span>
* <span data-ttu-id="bdbd4-3221">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3221">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="bdbd4-3222">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3222">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="bdbd4-3223">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3223">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="bdbd4-3224">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3224">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="bdbd4-3225">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3225">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="bdbd4-3226">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3226">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="bdbd4-3227">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3227">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-3228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3228">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-3229">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3229">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-3230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3230">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-3231">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3231">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="bdbd4-3232">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3232">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="bdbd4-3233">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3233">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-3234">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3234">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-3235">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3235">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="bdbd4-3236">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3236">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="bdbd4-3237">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3237">Az.Insights</span></span>
* <span data-ttu-id="bdbd4-3238">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3238">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="bdbd4-3239">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3239">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="bdbd4-3240">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3240">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="bdbd4-3241">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3241">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-3242">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3242">Az.Network</span></span>
* <span data-ttu-id="bdbd4-3243">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3243">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="bdbd4-3244">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3244">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="bdbd4-3245">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3245">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="bdbd4-3246">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3246">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="bdbd4-3247">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3247">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bdbd4-3248">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3248">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bdbd4-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3249">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bdbd4-3250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3250">Az.PolicyInsights</span></span>
* <span data-ttu-id="bdbd4-3251">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3251">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-3252">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3252">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-3253"> https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3253">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="bdbd4-3254">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3254">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bdbd4-3255">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3255">Az.ServiceBus</span></span>
* <span data-ttu-id="bdbd4-3256">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3256">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bdbd4-3257">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3257">Az.ServiceFabric</span></span>
* <span data-ttu-id="bdbd4-3258">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3258">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="bdbd4-3259">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3259">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="bdbd4-3260">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3260">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="bdbd4-3261">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3261">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="bdbd4-3262">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3262">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="bdbd4-3263">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3263">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="bdbd4-3264">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3264">Az.Profile</span></span>
* <span data-ttu-id="bdbd4-3265">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3265">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="bdbd4-3266">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3266">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-3267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3267">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-3268">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3268">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="bdbd4-3269">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3269">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bdbd4-3270">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3270">Az.DataLakeStore</span></span>
* <span data-ttu-id="bdbd4-3271">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3271">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="bdbd4-3272">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3272">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="bdbd4-3273">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3273">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bdbd4-3274">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3274">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bdbd4-3275">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3275">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-3276">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3276">Az.Network</span></span>
* <span data-ttu-id="bdbd4-3277">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3277">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="bdbd4-3278">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3278">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-3279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3279">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-3280">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3280">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="bdbd4-3281">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3281">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="bdbd4-3282">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3282">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="bdbd4-3283">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3283">Azure.Storage</span></span>
* <span data-ttu-id="bdbd4-3284">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3284">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="bdbd4-3285">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3285">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="bdbd4-3286">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3286">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bdbd4-3287">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3287">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="bdbd4-3288">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3288">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bdbd4-3289">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3289">Az.CognitiveServices</span></span>
* <span data-ttu-id="bdbd4-3290">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3290">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bdbd4-3291">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3291">Az.Compute</span></span>
* <span data-ttu-id="bdbd4-3292">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3292">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="bdbd4-3293">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3293">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="bdbd4-3294">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3294">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="bdbd4-3295">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3295">Az.DataFactoryV2</span></span>
* <span data-ttu-id="bdbd4-3296">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3296">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bdbd4-3297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3297">Az.Network</span></span>
* <span data-ttu-id="bdbd4-3298">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3298">Added NetworkProfile functionality.</span></span> <span data-ttu-id="bdbd4-3299">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3299">new cmdlets added</span></span>
    - <span data-ttu-id="bdbd4-3300">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3300">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="bdbd4-3301">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3301">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="bdbd4-3302">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3302">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="bdbd4-3303">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3303">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="bdbd4-3304">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3304">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="bdbd4-3305">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3305">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="bdbd4-3306">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3306">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="bdbd4-3307">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3307">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="bdbd4-3308">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3308">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bdbd4-3309">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3309">Az.RedisCache</span></span>
* <span data-ttu-id="bdbd4-3310">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3310">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="bdbd4-3311">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3311">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="bdbd4-3312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3312">Az.Resources</span></span>
* <span data-ttu-id="bdbd4-3313">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3313">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bdbd4-3314">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3314">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="bdbd4-3315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3315">Az.Sql</span></span>
* <span data-ttu-id="bdbd4-3316">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3316">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bdbd4-3317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3317">Az.Websites</span></span>
* <span data-ttu-id="bdbd4-3318">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3318">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="bdbd4-3319">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3319">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="bdbd4-3320">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3320">0.2.0 - September 2018</span></span>
 <span data-ttu-id="bdbd4-3321">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="bdbd4-3321">Initial Release</span></span>