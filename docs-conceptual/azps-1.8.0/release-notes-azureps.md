---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 287e9e1f066d0768e7f572ca7f5f2ee2b78931d9
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386978"
---
## <a name="180---april-2019"></a><span data-ttu-id="cd882-103">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd882-104">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="cd882-104">Highlights since the last major release</span></span>
* <span data-ttu-id="cd882-105">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cd882-105">General availability of `Az` module</span></span>
* <span data-ttu-id="cd882-106">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd882-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd882-107">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd882-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd882-108">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd882-109">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd882-110">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd882-111">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="cd882-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd882-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-112">Az.Accounts</span></span>
* <span data-ttu-id="cd882-113">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd882-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd882-114">Az.Batch</span></span>
* <span data-ttu-id="cd882-115">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd882-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd882-116">Az.Cdn</span></span>
* <span data-ttu-id="cd882-117">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd882-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd882-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd882-119">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-120">Az.Compute</span></span>
* <span data-ttu-id="cd882-121">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cd882-122">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-123">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd882-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd882-124">Az.DataFactory</span></span>
* <span data-ttu-id="cd882-125">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-127">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd882-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd882-128">Az.EventGrid</span></span>
* <span data-ttu-id="cd882-129">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd882-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd882-130">Az.EventHub</span></span>
* <span data-ttu-id="cd882-131">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cd882-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd882-132">Az.HDInsight</span></span>
* <span data-ttu-id="cd882-133">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd882-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd882-134">Az.IotHub</span></span>
* <span data-ttu-id="cd882-135">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd882-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd882-136">Az.KeyVault</span></span>
* <span data-ttu-id="cd882-137">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-138">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cd882-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd882-139">Az.MachineLearning</span></span>
* <span data-ttu-id="cd882-140">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cd882-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd882-141">Az.Media</span></span>
* <span data-ttu-id="cd882-142">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd882-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd882-143">Az.Monitor</span></span>
  * <span data-ttu-id="cd882-144">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="cd882-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cd882-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cd882-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cd882-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cd882-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cd882-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd882-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd882-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd882-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd882-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd882-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cd882-150">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-151">Az.Network</span></span>
* <span data-ttu-id="cd882-152">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-153">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cd882-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cd882-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="cd882-155">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd882-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd882-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd882-157">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cd882-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cd882-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cd882-159">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd882-161">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-162">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="cd882-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cd882-163">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cd882-164">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd882-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd882-165">Az.RedisCache</span></span>
* <span data-ttu-id="cd882-166">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-167">Az.Resources</span></span>
* <span data-ttu-id="cd882-168">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-169">Az.Sql</span></span>
* <span data-ttu-id="cd882-170">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cd882-171">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-172">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cd882-173">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cd882-174">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cd882-175">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="cd882-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cd882-176">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-177">Az.Websites</span></span>
* <span data-ttu-id="cd882-178">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cd882-179">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd882-180">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cd882-181">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="cd882-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cd882-182">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd882-183">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="cd882-183">Highlights since the last major release</span></span>
* <span data-ttu-id="cd882-184">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cd882-184">General availability of `Az` module</span></span>
* <span data-ttu-id="cd882-185">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd882-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd882-186">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd882-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd882-187">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd882-188">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd882-189">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd882-190">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="cd882-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd882-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-191">Az.Accounts</span></span>
* <span data-ttu-id="cd882-192">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd882-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd882-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd882-194">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="cd882-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cd882-195">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="cd882-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd882-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-196">Az.Automation</span></span>
* <span data-ttu-id="cd882-197">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cd882-198">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cd882-199">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="cd882-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-200">Az.Compute</span></span>
* <span data-ttu-id="cd882-201">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd882-202">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="cd882-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd882-204">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd882-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd882-205">Az.DataFactory</span></span>
* <span data-ttu-id="cd882-206">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cd882-207">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-208">Az.Resources</span></span>
* <span data-ttu-id="cd882-209">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cd882-210">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cd882-211">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="cd882-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cd882-212">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd882-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cd882-213">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cd882-214">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd882-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-215">Az.Sql</span></span>
* <span data-ttu-id="cd882-216">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="cd882-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd882-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-217">Az.Storage</span></span>
* <span data-ttu-id="cd882-218">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="cd882-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cd882-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd882-219">New-AzStorageContext</span></span>
* <span data-ttu-id="cd882-220">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="cd882-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cd882-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd882-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd882-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd882-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd882-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cd882-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cd882-225">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="cd882-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cd882-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd882-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd882-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd882-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd882-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd882-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cd882-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd882-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cd882-230">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd882-231">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="cd882-231">Highlights since the last major release</span></span>
* <span data-ttu-id="cd882-232">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cd882-232">General availability of `Az` module</span></span>
* <span data-ttu-id="cd882-233">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cd882-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd882-234">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cd882-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd882-235">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd882-236">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd882-237">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd882-238">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="cd882-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd882-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-239">Az.Automation</span></span>
* <span data-ttu-id="cd882-240">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="cd882-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cd882-241">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="cd882-241">Dynamic grouping</span></span>
    * <span data-ttu-id="cd882-242">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="cd882-242">Pre-Post script</span></span>
    * <span data-ttu-id="cd882-243">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="cd882-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-244">Az.Compute</span></span>
