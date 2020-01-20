---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319302"
---
## <a name="180---april-2019"></a><span data-ttu-id="34b78-103">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="34b78-104">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="34b78-104">Highlights since the last major release</span></span>
* <span data-ttu-id="34b78-105">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="34b78-105">General availability of `Az` module</span></span>
* <span data-ttu-id="34b78-106">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="34b78-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="34b78-107">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="34b78-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="34b78-108">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="34b78-109">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="34b78-110">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="34b78-111">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="34b78-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="34b78-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-112">Az.Accounts</span></span>
* <span data-ttu-id="34b78-113">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="34b78-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="34b78-114">Az.Batch</span></span>
* <span data-ttu-id="34b78-115">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="34b78-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="34b78-116">Az.Cdn</span></span>
* <span data-ttu-id="34b78-117">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="34b78-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="34b78-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="34b78-119">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-120">Az.Compute</span></span>
* <span data-ttu-id="34b78-121">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="34b78-122">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-123">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="34b78-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="34b78-124">Az.DataFactory</span></span>
* <span data-ttu-id="34b78-125">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-127">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="34b78-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="34b78-128">Az.EventGrid</span></span>
* <span data-ttu-id="34b78-129">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="34b78-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="34b78-130">Az.EventHub</span></span>
* <span data-ttu-id="34b78-131">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="34b78-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="34b78-132">Az.HDInsight</span></span>
* <span data-ttu-id="34b78-133">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="34b78-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="34b78-134">Az.IotHub</span></span>
* <span data-ttu-id="34b78-135">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="34b78-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34b78-136">Az.KeyVault</span></span>
* <span data-ttu-id="34b78-137">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-138">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="34b78-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="34b78-139">Az.MachineLearning</span></span>
* <span data-ttu-id="34b78-140">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="34b78-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="34b78-141">Az.Media</span></span>
* <span data-ttu-id="34b78-142">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="34b78-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="34b78-143">Az.Monitor</span></span>
  * <span data-ttu-id="34b78-144">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="34b78-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="34b78-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="34b78-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="34b78-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="34b78-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="34b78-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="34b78-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="34b78-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="34b78-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="34b78-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="34b78-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="34b78-150">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-151">Az.Network</span></span>
* <span data-ttu-id="34b78-152">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-153">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="34b78-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="34b78-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="34b78-155">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="34b78-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="34b78-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="34b78-157">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="34b78-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="34b78-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="34b78-159">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="34b78-161">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-162">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="34b78-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="34b78-163">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="34b78-164">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="34b78-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="34b78-165">Az.RedisCache</span></span>
* <span data-ttu-id="34b78-166">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-167">Az.Resources</span></span>
* <span data-ttu-id="34b78-168">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-169">Az.Sql</span></span>
* <span data-ttu-id="34b78-170">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="34b78-171">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-172">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="34b78-173">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="34b78-174">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="34b78-175">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="34b78-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="34b78-176">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-177">Az.Websites</span></span>
* <span data-ttu-id="34b78-178">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="34b78-179">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="34b78-180">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="34b78-181">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="34b78-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="34b78-182">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="34b78-183">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="34b78-183">Highlights since the last major release</span></span>
* <span data-ttu-id="34b78-184">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="34b78-184">General availability of `Az` module</span></span>
* <span data-ttu-id="34b78-185">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="34b78-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="34b78-186">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="34b78-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="34b78-187">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="34b78-188">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="34b78-189">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="34b78-190">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="34b78-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="34b78-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-191">Az.Accounts</span></span>
* <span data-ttu-id="34b78-192">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="34b78-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34b78-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="34b78-194">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="34b78-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="34b78-195">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="34b78-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="34b78-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-196">Az.Automation</span></span>
* <span data-ttu-id="34b78-197">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="34b78-198">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="34b78-199">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="34b78-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-200">Az.Compute</span></span>
* <span data-ttu-id="34b78-201">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="34b78-202">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="34b78-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="34b78-204">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="34b78-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="34b78-205">Az.DataFactory</span></span>
* <span data-ttu-id="34b78-206">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="34b78-207">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-208">Az.Resources</span></span>
* <span data-ttu-id="34b78-209">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="34b78-210">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="34b78-211">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="34b78-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="34b78-212">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="34b78-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="34b78-213">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="34b78-214">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="34b78-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-215">Az.Sql</span></span>
* <span data-ttu-id="34b78-216">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="34b78-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="34b78-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-217">Az.Storage</span></span>
* <span data-ttu-id="34b78-218">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="34b78-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="34b78-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="34b78-219">New-AzStorageContext</span></span>
* <span data-ttu-id="34b78-220">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="34b78-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="34b78-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="34b78-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="34b78-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="34b78-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="34b78-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="34b78-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="34b78-225">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="34b78-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="34b78-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="34b78-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="34b78-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="34b78-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="34b78-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="34b78-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="34b78-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="34b78-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="34b78-230">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="34b78-231">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="34b78-231">Highlights since the last major release</span></span>
* <span data-ttu-id="34b78-232">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="34b78-232">General availability of `Az` module</span></span>
* <span data-ttu-id="34b78-233">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="34b78-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="34b78-234">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="34b78-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="34b78-235">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="34b78-236">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="34b78-237">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="34b78-238">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="34b78-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="34b78-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-239">Az.Automation</span></span>
* <span data-ttu-id="34b78-240">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="34b78-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="34b78-241">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="34b78-241">Dynamic grouping</span></span>
    * <span data-ttu-id="34b78-242">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="34b78-242">Pre-Post script</span></span>
    * <span data-ttu-id="34b78-243">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="34b78-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-244">Az.Compute</span></span>
