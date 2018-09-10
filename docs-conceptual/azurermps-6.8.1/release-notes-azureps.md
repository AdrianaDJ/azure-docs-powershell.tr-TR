---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383847"
---
# <a name="release-notes"></a><span data-ttu-id="3d19b-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="3d19b-103">Release notes</span></span>

<span data-ttu-id="3d19b-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3d19b-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="3d19b-105">6.8.1 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d19b-106">Genel</span><span class="sxs-lookup"><span data-stu-id="3d19b-106">General</span></span>
* <span data-ttu-id="3d19b-107">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d19b-108">Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d19b-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d19b-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d19b-110">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d19b-111">https://github.com/Azure/azure-powershell/issues/6603 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="3d19b-112">Import-AzureRmApiManagementApi ve \*-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor</span><span class="sxs-lookup"><span data-stu-id="3d19b-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="3d19b-113">https://github.com/Azure/azure-powershell/issues/6879 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="3d19b-114">CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="3d19b-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="3d19b-115">4.0.4-preview nuget’e yükselterek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="3d19b-116">https://github.com/Azure/azure-powershell/issues/6853 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="3d19b-117">Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="3d19b-118">https://github.com/Azure/azure-powershell/issues/6814 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="3d19b-119">Odata filtresi API üzerinde Ada Göre Arama için düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="3d19b-120">Azure İzleyici günlükçüsüne yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-121">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-122">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3d19b-123">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3d19b-124">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d19b-125">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-126">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-127">Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d19b-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d19b-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d19b-129">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="3d19b-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-130">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-131">Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-133">Düzeltilen sorunlar</span><span class="sxs-lookup"><span data-stu-id="3d19b-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d19b-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d19b-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d19b-135">Çoklu değer yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3d19b-136">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="3d19b-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3d19b-137">Alt ağ yönlendirme yöntemi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3d19b-138">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3d19b-139">Profillerde Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3d19b-140">Profillerde Beklenen durum kodu aralığı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3d19b-141">Uç noktalarda Özel Üst Bilgi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="3d19b-142">6.8.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d19b-143">Genel</span><span class="sxs-lookup"><span data-stu-id="3d19b-143">General</span></span>
* <span data-ttu-id="3d19b-144">Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-145">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-146">Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-147">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-148">Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3d19b-149">Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3d19b-150">Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3d19b-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="3d19b-152">New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri</span><span class="sxs-lookup"><span data-stu-id="3d19b-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-153">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-154">Varsayılan model gösterimi tablo görünümü olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d19b-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d19b-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d19b-156">Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-157">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-158">Marketten yönetilen uygulamayla ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-160">Sorunlar için düzeltme</span><span class="sxs-lookup"><span data-stu-id="3d19b-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d19b-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d19b-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d19b-162">Çoklu değer yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3d19b-163">Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi</span><span class="sxs-lookup"><span data-stu-id="3d19b-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3d19b-164">Alt ağ yönlendirme yöntemi desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3d19b-165">Uç noktalarda IP adresi aralıkları (alt ağları) desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3d19b-166">Profillerde Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3d19b-167">Profillerde Beklenen durum kodu aralığı desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3d19b-168">Uç noktalarda Özel Üst Bilgi desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d19b-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d19b-169">AzureRM.Websites</span></span>
* <span data-ttu-id="3d19b-170">Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="3d19b-171">6.7.0 - Ağustos 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-172">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-173">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d19b-174">Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="3d19b-175">Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="3d19b-176">'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="3d19b-177">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3d19b-177">Azure.Storage</span></span>
* <span data-ttu-id="3d19b-178">Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3d19b-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="3d19b-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3d19b-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d19b-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d19b-181">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="3d19b-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="3d19b-183">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d19b-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d19b-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d19b-185">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="3d19b-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3d19b-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="3d19b-187">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3d19b-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3d19b-188">AzureRM.Automation</span></span>
* <span data-ttu-id="3d19b-189">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="3d19b-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="3d19b-190">AzureRM.Backup</span></span>
* <span data-ttu-id="3d19b-191">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3d19b-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3d19b-192">AzureRM.Batch</span></span>
* <span data-ttu-id="3d19b-193">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="3d19b-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="3d19b-194">AzureRM.Billing</span></span>
* <span data-ttu-id="3d19b-195">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="3d19b-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d19b-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="3d19b-197">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3d19b-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3d19b-199">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-200">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-201">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d19b-202">New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="3d19b-203">Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.</span><span class="sxs-lookup"><span data-stu-id="3d19b-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="3d19b-204">Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3d19b-205">Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3d19b-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3d19b-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="3d19b-207">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="3d19b-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3d19b-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="3d19b-209">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="3d19b-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d19b-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="3d19b-211">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="3d19b-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="3d19b-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="3d19b-213">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d19b-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d19b-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d19b-215">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3d19b-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d19b-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3d19b-217">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d19b-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d19b-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d19b-219">DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="3d19b-220">Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3d19b-221">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d19b-222">Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="3d19b-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="3d19b-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="3d19b-224">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="3d19b-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="3d19b-225">AzureRM.Dns</span></span>
* <span data-ttu-id="3d19b-226">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3d19b-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d19b-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3d19b-228">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d19b-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d19b-230">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="3d19b-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3d19b-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="3d19b-232">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d19b-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d19b-233">AzureRM.Insights</span></span>
* <span data-ttu-id="3d19b-234">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3d19b-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="3d19b-236">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-238">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3d19b-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d19b-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3d19b-240">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="3d19b-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3d19b-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="3d19b-242">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="3d19b-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3d19b-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="3d19b-244">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="3d19b-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3d19b-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="3d19b-246">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="3d19b-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="3d19b-247">AzureRM.Media</span></span>
* <span data-ttu-id="3d19b-248">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-249">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-250">Set-AzureRmLocalNetworkGateway örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="3d19b-251">Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3d19b-252">Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="3d19b-253">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3d19b-254">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3d19b-255">Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3d19b-256">ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3d19b-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="3d19b-257">Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="3d19b-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3d19b-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="3d19b-259">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="3d19b-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d19b-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3d19b-261">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3d19b-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d19b-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3d19b-263">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d19b-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d19b-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d19b-265">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="3d19b-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="3d19b-267">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d19b-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d19b-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d19b-269">Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="3d19b-270">Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="3d19b-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="3d19b-271">Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="3d19b-272">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d19b-273">Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="3d19b-274">Yönetilen disklerin geri yüklendiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3d19b-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3d19b-275">Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3d19b-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="3d19b-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3d19b-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3d19b-277">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3d19b-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d19b-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3d19b-279">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3d19b-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3d19b-280">AzureRM.Relay</span></span>
* <span data-ttu-id="3d19b-281">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-282">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-283">Abonelik kapsamındaki şablon dağıtımı destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="3d19b-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="3d19b-284">Yeni Cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="3d19b-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d19b-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d19b-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d19b-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d19b-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d19b-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3d19b-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="3d19b-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="3d19b-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="3d19b-292">Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="3d19b-293">New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="3d19b-294">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3d19b-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3d19b-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3d19b-296">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-298">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d19b-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d19b-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d19b-300">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-301">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-302">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d19b-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d19b-303">AzureRM.Storage</span></span>
* <span data-ttu-id="3d19b-304">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="3d19b-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d19b-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="3d19b-306">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3d19b-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3d19b-307">AzureRM.Tags</span></span>
* <span data-ttu-id="3d19b-308">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d19b-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d19b-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d19b-310">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="3d19b-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="3d19b-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="3d19b-312">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d19b-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d19b-313">AzureRM.Websites</span></span>
* <span data-ttu-id="3d19b-314">Azure ClientRuntime'ın en son sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="3d19b-315">6.6.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d19b-316">Genel</span><span class="sxs-lookup"><span data-stu-id="3d19b-316">General</span></span>
* <span data-ttu-id="3d19b-317">Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-318">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-319">Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="3d19b-320">Common.Storage'a ps1xml türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d19b-321">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3d19b-321">Azure.Storage</span></span>
* <span data-ttu-id="3d19b-322">DefaultProfile’dan Depolama Bağlamı almak için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="3d19b-323">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d19b-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d19b-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d19b-325">https://github.com/Azure/azure-powershell/issues/6370 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="3d19b-326">PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="3d19b-327">https://github.com/Azure/azure-powershell/issues/6515 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="3d19b-328">Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="3d19b-329">https://github.com/Azure/azure-powershell/issues/6560 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="3d19b-330">apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-331">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-332">PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="3d19b-333">Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="3d19b-334">Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="3d19b-335">(ResouceGroupName parametresi artık isteğe bağlı.)</span><span class="sxs-lookup"><span data-stu-id="3d19b-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="3d19b-336">Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="3d19b-337">Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="3d19b-338">New-AzureRmDisk örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="3d19b-339">'New-AzureRmVM' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="3d19b-340">Set-AzureRmVMOSDisk açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="3d19b-341">Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d19b-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d19b-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d19b-343">ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="3d19b-344">Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.</span><span class="sxs-lookup"><span data-stu-id="3d19b-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="3d19b-345">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="3d19b-346">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d19b-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d19b-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d19b-348">DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d19b-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d19b-350">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d19b-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d19b-351">AzureRM.Insights</span></span>
* <span data-ttu-id="3d19b-352">Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="3d19b-353">Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı</span><span class="sxs-lookup"><span data-stu-id="3d19b-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-355">Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-356">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-357">LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-358">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-359">'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="3d19b-360">'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-362">Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="3d19b-363">birkaç sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-364">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-365">Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="3d19b-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="3d19b-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3d19b-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3d19b-367">Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="3d19b-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="3d19b-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="3d19b-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="3d19b-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="3d19b-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="3d19b-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="3d19b-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="3d19b-371">Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="3d19b-372">Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d19b-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d19b-373">AzureRM.Storage</span></span>
* <span data-ttu-id="3d19b-374">Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="3d19b-375">Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="3d19b-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="3d19b-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d19b-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3d19b-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d19b-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3d19b-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d19b-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3d19b-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3d19b-379">AzureRM.Tags</span></span>
* <span data-ttu-id="3d19b-380">Tag cmdlet'inin yardımında hatayı deyim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3d19b-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="3d19b-381">6.5.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-382">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-383">'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d19b-384">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3d19b-384">Azure.Storage</span></span>
* <span data-ttu-id="3d19b-385">Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği</span><span class="sxs-lookup"><span data-stu-id="3d19b-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="3d19b-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3d19b-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="3d19b-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3d19b-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d19b-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d19b-389">AS'ye gerekli ResourceGroupName özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3d19b-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3d19b-390">AzureRM.Automation</span></span>
* <span data-ttu-id="3d19b-391">'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-392">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-393">Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="3d19b-394">'Add-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3d19b-395">'Remove-AzureRmVmssExtension' için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3d19b-396">'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="3d19b-397">New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d19b-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d19b-399">PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-401">Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3d19b-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d19b-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3d19b-403">New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-404">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-405">Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="3d19b-406">Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="3d19b-407">New-AzureRmApplicationGateway : EnableFIPS bayrağı ve Zones desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="3d19b-408">New-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="3d19b-409">Set-AzureRmApplicationGatewaySku : Yeni Standard_v2 ve WAF_v2 sku'ları eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="3d19b-410">RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3d19b-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3d19b-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3d19b-411">AzureRM.Relay</span></span>
* <span data-ttu-id="3d19b-412">Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3d19b-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-413">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-414">Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="3d19b-415">Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="3d19b-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="3d19b-416">Get-AzureRmRoleAssignment cmdlet’i düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="3d19b-417">-ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="3d19b-418">'-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-420">Liste cmdlet’lerine top ve skip parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="3d19b-421">Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :</span><span class="sxs-lookup"><span data-stu-id="3d19b-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="3d19b-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d19b-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d19b-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d19b-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d19b-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d19b-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d19b-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d19b-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d19b-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d19b-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="3d19b-427">PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d19b-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d19b-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d19b-429">'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-430">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-431">Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="3d19b-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3d19b-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="3d19b-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3d19b-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d19b-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d19b-434">AzureRM.Websites</span></span>
* <span data-ttu-id="3d19b-435">Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.</span><span class="sxs-lookup"><span data-stu-id="3d19b-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="3d19b-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="3d19b-437">`Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor</span><span class="sxs-lookup"><span data-stu-id="3d19b-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="3d19b-438">6.4.0 - Temmuz 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d19b-439">Genel</span><span class="sxs-lookup"><span data-stu-id="3d19b-439">General</span></span>
* <span data-ttu-id="3d19b-440">Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-441">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-442">Temel çıkış türlerine Ps1Xml özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-443">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-444">VMSS için IP Etiketi özelliği</span><span class="sxs-lookup"><span data-stu-id="3d19b-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="3d19b-445">'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="3d19b-446">New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3d19b-447">VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="3d19b-448">New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="3d19b-449">VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği</span><span class="sxs-lookup"><span data-stu-id="3d19b-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="3d19b-450">Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3d19b-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d19b-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3d19b-452">Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="3d19b-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d19b-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3d19b-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d19b-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3d19b-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d19b-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d19b-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d19b-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d19b-457">Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3d19b-458">Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3d19b-459">Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="3d19b-460">DataLake cmdlet'lerinin test konumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d19b-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d19b-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d19b-462">Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="3d19b-463">New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="3d19b-464">Varsayılan Parametre kümesi sağlandı.</span><span class="sxs-lookup"><span data-stu-id="3d19b-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="3d19b-465">Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-467">Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-468">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-469">Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3d19b-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="3d19b-470">ARM aracılığıyla ExpressRoute Partner API'leri özelliği için yeni komutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="3d19b-471">Get-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3d19b-472">Set-AzureRmExpressRouteCrossConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3d19b-473">Add-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d19b-474">Get-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d19b-475">Remove-AzureRmExpressRouteCrossConnectionPeering eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d19b-476">Get-AzureRMExpressRouteCrossConnectionArpTable eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3d19b-477">Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3d19b-478">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d19b-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d19b-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d19b-480">Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="3d19b-481">Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="3d19b-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="3d19b-482">Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d19b-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-483">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-484">Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="3d19b-485">Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="3d19b-486">Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="3d19b-487">control parametresine -Effective ve -All anahtarları eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="3d19b-488">Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="3d19b-489">Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3d19b-490">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3d19b-491">Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="3d19b-492">Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3d19b-493">Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3d19b-494">'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="3d19b-495">'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="3d19b-496">'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="3d19b-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d19b-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d19b-498">Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-499">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-500">New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="3d19b-501">Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="3d19b-502">6.3.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-503">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-504">Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="3d19b-505">'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur</span><span class="sxs-lookup"><span data-stu-id="3d19b-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d19b-506">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3d19b-506">Azure.Storage</span></span>
* <span data-ttu-id="3d19b-507">Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-508">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-509">'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="3d19b-510">Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="3d19b-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3d19b-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3d19b-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3d19b-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3d19b-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3d19b-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3d19b-514">Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="3d19b-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d19b-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="3d19b-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d19b-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="3d19b-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d19b-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="3d19b-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d19b-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="3d19b-519">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d19b-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="3d19b-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d19b-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="3d19b-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3d19b-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="3d19b-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3d19b-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="3d19b-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d19b-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="3d19b-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d19b-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="3d19b-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d19b-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="3d19b-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d19b-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="3d19b-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3d19b-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="3d19b-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3d19b-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3d19b-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="3d19b-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="3d19b-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3d19b-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3d19b-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3d19b-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="3d19b-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3d19b-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="3d19b-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3d19b-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3d19b-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d19b-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3d19b-535">Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="3d19b-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-537">Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3d19b-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d19b-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3d19b-539">Policy Insights cmdlet'leri genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3d19b-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="3d19b-540">API 2018-04-04 sürümünü kullanın</span><span class="sxs-lookup"><span data-stu-id="3d19b-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="3d19b-541">PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d19b-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d19b-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d19b-543">RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="3d19b-544">Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="3d19b-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-545">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-546">Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d19b-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d19b-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d19b-548">Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d19b-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d19b-549">AzureRM.Websites</span></span>
* <span data-ttu-id="3d19b-550">'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="3d19b-551">'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="3d19b-552">6.2.1 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="3d19b-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d19b-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3d19b-554">PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="3d19b-555">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-556">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-557">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d19b-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d19b-558">AzureRM.Compute</span></span>
* <span data-ttu-id="3d19b-559">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="3d19b-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="3d19b-560">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="3d19b-561">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d19b-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d19b-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d19b-563">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="3d19b-564">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="3d19b-565">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="3d19b-566">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="3d19b-567">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="3d19b-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d19b-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d19b-569">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-570">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-571">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d19b-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d19b-572">AzureRM.Resources</span></span>
* <span data-ttu-id="3d19b-573">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3d19b-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3d19b-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3d19b-575">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="3d19b-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-576">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-577">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3d19b-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="3d19b-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d19b-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d19b-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d19b-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d19b-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d19b-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d19b-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d19b-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d19b-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d19b-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d19b-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d19b-583">AzureRM.Websites</span></span>
* <span data-ttu-id="3d19b-584">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="3d19b-585">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="3d19b-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d19b-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d19b-586">AzureRM.Profile</span></span>
* <span data-ttu-id="3d19b-587">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d19b-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d19b-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d19b-589">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="3d19b-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d19b-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d19b-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d19b-591">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="3d19b-592">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="3d19b-593">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="3d19b-594">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="3d19b-595">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="3d19b-596">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="3d19b-597">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-597">Added support for MSI identity</span></span>
* <span data-ttu-id="3d19b-598">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="3d19b-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="3d19b-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3d19b-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="3d19b-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d19b-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="3d19b-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3d19b-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="3d19b-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3d19b-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3d19b-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3d19b-603">AzureRM.Batch</span></span>
* <span data-ttu-id="3d19b-604">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="3d19b-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="3d19b-605">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="3d19b-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3d19b-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3d19b-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="3d19b-607">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="3d19b-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d19b-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d19b-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d19b-609">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="3d19b-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3d19b-610">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="3d19b-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="3d19b-611">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="3d19b-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="3d19b-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d19b-612">AzureRM.Network</span></span>
* <span data-ttu-id="3d19b-613">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="3d19b-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="3d19b-614">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="3d19b-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d19b-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="3d19b-616">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="3d19b-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d19b-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d19b-618">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="3d19b-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d19b-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d19b-620">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="3d19b-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="3d19b-621">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d19b-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d19b-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d19b-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d19b-623">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="3d19b-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d19b-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d19b-624">AzureRM.Sql</span></span>
* <span data-ttu-id="3d19b-625">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3d19b-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="3d19b-626">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3d19b-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="3d19b-627">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3d19b-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="3d19b-628">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3d19b-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="3d19b-629">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="3d19b-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="3d19b-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d19b-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d19b-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d19b-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d19b-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d19b-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d19b-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d19b-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d19b-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d19b-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d19b-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d19b-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d19b-636">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3d19b-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