* <span data-ttu-id="cd882-245">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cd882-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cd882-246">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd882-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd882-247">Az.KeyVault</span></span>
* <span data-ttu-id="cd882-248">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-249">Az.Network</span></span>
* <span data-ttu-id="cd882-250">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cd882-251">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd882-253">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cd882-254">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-255">Az.Resources</span></span>
* <span data-ttu-id="cd882-256">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cd882-257">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-258">Az.Sql</span></span>
* <span data-ttu-id="cd882-259">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd882-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-260">Az.Storage</span></span>
* <span data-ttu-id="cd882-261">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="cd882-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cd882-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd882-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd882-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd882-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cd882-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cd882-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cd882-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cd882-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cd882-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-268">Az.Websites</span></span>
* <span data-ttu-id="cd882-269">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="cd882-270">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd882-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-271">Az.Accounts</span></span>
* <span data-ttu-id="cd882-272">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cd882-273">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd882-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-274">Az.Automation</span></span>
* <span data-ttu-id="cd882-275">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd882-276">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cd882-277">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="cd882-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd882-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd882-278">Az.Cdn</span></span>
* <span data-ttu-id="cd882-279">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-280">Az.Compute</span></span>
* <span data-ttu-id="cd882-281">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd882-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd882-282">Az.DataFactory</span></span>
* <span data-ttu-id="cd882-283">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd882-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd882-284">Az.LogicApp</span></span>
* <span data-ttu-id="cd882-285">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="cd882-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-286">Az.Network</span></span>
* <span data-ttu-id="cd882-287">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd882-289">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cd882-290">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="cd882-290">SDK Update</span></span>
* <span data-ttu-id="cd882-291">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cd882-292">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-293">Az.Resources</span></span>
* <span data-ttu-id="cd882-294">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cd882-295">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cd882-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cd882-296">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cd882-297">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cd882-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cd882-298">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cd882-299">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cd882-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-300">Az.Sql</span></span>
* <span data-ttu-id="cd882-301">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cd882-302">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd882-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-303">Az.Storage</span></span>
* <span data-ttu-id="cd882-304">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd882-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cd882-305">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cd882-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd882-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd882-307">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd882-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-308">Az.Automation</span></span>
* <span data-ttu-id="cd882-309">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cd882-310">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cd882-311">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd882-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd882-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd882-313">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-314">Az.Compute</span></span>
* <span data-ttu-id="cd882-315">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cd882-316">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cd882-317">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cd882-318">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="cd882-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-320">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd882-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd882-321">Az.EventHub</span></span>
* <span data-ttu-id="cd882-322">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="cd882-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd882-323">Az.KeyVault</span></span>
* <span data-ttu-id="cd882-324">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd882-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd882-325">Az.LogicApp</span></span>
* <span data-ttu-id="cd882-326">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cd882-327">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cd882-328">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="cd882-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cd882-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd882-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd882-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd882-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd882-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd882-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd882-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd882-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cd882-333">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="cd882-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cd882-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd882-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd882-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd882-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd882-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd882-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd882-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd882-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cd882-338">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd882-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd882-339">Az.Monitor</span></span>
* <span data-ttu-id="cd882-340">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-341">Az.Network</span></span>
* <span data-ttu-id="cd882-342">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd882-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd882-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd882-344">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="cd882-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cd882-345">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="cd882-346">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="cd882-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-347">Az.Resources</span></span>
* <span data-ttu-id="cd882-348">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd882-349">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cd882-350">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cd882-351">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-352">Az.Sql</span></span>
* <span data-ttu-id="cd882-353">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cd882-354">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-355">Az.Websites</span></span>
* <span data-ttu-id="cd882-356">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cd882-357">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd882-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-358">Az.Accounts</span></span>
* <span data-ttu-id="cd882-359">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd882-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd882-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd882-360">Az.AnalysisServices</span></span>
<span data-ttu-id="cd882-361">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="cd882-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-362">Az.Compute</span></span>
* <span data-ttu-id="cd882-363">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cd882-364">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cd882-365">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-366">Az.RecoveryServices</span></span>
<span data-ttu-id="cd882-367">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="cd882-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-368">Az.Resources</span></span>
* <span data-ttu-id="cd882-369">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="cd882-370">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cd882-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd882-371">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="cd882-372">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cd882-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-373">Az.Sql</span></span>
* <span data-ttu-id="cd882-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd882-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cd882-375">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cd882-376">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cd882-377">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd882-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-378">Az.Accounts</span></span>
* <span data-ttu-id="cd882-379">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="cd882-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd882-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd882-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd882-381">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="cd882-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd882-383">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="cd882-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cd882-384">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd882-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-385">Az.Accounts</span></span>
* <span data-ttu-id="cd882-386">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd882-387">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd882-388">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd882-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd882-389">Az.Aks</span></span>
* <span data-ttu-id="cd882-390">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd882-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-391">Az.Automation</span></span>
* <span data-ttu-id="cd882-392">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cd882-393">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd882-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd882-394">Az.Cdn</span></span>
* <span data-ttu-id="cd882-395">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-396">Az.Compute</span></span>
* <span data-ttu-id="cd882-397">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cd882-398">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cd882-399">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd882-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd882-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd882-401">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd882-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd882-402">Az.DataFactory</span></span>
* <span data-ttu-id="cd882-403">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-405">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cd882-406">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cd882-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cd882-407">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd882-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd882-408">Az.IotHub</span></span>
* <span data-ttu-id="cd882-409">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd882-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd882-410">Az.KeyVault</span></span>
* <span data-ttu-id="cd882-411">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-412">Az.Network</span></span>
* <span data-ttu-id="cd882-413">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-414">Az.Resources</span></span>
* <span data-ttu-id="cd882-415">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cd882-416">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cd882-417">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cd882-418">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cd882-419">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cd882-420">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cd882-421">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cd882-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd882-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd882-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd882-423">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cd882-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cd882-424">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-424">Fix some error messages.</span></span>
* <span data-ttu-id="cd882-425">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cd882-426">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd882-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd882-427">Az.SignalR</span></span>
* <span data-ttu-id="cd882-428">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-429">Az.Sql</span></span>
* <span data-ttu-id="cd882-430">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd882-431">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cd882-432">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cd882-433">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="cd882-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd882-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-434">Az.Storage</span></span>
* <span data-ttu-id="cd882-435">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd882-436">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cd882-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cd882-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cd882-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cd882-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cd882-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd882-439">Az.TrafficManager</span></span>
* <span data-ttu-id="cd882-440">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-441">Az.Websites</span></span>
* <span data-ttu-id="cd882-442">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd882-443">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cd882-444">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cd882-445">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="cd882-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd882-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-446">Az.Accounts</span></span>
* <span data-ttu-id="cd882-447">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-448">Az.Compute</span></span>
* <span data-ttu-id="cd882-449">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="cd882-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cd882-450">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cd882-451">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cd882-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-453">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cd882-454">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd882-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd882-455">Az.EventGrid</span></span>
* <span data-ttu-id="cd882-456">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cd882-457">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cd882-458">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="cd882-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd882-459">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="cd882-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd882-460">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="cd882-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd882-461">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="cd882-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cd882-462">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="cd882-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd882-463">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="cd882-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd882-464">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="cd882-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd882-465">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="cd882-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="cd882-466">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cd882-467">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd882-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd882-468">Az.IotHub</span></span>
* <span data-ttu-id="cd882-469">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd882-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd882-470">Az.LogicApp</span></span>
* <span data-ttu-id="cd882-471">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="cd882-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-472">Az.Resources</span></span>
* <span data-ttu-id="cd882-473">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cd882-474">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cd882-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cd882-475">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd882-476">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cd882-477">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cd882-478">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cd882-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd882-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd882-479">Az.SignalR</span></span>
* <span data-ttu-id="cd882-480">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cd882-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-481">Az.Sql</span></span>
* <span data-ttu-id="cd882-482">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="cd882-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd882-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-483">Az.Storage</span></span>
* <span data-ttu-id="cd882-484">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="cd882-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cd882-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd882-485">New-AzStorageContext</span></span>
* <span data-ttu-id="cd882-486">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cd882-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd882-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-488">Az.Websites</span></span>
* <span data-ttu-id="cd882-489">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cd882-490">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cd882-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cd882-491">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cd882-492">Genel</span><span class="sxs-lookup"><span data-stu-id="cd882-492">General</span></span>