* <span data-ttu-id="34b78-245">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="34b78-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="34b78-246">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="34b78-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34b78-247">Az.KeyVault</span></span>
* <span data-ttu-id="34b78-248">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-249">Az.Network</span></span>
* <span data-ttu-id="34b78-250">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="34b78-251">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="34b78-253">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="34b78-254">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-255">Az.Resources</span></span>
* <span data-ttu-id="34b78-256">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="34b78-257">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-258">Az.Sql</span></span>
* <span data-ttu-id="34b78-259">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="34b78-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-260">Az.Storage</span></span>
* <span data-ttu-id="34b78-261">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="34b78-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="34b78-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="34b78-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="34b78-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="34b78-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="34b78-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="34b78-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="34b78-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="34b78-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="34b78-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-268">Az.Websites</span></span>
* <span data-ttu-id="34b78-269">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="34b78-270">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="34b78-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-271">Az.Accounts</span></span>
* <span data-ttu-id="34b78-272">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="34b78-273">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="34b78-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-274">Az.Automation</span></span>
* <span data-ttu-id="34b78-275">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="34b78-276">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="34b78-277">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="34b78-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="34b78-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="34b78-278">Az.Cdn</span></span>
* <span data-ttu-id="34b78-279">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-280">Az.Compute</span></span>
* <span data-ttu-id="34b78-281">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="34b78-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="34b78-282">Az.DataFactory</span></span>
* <span data-ttu-id="34b78-283">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="34b78-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="34b78-284">Az.LogicApp</span></span>
* <span data-ttu-id="34b78-285">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="34b78-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-286">Az.Network</span></span>
* <span data-ttu-id="34b78-287">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="34b78-289">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="34b78-290">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="34b78-290">SDK Update</span></span>
* <span data-ttu-id="34b78-291">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="34b78-292">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-293">Az.Resources</span></span>
* <span data-ttu-id="34b78-294">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="34b78-295">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="34b78-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="34b78-296">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="34b78-297">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="34b78-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="34b78-298">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="34b78-299">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="34b78-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-300">Az.Sql</span></span>
* <span data-ttu-id="34b78-301">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="34b78-302">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="34b78-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-303">Az.Storage</span></span>
* <span data-ttu-id="34b78-304">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="34b78-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="34b78-305">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="34b78-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34b78-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="34b78-307">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="34b78-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-308">Az.Automation</span></span>
* <span data-ttu-id="34b78-309">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="34b78-310">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="34b78-311">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="34b78-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="34b78-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="34b78-313">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-314">Az.Compute</span></span>
* <span data-ttu-id="34b78-315">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="34b78-316">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="34b78-317">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="34b78-318">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="34b78-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-320">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="34b78-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="34b78-321">Az.EventHub</span></span>
* <span data-ttu-id="34b78-322">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="34b78-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34b78-323">Az.KeyVault</span></span>
* <span data-ttu-id="34b78-324">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="34b78-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="34b78-325">Az.LogicApp</span></span>
* <span data-ttu-id="34b78-326">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="34b78-327">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="34b78-328">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="34b78-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="34b78-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="34b78-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="34b78-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="34b78-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="34b78-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="34b78-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="34b78-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="34b78-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="34b78-333">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="34b78-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="34b78-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="34b78-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="34b78-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="34b78-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="34b78-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="34b78-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="34b78-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="34b78-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="34b78-338">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="34b78-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="34b78-339">Az.Monitor</span></span>
* <span data-ttu-id="34b78-340">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-341">Az.Network</span></span>
* <span data-ttu-id="34b78-342">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="34b78-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="34b78-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="34b78-344">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="34b78-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="34b78-345">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="34b78-346">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="34b78-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-347">Az.Resources</span></span>
* <span data-ttu-id="34b78-348">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="34b78-349">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="34b78-350">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="34b78-351">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-352">Az.Sql</span></span>
* <span data-ttu-id="34b78-353">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="34b78-354">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-355">Az.Websites</span></span>
* <span data-ttu-id="34b78-356">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="34b78-357">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="34b78-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-358">Az.Accounts</span></span>
* <span data-ttu-id="34b78-359">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="34b78-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="34b78-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34b78-360">Az.AnalysisServices</span></span>
<span data-ttu-id="34b78-361">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="34b78-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-362">Az.Compute</span></span>
* <span data-ttu-id="34b78-363">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="34b78-364">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="34b78-365">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-366">Az.RecoveryServices</span></span>
<span data-ttu-id="34b78-367">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="34b78-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-368">Az.Resources</span></span>
* <span data-ttu-id="34b78-369">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="34b78-370">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="34b78-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="34b78-371">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="34b78-372">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="34b78-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-373">Az.Sql</span></span>
* <span data-ttu-id="34b78-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="34b78-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="34b78-375">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="34b78-376">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="34b78-377">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="34b78-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-378">Az.Accounts</span></span>
* <span data-ttu-id="34b78-379">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="34b78-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="34b78-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="34b78-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="34b78-381">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="34b78-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="34b78-383">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="34b78-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="34b78-384">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="34b78-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-385">Az.Accounts</span></span>
* <span data-ttu-id="34b78-386">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="34b78-387">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="34b78-388">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="34b78-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="34b78-389">Az.Aks</span></span>
* <span data-ttu-id="34b78-390">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="34b78-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-391">Az.Automation</span></span>
* <span data-ttu-id="34b78-392">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="34b78-393">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="34b78-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="34b78-394">Az.Cdn</span></span>
* <span data-ttu-id="34b78-395">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-396">Az.Compute</span></span>
* <span data-ttu-id="34b78-397">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="34b78-398">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="34b78-399">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="34b78-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="34b78-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="34b78-401">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="34b78-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="34b78-402">Az.DataFactory</span></span>
* <span data-ttu-id="34b78-403">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-405">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="34b78-406">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="34b78-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="34b78-407">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="34b78-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="34b78-408">Az.IotHub</span></span>
* <span data-ttu-id="34b78-409">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="34b78-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34b78-410">Az.KeyVault</span></span>
* <span data-ttu-id="34b78-411">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-412">Az.Network</span></span>
* <span data-ttu-id="34b78-413">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-414">Az.Resources</span></span>
* <span data-ttu-id="34b78-415">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="34b78-416">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="34b78-417">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="34b78-418">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="34b78-419">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="34b78-420">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="34b78-421">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="34b78-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="34b78-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34b78-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="34b78-423">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="34b78-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="34b78-424">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-424">Fix some error messages.</span></span>
* <span data-ttu-id="34b78-425">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="34b78-426">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="34b78-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="34b78-427">Az.SignalR</span></span>
* <span data-ttu-id="34b78-428">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-429">Az.Sql</span></span>
* <span data-ttu-id="34b78-430">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="34b78-431">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="34b78-432">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="34b78-433">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="34b78-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="34b78-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-434">Az.Storage</span></span>
* <span data-ttu-id="34b78-435">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="34b78-436">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="34b78-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="34b78-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="34b78-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="34b78-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="34b78-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="34b78-439">Az.TrafficManager</span></span>
* <span data-ttu-id="34b78-440">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-441">Az.Websites</span></span>
* <span data-ttu-id="34b78-442">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="34b78-443">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="34b78-444">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="34b78-445">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="34b78-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="34b78-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-446">Az.Accounts</span></span>
* <span data-ttu-id="34b78-447">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-448">Az.Compute</span></span>
* <span data-ttu-id="34b78-449">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="34b78-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="34b78-450">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="34b78-451">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="34b78-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-453">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="34b78-454">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="34b78-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="34b78-455">Az.EventGrid</span></span>
* <span data-ttu-id="34b78-456">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="34b78-457">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="34b78-458">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="34b78-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="34b78-459">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="34b78-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="34b78-460">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="34b78-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="34b78-461">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="34b78-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="34b78-462">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="34b78-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="34b78-463">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="34b78-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="34b78-464">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="34b78-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="34b78-465">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="34b78-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="34b78-466">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="34b78-467">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="34b78-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="34b78-468">Az.IotHub</span></span>
* <span data-ttu-id="34b78-469">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="34b78-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="34b78-470">Az.LogicApp</span></span>
* <span data-ttu-id="34b78-471">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="34b78-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-472">Az.Resources</span></span>
* <span data-ttu-id="34b78-473">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="34b78-474">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="34b78-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="34b78-475">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="34b78-476">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="34b78-477">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="34b78-478">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="34b78-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="34b78-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="34b78-479">Az.SignalR</span></span>
* <span data-ttu-id="34b78-480">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="34b78-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-481">Az.Sql</span></span>
* <span data-ttu-id="34b78-482">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="34b78-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="34b78-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-483">Az.Storage</span></span>
* <span data-ttu-id="34b78-484">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="34b78-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="34b78-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="34b78-485">New-AzStorageContext</span></span>
* <span data-ttu-id="34b78-486">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="34b78-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="34b78-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-488">Az.Websites</span></span>
* <span data-ttu-id="34b78-489">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="34b78-490">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="34b78-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="34b78-491">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="34b78-492">Genel</span><span class="sxs-lookup"><span data-stu-id="34b78-492">General</span></span>