- <span data-ttu-id="cd882-493">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="cd882-493">General Availability of Az Module</span></span>
- <span data-ttu-id="cd882-494">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="cd882-494">Online help for each module</span></span>
- <span data-ttu-id="cd882-495">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cd882-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cd882-496">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cd882-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd882-497">Az.Accounts</span></span>
- <span data-ttu-id="cd882-498">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd882-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="cd882-499">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd882-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd882-500">Az.ApiManagement</span></span>
- <span data-ttu-id="cd882-501">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="cd882-501">Fixes for #7002</span></span>
- <span data-ttu-id="cd882-502">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cd882-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd882-503">Az.Batch</span></span>
- <span data-ttu-id="cd882-504">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cd882-505">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="cd882-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cd882-506">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cd882-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd882-507">Az.Billing</span></span>
- <span data-ttu-id="cd882-508">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cd882-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cd882-509">Az.CognitivServices</span></span>
- <span data-ttu-id="cd882-510">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cd882-511">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd882-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="cd882-513">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cd882-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cd882-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cd882-515">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd882-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="cd882-517">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cd882-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd882-518">Az.Monitor</span></span>
- <span data-ttu-id="cd882-519">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cd882-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd882-520">Az.KeyVault</span></span>
- <span data-ttu-id="cd882-521">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cd882-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd882-522">Az.MachineLearning</span></span>
- <span data-ttu-id="cd882-523">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cd882-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd882-524">Az.Media</span></span>
- <span data-ttu-id="cd882-525">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="cd882-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd882-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-526">Az.Network</span></span>
<span data-ttu-id="cd882-527">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cd882-528">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="cd882-528">New cmdlets added:</span></span>
        - <span data-ttu-id="cd882-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd882-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd882-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd882-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd882-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd882-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cd882-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cd882-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cd882-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cd882-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd882-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cd882-537">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cd882-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd882-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cd882-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd882-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd882-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd882-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd882-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd882-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cd882-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cd882-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cd882-543">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="cd882-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cd882-544">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cd882-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd882-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd882-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd882-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd882-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd882-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cd882-548">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cd882-549">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cd882-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd882-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="cd882-551">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cd882-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd882-552">Az.Profile</span></span>
- <span data-ttu-id="cd882-553">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="cd882-555">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cd882-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-556">Az.Resources</span></span>
- <span data-ttu-id="cd882-557">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd882-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd882-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="cd882-559">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="cd882-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cd882-560">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cd882-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cd882-561">Az.SIgnalR</span></span>
- <span data-ttu-id="cd882-562">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="cd882-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cd882-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-563">Az.Sql</span></span>
- <span data-ttu-id="cd882-564">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cd882-565">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cd882-566">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd882-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-567">Az.Storage</span></span>
- <span data-ttu-id="cd882-568">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd882-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-569">Az.Websites</span></span>
- <span data-ttu-id="cd882-570">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cd882-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cd882-571">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cd882-572">Genel</span><span class="sxs-lookup"><span data-stu-id="cd882-572">General</span></span>

* <span data-ttu-id="cd882-573">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="cd882-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd882-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-574">Az.Compute</span></span>

* <span data-ttu-id="cd882-575">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd882-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="cd882-577">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cd882-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd882-578">Az.FrontDoor</span></span>

* <span data-ttu-id="cd882-579">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-579">Fixed some broken links</span></span>
    - <span data-ttu-id="cd882-580">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cd882-581">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd882-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd882-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="cd882-583">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cd882-584">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd882-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-585">Az.Resources</span></span>

* <span data-ttu-id="cd882-586">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="cd882-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cd882-587">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cd882-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-588">Az.Sql</span></span>

* <span data-ttu-id="cd882-589">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="cd882-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cd882-590">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cd882-591">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd882-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd882-592">Az.Storage</span></span>

* <span data-ttu-id="cd882-593">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cd882-594">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cd882-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd882-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd882-596">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="cd882-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd882-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cd882-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd882-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd882-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-599">Az.Websites</span></span>