- <span data-ttu-id="34b78-493">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="34b78-493">General Availability of Az Module</span></span>
- <span data-ttu-id="34b78-494">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="34b78-494">Online help for each module</span></span>
- <span data-ttu-id="34b78-495">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="34b78-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="34b78-496">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="34b78-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="34b78-497">Az.Accounts</span></span>
- <span data-ttu-id="34b78-498">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="34b78-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="34b78-499">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="34b78-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34b78-500">Az.ApiManagement</span></span>
- <span data-ttu-id="34b78-501">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="34b78-501">Fixes for #7002</span></span>
- <span data-ttu-id="34b78-502">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="34b78-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="34b78-503">Az.Batch</span></span>
- <span data-ttu-id="34b78-504">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="34b78-505">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="34b78-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="34b78-506">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="34b78-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="34b78-507">Az.Billing</span></span>
- <span data-ttu-id="34b78-508">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="34b78-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="34b78-509">Az.CognitivServices</span></span>
- <span data-ttu-id="34b78-510">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="34b78-511">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="34b78-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="34b78-513">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="34b78-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="34b78-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="34b78-515">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="34b78-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="34b78-517">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="34b78-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="34b78-518">Az.Monitor</span></span>
- <span data-ttu-id="34b78-519">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="34b78-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="34b78-520">Az.KeyVault</span></span>
- <span data-ttu-id="34b78-521">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="34b78-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="34b78-522">Az.MachineLearning</span></span>
- <span data-ttu-id="34b78-523">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="34b78-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="34b78-524">Az.Media</span></span>
- <span data-ttu-id="34b78-525">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="34b78-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="34b78-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-526">Az.Network</span></span>
<span data-ttu-id="34b78-527">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="34b78-528">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="34b78-528">New cmdlets added:</span></span>
        - <span data-ttu-id="34b78-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34b78-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34b78-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34b78-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34b78-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="34b78-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="34b78-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="34b78-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="34b78-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="34b78-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="34b78-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="34b78-537">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="34b78-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34b78-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="34b78-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34b78-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="34b78-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="34b78-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="34b78-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34b78-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="34b78-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="34b78-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="34b78-543">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="34b78-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="34b78-544">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="34b78-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34b78-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="34b78-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34b78-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="34b78-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="34b78-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="34b78-548">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="34b78-549">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="34b78-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="34b78-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="34b78-551">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="34b78-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="34b78-552">Az.Profile</span></span>
- <span data-ttu-id="34b78-553">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="34b78-555">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="34b78-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-556">Az.Resources</span></span>
- <span data-ttu-id="34b78-557">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="34b78-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34b78-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="34b78-559">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="34b78-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="34b78-560">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="34b78-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="34b78-561">Az.SIgnalR</span></span>
- <span data-ttu-id="34b78-562">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="34b78-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="34b78-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-563">Az.Sql</span></span>
- <span data-ttu-id="34b78-564">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="34b78-565">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="34b78-566">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="34b78-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-567">Az.Storage</span></span>
- <span data-ttu-id="34b78-568">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="34b78-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-569">Az.Websites</span></span>
- <span data-ttu-id="34b78-570">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="34b78-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="34b78-571">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="34b78-572">Genel</span><span class="sxs-lookup"><span data-stu-id="34b78-572">General</span></span>

* <span data-ttu-id="34b78-573">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="34b78-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="34b78-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-574">Az.Compute</span></span>

* <span data-ttu-id="34b78-575">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="34b78-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="34b78-577">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="34b78-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="34b78-578">Az.FrontDoor</span></span>

* <span data-ttu-id="34b78-579">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-579">Fixed some broken links</span></span>
    - <span data-ttu-id="34b78-580">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="34b78-581">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="34b78-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="34b78-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="34b78-583">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="34b78-584">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="34b78-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-585">Az.Resources</span></span>