* <span data-ttu-id="cd882-600">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cd882-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="cd882-601">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cd882-602">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd882-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cd882-603">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd882-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd882-604">Az.ApiManagement</span></span>
* <span data-ttu-id="cd882-605">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="cd882-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cd882-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd882-606">Az.Automation</span></span>
* <span data-ttu-id="cd882-607">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="cd882-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd882-608">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cd882-609">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cd882-610">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cd882-611">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd882-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-612">Az.Compute</span></span>
* <span data-ttu-id="cd882-613">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cd882-614">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="cd882-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd882-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd882-616">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="cd882-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cd882-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cd882-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cd882-618">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd882-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-619">Az.Network</span></span>
* <span data-ttu-id="cd882-620">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cd882-621">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cd882-622">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="cd882-623">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cd882-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd882-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cd882-625">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cd882-626">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="cd882-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cd882-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cd882-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cd882-628">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cd882-629">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="cd882-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cd882-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cd882-630">Az.Relay</span></span>
* <span data-ttu-id="cd882-631">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd882-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-632">Az.Resources</span></span>
* <span data-ttu-id="cd882-633">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cd882-634">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cd882-635">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cd882-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd882-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd882-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd882-637">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cd882-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-638">Az.Sql</span></span>
* <span data-ttu-id="cd882-639">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cd882-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd882-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd882-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd882-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd882-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd882-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd882-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd882-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd882-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd882-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd882-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd882-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd882-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cd882-648">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cd882-649">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cd882-650">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cd882-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cd882-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd882-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cd882-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd882-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cd882-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cd882-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cd882-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cd882-655">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cd882-656">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cd882-657">Genel</span><span class="sxs-lookup"><span data-stu-id="cd882-657">General</span></span>
* <span data-ttu-id="cd882-658">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="cd882-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cd882-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd882-659">Az.Profile</span></span>
* <span data-ttu-id="cd882-660">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cd882-661">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cd882-662">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cd882-663">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cd882-664">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cd882-665">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cd882-666">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd882-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd882-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd882-668">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-669">Az.Compute</span></span>
* <span data-ttu-id="cd882-670">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cd882-671">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="cd882-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cd882-672">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-674">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cd882-675">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cd882-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cd882-676">Az.Insights</span></span>
* <span data-ttu-id="cd882-677">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cd882-678">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="cd882-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cd882-679">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cd882-680">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="cd882-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-681">Az.Network</span></span>
* <span data-ttu-id="cd882-682">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="cd882-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cd882-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd882-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cd882-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cd882-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cd882-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd882-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cd882-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cd882-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cd882-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd882-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cd882-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd882-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd882-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd882-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd882-690">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-691">Az.Resources</span></span>
* <span data-ttu-id="cd882-692">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="cd882-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cd882-693">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="cd882-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd882-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd882-694">Az.ServiceBus</span></span>
* <span data-ttu-id="cd882-695">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd882-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd882-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd882-697">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cd882-698">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cd882-699">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cd882-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cd882-700">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cd882-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cd882-701">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cd882-702">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cd882-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd882-703">Az.Profile</span></span>
* <span data-ttu-id="cd882-704">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="cd882-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cd882-705">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="cd882-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-706">Az.Compute</span></span>
* <span data-ttu-id="cd882-707">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cd882-708">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd882-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd882-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd882-710">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="cd882-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cd882-711">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="cd882-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cd882-712">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="cd882-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd882-713">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd882-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd882-714">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="cd882-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-715">Az.Network</span></span>
* <span data-ttu-id="cd882-716">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cd882-717">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-718">Az.Resources</span></span>
* <span data-ttu-id="cd882-719">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cd882-720">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="cd882-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cd882-721">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cd882-722">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="cd882-722">Azure.Storage</span></span>
* <span data-ttu-id="cd882-723">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="cd882-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cd882-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd882-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cd882-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd882-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd882-726">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="cd882-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cd882-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cd882-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="cd882-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd882-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd882-729">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="cd882-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd882-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd882-730">Az.Compute</span></span>
* <span data-ttu-id="cd882-731">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cd882-732">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cd882-733">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cd882-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cd882-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cd882-735">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="cd882-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd882-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd882-736">Az.Network</span></span>
* <span data-ttu-id="cd882-737">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="cd882-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cd882-738">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-738">new cmdlets added</span></span>
    - <span data-ttu-id="cd882-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd882-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd882-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd882-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd882-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd882-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd882-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd882-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd882-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cd882-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cd882-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd882-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cd882-745">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cd882-746">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cd882-747">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd882-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd882-748">Az.RedisCache</span></span>
* <span data-ttu-id="cd882-749">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="cd882-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cd882-750">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd882-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd882-751">Az.Resources</span></span>
* <span data-ttu-id="cd882-752">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="cd882-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd882-753">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd882-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd882-754">Az.Sql</span></span>
* <span data-ttu-id="cd882-755">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="cd882-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd882-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd882-756">Az.Websites</span></span>
* <span data-ttu-id="cd882-757">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="cd882-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cd882-758">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="cd882-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cd882-759">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="cd882-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cd882-760">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="cd882-760">Initial Release</span></span>