* <span data-ttu-id="34b78-586">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="34b78-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="34b78-587">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="34b78-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-588">Az.Sql</span></span>

* <span data-ttu-id="34b78-589">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="34b78-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="34b78-590">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="34b78-591">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="34b78-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="34b78-592">Az.Storage</span></span>

* <span data-ttu-id="34b78-593">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="34b78-594">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="34b78-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="34b78-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="34b78-596">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="34b78-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="34b78-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="34b78-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="34b78-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="34b78-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-599">Az.Websites</span></span>

* <span data-ttu-id="34b78-600">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="34b78-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="34b78-601">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="34b78-602">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="34b78-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="34b78-603">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="34b78-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="34b78-604">Az.ApiManagement</span></span>
* <span data-ttu-id="34b78-605">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="34b78-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="34b78-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="34b78-606">Az.Automation</span></span>
* <span data-ttu-id="34b78-607">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="34b78-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="34b78-608">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="34b78-609">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="34b78-610">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="34b78-611">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="34b78-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-612">Az.Compute</span></span>
* <span data-ttu-id="34b78-613">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="34b78-614">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="34b78-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="34b78-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="34b78-616">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="34b78-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="34b78-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="34b78-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="34b78-618">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="34b78-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-619">Az.Network</span></span>
* <span data-ttu-id="34b78-620">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="34b78-621">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="34b78-622">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="34b78-623">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="34b78-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="34b78-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="34b78-625">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="34b78-626">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="34b78-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="34b78-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="34b78-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="34b78-628">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="34b78-629">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="34b78-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="34b78-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="34b78-630">Az.Relay</span></span>
* <span data-ttu-id="34b78-631">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="34b78-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-632">Az.Resources</span></span>
* <span data-ttu-id="34b78-633">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="34b78-634">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="34b78-635">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="34b78-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="34b78-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34b78-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="34b78-637">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="34b78-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-638">Az.Sql</span></span>
* <span data-ttu-id="34b78-639">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="34b78-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="34b78-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="34b78-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="34b78-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="34b78-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="34b78-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="34b78-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="34b78-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="34b78-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="34b78-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="34b78-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="34b78-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="34b78-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="34b78-648">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="34b78-649">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="34b78-650">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="34b78-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="34b78-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="34b78-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="34b78-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="34b78-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="34b78-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="34b78-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="34b78-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="34b78-655">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="34b78-656">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="34b78-657">Genel</span><span class="sxs-lookup"><span data-stu-id="34b78-657">General</span></span>
* <span data-ttu-id="34b78-658">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="34b78-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="34b78-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="34b78-659">Az.Profile</span></span>
* <span data-ttu-id="34b78-660">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="34b78-661">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="34b78-662">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="34b78-663">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="34b78-664">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="34b78-665">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="34b78-666">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="34b78-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="34b78-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="34b78-668">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-669">Az.Compute</span></span>
* <span data-ttu-id="34b78-670">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="34b78-671">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="34b78-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="34b78-672">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-674">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="34b78-675">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="34b78-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="34b78-676">Az.Insights</span></span>
* <span data-ttu-id="34b78-677">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="34b78-678">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="34b78-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="34b78-679">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="34b78-680">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="34b78-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-681">Az.Network</span></span>
* <span data-ttu-id="34b78-682">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="34b78-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="34b78-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="34b78-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="34b78-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="34b78-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="34b78-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="34b78-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="34b78-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="34b78-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="34b78-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="34b78-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="34b78-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="34b78-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="34b78-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="34b78-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="34b78-690">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-691">Az.Resources</span></span>
* <span data-ttu-id="34b78-692">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="34b78-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="34b78-693">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="34b78-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="34b78-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="34b78-694">Az.ServiceBus</span></span>
* <span data-ttu-id="34b78-695">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="34b78-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="34b78-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="34b78-697">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="34b78-698">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="34b78-699">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="34b78-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="34b78-700">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="34b78-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="34b78-701">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="34b78-702">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="34b78-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="34b78-703">Az.Profile</span></span>
* <span data-ttu-id="34b78-704">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="34b78-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="34b78-705">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="34b78-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-706">Az.Compute</span></span>
* <span data-ttu-id="34b78-707">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="34b78-708">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="34b78-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="34b78-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="34b78-710">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="34b78-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="34b78-711">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="34b78-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="34b78-712">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="34b78-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="34b78-713">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="34b78-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="34b78-714">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="34b78-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-715">Az.Network</span></span>
* <span data-ttu-id="34b78-716">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="34b78-717">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-718">Az.Resources</span></span>
* <span data-ttu-id="34b78-719">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="34b78-720">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="34b78-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="34b78-721">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="34b78-722">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="34b78-722">Azure.Storage</span></span>
* <span data-ttu-id="34b78-723">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="34b78-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="34b78-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="34b78-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="34b78-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="34b78-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="34b78-726">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="34b78-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="34b78-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="34b78-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="34b78-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="34b78-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="34b78-729">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="34b78-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="34b78-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="34b78-730">Az.Compute</span></span>
* <span data-ttu-id="34b78-731">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="34b78-732">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="34b78-733">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="34b78-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34b78-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="34b78-735">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="34b78-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="34b78-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="34b78-736">Az.Network</span></span>
* <span data-ttu-id="34b78-737">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="34b78-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="34b78-738">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-738">new cmdlets added</span></span>
    - <span data-ttu-id="34b78-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="34b78-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="34b78-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="34b78-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="34b78-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="34b78-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="34b78-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="34b78-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="34b78-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="34b78-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="34b78-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="34b78-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="34b78-745">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="34b78-746">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="34b78-747">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="34b78-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="34b78-748">Az.RedisCache</span></span>
* <span data-ttu-id="34b78-749">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="34b78-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="34b78-750">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="34b78-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="34b78-751">Az.Resources</span></span>
* <span data-ttu-id="34b78-752">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="34b78-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="34b78-753">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="34b78-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="34b78-754">Az.Sql</span></span>
* <span data-ttu-id="34b78-755">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="34b78-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="34b78-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="34b78-756">Az.Websites</span></span>
* <span data-ttu-id="34b78-757">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="34b78-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="34b78-758">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="34b78-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="34b78-759">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="34b78-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="34b78-760">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="34b78-760">Initial Release</span></span>